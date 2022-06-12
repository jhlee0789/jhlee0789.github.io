Final Project
================
Junhee Lee
2022-06-13

### Introduction

-   The purpose of this study is to find the subway station where the
    delay of the subway line is majorly occured

-   To solve this problem, the data below has been used

    -   Operated subway data
    -   Scheduled subway data

-   The time and space considered for this study is written as below

    -   Target space: Seoul metro line 9 bound to VHS Medical Center
        (Gimpo Int’l Airport → VHS Medical Center)
    -   Target time: 03/08/2021 \~ 03/12/2021, morning peak time
        (07:00\~10:00)

-   There are two types of subway exist on line 9: local train & express
    train

    -   Local train: stops at all station
    -   Express train: stops only at some stations
    -   In this study, only express train is considered

<figure>
<img
src="https://w.namu.la/s/79add8bc7809eacbc47c6e76b0a8575c5105d0276322fbe24347e5134a91934f9838bfff352b664397b975695b691ebd14fdb9fe9da20d6f3270387e36f362c117821a6a2dc4b39cfdc440b1d0ab47bd2f74ebd284f620dc550aaa4aa934aed5"
style="width:50.0%" alt="Image from theissaclee.com" />
<figcaption aria-hidden="true">Image from theissaclee.com</figcaption>
</figure>

### Data Analysis

-   Considered two type of delay time: arrival delay & departure delay

    -   Arrival delay: difference between operated subway arrival time
        and scheduled subway arrival time
    -   Departure delay: difference between operated subway departure
        time and scheduled subway departure time
    -   In this study, information of arrival delay and departure delay
        from terminal stations have been excluded

-   The distribution of arrival delay time and departure delay time of
    each station is shown as below
    ![](finalProject-v2_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-2-2.png)<!-- -->

-   Convert delay time by subtract the departure delay time of the
    origin of the train (X4102, Gimpo Int’l Ariport)
    ![](finalProject-v2_files/figure-gfm/unnamed-chunk-3-1.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-3-2.png)<!-- -->

-   The delay time increases at stations whose ID is between X4113 and
    X4120

-   The delay time decreases at stations whose ID is between X4123 and
    X4130

### Analysis of Data Correlation

-   Correlation of arrival delay and departure delay from current
    station and previous station
    -   Arrival delay and departure delay has high correlation
    -   Compared with previous station, arrival delay from current
        station and departure delay from previous station has the
        highest correlation

![](finalProject-v2_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-4-2.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-4-3.png)<!-- -->

-   Correlation for each station
    -   In many station, correlation of departure delay from previous
        station and arrival delay from current station is higher than
        correlation of departure delay and arrival delay from current
        station
    -   However, at the section between X4110 and X4113, X4113 and
        X4115, X4120 and X4123, X4130 and X4133, departure delay from
        previous station and arrival delay from current station does not
        shown the correlation better than departure delay and arrival
        delay from current station

<!-- -->

    ## [1] "Previous Station ID: X4102"
    ## [1] "Current Station ID: X4105"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-1.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-2.png)<!-- -->

    ## [1] "Previous Station ID: X4105"
    ## [1] "Current Station ID: X4107"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-3.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-4.png)<!-- -->

    ## [1] "Previous Station ID: X4107"
    ## [1] "Current Station ID: X4110"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-5.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-6.png)<!-- -->

    ## [1] "Previous Station ID: X4110"
    ## [1] "Current Station ID: X4113"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-7.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-8.png)<!-- -->

    ## [1] "Previous Station ID: X4113"
    ## [1] "Current Station ID: X4115"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-9.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-10.png)<!-- -->

    ## [1] "Previous Station ID: X4115"
    ## [1] "Current Station ID: X4117"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-11.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-12.png)<!-- -->

    ## [1] "Previous Station ID: X4117"
    ## [1] "Current Station ID: X4120"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-13.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-14.png)<!-- -->

    ## [1] "Previous Station ID: X4120"
    ## [1] "Current Station ID: X4123"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-15.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-16.png)<!-- -->

    ## [1] "Previous Station ID: X4123"
    ## [1] "Current Station ID: X4125"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-17.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-18.png)<!-- -->

    ## [1] "Previous Station ID: X4125"
    ## [1] "Current Station ID: X4127"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-19.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-20.png)<!-- -->

    ## [1] "Previous Station ID: X4127"
    ## [1] "Current Station ID: X4129"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-21.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-22.png)<!-- -->

    ## [1] "Previous Station ID: X4129"
    ## [1] "Current Station ID: X4130"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-23.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-24.png)<!-- -->

    ## [1] "Previous Station ID: X4130"
    ## [1] "Current Station ID: X4133"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-25.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-26.png)<!-- -->

    ## [1] "Previous Station ID: X4133"
    ## [1] "Current Station ID: X4136"

![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-27.png)<!-- -->![](finalProject-v2_files/figure-gfm/unnamed-chunk-5-28.png)<!-- -->
