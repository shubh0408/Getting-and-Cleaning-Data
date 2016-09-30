# Getting-and-Cleaning-Data
getwd()
setwd("C:/Users/shubham.arora/Desktop/Coursera_Cleaning_Data")
input_data <-read.csv("input_data.csv")


#1.
str(input_data)
data_1 <- input_data[input_data$VAL == 24,]

summary(data_1$SERIALNO)



#3.
row <- 18:23
col <- 7:15
input_data_2 <- read.xlsx("input_data_2.csv", colIndex = col, rowIndex = row)


#4.
library(XML)
fileurl <- "C:/Users/shubham.arora/Desktop/Coursera_Cleaning_Data/getdata%2Fdata%2Frestaurants.xml"
doc <- xmlTreeParse(fileurl,useInternal=TRUE)
rootnode <- xmlRoot(doc)
xmlName(rootnode)

xmlSApply(rootnode,"//li[@class='zipcode']",xmlValue)



