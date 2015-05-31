
# Summary


````julia
using OnlineStats, DataFrames
````





### Create fit with the first batch
````julia
srand(620)
o = Summary(randn(100))
````





### Update model with many batches
````julia
for i = 1:10000
    update!(o, randn(100))
end
````





### Check summary statistics
````julia
julia> DataFrame(o)
1x5 DataFrame
| Row | μ           | σ²       | max     | min      | nobs    |
|-----|-------------|----------|---------|----------|---------|
| 1   | 0.000253569 | 0.999379 | 4.57004 | -4.79766 | 1000100 |

````



