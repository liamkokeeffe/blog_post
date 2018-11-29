---
title: "Top 5 Most Popular R Packages"
author: "Liam O'Keeffe"
date: "11/28/2018"
output: pdf_document
---

## 1. ggplot2
ggplot2 is a data visulization package and with an average of 5,401 downloads a month, ggplot is the most downloaded R package to date. It was created by Hadley Wickham in 2005 and is still well-supported by him and his team. It is very popular for a variety of reasons; it is well-supported, easy to use, aesthetically pleasing and built for multi-variate data. Here is an example of a very aesthetically pleasing graph using the built in R diamonds data set.

```{r graph, include=TRUE, message=FALSE}
library(ggplot2)
library(ggthemes)
ggplot(data = diamonds,
       aes(x = carat, y = price)) +
  geom_point(aes(color = clarity)) +
  geom_smooth(color = "black", size = 0.8, linetype = 2) +
  theme_few()
```

## 2. R6
R6 is an implementation of object oriented programming for R. R does have built in reference classes however this package is simpler, more efficient and less clunky. R6 has a monthly average of 5,242 downloads making it the second most popular R package. The package creates classes with referance semantic and support inheritance, staples of object oriented programming. This is an examples of creating an R6 reference object generator.

```{r r6, include=TRUE}
library(R6)
R6Class(classname = "Example", public = list(), private = NULL,
      active = NULL, inherit = NULL, lock_objects = TRUE, class = TRUE,
      portable = TRUE, lock_class = FALSE, cloneable = TRUE,
      parent_env = parent.frame())
```

## 3. tidyverse
tidyverse is a system of packages for data analytics, including, manipulation, exploration and visualization. The main advantages of using tidyverse are consistent functions among packages and workflow coverage which lead to greater productivity. tidyverse has an average of 4987 downloads per month putting it in 3rd place in regard to downloads per month. Here is an example that shows the packages that are loaded with tidyverse and some conflicts that arise when loading the tidyverse package.

```{r tidy, include=TRUE}
library(tidyverse)
```

## 4. dplyr
The fourth most popular R package is the dplyr package, with 4954 downloads per month. dplyr is a package that helps manipulate data frame like objects. Through the functions mutate, select, filter, summarise, and arrange, users are able to efficiently manipulate data to their likings. The simple syntax and ability to chain functions makes dplyr a very effective and widely used tool. This is an example of using dplyr to find the mpg, hp and gear of cars that have a mpg greater than 25 using the mtcars built in R dataset.

```{r dplyr, include=TRUE}
library(dplyr)
mtcars %>% select(mpg, hp, gear) %>% filter(mpg > 25) %>% group_by(gear)
```

## 5. openssl
Last but not least, the fifth most popular package is the openssl package with 4601 monthly downloads. openssl is a cryptography library that provides open source implementation of the Secure Sockets Layer and Transport Layer Security protocols. This package is helpful in generating RSA keys, managing certificates and performing encryption/decryption. Here is an example of a function that prompts the user for their password to read their protected private key, in order to perform encryption/decryption.

```{r open, include=TRUE}
library(openssl)
invisible(askpass(prompt = "Please enter your password: "))
```


## References
1. [rdocumentation](https://www.rdocumentation.org/trends)
2. [adrienne-marshall.github](https://adrienne-marshall.github.io/ggplot2_workshop/)
3. [cran.r-project.org](https://cran.r-project.org/web/packages/R6/R6.pdf)
4. [rviews.rstudio](https://rviews.rstudio.com/2017/06/08/what-is-the-tidyverse/)
5. [cran.r-project.org](https://cran.r-project.org/web/packages/openssl/openssl.pdf)
6. [github.com](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#lists)
