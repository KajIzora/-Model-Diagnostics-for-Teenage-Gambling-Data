## Project Description

This project focuses on diagnosing a linear regression model for teenage gambling behavior using the `teengamb` dataset (from the **faraway** R package). The main goals are to:

1. **Investigate Potential Violations of Model Assumptions**  
   - Check for heteroscedasticity using residual-versus-fitted plots and formal F-tests.  
   - Examine normality of residuals via Q-Q plots, histograms, and statistical tests (Shapiro-Wilk, Kolmogorov-Smirnov).  

2. **Identify Influential Observations**  
   - Detect high-leverage points by examining the hat matrix.  
   - Identify outliers via studentized (externally studentized) residuals and a Bonferroni-corrected threshold.  
   - Pinpoint influential data points with Cook’s Distance.  

3. **Assess the Effect of Removing Influential Points**  
   - Compare parameter estimates, R-squared, and residual standard error before and after omitting identified influential points.  

These methods illustrate a standard diagnostic workflow in linear regression, ensuring that the final model is robust and that any violations are addressed or acknowledged.  

---

### Required

This project uses the following r libraries:

   ```r
   library(faraway)
   library(car)
   ```

---

### Key Takeaways

- **Heteroscedasticity** was detected, meaning non-constant variance of residuals.  
- **Non-normal** residuals were also indicated by tests and Q-Q plots.  
- Observations **#24 and #39** appear particularly **influential**, suggesting the possibility of removing or transforming these points or the response to improve model fit.

---

### Acknowledgments

- The **faraway** package and its contributors for providing useful datasets and functions.  
- Original reference: Ide-Smith & Lea (1988), *Journal of Gambling Behavior*, 4, 110–118.

