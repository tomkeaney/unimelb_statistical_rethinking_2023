# unimelb_statistical_rethinking_2023

A follow along of Richard McElreath's statistical rethinking course, to which he graciously provides open access. Based in the School of Biosciences at Melbourne uni.

[Course outline](https://github.com/rmcelreath/stat_rethinking_2023)

[Youtube lectures](https://www.youtube.com/playlist?list=PLDcUM9US4XdPz-KxHM4XHt7uUVGWWVSus)

Lectures come out twice a week, starting on the 2nd of January. We'll run a week behind the actual course so that you have more flexibility with fitting the lectures into your week. 

## Notes

Updated notes can be accessed [here](https://tomkeaney.github.io/unimelb_statistical_rethinking_2023/)

## Discussion session

We will **meet every Thursday at 11am in Drummond North** 

The purpose of this session is to discuss the weeks lectures and tackle the problems provided. If you can't make it, no problem! Join via the zoom link listed below. This means you simply need to listen to two hour-long lectures each week before the Thursday. I have quite thorough notes from previous years of the course, but it would be great if we could create a new markdown document to call upon in future. I'll upload these to this page weekly, following our discussion session. 

**Zoom link**: https://unimelb.zoom.us/j/84067147015?pwd=YUJ4RGNXck1QUjdRN1RYRlJlVEJlUT09

Password: 682590

## Coding Bayesian models in R

There are at least two options for how to follow along with the R code presented in the lectures. You can choose to follow the lectures and fit models using McElreath's `rethinking` package. Or, you can follow my suggestion and fit models using the `brms` package - a near complete conversion of the course to tidyverse + brms style is available [here](https://bookdown.org/content/4857/). Check out the course outline if you have a specific preference for another option. 

Whatever you choose, to fit bayesian models you'll need to install `rstan` and `cmdstanr` on your computer. 

To do this, here are instructions straight from McElreath's rehtinking github repo:

First, install the C++ toolchain and install the `rstan` package. Go to https://mc-stan.org/users/interfaces/rstan.html and follow the instructions for your platform. The biggest challenge is getting a C++ compiler configured to work with your installation of R. The instructions are quite thorough. Obey them, and you'll succeed.

Second, install the `cmdstanr` package. Visit https://mc-stan.org/cmdstanr/. The first time you install `cmdstanr`, you will also need compile the libraries with `cmdstanr::install_cmdstan()`. All this of this bother is worth it. You just have to do it once.

Third, once `rstan` and `cmdstanr` are installed (almost there), then you can install `rethinking` or `brms` from within R using:

**rethinking**

`install.packages(c("coda","mvtnorm","devtools","loo","dagitty","shape"))
devtools::install_github("rmcelreath/rethinking")`

**brms**

Really easy, just install the `brms` package in R
