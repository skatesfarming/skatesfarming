- 👋 Hi, I’m @skatesfarming
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
skatesfarming/skatesfarming is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

# Warm up exercise
#  Part b)
# i.
8+3
# ii.
9*8
# iii.
(16+7)*33
# iv.
sqrt(169)


# Part c) Create a vector with the elements (1,2,3,4,5,6,7,8,9,10) and call it x:
x<- c(1,2,3,4,5,6,7,8,9,10)   # we can use the arrow aswell it means that this
                              # expression() goes into this <-
x = c(1,2,3,4,5,6,7,8,9,10)


# Part d) Find the mean, median and standard deviation of x:
Mean.X = mean(x)
Median.X = median(x)
Stand.DEV.X = sd(x)
# NB that I have calculated the mean, median and sd of x and give them a variable name. 
# Thus, they will appear on the global environment. They answer will also appear in the 
# console window if you type the name of the variable, e.g.
Mean.X
Median.X
Stand.DEV.X

# Part e) Use logical expressions to find which elements of x are 
# i.
x>5       # This gives you a vector with the logical expression TRUE and FALSE for each element of the vector x regarding the condition x>5
x[x>5]    # This gives you the elements of vector x that are bigger than 5
# ii.
x==3
x[x==3]
# iii.
x<7&x>2
x[x<7&x>2]


# part f) Create another vector "y" where every element is the square of the corresponding element in "x": y=x^2
y = x^2

# Part g) Create a scatter plot of y as a function of x. Format the plot with lines and colours
plot(x,y, type = "l", xlab = "X variable", ylab = "Y variable", col = "red", main = "scatterplot of y=x^2", lwd = 0.3)



# Part h) 	Create a vector of character strings with 10 names of students in the class (call it "StudentNames"). 
# Also create a vector of their heights ("StudentHeights"), and use "StudentNames" to name the corresponding elements 
# in "StudentHeights".
StudentNames<-c("Peter 1", "Peter 2", "Peter 3","Peter 4", "Peter 5", "Peter 6", "Peter 7", "Peter 8","Peter 9", "Peter 10") # Vector with student names
StudentHeights<- c(123,234,222,333,412,123,100,40,333,678) # vector with student heights
names(StudentHeights)<-StudentNames 
# using function names() to name every element in vector StudentHeights with the corresponding element in vector StudentNames



# Exercise 1: Generating data from a distribution
# Part a) a)	Generate 100 points from a normal (bell-curve) distribution, with a 
# mean of 0 and a standard deviation of 1, and store them in a vector called "Random".
Random<-rnorm(100, mean = 0, sd = 1)


# Part b)	Create a histogram of the vector "random"
hist(Random)
# if you want to change the bin colours or the axis labels type ?hist() in the console window


# Part c) Repeat a) and b) but with the uniform distribution.
Random.unif=runif(100, min=-2, max = 2)
hist(Random.unif)


# Part d)	Create three more vectors:
  # a. a vector of 1000 evenly spaced elements between 0 and 1,
  seq(from = 0, to = 1, length.out = 1000)
  length(seq(from = 0, to = 1, length.out = 1000)) # A way to check the length of a vector

  # b.	a vector in which the first 500 elements are the word "Male" and the second 500 elements are the word "Female",
  rep(c("Male", "Female"), each= 500)

  # c.	and a vector where the sequence 1,2,3 is repeated 10 times.
  rep(c(1,2,3), times = 10)

  
  
  
# Exercise 2:	Importing your own data
# Part a)	Import the plantGrowthExpt.csv data into a dataframe called "plantGrowthExpt"
Plant.Data=read.csv("plantGrowthExpt.csv")
# or file.choose()

# Make sure you set your working directory and keep or your data files in the same folder you have your R scripts

Plant.Data$treatment#just used to display that row 
View(plant_data) #To see full data 

# part b)	Calculate the mean of the "height.cm" column.
mean(Plant.Data$height.cm)

# part c)	Plot the "biomass.gm" column as a function of "height.cm".
plot(Plant.Data$height.cm, Plant.Data$biomass.gm, xlab = "Height (cm)", ylab = "Biomass (gm)", pch = 19)

# part d) Find the line of best fit and plot it on the same figure as the previous plot. 
Linear.model= lm(Plant.Data$biomass.gm ~ Plant.Data$height.cm) # Produces a linear model for the dataset

abline(Linear.model, col = "red", lwd = 3) # Addsthe linear model line to the previous plot 

volume_pyramid = function(l, w, h)
{
  volume = (l * w * h)/3
  
  return(volume)
}
volume_pyramid(l=2, w=5, h=4)
