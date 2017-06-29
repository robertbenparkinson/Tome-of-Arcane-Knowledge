# Generic randomForest Code in R and Notes

## Import Libaries and test set

```r
library(randomForest)

url <- 'dataset.csv'
the_data_set <- read.csv(url, header = TRUE, sep = ";", stringsAsFactors = FALSE)

```
Check to make sure that it imported correctly and you didn't screw it up.

```r
head(the_data_set)
foot(the_data_set)
```

If need be skip the appropriate rows from the top `skip=10`.

Sample Your data and build training data set and testing data set
Remeber the 60/40 Rule -- 60% of the data is set aside for the training set and 40% is set aside for the testing set.

```r
samp <- sample(nrow(the_data_set), 0.6 * nrow(the_data_set))
train <- the_data_set[samp, ]
test <- the_data_set[-samp, ]

##or using any other method
```

Remove the column you are testing for.


numTrain <- 10000

rows <- sample(1:nrow(train), numTrain)
lables <- as.factor(unlist(train[rows,1]))
train1 <- train[rows,-1]



wine$taste <- ifelse(wine$quality < 6, 'bad', 'good')
wine$taste[wine$quality == 6] <- 'normal'
wine$taste <- as.factor(wine$taste)

table(wine$taste)

set.seed(123)

samp <- sample(nrow(wine), 0.6 * nrow(wine))
train <- wine[samp, ]
test <- wine[-samp, ]

library(randomForest)
model <- randomForest(taste ~ . - quality, data = train, ntree = 500, mtry=3)
model

pred <- predict(model, newdata = test)
table(pred, test$taste)

