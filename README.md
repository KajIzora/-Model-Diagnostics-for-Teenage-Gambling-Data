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

# README

### Overview

This repository contains all the materials for **Mini Project 3: Model Diagnostics for Teenage Gambling Data**. The project involves fitting a linear model to the `teengamb` dataset, followed by a thorough diagnostic analysis to validate the assumptions of the model. 

### Contents

- **`mini_project_3.Rmd`** (or similarly named R Markdown file):  
  This is the main R Markdown document containing all code, detailed explanations, and visuals (residual plots, leverage plots, Cook’s Distance, etc.). It renders into an HTML or PDF report.

- **`teengamb_diagnostics.html`** (optional):  
  The compiled HTML version of the R Markdown file (if you choose to include it) for easy viewing in a web browser.

- **This `README.md`**:  
  Provides an overview of the project, instructions for setup, and usage notes.

### Data

- **`teengamb`**:  
  - Comes from the **faraway** R package.  
  - Represents survey data on teenage gambling in Britain, containing the following variables:  
    - `sex`: 0 = male, 1 = female  
    - `status`: Socioeconomic status score based on parents’ occupation  
    - `income`: Weekly income in pounds  
    - `verbal`: Verbal score (number of words correctly defined out of 12)  
    - `gamble`: Expenditure on gambling in pounds per year  

You do not need to manually provide the data file since installing **faraway** in R gives direct access to `teengamb`.

### Setup Instructions

1. **Clone or Download** this repository.  
2. **Open R or RStudio**.  
3. **Install Required Packages** (if needed):
   ```r
   install.packages(c("faraway", "car"))
   ```
4. **Open the R Markdown File** (`mini_project_3.Rmd`).  
5. **Knit/Render** the `.Rmd` file to produce an HTML or PDF report with the diagnostic results.

### How to Run the Analysis

1. **Load the libraries**:  
   ```r
   library(faraway)
   library(car)
   ```
2. **Run the code cells** sequentially in `mini_project_3.Rmd`.  
   - The first few code blocks will fit the linear model, plot diagnostics, run tests, and identify outliers/influential points.  
   - Later blocks show changes in parameter estimates when removing certain observations.  
3. **Interpret the Output**:  
   - Residual plots, F-tests, QQ plots, etc., give you insight into model assumptions.  
   - Cook’s Distance, high leverage, and studentized residuals highlight observations that heavily influence the model.  

### Key Takeaways

- **Heteroscedasticity** was detected, meaning non-constant variance of residuals.  
- **Non-normal** residuals were also indicated by tests and Q-Q plots.  
- Observations **#24 and #39** appear particularly **influential**, suggesting the possibility of removing or transforming these points or the response to improve model fit.  

### Acknowledgments

- The **faraway** package and its contributors for providing useful datasets and functions.  
- Original reference: Ide-Smith & Lea (1988), *Journal of Gambling Behavior*, 4, 110–118.

