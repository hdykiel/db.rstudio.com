---
title: New versions of modeldb and tidypredict now on CRAN
author: ''
date: '2019-03-05'
slug: modeldb-1-2
categories: 
 - tools
---

## modeldb 0.1.2

- Removes pipes and other `dplyr` dependencies from internal `mlr()` function
- Consolidates duplicated database operations in `mlr()`
- Fixes an issue in `simple_kmeans_db()` when specifying variables

## tidypredict 0.3.0

### New features

- Adds support for MARS models provided by the `earth` package

### Improvements

- New parsed models are now list objects as opposed to data frames.

- tidypredict_to_column() no longer supports `ranger` and `randomForest` because of the multiple queries generated by multiple trees.

- All functions that read the parsed models and create the tidy eval formula now use the list object.  

- Most of the code that depends on dplyr programming has been removed.

- Removes dependencies on: tidyr, tibble

### Bug Fixes

- It now returns all of the trees instead of just one for tree based models (`randomForest` & `ranger`) (#29)