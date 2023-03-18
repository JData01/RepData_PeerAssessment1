---
title: "Reproducible Research: Peer Assessment 1"
output: 
  html_document:
    keep_md: true
---


## Loading and preprocessing the data

```r
# Loading and preprocessing the data
data.initial <- read.csv(unz("activity.zip", "activity.csv"), sep=",")
data.initial$date <- as.Date(data.initial$date)
```

## What is mean total number of steps taken per day?
![](PA1_template_files/figure-html/unnamed-chunk-2-1.png)<!-- -->

Mean of the total number of steps per day: **10766.2**   
Median of the total number of steps per day: **10765**

## What is the average daily activity pattern?
![](PA1_template_files/figure-html/unnamed-chunk-3-1.png)<!-- -->

Which 5-minute interval, on average across all the days in the dataset, contains the maximum number of steps? Interval **835**


## Imputing missing values

![](PA1_template_files/figure-html/unnamed-chunk-4-1.png)<!-- -->

The total number of missing values in the dataset is **2304**

For filling in all of the missing values in the dataset, the mean for that 5-minute interval across all days was used.

Mean of the total number of steps per day (NA filled): **10766.2**   
Median of the total number of steps per day (NA filled): **10766.2**

The impact of imputing the missing data on the estimates of the total daily number of steps is 
**0** , on the mean and **1.2** on the median.

## Are there differences in activity patterns between weekdays and weekends?
![](PA1_template_files/figure-html/unnamed-chunk-5-1.png)<!-- -->
