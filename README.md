
<!-- README.md is generated from README.Rmd. Please edit that file -->
![](https://avatars3.githubusercontent.com/u/515326?v=3&s=400)

Description
===========

`rcanvas` is a bouquet of functions to query your institution's instance of the [Canvas LMS.](https://www.canvaslms.com)

Installation
============

`rcanvas` is not on CRAN, but can be installed via:

``` r
devtools::install_github("daranzolin/rcanvas")
library(rcanvas)
```

Setup
=====

Some prep work is required before use. You must first stash two items in your `.Renviron` file: (1) your third-party access token, available through your Canvas LMS account settings; and (2) your institution's particular domain. (e.g. `"https://<domain>.instructure/"`) Name your token `CANVAS_API_TOKEN`, and your domain `CANVAS_DOMAIN`. For help on setting up your `.Renviron` (and all things R) see Jenny Bryan's [Stat545 page.](http://stat545.com/bit003_api-key-env-var.html)

Usage
=====

Each function returns a `data.frame` with course information.

``` r
###Get all courses:
get_course_list()

###Get course analytics data:
get_course_analytics_data(course_id = 20, type = "activity")

###Get course member data:
get_course_members(courses_id = 20, type = "students")

###Get course items:
get_course_items(course_id = 20, item = "discussion_topics")
```

------------------------------------------------------------------------

Future Work
===========

-   Additional functions
-   More precise querying
-   Tests
