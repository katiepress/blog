---
title: 'Tidy Tuesday: Olympic Medals'
author: Katie Press
date: '2021-07-26'
slug: tidy-tuesday-olympic-medals
categories:
  - TidyTuesday
tags:
  - Animation
  - Olympics
autoThumbnailImage: false
thumbnailImage: /img/still_plot_small.png
thumbnailImagePosition: top
coverImage: /img/still_plot.png
coverMeta: out
coverSize: partial
metaAlignment: center
summary: "Creating an animated bump chart of Olympic medals over time with ggplot2"
---

<script src="/rmarkdown-libs/core-js/shim.min.js"></script>
<script src="/rmarkdown-libs/react/react.min.js"></script>
<script src="/rmarkdown-libs/react/react-dom.min.js"></script>
<script src="/rmarkdown-libs/reactwidget/react-tools.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/reactable-binding/reactable.js"></script>
<script src="/rmarkdown-libs/core-js/shim.min.js"></script>
<script src="/rmarkdown-libs/react/react.min.js"></script>
<script src="/rmarkdown-libs/react/react-dom.min.js"></script>
<script src="/rmarkdown-libs/reactwidget/react-tools.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/reactable-binding/reactable.js"></script>
<script src="/rmarkdown-libs/core-js/shim.min.js"></script>
<script src="/rmarkdown-libs/react/react.min.js"></script>
<script src="/rmarkdown-libs/react/react-dom.min.js"></script>
<script src="/rmarkdown-libs/reactwidget/react-tools.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/reactable-binding/reactable.js"></script>
<script src="/rmarkdown-libs/core-js/shim.min.js"></script>
<script src="/rmarkdown-libs/react/react.min.js"></script>
<script src="/rmarkdown-libs/react/react-dom.min.js"></script>
<script src="/rmarkdown-libs/reactwidget/react-tools.js"></script>
<script src="/rmarkdown-libs/htmlwidgets/htmlwidgets.js"></script>
<script src="/rmarkdown-libs/reactable-binding/reactable.js"></script>
<!--more-->

## Background

This week’s Tidy Tuesday data is from the Olympic games over time. I thought it would be interesting to create a chart of the countries with the most medals at each Olympic games to see how things changed over time.

## Data Import and Cleaning

``` r
knitr::opts_chunk$set(echo = TRUE,message=FALSE,warning=FALSE)
library(tidyverse)
library(lubridate)
library(janitor)
library(ggplot2)
library(gganimate)
library(ggflags)
library(countrycode)
library(reactable)
#devtools::install_github("rensa/ggflags")
```

Get the provided data from the tidytuesdayR package first. I was expecting one file but there were two, so now I have a list of dataframes which I can unlist into my global environment. I’m not sure if I’ll need the second dataset (regions), but I will go ahead and add them to the olympics dataset just in case.

``` r
data <- tidytuesdayR::tt_load('2021-07-27')
```

    ## 
    ##  Downloading file 1 of 2: `olympics.csv`
    ##  Downloading file 2 of 2: `regions.csv`

``` r
list2env(data, .GlobalEnv)
```

    ## <environment: R_GlobalEnv>

``` r
regions <- regions %>% 
  clean_names()

olympics <- olympics %>% 
  left_join(regions)
```

Count the Olympic medals by country by year. I’m counting one medal per event otherwise they would be over-counted due to the team events since every person on the team gets a medal. I need to use season and not just year when I’m aggregating, because some of the older events had summer and winter Olympics in the same year. Also adding the total medals per region/year.

``` r
year_df <- olympics %>% 
  count(year, region, season, event, medal) %>% 
  count(year, region, season, medal) %>% 
  filter(!is.na(medal)) %>% 
  rename("medal_n" = n)

year_df <- year_df %>% 
  group_by(year, season, region) %>% 
  mutate(medal_total = sum(medal_n)) %>% 
  ungroup()
```

Add the number of athletes by country by year. Using extra demographic variables in case any athletes have the same name.

``` r
year_df <- olympics %>% 
  count(year, season, region, sex, age, name) %>% 
  count(year, season, region) %>% 
  rename("athlete_total" = n) %>% 
  right_join(year_df)
```

Now I have to decide which counties to include in the chart since there are so many. Let’s look at the average number of medals over the last 10 Olympic games. This will be separate for summer and winter because the number and type of events is different for the winter games. I’m just going to save these country names in a vector called “summer.top.10.”

``` r
year_df %>%
  filter(season == "Summer", year > 1979) %>%
  distinct(year, region, medal_total) %>%
  group_by(region) %>%
  summarise(avg_medals = round(mean(medal_total), 2)) %>%
  arrange(desc(avg_medals)) %>%
  react_table()
```

<div id="htmlwidget-1" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-1">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"region":["USA","Russia","Germany","China","UK","Australia","France","South Korea","Japan","Italy","Cuba","Ukraine","Romania","Hungary","Canada","Netherlands","Bulgaria","Poland","Belarus","Spain","Kazakhstan","Brazil","Sweden","New Zealand","Czech Republic","Kenya","Azerbaijan","Denmark","Serbia","Jamaica","Norway","Turkey","Ethiopia","North Korea","Greece","Uzbekistan","Switzerland","Georgia","South Africa","Iran","Croatia","Finland","Slovakia","Mexico","Argentina","Indonesia","Lithuania","Belgium","Slovenia","Thailand","Armenia","Nigeria","Austria","Colombia","Taiwan","Latvia","Zimbabwe","Individual Olympic Athletes","Ireland","Mongolia","Morocco","Algeria","Egypt","Malaysia","Estonia","India","Namibia","Tanzania","Trinidad","Tunisia","Portugal","Venezuela","Moldova","Bahamas","Bahrain","Chile","Israel","Ivory Coast","Kyrgyzstan","Saudi Arabia","Dominican Republic","Puerto Rico","Costa Rica","Tajikistan","Vietnam",null,"Qatar","Afghanistan","Barbados","Botswana","Burundi","Cameroon","Curacao","Cyprus","Djibouti","Ecuador","Eritrea","Fiji","Gabon","Ghana","Grenada","Guatemala","Guyana","Iceland","Jordan","Kosovo","Kuwait","Lebanon","Macedonia","Mauritius","Montenegro","Mozambique","Niger","Pakistan","Panama","Paraguay","Peru","Philippines","Senegal","Sri Lanka","Sudan","Suriname","Syria","Togo","Tonga","Uganda","United Arab Emirates","Uruguay","Virgin Islands, US","Zambia"],"avg_medals":[111.33,98.89,70.6,60.56,35.5,33.3,31.3,27.22,26.67,26.4,22.62,21,20.4,20.33,19.89,16.1,15.78,15.44,14,13.7,11.67,11,10.5,9.89,9.22,9,7.33,7.2,7,6.4,6.11,5.89,5.88,5.88,5.7,5.5,5.4,5.33,5,4.88,4.71,4.7,4.67,3.9,3.75,3.75,3.57,3.5,3.29,3.22,3.2,3.14,3,3,2.75,2.67,2.67,2.5,2.5,2.5,2.44,2.43,2.4,2.2,2.17,2.14,2,2,2,2,1.88,1.83,1.75,1.71,1.5,1.5,1.5,1.5,1.5,1.5,1.4,1.4,1.33,1.33,1.33,1.33,1.25,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1,1]},"columns":[{"accessor":"region","name":"region","type":"character"},{"accessor":"avg_medals","name":"avg_medals","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"44a43d222837c06b5d5bee56425c4958","key":"44a43d222837c06b5d5bee56425c4958"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

And here are the top countries for the winter games, which I will save in a winter.top.10 vector.

``` r
year_df %>%
  filter(season == "Winter", year > 1979) %>%
  distinct(year, region, medal_total) %>%
  group_by(region) %>%
  summarise(avg_medals = round(mean(medal_total), 2)) %>%
  arrange(desc(avg_medals)) %>%
  react_table()
```

<div id="htmlwidget-2" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-2">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"region":["Germany","Russia","USA","Norway","Austria","Canada","Italy","Switzerland","Netherlands","Finland","China","South Korea","Sweden","France","Czech Republic","Japan","Poland","Slovenia","Croatia","Belarus","Estonia","Latvia","Liechtenstein","Australia","Luxembourg","Serbia","Kazakhstan","Ukraine","Slovakia","UK","Bulgaria","Belgium","Denmark","Hungary","New Zealand","North Korea","Spain","Uzbekistan"],"avg_medals":[28.2,22.3,18.7,17.8,13.8,13.8,9,8.9,8.78,8,7.57,7.57,7.5,7.4,4.11,4.1,4,3.75,2.75,2.5,2.33,2.33,2.33,2,2,2,1.75,1.75,1.67,1.62,1.5,1,1,1,1,1,1,1]},"columns":[{"accessor":"region","name":"region","type":"character"},{"accessor":"avg_medals","name":"avg_medals","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"7dd52905b79de4a0639bace79cdced66","key":"7dd52905b79de4a0639bace79cdced66"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

Now filter to get the medals per year for the top 10 countries (by season as well). I can use seq\_along to order them 1 through 10 after grouping by year. However, there is going to be a problem because in some years, multiple regions have the same number of medals. For example, in 1988, Italy, Japan, and Australia each have 14 medals.

``` r
summer_medals <- year_df %>% 
  filter(season == "Summer", year > 1979, region %in% summer.top.10) %>%
  distinct(year, region, medal_total) %>% 
  arrange(year, desc(medal_total)) %>% 
  group_by(year) %>% 
  mutate(rank = seq_along(medal_total))

summer_medals %>% 
  get_dupes(year, medal_total) %>% 
  react_table()
```

<div id="htmlwidget-3" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-3">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"year":[1984,1984,1988,1988,1988,2000,2000,2000,2000,2004,2004,2008,2008,2012,2012,2012,2012,2016,2016],"medal_total":[32,32,14,14,14,28,28,58,58,30,30,41,41,28,28,35,35,42,42],"dupe_count":[2,2,3,3,3,2,2,2,2,2,2,2,2,2,2,2,2,2,2],"region":["China","Italy","Australia","Italy","Japan","South Korea","UK","Australia","China","South Korea","UK","France","Germany","Italy","South Korea","Australia","France","France","Germany"],"rank":[4,5,8,9,10,8,9,3,4,9,10,6,7,9,10,7,8,5,6]},"columns":[{"accessor":"year","name":"year","type":"numeric"},{"accessor":"medal_total","name":"medal_total","type":"numeric"},{"accessor":"dupe_count","name":"dupe_count","type":"numeric"},{"accessor":"region","name":"region","type":"character"},{"accessor":"rank","name":"rank","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"64eb2ebbdad57405a9ae7cfeac6f4b05","key":"64eb2ebbdad57405a9ae7cfeac6f4b05"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

I could rank them with a random tie-breaker, but I think I’m going to try something else. I’ll make a new column for the previous rank, and then order by year, medal number, and previous rank. That way if the number of medals is tied, it will rely on the previous year’s ranking to break the tie. This will also mean that more regions can stay the same from one year to another instead of bouncing all around due to a random tie breaker, which I think will make the chart much easier to read.

``` r
summer_medals <- summer_medals %>% 
  arrange(region, year) %>% 
  group_by(region) %>% 
  mutate(prev_rank = lag(rank)) %>% 
  #get_dupes(year, medal_total) %>% 
  arrange(year, desc(medal_total), prev_rank) %>% 
  group_by(year) %>% 
  mutate(final_rank = seq_along(region)) %>% 
  ungroup()

summer_medals %>% 
  filter(year != 1980) %>% 
  react_table()
```

<div id="htmlwidget-4" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-4">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"year":[1984,1984,1984,1984,1984,1984,1984,1984,1984,1988,1988,1988,1988,1988,1988,1988,1988,1988,1988,1992,1992,1992,1992,1992,1992,1992,1992,1992,1992,1996,1996,1996,1996,1996,1996,1996,1996,1996,1996,2000,2000,2000,2000,2000,2000,2000,2000,2000,2000,2004,2004,2004,2004,2004,2004,2004,2004,2004,2004,2008,2008,2008,2008,2008,2008,2008,2008,2008,2008,2012,2012,2012,2012,2012,2012,2012,2012,2012,2012,2016,2016,2016,2016,2016,2016,2016,2016,2016,2016],"region":["USA","Germany","UK","Italy","China","Japan","France","Australia","South Korea","Germany","Russia","USA","South Korea","China","UK","France","Italy","Japan","Australia","Russia","USA","Germany","China","France","South Korea","Australia","Japan","UK","Italy","USA","Germany","Russia","China","Australia","France","Italy","South Korea","UK","Japan","USA","Russia","China","Australia","Germany","France","Italy","South Korea","UK","Japan","USA","Russia","China","Australia","Germany","Japan","France","Italy","South Korea","UK","USA","China","Russia","UK","Australia","Germany","France","South Korea","Italy","Japan","USA","China","Russia","UK","Germany","Japan","Australia","France","South Korea","Italy","USA","China","UK","Russia","Germany","France","Japan","Australia","Italy","South Korea"],"medal_total":[173,59,37,32,32,31,28,24,19,142,131,94,33,28,24,16,14,14,14,112,108,82,53,29,28,27,22,20,19,101,65,63,51,41,37,35,27,15,14,91,89,58,58,56,38,34,28,28,18,101,90,64,50,49,37,33,32,30,30,110,100,72,48,46,41,41,31,27,25,103,89,82,65,44,38,35,35,28,28,121,70,67,56,42,42,41,29,28,21],"rank":[1,2,3,5,4,6,7,8,9,1,2,3,4,5,6,7,9,10,8,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,4,3,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,7,6,8,9,10,1,2,3,4,5,6,7,8,10,9,1,2,3,4,6,5,7,8,9,10],"prev_rank":["NA",2,3,4,"NA","NA",5,6,"NA",2,1,1,9,4,3,7,5,6,8,2,3,1,5,7,4,8,10,6,9,2,3,1,4,7,5,10,6,9,8,1,3,4,5,2,6,7,8,9,10,1,2,4,3,5,10,6,7,8,9,1,3,2,10,4,5,7,9,8,6,1,2,3,4,7,10,5,6,8,9,1,2,4,3,5,8,6,7,9,10],"final_rank":[1,2,3,4,5,6,7,8,9,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10,1,2,3,4,5,6,7,8,9,10]},"columns":[{"accessor":"year","name":"year","type":"numeric"},{"accessor":"region","name":"region","type":"character"},{"accessor":"medal_total","name":"medal_total","type":"numeric"},{"accessor":"rank","name":"rank","type":"numeric"},{"accessor":"prev_rank","name":"prev_rank","type":"numeric"},{"accessor":"final_rank","name":"final_rank","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"a5442c2a0d7220188f856a6ed56157f9","key":"a5442c2a0d7220188f856a6ed56157f9"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
temp_levels <- summer_medals %>% 
  filter(year == 1988) %>% 
  mutate(region = factor(region)) %>% 
  mutate(region = fct_reorder(region, final_rank))

summer_medals <- summer_medals %>% 
  mutate(region = factor(region, levels = temp_levels$region))

summer_medals$team_country <- countrycode(summer_medals$region, "country.name", "iso2c")

summer_medals <- summer_medals %>% mutate(team_country = str_to_lower(team_country))
```

For the plot I decided to start at 1988, because that is the first year that all 10 countries were in the games. This way the chart will be consistent from beginning to end. What I’m doing here is making sure that I have the theme and look of the plot the way I want it before I animate it. Notes on this:

-   For the geom\_point I had to add the grouping aesthetic because if I didn’t, the lines would show up in the animation and the points would not, although the geom\_flag worked fine. I tried a bunch of different things and finally got this to work so hopefully it saves someone else the aggravation.
-   I used alpha in geom\_line to make it slightly more transparent, this is just a stylistic choice and could be deleted for a solid color line.
-   In the geom\_flag I commented out the filter that I use on the final animated plot so that all the dots are not covered by flags and I can make sure the dots look the way I want them to. I decided to use solid color and no alpha for the points.
-   The color scheme was inspired by this [cover image from Sports Illustrated](https://www.si.com/.image/c_limit%2Ccs_srgb%2Cq_auto:good%2Cw_700/MTgwMjA0NjA1NjA1NDIyMjAy/dcovtokyo_v.webp)

``` r
summer_medals %>% 
  filter(year >= 1988) %>% 
  ggplot(., aes(x = year, y = final_rank, color = region)) +
  geom_point(aes(group = seq_along(final_rank), color = region), size = 4) +
  geom_line(aes(color = region, alpha=1), size = 2) +
  scale_x_continuous(breaks = seq(1980, 2016, 4))+
  scale_y_reverse(breaks = seq(1, 10, 1))+ 
  scale_color_manual(values = olympic.pal2)+
  geom_flag(data = summer_medals %>% 
              #filter(year >1984), 
              filter(year == 1988),
            aes(country = team_country),
            size = 8) +
  ggtitle("Countries With the Most Olympic Medals by Year")+
    ylab("Rank")+
  labs(caption = "@katie_press | kpress.dev")+
  theme_minimal()+
  my_theme
```

<img src="/post/2021-07-26-tidy-tuesday-olympic-medals/index.en-us_files/figure-html/unnamed-chunk-13-1.png" width="672" />

Now for the final plot all I’m doing is adding transition\_reveal using the year as the reveal, and saving as an object.

``` r
final.plot <- summer_medals %>% 
  filter(year >= 1988) %>% 
  ggplot(., aes(x = year, y = final_rank, color = region)) +
  geom_point(aes(group = seq_along(final_rank), color = region), size = 4) +
  geom_line(aes(color = region, alpha=1), size = 2) +
  scale_x_continuous(breaks = seq(1980, 2016, 4))+
  scale_y_reverse(breaks = seq(1, 10, 1))+ 
  scale_color_manual(values = olympic.pal2)+
  geom_flag(data = summer_medals %>% filter(year >1984), 
            aes(country = team_country),
            size = 8) +
  ggtitle("Countries With the Most Olympic Medals by Year")+
    ylab("Rank")+
  labs(caption = "@katie_press | kpress.dev")+
  theme_minimal()+
  my_theme +
  transition_reveal(year)
```

Finally I can save the animation as a gif to share. I’m using end\_pause here so that my gif pauses for a few seconds once it gets to the end of the animation.

``` r
final.animated <- animate(final.plot, renderer = gifski_renderer("olympics.gif"), width = 8, height = 5, units = "in", res = 300, dev= "png", end_pause = 10)
```

<img src="/img/olympics.gif" alt="Olympic Medals" class="center">
