---
layout: post
title: NaN Values in Python
subtitle: through Numpy and Pandas 
---

Nan values in Numpy is denoted by `numpy.nan`. Its type is actually `float`! For some [reason](http://pandas.pydata.org/pandas-docs/stable/gotchas.html#support-for-integer-na), NaN values cannot have type `int`. This might introduce some problems in Pandas dataframes, when some values are `int` and some values are missing. When a Series in Pandas contains both `int` and `NaN` values, the Series is automatically recast into `dtype=float64`, or `dtype=object`.

It is important to keep in mind of this automatic conversion when comparing almost equivalent dataframes, as some columns dtype might be different from the intended one.
