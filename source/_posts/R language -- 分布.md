---
layout: R language -- distribution
title: R language -- distribution
date: 2021-01-28 23:30:50
tags: R；norm
---

rnorm(n, mean = 0, sd = 1)   高斯(正态)

rexp(n, rate = 1)    指数

rgamma(n, shape, scale=1)    γ分布

rpois(n, lambda)     poisson分布

rweibull(n, shape, scale = 1)    weibull分布

rcauchy(n, location = 0, scale = 1)    cauchy分布

rbeta(n, shape1, shape2)    β分布

rt(n, df)    t分布

rf(n, df1, df2)    F分布

rchisq(n, df)    χ²分布

rbinom(n, size, prob)    二项

rgeom(n, prob)    几何

hyper(nn, m, n, k)    超几何

rlogis(n, location = 0, scale = 1)    logistic分布

rlnorm(n, meanly = 0, slog = 1)   对数正态

rnbinom(n, size, prob)    负二项分布

runic(n, min = 0, max = 1)   均匀分布

wilcox(nn, m, n), rsignrank(nn, n)    wilcoxon分布

所有的函数都可以使用d, p或q来替换r分别得到概率密度(dfunc(x, ...)), 累积概率密度(pfunc(x, ...)), 分位数(qfunc(p, ...), 0< p <1).



#好记性不如烂笔头系列#