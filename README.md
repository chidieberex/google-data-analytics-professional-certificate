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

ggplot(data = penguins) +
  geom_jitter(mapping = aes(x=flipper_length_mm, y=body_mass_g))

ggplot(data = diamonds) +
  geom_bar(mapping = aes(x=cut))

ggplot(data = diamonds) +
  geom_bar(mapping = aes(x=cut, color=cut))

ggplot(data = diamonds) +
  geom_bar(mapping = aes(x=cut, fill=cut))

ggplot(data = diamonds) +
  geom_bar(mapping = aes(x=cut, fill=clarity))


`tuesday, october 03, 2023 at about 10:20 cst`

ggplot(data = penguins) +
  geom_point(mapping = aes(x=flipper_length_mm, y=body_mass_g)) +
  facet_wrap(~species)


`wednesday, october 04, 2023 at about 03:20 cst`

`lesson 7 week 4 hands-on activities`

hotel_bookings <- read.csv("hotel_bookings.csv")

head(hotel_bookings)

colnames(hotel_bookings)

install.packages('ggplot2')
library(ggplot2)

ggplot(data = hotel_bookings) +
  geom_bar(mapping = aes(x = distribution_channel))

ggplot(data = hotel_bookings) +
  geom_bar(mapping = aes(x = distribution_channel, fill=deposit_type))

ggplot(data = hotel_bookings) +
  geom_bar(mapping = aes(x = distribution_channel, fill=market_segment))

ggplot(data = hotel_bookings) +
  geom_bar(mapping = aes(x = distribution_channel)) +
  facet_wrap(~deposit_type)

ggplot(data = hotel_bookings) +
  geom_bar(mapping = aes(x = distribution_channel)) +
  facet_wrap(~deposit_type) +
  theme(axis.text.x = element_text(angle = 45))

ggplot(data = hotel_bookings) +
  geom_bar(mapping = aes(x = distribution_channel)) +
  facet_wrap(~market_segment) +
  theme(axis.text.x = element_text(angle = 45))

ggplot(data = hotel_bookings) +
  geom_bar(mapping = aes(x = distribution_channel)) +
  facet_grid(~deposit_type) +
  theme(axis.text.x = element_text(angle = 45))

ggplot(data = hotel_bookings) +
  geom_bar(mapping = aes(x = distribution_channel)) +
  facet_wrap(~deposit_type~market_segment) +
  theme(axis.text.x = element_text(angle = 45))

























