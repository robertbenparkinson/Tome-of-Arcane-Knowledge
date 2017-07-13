# How to Grow a Decision Tree

Simple Example

## Install various libraries 

```r
library(ggplot2)
library(rpart)
library(caret)
library(rattle)
library(e1071)
```

## Down load data set
```r
data("iris")
```

## Check out the Data
```r
summary(iris)
qplot(Petal.Length,Petal.Width,colour=Species,data=iris)
```

## Create training and test sets
```r
train.flag <- createDataPartition(y=iris$Species,p=0.5,list=FALSE)
training <- iris[train.flag,]
Validation <- iris[-train.flag,]
```
## Grow Decision Tree
```r
modfit <- train(Species~.,method="rpart",data=training) 
```

## Create some not so pretty decision trees
```r
plot(modfit)
text(modfit)
```

## Create fancy decision trees
```r
fancyRpartPlot(modfit$finalModel)
```
