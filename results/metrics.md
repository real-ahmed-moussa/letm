# Model Results

Original results from the analysis. Do not update — these are the published metrics.

## Pointwise MSE at Stress-Test Observations

| Method | k / h | Test Year | Actual | Predicted | MSE |
|---|---|---|---|---|---|
| k-NN Regression | k = 85 | 1943 | 16.00 | 47.56 | 995.96 |
| Gaussian Kernel | h = 85 | 1943 | 16.00 | 46.98 | 959.82 |
| k-NN Regression | k = 85 | 2015 | 70.83 | 60.61 | 104.54 |

## Notes

- MSE computed as the squared error at a single test point: `(actual − predicted)²`
- The 1943 wartime minimum serves as the primary stress test: both methods at maximum smoothing predict ≈ 47 years, missing the observed 16-year collapse by nearly 32 years
- The 2015 plateau (actual: 70.83) is less sensitive to over-smoothing; k = 85 predicts 60.61 (MSE = 104.54)
- Gaussian kernel (h = 85) achieves slightly lower MSE at 1943 than k-NN (k = 85): 959.82 vs 995.96
