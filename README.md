# google-data-analytics-professional-certificate

`monday, october 02, 2023`

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

`tuesday, october 03, 2023`

ggplot(data=penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g))

ggplot(data=penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g, color=species))

ggplot(data=penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g, shape=species))

ggplot(data=penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g, shape=species, color=species))

ggplot(data=penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g, shape=species, color=species, size=species))

ggplot(data=penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g, alpha=species))

ggplot(data=penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g, color="purple"))


`note: aesthetics for points include x, y, color, shape, size, and alpha`

ggplot(data = penguins) +
  geom_smooth(mapping = aes(x=flipper_length_mm, y=body_mass_g)) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g))

ggplot(data=penguins) +
  geom_smooth(mapping = aes(x=flipper_length_mm, y=body_mass_g, linetype=species))




