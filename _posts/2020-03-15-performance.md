# Assessing regression models in R

R has unmatched abilities to fit, examine and visualize statistical models.

Today, I noticed the [performance R package](https://easystats.github.io/performance/index.html), which provides a unified interface to assess model fit and quality for many different regression models. 

It is part of a growing set of packages under the [easystats](https://easystats.github.io/blog/posts/) umbrella - a suite of R packages designed to make the use of advanced statistical techniques easy.

`performance` includes functions to report many different metrics, including various flavours of `R-squared`, `Intraclass Correlation Coefficients` (ICC) as well as checks for violations of assumptions such as `overdispersion`, `zero-inflation` or `singular model fits`. 

And if you are looking for a one-stop-shop, search no more:

```r
model <- lm(mpg ~ wt * cyl + gear, data = mtcars)
check_model(model)
```

![Comprehensive model assessment plot](https://easystats.github.io/performance/reference/figures/unnamed-chunk-13-1.png)

Check out the [performance package's website](https://easystats.github.io/performance/index.html) to learn more!
