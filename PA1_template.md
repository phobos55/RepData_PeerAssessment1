# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data


```r
data <- read.csv("activity.csv")
Data <- data[which(data$steps!= "NA"), ]
DataF <- aggregate(steps ~ date, data = Data, sum)
```

## What is mean total number of steps taken per day?

```r
hist(DataF$steps,main="Histogram of Steps",xlab="Steps")
```

![](./PA1_template_files/figure-html/unnamed-chunk-2-1.png) 

####Calculate and report the mean and median total number of steps taken per day

```r
mean(DataF$steps)
```

```
## [1] 10766.19
```

```r
median(DataF$steps)
```

```
## [1] 10765
```
-The mean of steps per day is 1.0766189\times 10^{4}  
-The median of steps per day is 10765  

## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
