# measures of Spread
- **Range** (min-max)
- **Variance** (Roughly the average squared deviation of the mean)
  - Sample variance 
    ![formula](https://render.githubusercontent.com/render/math?math=s^2=\frac{\sum_{i=1}^n(x_i-x_i)^2}{n-1})
    - why we do not use absolute valuse? think about it. weights larger deviatins more than smaller deviations.
  - Population Variance ![formula](https://render.githubusercontent.com/render/math?math=\sigma^2)
- **Standard Deviation** 
  - think about variability and diversity, do not confuse them. variability is about distribution against center, diversity is about number of different items.
- **inter-quartile range (IQR)**
  - range of the middle 50% of the data, distance between the first quartile (25th percentile) and third quartile (75th percentile)

    ![formula](https://render.githubusercontent.com/render/math?math=IQR=Q3-Q1)


# Robust Statistics
we define robust statistics as measures on which extreme observatins have little effect.


measure/robustness | robust | non-robust
------------ | ------------- | -------------
center   | median  | mean
spread   | IQR   | SD, range

- robust measures are more useful for describing skewed distributions with extreme observations
- non-robust measures ore more usefuul for describing symmetric distributions


# Transformation data
- a transformation is a _rescale_ of the data using a function
- when data are very strongly skewed, we sometimes transform them so they are easier to model.
### (natural) log transformation
- often applied when much of the data cluster near zero (relative to larger values in the dataset) and all observations are positive.
- to make the relationship between the variables more linear, and hence easier to model with simple methods.

### square root
### inverse
