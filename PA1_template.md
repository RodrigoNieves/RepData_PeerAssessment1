# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data
1. Load the data

```r
rawData = read.csv("activity.csv", na.strings = "NA")
```

2. Converting dates

```r
rawData$formatDate = as.Date(rawData$date,"%Y-%m-%d")
```
## What is mean total number of steps taken per day?

1. Calculating total number of steps per day

```r
steps = aggregate(rawData$steps ~ rawData$formatDate, FUN = sum)
```

2. Histogram of the number of steps per day

```r
hist(steps$`rawData$steps`,xlab = "Total number of steps per day",ylab = "Frequency")
```

![](PA1_template_files/figure-html/unnamed-chunk-4-1.png) 
3. Mean and median of the total number of steps per day

```r
meanSteps = mean(steps$`rawData$steps`)
medianSteps = median(steps$`rawData$steps`)
```
The mean of steps per day is: 1.0766189\times 10^{4}.  
The median of steps per day is: 10765.  

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
