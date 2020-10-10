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


* | robust | non-robust
------------ | ------------- | -------------
center   | median  | mean
spread   | IQR   | SD, range
