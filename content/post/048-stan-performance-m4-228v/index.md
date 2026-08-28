---
title: Performance Comparison of Stan on Intel 228V vs Apple Air M4
slug: stan-performance-m4-228v
date: 2026-08-28 20:09:09+0200
tags:
    - open-source
    - software
    - laptops
---

Apple Silicon is definitely impressive in benchmarks. For real world tasks, however, they recommend running testing against real applications. Now, I'm not running any rigorous tests. Just some informal tests and eye-balling the times.

The most intensive task I've been doing this month is building and running stan models. For those not in the know, [Stan](https://mc-stan.org/) is a software for bayesian data analysis. The documentation is really good. It essentially provides a rich C-like DSL (minus the memory management) to write bayesian models. It then transpiles this to C++, compiles it, and then runs it. For small datasets, both compilation and runtime become comparable.

As against my earlier announcement about the [use of macbook](../macos-dislike/), I eventually returned to Linux as a found a good deal on a T14 Thinkpad with Intel 228V, which has very reasonable battery life to get me through full conference days and long journeys. But I have the M4 Macbook Air lying around that I don't want to give, because I want to use it for occasionally testing [my libraries](https://github.com/digikar99) on MacOS. Cloud-hosted solutions for MacOS cost on the order of 60 USD/month, which basically means you can get a full macbook in a few months. Very unaffordable.

But more recently, I found some time and peace of mind to dive into [tunneling](https://github.com/anderspitman/awesome-tunneling) and set up a [cloudflared tunnel](https://developers.cloudflare.com/tunnel/) to access my macbook through a public domain. This means I can now access my dormant macbook from anywhere even if I don't have a public-facing static IP.

But is it any useful? Apple M4 packs a punch. Depending on the metric, [it is about 25-50% faster than Intel 228V](https://www.cpu-monkey.com/en/compare_cpu-intel_core_ultra_5_228v-vs-apple_m4). I also noticed that while 228V has a peak of 4.5GHz, in reality, it only spends a minute or two above 3GHz, and often settles down to 2.5GHz. I don't know how all the benchmark numbers compare against thermal throttlings. [Benchmark numbers also don't have strong cross-domain correlations.](https://www.reddit.com/r/hardware/comments/pitid6/eli5_why_does_it_seem_like_cinebench_is_now_the/)

So, the question then becomes, for my particular use case, which is compiling and running Stan Models, how do Intel 228V and Apple M4 compare? I also found an officially maintained [stan-dev/performance-tests-cmdstan](https://github.com/stan-dev/performance-tests-cmdstan) repository that I hope is representative of my usage. So, [depending on how lucky you are], the following should allow you to benchmark stan on your computer. As of this writing, I'm on commit `b329e269` of the repository.

```sh
git clone --recursive https://github.com/stan-dev/performance-tests-cmdstan.git
python3 runPerformanceTests.py -j N -runj N stat_comp_benchmarks # N is the number of cores
```

You might want to prefix that last command with `time` which is what I do for obtaining the below numbers. They represent duration in minutes; thus lower the better. For whatever reason, Intel 228V did not throttle while running this workload. It consistently had at least one core above 4GHz. 

| Test \ Platform          | Intel 228V | Apple M4 (Powersave) | Apple M4 (Full) |
|--------------------------|------------|----------------------|-----------------|
| 4 cores compile + run  | 2:25       | 4:10                 | 2:07            |
| 1 core compile + run   | 2:40       | 3:55                 | 1:57            |
| 4 cores run            | 0:35       | 2:10                 | 1:05            |
| 1 core run             | 0:55       | 1:55                 | 1:00            |
| 4 cores compile (diff) | 1:50       | 2:00                 | 1:07            |
| 1 core compile (diff)  | 1:45       | 2:00                 | 0:57            |

Well, these were obtained by eye-balling about 2 runs each, just to check if they differ. Often, the difference between subsequent runs was less than 1 second. So, nothing rigorous, but nothing totally off either. It does seem that multiple cores has negligible impact on the runs. If anything, on MacOS, the multiple cores actually degraded the run! It's also possible that difference in compilation times are due to the difference between g++ on Linux and clang++ on MacOS; I could not trivially get the system to compile with clang++. There could also be a bunch of different optimization flags that are not being used.

That said, it seems this is not the workload where I will get any significant benefits from Apple Silicon in the immediate future. There are similar reports and discussions [here](https://github.com/tuhdo/tuhdo.github.io/blob/8a26ccfea91c1e5fea7b18c110bf11746a37ee5a/emacs-tutor/zen3_vs_m1.org), [here](https://discourse.mc-stan.org/t/anyone-planning-on-getting-an-m1-machine-to-benchmark/19344/3) and [here](https://discourse.mc-stan.org/t/stan-on-m4-mac/37240/16). Most of the reported gains seem to be from testing a 2018-era CPU to the M-series Apple Silicon :/. That's not to dismiss the energy efficiency of Apple Silicon. M4 gets me about 2 conference days(!) on a single charge. Its standby time is also something that might put smartphones to shame. But at least for this particular workload, it doesn't seem it's a great fit.

