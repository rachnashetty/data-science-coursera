# Obtaining R Packages

Date: 20th July, 2016

*For R 3.3.1 on Ubuntu 14.04*

## `install.packages()`

The command `install.packages()` is used to install packages in R.

```R
>install.packages("PackageName") #Installs package
>install.packages(c("slidify","ggplot2","devtools")) #Creates a character vector c and installs all packages within c
```

If you're using a more recent version of R, it might return an error message like `slidify is not available for R 3.3.1`. To fix this, we have to install `slidify` from **Github** on R using:

```R
> library(devtools)
> install_github('ramnathv/slidify') # Or install_github('slidify','ramnathv')
> install_github('ramnathv/slidifyLibraries') # Or install_github('slidifyLibraries', 'ramnathv') 
```
The commented option might return the "Username deprecated" error, which can be ignored or fixed using the uncommented part of the code. If this works, great! Else, you might get an issue like `no library "devtools" found` (Not the exact words). To fix this up, follow the next section. 

## Installing `devtools`
In R, use:

```R
$ install.packages("devtools") 
```

If this works, then you just have to follow the steps to install slidify after devtools. However, this returned the following error for me:
![Error while trying to install `devtools`](figures/error.png)

I tried a number of things like `$ sudo apt-get install libssl-dev` but they didn't work for me again. The last thing that finally worked was : 

`$ sudo apt-get install libcurl4-openssl-dev`

So after this, all I had to do was to install devtools and slidify in the respective order. 






