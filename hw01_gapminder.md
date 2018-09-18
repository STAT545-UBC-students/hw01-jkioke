hw01\_gapminder
================
kioke
September 17, 2018

``` r
data(rock)
      rock
```

    ##     area     peri     shape   perm
    ## 1   4990 2791.900 0.0903296    6.3
    ## 2   7002 3892.600 0.1486220    6.3
    ## 3   7558 3930.660 0.1833120    6.3
    ## 4   7352 3869.320 0.1170630    6.3
    ## 5   7943 3948.540 0.1224170   17.1
    ## 6   7979 4010.150 0.1670450   17.1
    ## 7   9333 4345.750 0.1896510   17.1
    ## 8   8209 4344.750 0.1641270   17.1
    ## 9   8393 3682.040 0.2036540  119.0
    ## 10  6425 3098.650 0.1623940  119.0
    ## 11  9364 4480.050 0.1509440  119.0
    ## 12  8624 3986.240 0.1481410  119.0
    ## 13 10651 4036.540 0.2285950   82.4
    ## 14  8868 3518.040 0.2316230   82.4
    ## 15  9417 3999.370 0.1725670   82.4
    ## 16  8874 3629.070 0.1534810   82.4
    ## 17 10962 4608.660 0.2043140   58.6
    ## 18 10743 4787.620 0.2627270   58.6
    ## 19 11878 4864.220 0.2000710   58.6
    ## 20  9867 4479.410 0.1448100   58.6
    ## 21  7838 3428.740 0.1138520  142.0
    ## 22 11876 4353.140 0.2910290  142.0
    ## 23 12212 4697.650 0.2400770  142.0
    ## 24  8233 3518.440 0.1618650  142.0
    ## 25  6360 1977.390 0.2808870  740.0
    ## 26  4193 1379.350 0.1794550  740.0
    ## 27  7416 1916.240 0.1918020  740.0
    ## 28  5246 1585.420 0.1330830  740.0
    ## 29  6509 1851.210 0.2252140  890.0
    ## 30  4895 1239.660 0.3412730  890.0
    ## 31  6775 1728.140 0.3116460  890.0
    ## 32  7894 1461.060 0.2760160  890.0
    ## 33  5980 1426.760 0.1976530  950.0
    ## 34  5318  990.388 0.3266350  950.0
    ## 35  7392 1350.760 0.1541920  950.0
    ## 36  7894 1461.060 0.2760160  950.0
    ## 37  3469 1376.700 0.1769690  100.0
    ## 38  1468  476.322 0.4387120  100.0
    ## 39  3524 1189.460 0.1635860  100.0
    ## 40  5267 1644.960 0.2538320  100.0
    ## 41  5048  941.543 0.3286410 1300.0
    ## 42  1016  308.642 0.2300810 1300.0
    ## 43  5605 1145.690 0.4641250 1300.0
    ## 44  8793 2280.490 0.4204770 1300.0
    ## 45  3475 1174.110 0.2007440  580.0
    ## 46  1651  597.808 0.2626510  580.0
    ## 47  5514 1455.880 0.1824530  580.0
    ## 48  9718 1485.580 0.2004470  580.0

``` r
head(rock)
```

    ##   area    peri     shape perm
    ## 1 4990 2791.90 0.0903296  6.3
    ## 2 7002 3892.60 0.1486220  6.3
    ## 3 7558 3930.66 0.1833120  6.3
    ## 4 7352 3869.32 0.1170630  6.3
    ## 5 7943 3948.54 0.1224170 17.1
    ## 6 7979 4010.15 0.1670450 17.1

``` r
(ncol(rock))
```

    ## [1] 4

``` r
(summary(rock))
```

    ##       area            peri            shape              perm        
    ##  Min.   : 1016   Min.   : 308.6   Min.   :0.09033   Min.   :   6.30  
    ##  1st Qu.: 5305   1st Qu.:1414.9   1st Qu.:0.16226   1st Qu.:  76.45  
    ##  Median : 7487   Median :2536.2   Median :0.19886   Median : 130.50  
    ##  Mean   : 7188   Mean   :2682.2   Mean   :0.21811   Mean   : 415.45  
    ##  3rd Qu.: 8870   3rd Qu.:3989.5   3rd Qu.:0.26267   3rd Qu.: 777.50  
    ##  Max.   :12212   Max.   :4864.2   Max.   :0.46413   Max.   :1300.00

``` r
str(rock)
```

    ## 'data.frame':    48 obs. of  4 variables:
    ##  $ area : int  4990 7002 7558 7352 7943 7979 9333 8209 8393 6425 ...
    ##  $ peri : num  2792 3893 3931 3869 3949 ...
    ##  $ shape: num  0.0903 0.1486 0.1833 0.1171 0.1224 ...
    ##  $ perm : num  6.3 6.3 6.3 6.3 17.1 17.1 17.1 17.1 119 119 ...

``` r
rock$area
```

    ##  [1]  4990  7002  7558  7352  7943  7979  9333  8209  8393  6425  9364
    ## [12]  8624 10651  8868  9417  8874 10962 10743 11878  9867  7838 11876
    ## [23] 12212  8233  6360  4193  7416  5246  6509  4895  6775  7894  5980
    ## [34]  5318  7392  7894  3469  1468  3524  5267  5048  1016  5605  8793
    ## [45]  3475  1651  5514  9718