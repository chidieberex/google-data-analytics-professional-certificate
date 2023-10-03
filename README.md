# google-data-analytics-professional-certificate

r programming language:

install.packages("ggplot2")
install.packages("palmerpenguins")
install.packages("tidyverse")

library(ggplot2)
library(palmerpenguins)
library(tidyverse)

data(penguins)
View(penguins)

ggplot(data=penguins, mapping=aes(x=flipper_length_mm, y=body_mass_g)) + geom_point()

ggplot(data=penguins) + geom_point(mapping=aes(x=flipper_length_mm, y=body_mass_g))

ggplot(data = penguins) + geom_point(mapping = aes(x=bill_length_mm, y=bill_depth_mm))


?geom_bar

?geom_point
