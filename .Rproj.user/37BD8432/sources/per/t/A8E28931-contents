library(data.table)
library(tidyverse)
library(DataExplorer)
library(caTools)

train=fread("train.csv")
test=fread("test.csv")

DataExplorer::create_report(train)

head(train)
str(train)
colSums(is.na(train))
summary(train)

hist(train$LotFrontage)

train[is.na(train$Alley),"Alley"]="No access"
train[is.na(train$LotFrontage),"LotFrontage"]=69

hist(train$MasVnrArea)

train[is.na(train$MasVnrArea),"MasVnrArea"]=0

hist(train$GarageYrBlt)

hist(train$YearBuilt-train$GarageYrBlt)

train[is.na(train$GarageYrBlt),"GarageYrBlt"]=train[is.na(train$GarageYrBlt),"YearBuilt"]

colSums(is.na(train))
table(train$MasVnrType)
train[is.na(train$MasVnrType),"MasVnrType"]="None"

table(train$BsmtQual)

train[is.na(train$BsmtQual),"BsmtQual"]=sample(c("Gd","TA"),prob = c(0.5,0.5),size = 1)

table(train$BsmtQual)

table(train$BsmtCond)

train[is.na(train$BsmtCond),"BsmtCond"]="TA"

table(train$BsmtExposure)

train[is.na(train$BsmtCond),"BsmtCond"]="TA"

table(train$BsmtExposure)

train[is.na(train$BsmtExposure),"BsmtExposure"]=sample(c("Av",  "Gd",  "Mn",  "No" ),prob = c(221, 134, 114, 953),size = 1)

