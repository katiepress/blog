---
title: 'The Office Part I: Employee Attrition'
author: Katie Press
date: '2021-06-22'
slug: the-office-part-i
categories:
  - Projects
tags:
  - Datasets
  - Modeling
  - The Office
autoThumbnailImage: false
thumbnailImage: /img/jobrole_small.png
thumbnailImagePosition: bottom
coverImage: /img/jobrole.png
metaAlignment: center
summary: "Ask me about regression modeling and if you don't, I'll tell you anyway"
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

# Background

This post is partially inspired by one of my favorite blogs ever, [Ask a Manager](https://www.askamanager.org). I am obsessed with this content - partly because Alison (the writer) is super smart and gives good advice, partly for the pure entertainment value. I’ll be linking to some great posts along the way, but in the meantime here is a [list of Alison’s favorite posts ever](https://www.askamanager.org/favorite-posts).

In the past whenever I needed to create a predictive model, I was always frustrated because I wanted to know what the best model would be given all possible combinations of variables. But you wouldn’t want to test all combinations of all variables, because some of them are too similar and would over-inflate the model. For example, I wouldn’t use a variable like “age at event x” and another variable “age over 18 at event x” in one model.

A few weeks ago I was taking an online Python course and the course was covering truth tables, which look like this:

<div id="htmlwidget-1" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-1">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"A":["T","T","F","F"],"B":["T","F","T","F"],"A or B":["T","T","T","F"]},"columns":[{"accessor":"A","name":"A","type":"character"},{"accessor":"B","name":"B","type":"character"},{"accessor":"A or B","name":"A or B","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"3cfd29b6f3d066606c9d8f2556fa7b45","key":"3cfd29b6f3d066606c9d8f2556fa7b45"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

In order for the third column (A or B) to be true, either A or B, or both A and B need to be true.

I realized I needed to do was figure out how to recreate a truth table where each column represents a group of potential variables for the model. This post is based on a real project, but I needed some publicly-available data to demonstrate with. I know there is a heart disease that is often used for prediction, but that’s kind of…boring. Also there weren’t that many variables.

Then I came across this HR employee attrition dataset on [Kaggle](https://www.kaggle.com/vjchoudhary7/hr-analytics-case-study?select=general_data.csv) and thought that might be more interesting, given some of the crazy stories I’ve read on Ask a Manager over the years that often resulted in people leaving,, sometimes in rather [spectacular fashion](https://www.askamanager.org/2017/10/resigning-via-cod-a-glorious-out-of-office-message-and-other-quitting-stories.html).

In this post I’ll cover a little bit of data import and cleaning, visualization, and finally how to create a *bunch* of models at once. I’ve loaded the following packages:

-   tidyverse
-   lubridate
-   janitor
-   knitr
-   ggplot2
-   readxl
-   ggridges
-   broom
-   glue

# Data Import

I downloaded the csv files from [Kaggle](https://www.kaggle.com/vjchoudhary7/hr-analytics-case-study?select=general_data.csv) and created an R Project in the same folder.

-   Get list of csv files
-   Use purrr::map to read csv into a list of tibbles
-   Name the tibbles in the list (this is why I put “full.names = TRUE”)
-   Map over the tibbles with janitor’s clean\_names function to make the column names all lower case separated by underscores.

``` r
temp.list <- list.files(full.names = TRUE, pattern = "*.csv", path = "~/Desktop/Rproj/employee/")

data_list <- map(temp.list, read_csv)

names(data_list) <- word(temp.list, -2, sep = "/|\\.csv")

data_list <- data_list %>% 
  map( ~.x %>% clean_names)
```

I have a list of five tibbles, two of which are timestamp datasets and not in tidy format yet.

``` r
summary(data_list)
```

    ##                      Length Class       Mode
    ## employee_survey_data   4    spec_tbl_df list
    ## general_data          24    spec_tbl_df list
    ## in_time              262    spec_tbl_df list
    ## manager_survey_data    3    spec_tbl_df list
    ## out_time             262    spec_tbl_df list

## General Data

We have a general dataset, a manager survey, and an employee survey. These three tables can be joined on employee ID.

Side note: If you are a manager, try not to force your employees to [complete a daily mental health survey](https://www.askamanager.org/2020/07/my-manager-makes-us-do-mental-health-surveys-every-day.html), it’s not a great look and [they’ll probably all quit](https://www.askamanager.org/2020/12/update-my-manager-makes-us-do-mental-health-surveys-every-day.html).

``` r
data <- data_list$general_data %>%
  left_join(data_list$employee_survey_data) %>%
  left_join(data_list$manager_survey_data) %>%
  select(employee_id, everything())
```

## Time Data

This is what the time data looks like currently. Notice each column is a date, except for the first one which corresponds to the employee ID. This is exactly what tidyr is for.

<div id="htmlwidget-2" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-2">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"x1":[1,2,3,4,5,6],"x2015_01_01":[null,null,null,null,null,null],"x2015_01_02":["2015-01-02T09:43:45","2015-01-02T10:15:44","2015-01-02T10:17:41","2015-01-02T10:05:06","2015-01-02T10:28:17","2015-01-02T09:43:08"],"x2015_01_05":["2015-01-05T10:08:48","2015-01-05T10:21:05","2015-01-05T09:50:50","2015-01-05T09:56:32","2015-01-05T09:49:58","2015-01-05T10:14:00"],"x2015_01_06":["2015-01-06T09:54:26",null,"2015-01-06T10:14:13","2015-01-06T10:11:07","2015-01-06T09:45:28","2015-01-06T10:08:42"],"x2015_01_07":["2015-01-07T09:34:31","2015-01-07T09:45:17","2015-01-07T09:47:27","2015-01-07T09:37:30","2015-01-07T09:49:37","2015-01-07T10:18:15"]},"columns":[{"accessor":"x1","name":"x1","type":"numeric"},{"accessor":"x2015_01_01","name":"x2015_01_01","type":"logical"},{"accessor":"x2015_01_02","name":"x2015_01_02","type":"Date"},{"accessor":"x2015_01_05","name":"x2015_01_05","type":"Date"},{"accessor":"x2015_01_06","name":"x2015_01_06","type":"Date"},{"accessor":"x2015_01_07","name":"x2015_01_07","type":"Date"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"726fca72279d9c6f2e6441b64b1ca6fc","key":"726fca72279d9c6f2e6441b64b1ca6fc"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

Using pivot\_longer, I can preserve the employee ID in one column, put the date in another column, and the timestamp in a third column. I usually use lubridate to format dates, in this case I also had to get rid of the “x” at the beginning of the character because otherwise it would be NA. I’m also going to add the timestamps for clocking out.

``` r
time_data <- data_list$in_time %>%
  pivot_longer(!x1, names_to = "date", values_to = "time_in") %>%
  mutate(date = ymd(str_remove_all(date, "x"))) %>%
  left_join(
    data_list$out_time %>%
      pivot_longer(!x1, names_to = "date", values_to = "time_out") %>%
      mutate(date = ymd(str_remove_all(date, "x")))
  ) %>% 
  rename("employee_id" = x1)
```

Create some additional variables for aggregation later. This would be especially useful for any [nosy coworkers](https://www.askamanager.org/2015/01/my-coworker-is-trying-to-track-my-hours-and-pto.html) who might want to [track your hours](https://www.askamanager.org/2014/09/my-coworker-is-tracking-my-hours.html).

-   Number of hours worked each day
-   Week column

``` r
time_data <- time_data %>% 
  mutate(hours = round(time_length(time_in %--% time_out, "hour"), 2)) %>% 
  mutate(hours = replace_na(hours, 0)) %>% 
  mutate(week = week(date))
```

Much better

<div id="htmlwidget-3" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-3">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"employee_id":[1,1,1,1,1,1],"date":["2015-01-01","2015-01-02","2015-01-05","2015-01-06","2015-01-07","2015-01-08"],"time_in":[null,"2015-01-02T09:43:45","2015-01-05T10:08:48","2015-01-06T09:54:26","2015-01-07T09:34:31","2015-01-08T09:51:09"],"time_out":[null,"2015-01-02T16:56:15","2015-01-05T17:20:11","2015-01-06T17:19:05","2015-01-07T16:34:55","2015-01-08T17:08:32"],"hours":[0,7.21,7.19,7.41,7.01,7.29],"week":[1,1,1,1,1,2]},"columns":[{"accessor":"employee_id","name":"employee_id","type":"numeric"},{"accessor":"date","name":"date","type":"Date"},{"accessor":"time_in","name":"time_in","type":"Date"},{"accessor":"time_out","name":"time_out","type":"Date"},{"accessor":"hours","name":"hours","type":"numeric"},{"accessor":"week","name":"week","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"0015e5d04f9520b79749239f5f043de6","key":"0015e5d04f9520b79749239f5f043de6"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

# Data Cleaning

Using the data dictionary Excel file provided from Kaggle, I’m recoding some of the numeric variables as factors for better visualization in charts. Also create a numeric variable for attrition (to be used later in modeling).

``` r
data <- data %>%
  mutate(education_2 = factor(
    education,
    labels = c("Below College", "College", "Bachelors", "Masters", "Doctoral"),
    ordered = TRUE
  )) %>%
  mutate(across(
    one_of(
      "environment_satisfaction",
      "job_involvement",
      "job_satisfaction"
    ),
    list("2" = ~ factor(
      ., labels = c("Low", "Medium", "High", "Very High"),
      ordered = TRUE
    ))
  )) %>%
  mutate(performance_rating_2 = factor(performance_rating, 
                                       labels = c("Excellent", "Outstanding"),
                                       ordered = TRUE)) %>%
  mutate(work_life_balance_2 = factor(work_life_balance, 
                                      labels = c("Bad", "Good", "Better", "Best"),
                                      ordered = TRUE)) %>% 
  mutate(business_travel = str_replace_all(business_travel, "_", " ")) %>% 
  mutate(attrition_2 = ifelse(attrition == "Yes", 1, 0))
```

Aggregate the timestamp data down to average hours worked per week and add to the dataset.

``` r
data <- time_data %>% 
  group_by(employee_id, week) %>% 
  summarise(week_hours = sum(hours)) %>% 
  group_by(employee_id) %>% 
  summarise(avg_weekly_hours = round(mean(week_hours, na.rm=TRUE))) %>% 
  right_join(data)
```

# Data Viz

Checking out some of the numeric variables, I can plot multiple histograms using ggplot and facet\_wrap. And here are some fun Ask a Manager posts to go along with them:

-   A reader’s direct report is [obsessed with her age](https://www.askamanager.org/2016/04/my-older-employee-has-an-issue-with-my-age.html)
-   What to do when [you’re working crazy hours and your boss reprimands you for coming in late](https://www.askamanager.org/2019/08/my-boss-lectured-me-about-arriving-on-time-when-im-working-a-ton-of-hours.html)
-   If you’re an entry level employee, maybe think twice before [giving your manager “constructive” feedback](https://www.askamanager.org/2018/10/my-entry-level-employee-gave-me-a-bunch-of-off-base-constructive-criticism.html)

``` r
data %>% 
  select("Age" = age, 
         "Average Weekly Hours" = avg_weekly_hours, 
         "Job Level" = job_level,
         "Number of Companies Worked" = num_companies_worked, 
         "Total Working Years" = total_working_years, 
         "Training Times Last Year" = training_times_last_year, 
         "Years at Company" = years_at_company,
         "Years Since Last Promotion" = years_since_last_promotion,
         "Years with Current Manager" = years_with_curr_manager) %>% 
  gather(item, number) %>% 
  ggplot(aes(number, color = item, fill = item))+
  geom_histogram(binwidth = 1)+
  facet_wrap(~item, scales = "free")+
  my_theme +
  theme(legend.position = "none",
        axis.text.y = element_blank(),
        axis.title.y = element_blank(),
        axis.title.x = element_blank(),
        axis.ticks.y = element_blank())
```

<img src="/post/2021-06-21-the-office-part-i/index.en-us_files/figure-html/unnamed-chunk-13-1.png" width="672" style="display: block; margin: auto;" />

## Bar Charts

For the categorical variables it’s not quite as easy to plot multiple charts at once. But I can start by nesting the data. This gives me a list of dataframes - one for every item I want to plot.

``` r
plot_data <- data %>% 
  select("Gender" = gender,
         "Marital Status" = marital_status,
         "Business Travel" = business_travel,
         "Work Life Balance" = work_life_balance_2,
         
         "Education" = education_2,
         "Education Field" = education_field,
         "Department" = department,
         "Job Role" = job_role,
         
         "Environment Satisfaction" = environment_satisfaction_2,
         "Job Involvement" = job_involvement_2,
         "Job Satisfaction" = job_satisfaction_2,
         "Performance Rating" = performance_rating_2
         ) %>% 
  gather(item, thing) %>% 
  count(item, thing) %>% 
  group_by(item) %>% 
  mutate(pct = n/sum(n)) %>% 
  group_nest(data = item)
```

<div id="htmlwidget-4" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-4">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"item":["Business Travel","Department","Education","Education Field","Environment Satisfaction","Gender"],"data":[{"thing":["Non-Travel","Travel Frequently","Travel Rarely"],"n":[450,831,3129],"pct":[0.102040816326531,0.18843537414966,0.70952380952381]},{"thing":["Human Resources","Research & Development","Sales"],"n":[189,2883,1338],"pct":[0.0428571428571429,0.653741496598639,0.303401360544218]},{"thing":["Bachelors","Below College","College","Doctoral","Masters"],"n":[1716,510,846,144,1194],"pct":[0.389115646258503,0.115646258503401,0.191836734693878,0.0326530612244898,0.270748299319728]},{"thing":["Human Resources","Life Sciences","Marketing","Medical","Other","Technical Degree"],"n":[81,1818,477,1392,246,396],"pct":[0.0183673469387755,0.412244897959184,0.108163265306122,0.315646258503401,0.0557823129251701,0.0897959183673469]},{"thing":["High","Low","Medium","Very High",null],"n":[1350,845,856,1334,25],"pct":[0.306122448979592,0.191609977324263,0.194104308390023,0.30249433106576,0.00566893424036281]},{"thing":["Female","Male"],"n":[1764,2646],"pct":[0.4,0.6]}]},"columns":[{"accessor":"item","name":"item","type":"character"},{"accessor":"data","name":"data","type":["vctrs_list_of","vctrs_vctr","list"]}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"05139e9d55802da7d1972ec5ba5bb2ac","key":"05139e9d55802da7d1972ec5ba5bb2ac"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

Now I can use map to iterate over the dataframes with my ggplot code. I’m actually using map2 here so that I can use the “item” column as titles for the charts (pasted in using glue). Now I have the plots in a new column and I can print them out.

``` r
plot_data <- plot_data %>%
  mutate(
    plot = map2(
      data,
      item,
      ~ ggplot(data = .x, aes(
        x = pct, y = thing, fill = thing
      )) +
        ggtitle(glue("{.y}")) +
        geom_col() +
        scale_x_continuous(labels = scales::percent_format(accuracy = 1)) +
        my_theme +
        theme(axis.title.y = element_blank(),
              axis.title.x = element_blank(),
              plot.title = element_text(size = 12))
    )
  )
```

    ## # A tibble: 6 × 3
    ##   item                                   data plot  
    ##   <chr>                    <list<tibble[,3]>> <list>
    ## 1 Business Travel                     [3 × 3] <gg>  
    ## 2 Department                          [3 × 3] <gg>  
    ## 3 Education                           [5 × 3] <gg>  
    ## 4 Education Field                     [6 × 3] <gg>  
    ## 5 Environment Satisfaction            [5 × 3] <gg>  
    ## 6 Gender                              [2 × 3] <gg>

I’m using ggarrange so that I can lay them out in a grid and make them the same size using horizontal + vertical alignment. Thankfully ggarrange already has a plotlist argument, so I don’t have to write out every plot in the list separately.

Note: If you don’t want NAs in your charts, you can replace them using fct\_explicit\_na from the forcats package.

Speaking of variables, here are some more related posts from Ask a Manager:

-   If your company has a [leadership training program for women](https://www.askamanager.org/2021/06/my-companys-leadership-programs-for-women-excludes-men.html), try not to be a jerk about it
-   Speaking of marital status, what happens when your [dad is dating your boss and they want you to go to couples therapy with them](https://www.askamanager.org/2018/05/my-dad-is-dating-my-boss-and-they-want-me-to-go-to-couples-therapy-with-them.html)?

``` r
ggpubr::ggarrange(
  plotlist = plot_data$plot,
  nrow = 4,
  ncol = 3,
  align = 'hv'
)
```

<img src="/post/2021-06-21-the-office-part-i/index.en-us_files/figure-html/unnamed-chunk-18-1.png" width="1152" style="display: block; margin: auto;" />

## Ridgeline Charts

I would like to visualize how some of the variables interact with each other. Ridgeline charts can be a good way to do that, and they look pretty cool.

``` r
ggplot(data, aes(x = monthly_income, y= job_role, fill = job_role))+
  geom_density_ridges()+
  scale_x_continuous(name = "Monthly Income", labels = scales::dollar)+
  ggtitle("Monthly Income by Job Role")+
  my_theme+
  theme(axis.title.y = element_blank())
```

<img src="/post/2021-06-21-the-office-part-i/index.en-us_files/figure-html/unnamed-chunk-19-1.png" width="768" style="display: block; margin: auto;" />

By level of education:

``` r
ggplot(data, aes(x = monthly_income, y= education_2, fill = education_2))+
  geom_density_ridges()+
  scale_x_continuous(name = "Monthly Income", labels = scales::dollar)+
  ggtitle("Monthly Income by Education Level")+
  my_theme+
  theme(axis.title.y = element_blank())
```

<img src="/post/2021-06-21-the-office-part-i/index.en-us_files/figure-html/unnamed-chunk-20-1.png" width="768" style="display: block; margin: auto;" />

# Creating the Models

Now that I’ve cleaned up and explored the data a little bit, it’s time to start the modeling process.

### Creating Variable Groups

To create my “truth table” for all possible combinations of variables to model, I need to group my variables into categories. Some of these probably could be grouped in different ways, but this is just for demonstration purposes so it doesn’t have to be perfect. I’m wrapping all the groups in the crossing() function from tidyr, which will expand these lists to all possible combinations of the different variable groups.

``` r
cross_df <- crossing(
    age = c("age", "total_working_years", "num_companies_worked"),
    demos = c("gender", "marital_status"),
    company_time = c(
      "years_at_company",
      "years_since_last_promotion",
      "years_with_curr_manager"
    ),
    work_life_balance = c(
      "distance_from_home",
      "business_travel",
      "work_life_balance",
      "avg_weekly_hours"
    ),
    level = c(
      "education",
      "job_level",
      "monthly_income",
      "stock_option_level"
    ),
    work_type = c("education_field", "department", "job_role"),
    performance = c(
      "performance_rating",
      "training_times_last_year",
      "percent_salary_hike"
    ),
    satisfaction = c("environment_satisfaction", "job_satisfaction")
  )
```

This is what the resulting tibble looks like. There are 5,184 different possible model combinations.

<div id="htmlwidget-5" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-5">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"age":["age","age","age","age","age","age"],"demos":["gender","gender","gender","gender","gender","gender"],"company_time":["years_at_company","years_at_company","years_at_company","years_at_company","years_at_company","years_at_company"],"work_life_balance":["avg_weekly_hours","avg_weekly_hours","avg_weekly_hours","avg_weekly_hours","avg_weekly_hours","avg_weekly_hours"],"level":["education","education","education","education","education","education"],"work_type":["department","department","department","department","department","department"],"performance":["percent_salary_hike","percent_salary_hike","performance_rating","performance_rating","training_times_last_year","training_times_last_year"],"satisfaction":["environment_satisfaction","job_satisfaction","environment_satisfaction","job_satisfaction","environment_satisfaction","job_satisfaction"]},"columns":[{"accessor":"age","name":"age","type":"character"},{"accessor":"demos","name":"demos","type":"character"},{"accessor":"company_time","name":"company_time","type":"character"},{"accessor":"work_life_balance","name":"work_life_balance","type":"character"},{"accessor":"level","name":"level","type":"character"},{"accessor":"work_type","name":"work_type","type":"character"},{"accessor":"performance","name":"performance","type":"character"},{"accessor":"satisfaction","name":"satisfaction","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"a383ebf86cb42f1395de98adf3b6c9c6","key":"a383ebf86cb42f1395de98adf3b6c9c6"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Creating Formulas

Now I have variables I need for the model but they’re all in different columns. I need to make it look more like the formula I’m going to use. To do that, I can use unite (also from tidyr). I’ll combine columns 1 through 8 into a new column called “formula,” separated by the plus sign because that’s the syntax the model will need as an input.

Then I paste the outcome variable (attrition\_2) in front of the formula, just like it would be in a glm model. Add a model name to help keep track of everything later on.

``` r
formula_df <- cross_df %>% 
  unite(formula, c(1:8), sep = "+") %>% 
  select(formula) %>% 
  mutate(formula = paste0("attrition_2 ~ ", formula)) %>% 
  mutate(model_name = row_number())
```

This is what the formula looks like

<div id="htmlwidget-6" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-6">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"formula":["attrition_2 ~ age+gender+years_at_company+avg_weekly_hours+education+department+percent_salary_hike+environment_satisfaction","attrition_2 ~ age+gender+years_at_company+avg_weekly_hours+education+department+percent_salary_hike+job_satisfaction","attrition_2 ~ age+gender+years_at_company+avg_weekly_hours+education+department+performance_rating+environment_satisfaction","attrition_2 ~ age+gender+years_at_company+avg_weekly_hours+education+department+performance_rating+job_satisfaction","attrition_2 ~ age+gender+years_at_company+avg_weekly_hours+education+department+training_times_last_year+environment_satisfaction","attrition_2 ~ age+gender+years_at_company+avg_weekly_hours+education+department+training_times_last_year+job_satisfaction"],"model_name":[1,2,3,4,5,6]},"columns":[{"accessor":"formula","name":"formula","type":"character"},{"accessor":"model_name","name":"model_name","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"c0638114d46e1ab1b56db320404d2219","key":"c0638114d46e1ab1b56db320404d2219"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

First I will create a function that I can map over my dataset of formulas. This is just a regular binomial logistic regression model.

``` r
mod_fun <- function(x) {glm(formula = as.formula(x), family = binomial("logit"), data = data)}
```

### Mapping the Models

Now map over the models. WARNING - this will take a minute. It’s a bit faster if you don’t ask for the odds ratios (exponentiated coefficients). If you have a very large dataset, you’re going to want to test this on just a couple of your formulas to make sure you’ve got everything set up right. If you have a really, really large dataset, you can always run it in batches as well. What this does is:

-   Map over each cell in the formula column using the formula I created
-   Using the broom package, create a new tidied column for the model summary and model fit
-   Unnest the model summary and fit info into a tidied dataframe

``` r
model_df <- formula_df %>% 
  mutate(models = map(formula, mod_fun), 
         model_summary = models %>% map(~tidy(., exponentiate = TRUE)), 
         model_fit = models %>% map(glance)) %>%
  select(model_name, model_summary, model_fit) %>%
  unnest(c(model_summary, model_fit)) %>%
  mutate_if(is.numeric, ~ round(., 3))
```

## Filtering Model Data

Now I have a tidy dataset of all the models of all possible combinations of variables in my pre-defined groups. I can filter based on whatever criteria is most important.

### Lowest AIC

For example, here is the model with the lowest AIC:

<div id="htmlwidget-7" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-7">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"model_name":[4925,4925,4925,4925,4925,4925],"term":["(Intercept)","total_working_years","marital_statusMarried","marital_statusSingle","years_with_curr_manager","avg_weekly_hours"],"estimate":[0.113,0.948,1.323,3.133,0.914,1.093],"std.error":[0.397,0.008,0.133,0.131,0.016,0.007],"statistic":[-5.496,-6.88,2.101,8.694,-5.496,13.134],"p.value":[0,0,0.036,0,0,0],"null.deviance":[3860.701,3860.701,3860.701,3860.701,3860.701,3860.701],"df.null":[4375,4375,4375,4375,4375,4375],"logLik":[-1651.434,-1651.434,-1651.434,-1651.434,-1651.434,-1651.434],"AIC":[3330.869,3330.869,3330.869,3330.869,3330.869,3330.869],"BIC":[3420.243,3420.243,3420.243,3420.243,3420.243,3420.243],"deviance":[3302.869,3302.869,3302.869,3302.869,3302.869,3302.869],"df.residual":[4362,4362,4362,4362,4362,4362],"nobs":[4376,4376,4376,4376,4376,4376]},"columns":[{"accessor":"model_name","name":"model_name","type":"numeric"},{"accessor":"term","name":"term","type":"character"},{"accessor":"estimate","name":"estimate","type":"numeric"},{"accessor":"std.error","name":"std.error","type":"numeric"},{"accessor":"statistic","name":"statistic","type":"numeric"},{"accessor":"p.value","name":"p.value","type":"numeric"},{"accessor":"null.deviance","name":"null.deviance","type":"numeric"},{"accessor":"df.null","name":"df.null","type":"numeric"},{"accessor":"logLik","name":"logLik","type":"numeric"},{"accessor":"AIC","name":"AIC","type":"numeric"},{"accessor":"BIC","name":"BIC","type":"numeric"},{"accessor":"deviance","name":"deviance","type":"numeric"},{"accessor":"df.residual","name":"df.residual","type":"numeric"},{"accessor":"nobs","name":"nobs","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"e8dce4c8b83f08f72089361796e61465","key":"e8dce4c8b83f08f72089361796e61465"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### All Significant Variables

Or I could look for models where every variable is statistically significant, or filter to ensure that the model contains one variable I’m particularly interested in.

<div id="htmlwidget-8" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-8">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"model_name":[869,869,869,869,869,869],"term":["(Intercept)","age","marital_statusMarried","marital_statusSingle","years_at_company","avg_weekly_hours"],"estimate":[0.231,0.961,1.277,2.964,0.947,1.094],"std.error":[0.406,0.005,0.132,0.131,0.01,0.007],"statistic":[-3.611,-7.336,1.848,8.326,-5.555,13.328],"p.value":[0,0,0.065,0,0,0],"null.deviance":[3870.464,3870.464,3870.464,3870.464,3870.464,3870.464],"df.null":[4384,4384,4384,4384,4384,4384],"logLik":[-1671.859,-1671.859,-1671.859,-1671.859,-1671.859,-1671.859],"AIC":[3365.718,3365.718,3365.718,3365.718,3365.718,3365.718],"BIC":[3435.964,3435.964,3435.964,3435.964,3435.964,3435.964],"deviance":[3343.718,3343.718,3343.718,3343.718,3343.718,3343.718],"df.residual":[4374,4374,4374,4374,4374,4374],"nobs":[4385,4385,4385,4385,4385,4385]},"columns":[{"accessor":"model_name","name":"model_name","type":"numeric"},{"accessor":"term","name":"term","type":"character"},{"accessor":"estimate","name":"estimate","type":"numeric"},{"accessor":"std.error","name":"std.error","type":"numeric"},{"accessor":"statistic","name":"statistic","type":"numeric"},{"accessor":"p.value","name":"p.value","type":"numeric"},{"accessor":"null.deviance","name":"null.deviance","type":"numeric"},{"accessor":"df.null","name":"df.null","type":"numeric"},{"accessor":"logLik","name":"logLik","type":"numeric"},{"accessor":"AIC","name":"AIC","type":"numeric"},{"accessor":"BIC","name":"BIC","type":"numeric"},{"accessor":"deviance","name":"deviance","type":"numeric"},{"accessor":"df.residual","name":"df.residual","type":"numeric"},{"accessor":"nobs","name":"nobs","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"de10cb6bd76212dad5ce23dc13dec461","key":"de10cb6bd76212dad5ce23dc13dec461"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Significance of Terms Across Models

I could look at how many times a particular term was considered significant across all models. It looks like environment satisfaction, job satisfaction, marital status, age,department, and education field are all near the top of the list. However, stock option level, gender, and a few of the job roles were not significant in many of the models (if at all).

<div id="htmlwidget-9" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-9">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"term":["(Intercept)","environment_satisfaction","job_satisfaction","marital_statusSingle","age","departmentResearch & Development","departmentSales","education_fieldLife Sciences","education_fieldMarketing","education_fieldMedical","education_fieldOther","education_fieldTechnical Degree","total_working_years","training_times_last_year","years_with_curr_manager","years_at_company","job_roleResearch Director","avg_weekly_hours","business_travelTravel Frequently","business_travelTravel Rarely","work_life_balance","num_companies_worked","marital_statusMarried","percent_salary_hike","years_since_last_promotion","monthly_income","performance_rating","job_roleResearch Scientist","job_roleManufacturing Director","education","job_roleSales Executive","job_level","distance_from_home","genderMale","job_roleHuman Resources","job_roleLaboratory Technician","job_roleManager","job_roleSales Representative","stock_option_level"],"num_significant":[3394,2592,2592,2592,1728,1728,1728,1728,1728,1728,1728,1728,1728,1728,1728,1691,1598,1296,1296,1296,1296,1193,1039,676,610,481,130,97,88,15,8,5,0,0,0,0,0,0,0]},"columns":[{"accessor":"term","name":"term","type":"character"},{"accessor":"num_significant","name":"num_significant","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"654350796f1ad84a7f3d94e800218f2c","key":"654350796f1ad84a7f3d94e800218f2c"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Odds Ratios of Significant Terms Across Models

I can also look at the statistically significant terms to see how their odds ratios differ across the models.

``` r
plot2 <- model_df %>% 
  filter(!str_detect(term, "Intercept"), p.value < .01) %>% 
  count(term, estimate) %>% 
  mutate(term = str_to_sentence(str_replace_all(term, "_", " "))) %>% 
  filter(estimate != 0, !str_detect(term, "income")) %>% 
  mutate(term = str_replace_all(term, "Marital status", "Marital status: "),
         term = str_replace_all(term, "Job role", "Job role: "),
         term = str_replace_all(term, "Education field", "Field: "),
         term = str_replace_all(term, "Department", "Dept: "),
         term = str_replace_all(term, "Business travel", "Travel: "))

ggplot(plot2, aes(x = estimate, y = term, fill = term)) +
  geom_density_ridges(scale = 2
) +
  theme_ridges() + 
  scale_x_continuous(name = "Odds Ratio")+
  theme(legend.position = "none")+
  ggtitle("Likelihood of Attrition", subtitle = "by Significant Terms Across All Models")+
  my_theme+
  theme(axis.title.y = element_blank(),
        axis.title.x = element_text(family = "Arial", hjust = .5))
```

<img src="/post/2021-06-21-the-office-part-i/index.en-us_files/figure-html/unnamed-chunk-31-1.png" width="768" style="display: block; margin: auto;" />

It looks like people who travel frequently have some of the highest odds ratios, which means they are more likely to leave their jobs. People who travel rarely are also likely to leave - in comparison to those who don’t travel at all. Single people and research directors also have high likelihoods of leaving. These four variables also seem to vary the most in terms of the odds ratio across all models. For example the lowest odds ratio for marital status: single was around 2.6 and the highest was around 3.4.

Average weekly hours, number of companies worked for, and years since last promotion all had a slightly higher likelihood of leaving, and their odds ratios were quite similar across all models. The lowest odds ratio for average weekly hours was 1.08, and the highest was 1.096.

Some variables are associated with lower likelihood of leaving, for example age (older) and years at the company, some education fields and job roles.

### Selecting a Final Model

I could use the information in the previous chart to filter down and select a final model. For example, I might want to ensure that the travel variable is included, along with marital status. And make sure they are both significant in whatever models I bring up. This set of filtering criteria gives me 648 models to choose from.

Speaking of marital status, there are so many good spouse-related posts.

-   A [job candidate’s suspicious husband](https://www.askamanager.org/2020/08/job-candidates-suspicious-husband-photographed-me-before-her-interview.html) photographs her interviewer
-   When you [accidentally start dating your new boss’s husband](https://www.askamanager.org/2019/11/ive-been-accidentally-dating-my-bosss-husband.html)

And speaking of travel, this is one of my favorite posts ever - this poor woman got in trouble for what she was wearing [when her boss made her pick him up in the middle of the night](https://www.askamanager.org/2016/11/im-in-trouble-for-what-i-wore-when-when-my-boss-made-me-pick-him-up-for-the-airport-in-the-middle-of-the-night.html). Just… wtf?

``` r
temp_models <- model_df %>% 
  group_by(model_name) %>% 
  filter(any(str_detect(term, "travel") & p.value < .05), any(str_detect(term, "marital") & p.value < .05))

distinct(temp_models, model_name) %>% nrow()
```

    ## [1] 648

That’s still probably too many, so I’ll add a filter for education field as well, since there are several fields that are less likely to leave. Now there are “only” 216 models.

``` r
temp_models <- temp_models %>% 
  group_by(model_name) %>% 
  filter(any(str_detect(term, "field") & p.value < .05))

distinct(temp_models, model_name) %>% nrow()
```

    ## [1] 216

You know what they say, people don’t quit a job they quit a boss. Especially if they have one of the [worst bosses of 2020](https://www.askamanager.org/2020/12/the-worst-boss-of-2020-is.html). Let’s also keep the years with current manager and job satisfaction variables. Down to only 36 models.

``` r
temp_models <- temp_models %>% 
  group_by(model_name) %>% 
  filter(any(str_detect(term, "job_sat") & p.value < .05), any(str_detect(term, "manager") & p.value < .05))

distinct(temp_models, model_name) %>% nrow()
```

    ## [1] 36

It looks like model 4998 is the winner with the lowest AIC out of those 36. All of the variables are significant except for job\_level, which is probably fine.

``` r
temp_models <- temp_models %>% 
  ungroup() %>% 
  filter(AIC == min(AIC))
```

<div id="htmlwidget-10" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-10">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"model_name":[4998,4998,4998,4998,4998,4998],"term":["(Intercept)","total_working_years","marital_statusMarried","marital_statusSingle","years_with_curr_manager","business_travelTravel Frequently"],"estimate":[1.445,0.948,1.268,2.834,0.911,3.931],"std.error":[0.365,0.008,0.13,0.128,0.016,0.198],"statistic":[1.007,-6.895,1.828,8.138,-5.741,6.899],"p.value":[0.314,0,0.067,0,0,0],"null.deviance":[3875.651,3875.651,3875.651,3875.651,3875.651,3875.651],"df.null":[4380,4380,4380,4380,4380,4380],"logLik":[-1706.42,-1706.42,-1706.42,-1706.42,-1706.42,-1706.42],"AIC":[3442.839,3442.839,3442.839,3442.839,3442.839,3442.839],"BIC":[3538.615,3538.615,3538.615,3538.615,3538.615,3538.615],"deviance":[3412.839,3412.839,3412.839,3412.839,3412.839,3412.839],"df.residual":[4366,4366,4366,4366,4366,4366],"nobs":[4381,4381,4381,4381,4381,4381]},"columns":[{"accessor":"model_name","name":"model_name","type":"numeric"},{"accessor":"term","name":"term","type":"character"},{"accessor":"estimate","name":"estimate","type":"numeric"},{"accessor":"std.error","name":"std.error","type":"numeric"},{"accessor":"statistic","name":"statistic","type":"numeric"},{"accessor":"p.value","name":"p.value","type":"numeric"},{"accessor":"null.deviance","name":"null.deviance","type":"numeric"},{"accessor":"df.null","name":"df.null","type":"numeric"},{"accessor":"logLik","name":"logLik","type":"numeric"},{"accessor":"AIC","name":"AIC","type":"numeric"},{"accessor":"BIC","name":"BIC","type":"numeric"},{"accessor":"deviance","name":"deviance","type":"numeric"},{"accessor":"df.residual","name":"df.residual","type":"numeric"},{"accessor":"nobs","name":"nobs","type":"numeric"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"5032e306a97f3f9d43d37bd9cfd546bf","key":"5032e306a97f3f9d43d37bd9cfd546bf"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

# Using the Model

What to do with the information from all these models? Some companies actually use predictive models that spy on their employees’ work computers and monitor their emails and LinkedIn activity to try and figure out who is thinking about leaving. What they do with this information may or may not be good (like a retention bonus), but it’s still creepy either way. I could create a sort of “attrition score” using the variables in this model.

## Item Analysis

Create some scores for each item in the model. Here I’ll write a little function to tell me the proportion of staff who left for each variable so I don’t have to copy and paste so much.

``` r
tbl_att <- function(df, col){
  col <- enquo(col)
  
  df %>% 
    count(!!col, attrition) %>% 
    group_by(!!col) %>% 
    mutate(pct = scales::percent(n/sum(n), accuracy = .1)) %>% 
    filter(attrition == "Yes")
}
```

### Total Number of Working Years

Looks like people who have worked for 0-1 years total have a high proportion of leavers.

<div id="htmlwidget-11" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-11">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"total_working_years":[0,1,2,3,4,5,6,7,8,9,10,11,12,13,14,15,16,17,18,19,20,21,22,23,24,25,26,28,31,33,34,40,"NA"],"attrition":["Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes"],"n":[15,119,27,27,36,48,66,54,47,30,75,21,15,9,12,15,9,9,12,9,6,3,6,6,9,3,3,3,3,3,3,6,2],"pct":["45.5%","49.2%","29.0%","21.4%","19.0%","18.2%","17.6%","22.2%","15.3%","10.5%","12.4%","19.8%","10.4%","8.3%","12.9%","12.5%","8.1%","9.1%","14.8%","13.6%","6.7%","2.9%","9.7%","9.1%","16.7%","7.1%","7.1%","7.1%","11.1%","14.3%","20.0%","100.0%","22.2%"]},"columns":[{"accessor":"total_working_years","name":"total_working_years","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"1746cd1b33aff4d3dbc038a435e3888a","key":"1746cd1b33aff4d3dbc038a435e3888a"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
data <- data %>% 
  mutate(total_working_years_score = ifelse(total_working_years < 2 & !is.na(total_working_years), 2, 0))
```

<div id="htmlwidget-12" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-12">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"total_working_years_score":[0,2],"attrition":["Yes","Yes"],"n":[577,134],"pct":["14.0%","48.7%"]},"columns":[{"accessor":"total_working_years_score","name":"total_working_years_score","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"692e2ced94eabe6dff4ad3ea39f63364","key":"692e2ced94eabe6dff4ad3ea39f63364"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Marital Status

Single people have the highest proportion of attrition

<div id="htmlwidget-13" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-13">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"marital_status":["Divorced","Married","Single"],"attrition":["Yes","Yes","Yes"],"n":[99,252,360],"pct":["10.1%","12.5%","25.5%"]},"columns":[{"accessor":"marital_status","name":"marital_status","type":"character"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"71b305e7c73661c022723bc4f0da329b","key":"71b305e7c73661c022723bc4f0da329b"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
data <- data %>% 
  mutate(marital_status_score = ifelse(marital_status == "Single", 1, 0))
```

<div id="htmlwidget-14" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-14">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"marital_status_score":[0,1],"attrition":["Yes","Yes"],"n":[351,360],"pct":["11.7%","25.5%"]},"columns":[{"accessor":"marital_status_score","name":"marital_status_score","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"cfaee0967d8d97ee1fb0b8c46c6affba","key":"cfaee0967d8d97ee1fb0b8c46c6affba"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Years with Current Manager

People with new managers (or new-to-them managers) are more likely to leave.

<div id="htmlwidget-15" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-15">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"years_with_curr_manager":[0,1,2,3,4,5,6,7,8,9,10,11,14],"attrition":["Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes","Yes"],"n":[255,33,150,57,33,12,12,93,30,18,9,3,6],"pct":["32.3%","14.5%","14.5%","13.4%","11.2%","12.9%","13.8%","14.4%","9.3%","9.4%","11.1%","4.5%","40.0%"]},"columns":[{"accessor":"years_with_curr_manager","name":"years_with_curr_manager","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"c70681c477534fabeb079c36b5beb0a5","key":"c70681c477534fabeb079c36b5beb0a5"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
data <- data %>% 
  mutate(years_manager_score = ifelse(years_with_curr_manager == 0, 1, 0))
```

<div id="htmlwidget-16" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-16">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"years_manager_score":[0,1],"attrition":["Yes","Yes"],"n":[456,255],"pct":["12.6%","32.3%"]},"columns":[{"accessor":"years_manager_score","name":"years_manager_score","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"047c23f5761b4962cd5217b3620b1be9","key":"047c23f5761b4962cd5217b3620b1be9"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Business Travel

People who travel at all are more likely to leave than those who don’t travel, but people who travel frequently have a higher proportion of attrition.

<div id="htmlwidget-17" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-17">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"business_travel":["Non-Travel","Travel Frequently","Travel Rarely"],"attrition":["Yes","Yes","Yes"],"n":[36,207,468],"pct":["8.0%","24.9%","15.0%"]},"columns":[{"accessor":"business_travel","name":"business_travel","type":"character"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"1daa35b77d9de60d519fd10711f59d3e","key":"1daa35b77d9de60d519fd10711f59d3e"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
data <- data %>% 
  mutate(travel_score = ifelse(business_travel == "Travel Frequently", 2, 
                               ifelse(business_travel == "Travel Rarely", 1, 0)))
```

<div id="htmlwidget-18" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-18">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"travel_score":[0,1,2],"attrition":["Yes","Yes","Yes"],"n":[36,468,207],"pct":["8.0%","15.0%","24.9%"]},"columns":[{"accessor":"travel_score","name":"travel_score","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"39ad65c13bf6857c375cdb6e7be734d1","key":"39ad65c13bf6857c375cdb6e7be734d1"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Job Level

Job level wasn’t significant in the model and I can see why, there’s not much distinction between levels as far as attrition goes. Maybe I’ll just reverse code for job level 5.

<div id="htmlwidget-19" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-19">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"job_level":[1,2,3,4,5],"attrition":["Yes","Yes","Yes","Yes","Yes"],"n":[252,285,96,51,27],"pct":["15.5%","17.8%","14.7%","16.0%","13.0%"]},"columns":[{"accessor":"job_level","name":"job_level","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"fccb8e7aa8ca37bc3d99d09fa2816b02","key":"fccb8e7aa8ca37bc3d99d09fa2816b02"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
data <- data %>% 
  mutate(job_level_score = ifelse(job_level == 5, -1, 0))
```

<div id="htmlwidget-20" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-20">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"job_level_score":[-1,0],"attrition":["Yes","Yes"],"n":[27,684],"pct":["13.0%","16.3%"]},"columns":[{"accessor":"job_level_score","name":"job_level_score","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"6a6bd5fb9184299248c73e3ae0159488","key":"6a6bd5fb9184299248c73e3ae0159488"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Education Field

Human resources are much more likely to leave than any other education field. This is the variable all the others in the model tested against, so it makes sense why all the other education fields looked like they were less likely to leave. What’s up with HR?

<div id="htmlwidget-21" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-21">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"education_field":["Human Resources","Life Sciences","Marketing","Medical","Other","Technical Degree"],"attrition":["Yes","Yes","Yes","Yes","Yes","Yes"],"n":[33,303,75,225,30,45],"pct":["40.7%","16.7%","15.7%","16.2%","12.2%","11.4%"]},"columns":[{"accessor":"education_field","name":"education_field","type":"character"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"34298f3003240d4d5a0a952d73681490","key":"34298f3003240d4d5a0a952d73681490"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
data <- data %>% 
  mutate(education_field_score = ifelse(education_field == "Human Resources", 2, 0))
```

<div id="htmlwidget-22" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-22">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"education_field_score":[0,2],"attrition":["Yes","Yes"],"n":[678,33],"pct":["15.7%","40.7%"]},"columns":[{"accessor":"education_field_score","name":"education_field_score","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"91969cbf99dea1dcb4f039def5ce4f6b","key":"91969cbf99dea1dcb4f039def5ce4f6b"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Training Times Last Year

It looks like maybe people who had a lot of training had lower attrition.

<div id="htmlwidget-23" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-23">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"training_times_last_year":[0,1,2,3,4,5,6],"attrition":["Yes","Yes","Yes","Yes","Yes","Yes","Yes"],"n":[30,30,282,258,48,51,12],"pct":["18.5%","14.1%","17.2%","17.5%","13.0%","14.3%","6.2%"]},"columns":[{"accessor":"training_times_last_year","name":"training_times_last_year","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"6a449f4335a616e152c954e245a40fbe","key":"6a449f4335a616e152c954e245a40fbe"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
data <- data %>% 
  mutate(training_score = ifelse(training_times_last_year < 4, 1, 0))
```

<div id="htmlwidget-24" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-24">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"training_score":[0,1],"attrition":["Yes","Yes"],"n":[111,600],"pct":["12.1%","17.2%"]},"columns":[{"accessor":"training_score","name":"training_score","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"87f37f1399037564ae7cdba1de3c5339","key":"87f37f1399037564ae7cdba1de3c5339"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

### Job Satisfaction

Job satisfaction - 4 is very high, 1 is low.

<div id="htmlwidget-25" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-25">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"job_satisfaction":[1,2,3,4,"NA"],"attrition":["Yes","Yes","Yes","Yes","Yes"],"n":[197,138,219,156,1],"pct":["22.9%","16.4%","16.6%","11.4%","5.0%"]},"columns":[{"accessor":"job_satisfaction","name":"job_satisfaction","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"51418b89419a429a3052b8486a505a9b","key":"51418b89419a429a3052b8486a505a9b"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

``` r
data <- data %>% 
  mutate(job_satisfaction_score = ifelse(is.na(job_satisfaction) | job_satisfaction == 4, 0,
                                         ifelse(between(job_satisfaction, 2,3), 1, 2))) 
```

<div id="htmlwidget-26" class="reactable html-widget" style="width:auto;height:auto;"></div>
<script type="application/json" data-for="htmlwidget-26">{"x":{"tag":{"name":"Reactable","attribs":{"data":{"job_satisfaction_score":[0,1,2],"attrition":["Yes","Yes","Yes"],"n":[157,357,197],"pct":["11.3%","16.5%","22.9%"]},"columns":[{"accessor":"job_satisfaction_score","name":"job_satisfaction_score","type":"numeric"},{"accessor":"attrition","name":"attrition","type":"character"},{"accessor":"n","name":"n","type":"numeric"},{"accessor":"pct","name":"pct","type":"character"}],"defaultPageSize":10,"paginationType":"numbers","showPageInfo":true,"minRows":1,"highlight":true,"bordered":true,"striped":true,"compact":true,"nowrap":true,"dataKey":"c7d7e0bfaa6166b4f7ac092d3e05c4f5","key":"c7d7e0bfaa6166b4f7ac092d3e05c4f5"},"children":[]},"class":"reactR_markup"},"evals":[],"jsHooks":[]}</script>

## Attrition Risk Score and Level

Now add them all up to create a score and plot it. There are some people who have an attrition score of 0, by the way, but none of them left.

``` r
data <- data %>% 
  select(employee_id, contains("score")) %>% 
  mutate(attrition_score = rowSums(.)) %>% 
  mutate(attrition_score = attrition_score -employee_id) %>% 
  left_join(data)

p1 <- count(data, attrition_score, attrition) %>% 
  group_by(attrition_score) %>% 
  mutate(pct = n/sum(n)) %>% 
  filter(attrition == "Yes") %>% 
  ggplot(aes(x = attrition_score, y = pct))+
  scale_y_continuous(name = "Percent Attrition", labels = scales::percent)+
  scale_x_continuous(name = "Attrition Score", breaks = seq(1,11,1))+
  geom_line(color = pal.9[6], size = 1.2)+
  my_theme
```

I can also make a risk level based on the scores.

``` r
data <- data %>%
  mutate(attrition_level = factor(
    ifelse(
      between(attrition_score, 0, 3),
      "Low",
      ifelse(between(attrition_score, 4, 6), "Medium", "High")
    ),
    levels = c("Low", "Medium", "High")
  ))


p2 <- data %>% 
  count(attrition_level, attrition) %>% 
  group_by(attrition_level) %>% 
  mutate(pct = n/sum(n)) %>% 
  filter(attrition == "Yes") %>% 
  ggplot(aes(x = attrition_level, y = pct, fill = attrition_level))+
  geom_col()+
  geom_text(aes(x = attrition_level, y = pct, label = scales::percent(pct), group = attrition_level),
                  position = position_stack(vjust = .5), color = "white", size = 5)+
  scale_fill_manual(values = c(pal.9[7], pal.9[8], pal.9[9]))+
  labs(x = "Attrition Level")+
  my_theme+
  theme(axis.text.y = element_blank(),
        axis.title.y = element_blank(),
        axis.ticks.y = element_blank())
```

``` r
ggpubr::ggarrange(p1, p2, align = 'hv')
```

<img src="/post/2021-06-21-the-office-part-i/index.en-us_files/figure-html/unnamed-chunk-64-1.png" width="576" style="display: block; margin: auto;" />

Next time maybe I’ll do some latent profile analysis on this dataset.
