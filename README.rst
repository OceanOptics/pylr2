Linear Regression Type II for Python
====================================

This python package (pylr2) provides linear regression type 2 (regress2), which are recommended when there is variability in both variables regressed. It uses linear regression type 1 from the statsmodels package.

Linear Regression Type 1 models supported are:
  - OLS: ordinary least square <default>
  - WLS: weighted least square
  - RLM: robust linear model

Linear Regression Type 2 models supported are:
  - major axis
  - reduced major axis ( also known as geometric mean) <default>
  - arithmetic mean

Example of usage:
::
    from pylr2 import regress2


    # Generate a dataset
    x = np.linspace(0, 10, 100)
    e = np.random.normal(size=len(x))
    y = x + e
    # Compute regression type 2
    results = regress2(x, y, _method_type_2="reduced major axis")

The package is an adaptation of the type 2 models from MBARI (https://www.mbari.org/products/research-software/matlab-scripts-linear-regressions/).