# casestudydsView(data$age)
str(data)
summary(data$smoker)
summary(data$age)
hist(data$age,col="red")

hist(data$bmi)
hist(data,col="green")
head(data)
str(data)
hist(data$charges,col="darkcyan")
head(data)
#shape of dataset
dim(data)
#type of data
str(data)
is.null(data$age)
is.null(data$sex)
is.null(data$bmi)
is.null(data$children)
is.null(data$smoker)
is.null(data$region)
data2 <- data[,-2]
data2
str(data2)
str(data)
data3 <- data2[,-4]
dataset <-data3[,-4]
str(dataset)
summary(dataset)
#removing duplicates in the dataset
fdataset <- dataset[!duplicated(dataset),]
str(fdataset)
#checking weather null values in dataset
is.null(fdataset)
#histogram
hist(fdataset$age,col="green")
hist(fdataset$bmi,col="cyan")
hist(fdataset$children,col="lightblue")
df1 <- data
df1$sex <- as.numeric(as.character(df1$sex))
df1$sex
x <- ggplot(dataset, aes(age, charges)) +
  geom_jitter(color = "blue", alpha = 0.5) +
  theme_light()
view(x)
