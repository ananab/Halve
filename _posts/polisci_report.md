The Influence of Army Size on The Employment Levels: in Post-WWII and Post-Korean War USA
================
Kai He
Feb 3rd, 2017

### Introduction

The main task of this analysis is to have a better understanding of Macroeconomics in the United States post-World War II. Specifically, the employment levels may be influenced by the Gross National Product (GNP), unemployment, and size of the army. The relative significance of these effects is examined by conducting statistical modeling on data collected annually between years 1947 and 1962. Through hypothesis testing, the question that whether the number of people in the military has an impact on employment rate is answered.

### Understanding the data

The dataset used in this analysis is relatively small. There are 16 annual observations for the years 1947 - 1962, each with a record of 7 factors for the corresponding year. These factors are:

-   Year
-   GNP, in billions
-   GNP deflator, with the year 1954 as the base year
-   Population of people over 14 years old, in millions
-   number of Employed, in millions
-   number of Unemployed, in 10 thousands
-   number of people in Armed Forces, in 10 thousands.

The entire dataset is shown in Table 1

|      |  GNP.deflator|      GNP|  Unemployed|  Armed.Forces|  Population|  Year|  Employed|
|------|-------------:|--------:|-----------:|-------------:|-----------:|-----:|---------:|
| 1947 |          83.0|  234.289|       235.6|         159.0|     107.608|  1947|    60.323|
| 1948 |          88.5|  259.426|       232.5|         145.6|     108.632|  1948|    61.122|
| 1949 |          88.2|  258.054|       368.2|         161.6|     109.773|  1949|    60.171|
| 1950 |          89.5|  284.599|       335.1|         165.0|     110.929|  1950|    61.187|
| 1951 |          96.2|  328.975|       209.9|         309.9|     112.075|  1951|    63.221|
| 1952 |          98.1|  346.999|       193.2|         359.4|     113.270|  1952|    63.639|
| 1953 |          99.0|  365.385|       187.0|         354.7|     115.094|  1953|    64.989|
| 1954 |         100.0|  363.112|       357.8|         335.0|     116.219|  1954|    63.761|
| 1955 |         101.2|  397.469|       290.4|         304.8|     117.388|  1955|    66.019|
| 1956 |         104.6|  419.180|       282.2|         285.7|     118.734|  1956|    67.857|
| 1957 |         108.4|  442.769|       293.6|         279.8|     120.445|  1957|    68.169|
| 1958 |         110.8|  444.546|       468.1|         263.7|     121.950|  1958|    66.513|
| 1959 |         112.6|  482.704|       381.3|         255.2|     123.366|  1959|    68.655|
| 1960 |         114.2|  502.601|       393.1|         251.4|     125.368|  1960|    69.564|
| 1961 |         115.7|  518.173|       480.6|         257.2|     127.852|  1961|    69.331|
| 1962 |         116.9|  554.894|       400.7|         282.7|     130.081|  1962|    70.551|

As the introduction stated, the main goal of this analysis is to examine the relationships between 4 of the 7 factors. Namely Employed, Unemployed, GNP, and Armed.Forces. An overview of the factors is shown in Fig. 1

![](polisci_report_files/figure-markdown_github/unnamed-chunk-3-1.png)

There is a lot of plotting going on in this figure and the first glance can be very messy. However, since the interest is to understand how employment levels are affected by the other factors, the main focus should be the bottom row only. In this row, the first three panels show relationships between Employment and each of the other factors in scatter plots, where a clear pattern would suggest a stronger relationship. The last panel shows the distribution of all employment values as a density plot. It should be noticed that the distribution of employment is not correspondent to the years.

Above the last row, the rest of Figure 1 also provides useful information. The diagonal panels are distributions of factors, and the other scatter plots demonstrate relationships between different factors, all similar to that with Employment. Above the diagonal, the correlations are shown as an indicator of how strong each relationship is, where the strongest relationship has a magnitude of 1 and a non-relationship has a value of 0. The last column of these numbers is most informative for this study.

From these plots, it is obvious that employment has a strong relationship with GNP, which is very intuitive because more people employed can create a greater value for the nation. What's somewhat counterintuitive is that the number of unemployed seems to have very little to do with employment. These findings are also supported by the correlations, shown as numbers above the diagonal in Figure 1.

Nonetheless, the important question we are trying to answer is that if the size of Armed Forces has an influence on employment. If we just look at the correlation, it may seem that the relationship between the two is not very strong (0.457). However, the scatter plot shows a rather strange pattern. As it is seen in the third panel in the last row, there are four data points with low employment and small size of the military, while the majority of the employment levels seem to decrease as the Armed Forces get bigger. Moreover, a similar pattern is observed for the relationship between Armed Forces and GNP, which is expected because employment and GNP are highly correlated. This observation is further examined by looking into the size of the military over year in Figure 2, and employment over year in Figure 3.

![](polisci_report_files/figure-markdown_github/unnamed-chunk-4-1.png)![](polisci_report_files/figure-markdown_github/unnamed-chunk-4-2.png)

As it is seen in these figures, the employment is steadily increasing over the years. However, the size of Armed Forces boosted suddenly in the year 1951 by nearly 150 millions people, and then gradually decreased again until the 60s. The first jump at 1951 marks the beginning of the Korean War, and the second increase in 1961 is due to the Berlin Crisis (1). From Figure 2, we can conclude that the 4 data points with small numbers of people in the army correspond to the period before the Korean War in 1950. Because of the drastic changes in international relations and the impact US foreign policies have on its economics, it is also reasonable to divide the dataset into two portions by 1951, and focus on the post-war period (1951 - 1962). The split datasets are shown in the tables 6 and 7.

### Methods

To answer the proposed question statistically, a hypothesis test should be conducted. In the hypothesis test, a Null Hypothesis is first assumed, stating that there is no relationship between the factors of interested. A probability of this assumption being true is calculated and reported by statistical modeling, and the relationship is typically determined likely to exist if the probability is below 5%. With regard to the original question concerning the entire dataset, we assume that the number of people in Armed Forces has no influence on employment of the USA for the period of 1947 to 1962.

Similarly, another hypothesis test is completed using split dataset after the Korean War. The Null Hypothesis is that the number of people in Armed Forces has no influence on employment of USA for the period of 1951 to 1962. Two more hypothesis tests are performed for the variables GNP and Unemployed on the full dataset. A linear regression is performed to examine each of these hypotheses, and the outputs are summarized in the Results section.

### Results

![](polisci_report_files/figure-markdown_github/unnamed-chunk-6-1.png)

| term         |    estimate|  std.error|  statistic|    p.value|
|:-------------|-----------:|----------:|----------:|----------:|
| (Intercept)  |  59.3012647|  3.2293472|  18.363236|  0.0000000|
| Armed.Forces |   0.0230781|  0.0119944|   1.924065|  0.0749178|

![](polisci_report_files/figure-markdown_github/unnamed-chunk-7-1.png)

| term         |    estimate|  std.error|  statistic|    p.value|
|:-------------|-----------:|----------:|----------:|----------:|
| (Intercept)  |  82.5703510|  3.7254926|   22.16361|  0.0000000|
| Armed.Forces |  -0.0532774|  0.0125349|   -4.25031|  0.0016887|

![](polisci_report_files/figure-markdown_github/unnamed-chunk-8-1.png)![](polisci_report_files/figure-markdown_github/unnamed-chunk-8-2.png)

| term        |    estimate|  std.error|  statistic|  p.value|
|:------------|-----------:|----------:|----------:|--------:|
| (Intercept) |  51.8435898|  0.6813716|   76.08710|        0|
| GNP         |   0.0347523|  0.0017057|   20.37407|        0|

| term        |    estimate|  std.error|  statistic|    p.value|
|:------------|-----------:|----------:|----------:|----------:|
| (Intercept) |  59.2863554|  2.8822925|  20.569167|  0.0000000|
| Unemployed  |   0.0188852|  0.0086842|   2.174674|  0.0472894|

### Discussion

In Table 2 and Table 3, the row labeled as Intercept corresponds to the Employed. This is called the Intercept because the estimated values represent an expected number of Employed people when there is no military, which is the y-intercept on the plot. The other row obviously represents the Armed Forces variable. For the columns, `estimate` is the expected value, `std.error` can be roughly considered as an indicator of the width of the gray uncertainty band around regression lines. The most important part, however, is the p-value in the Armed Forces row, which is the aforementioned probability that the null hypothesis is true and there is no relationship. The lower this p-value is, the less likely that there is no relationship, therefore the more likely there is a strong relationship between military size and Employment.

For the entire post-WWII period USA, the p-value is around 7.5%, which is greater than the typical cutoff at 5%. While it is still possible that there is a weak relationship between the number of people in the Armed Forces and Employment, any such relationship could be due to random chance. On the other hand, with a focus on the USA macroeconomics after Korean War, the p-value is only 0.17%. This is way lower than the 5% cutoff for p-values, which suggests that the relationship observed is very likely to be real. Recall that the strength of a relationship can be indicated by correlation in statistics. The correlation for Armed Forces and Employment in post-Korean War USA is -0.8023005, which is strong and negative. This suggests that in the period of 1951 to 1962, a downsize of the military is actually observed with a growth in Employment. It should be noted that this does not establish a causal effect between the two.

Similar to these results, the p-values for GNP and Unemployment are calculated for the post-WWII US. The p-value for GNP is shown as 0, but it is actually a very small number close to 0. Thus, the GNP is extremely likely to have a correlation with Employment. Lastly, the p-value for Unemployment is 4.7%, which is just below the cutoff. So there is possibly a relationship between Employment and Unemployment. The correlations are calculated as 0.963837 for GNP, and 0.653936 for Unemployed.

One source of error this analysis could have is that the dataset is very small. Any conclusion drawn from such a small dataset can be due to chance. A way around this is to use a little more advanced statistical techniques such as bootstrap, which reuses the data randomly in order to increase reliability. Since it is known that this dataset has many interacting factors (2), a linear regression using multiple explanatory variables might not work well. Instead, only one of the factors having correlations with each other should be kept.

### Conclusion

The dataset of macroeconomics in the post-WWII USA is explored with visualization and examined by hypothesis testing and linear regression. It is shown that the GNP most likely has a strong positive relationship with the Employment levels. Unemployment is also likely to have a positive impact on Employment. But Armed Forces Size may not have an influence on the Employment at all. However, there is a drastic change in the scale of the military because of the Korean War. If we focus on the data after the beginning of Korean War, there is actually a strong negative correlation between the Army size and Employment. Based on this results, any attempts to boost employment by investing in the Armed Forces should be strongly discouraged.

### References

<http://www.history.army.mil/html/books/045/45-3-1/cmhPub_45-3-1.pdf> 1. Donald A. Carter (2014). Forging the Shield The U.S. Army in Europe, 1951–1962.

1.  Julian Faraway (2016). faraway: Functions and Datasets for Books by Julian Faraway. R package version 1.0.7. <https://CRAN.R-project.org/package=faraway>

### Appendix

|  GNP.deflator|      GNP|  Unemployed|  Armed.Forces|  Population|  Year|  Employed|
|-------------:|--------:|-----------:|-------------:|-----------:|-----:|---------:|
|          83.0|  234.289|       235.6|         159.0|     107.608|  1947|    60.323|
|          88.5|  259.426|       232.5|         145.6|     108.632|  1948|    61.122|
|          88.2|  258.054|       368.2|         161.6|     109.773|  1949|    60.171|
|          89.5|  284.599|       335.1|         165.0|     110.929|  1950|    61.187|

|  GNP.deflator|      GNP|  Unemployed|  Armed.Forces|  Population|  Year|  Employed|
|-------------:|--------:|-----------:|-------------:|-----------:|-----:|---------:|
|          96.2|  328.975|       209.9|         309.9|     112.075|  1951|    63.221|
|          98.1|  346.999|       193.2|         359.4|     113.270|  1952|    63.639|
|          99.0|  365.385|       187.0|         354.7|     115.094|  1953|    64.989|
|         100.0|  363.112|       357.8|         335.0|     116.219|  1954|    63.761|
|         101.2|  397.469|       290.4|         304.8|     117.388|  1955|    66.019|
|         104.6|  419.180|       282.2|         285.7|     118.734|  1956|    67.857|
|         108.4|  442.769|       293.6|         279.8|     120.445|  1957|    68.169|
|         110.8|  444.546|       468.1|         263.7|     121.950|  1958|    66.513|
|         112.6|  482.704|       381.3|         255.2|     123.366|  1959|    68.655|
|         114.2|  502.601|       393.1|         251.4|     125.368|  1960|    69.564|
|         115.7|  518.173|       480.6|         257.2|     127.852|  1961|    69.331|
|         116.9|  554.894|       400.7|         282.7|     130.081|  1962|    70.551|

##### calculation of the correlations

``` r
cor(after_kw$Armed.Forces,after_kw$Employed)
```

    ## [1] -0.8023005

``` r
cor(after_kw$GNP,after_kw$Employed)
```

    ## [1] 0.963837

``` r
cor(after_kw$Unemployed,after_kw$Employed)
```

    ## [1] 0.653936
