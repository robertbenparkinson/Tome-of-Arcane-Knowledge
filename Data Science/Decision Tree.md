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
summary(iris)
qplot(Petal.Length,Petal.Width,colour=Species,data=iris)

train.flag <- createDataPartition(y=iris$Species,p=0.5,list=FALSE)
training <- iris[train.flag,]
Validation <- iris[-train.flag,]

modfit <- train(Species~.,method="rpart",data=training) 

fancyRpartPlot(modfit$finalModel)
```
