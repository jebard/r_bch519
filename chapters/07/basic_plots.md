# Basic plots in R

Basic plots in R are easily generated using functions like plot() or hist(), allowing users to visualize data distributions, relationships, and trends quickly. These plots serve as fundamental tools for exploratory data analysis, providing insights into the structure and characteristics of datasets before more advanced analyses are performed.

```R
my_points <- c(1,5,3,8,9,11)
plot(my_points)
barplot(my_points)
boxplot(my_points)
``` 
As you can see, very easy to generate a basic plot with minimal effort. There are many built in plot types, so feel free to explore generating these.

The plot() function also takes in a variety of parameters to customize the appearance of plots. Some basic options:

 - x: The x-axis data.
 - y: The y-axis data.
 - type: The type of plot to be drawn (e.g., "p" for points, "l" for lines, "b" for both).
 - main: The main title of the plot.
 - xlab: The label for the x-axis.
 - ylab: The label for the y-axis.
 - xlim: Limits for the x-axis.
 - ylim: Limits for the y-axis.
 - col: Color of the plotted elements.
 - pch: Symbol or character to use for plotting points.
 - lwd: Line width.
 - cex: Character expansion factor (for text and symbols).

```R
my_points <- c(1,5,3,8,9,11)
plot(my_points, type = "b")  # make a plot with both points and lines
plot(my_points, type = "b", col = "red", lwd=3)
```

The basic graphing functions in R are quite strong, but are some-what limited in flexibilty and we typically instead move on to another wonderful package: ggplot2.

## Behold the power of ggplot2
ggplot2 is a powerful R package for creating data visualizations. It is based on the grammar of graphics, allowing users to build complex plots layer by layer with a simple and intuitive syntax. 

```R
# Create example data
data <- data.frame(
  x = c(1, 2, 3, 4, 5),
  y = c(2, 3, 5, 4, 6)
)

# Create the plot
ggplot(data, aes(x = x, y = y)) + 
  geom_point() +
  labs(title = "Simple Scatter Plot", 
       x = "X-axis", 
       y = "Y-axis")
```

As you can see, the basic ggplot() function ingests a dataframe object, and specifies the x and y of the plot. Next we "+" an additional layer, instructing
ggplot to "add" the geom_point() to the base plot. Then again we "add" the labels, for the title, x and y axis. Here is another more complicated example to try:

```R
# Create example data
set.seed(123)
data <- data.frame(
  x = rnorm(100, mean = 5, sd = 2),
  y = 2 * data$x + rnorm(100, mean = 0, sd = 1)
)

# Create the plot
ggplot(data, aes(x = x, y = y)) + 
  geom_point() +                       # Add points
  geom_smooth(method = "lm", se = FALSE, color = "red") +  # Add linear regression line
  labs(title = "Scatter Plot with Linear Regression", 
       x = "X-axis", 
       y = "Y-axis")
```
Here you can see we added an additional layer on more complicated data to quickly add a linear regression line and color it red. Pretty quick and easy!


