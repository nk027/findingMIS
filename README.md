# Finding Most Influential Sets

R implementation of algorithms for most influential set selection (MISS) in regression models using the Dinkelbach algorithm.

## Setup

```r
# Dependencies
install.packages("Rcpp")
# Source functions
for (f in list.files("R", "\\.R$", full.names = TRUE)) {
  source(f, local = FALSE)
}
```

## Usage

```r
# Create model
model <- lm(y ~ 0 + x, data = your_data)
# Find most influential set of size k
result <- find_miss(model, k = 10)
# Find sets for sizes 1 to K
results <- find_misses(model, K = 5)
```

### Available Functions

- `find_miss(model, k)`: Find optimal set of size k
- `enumerate_miss(model, k)`: Exhaustive enumeration (small datasets)
- `greedy_miss(model, k)`: Greedy approximation

## Citation

If you use this software, please cite it.
