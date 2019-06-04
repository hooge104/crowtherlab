color palettes
================
Johan van den Hoogen
6/3/2019

# Color palettes for Crowther Lab

``` r
library(RColorBrewer)
library(viridis)
library(wesanderson)
library(tidyverse)

plot <- function(pal){
  ggplot(heatmap, aes(x = X2, y = X1, fill = value)) +
    geom_tile() + 
    scale_fill_gradientn(colours = pal) + 
    scale_x_discrete(expand = c(0, 0)) +
    scale_y_discrete(expand = c(0, 0)) + 
    coord_equal() 
}
```

### Spectral

``` r
spectral <- brewer.pal(9, "Spectral")
plot(spectral)
```

![](color_palettes_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

``` js
var spectral = ["#D53E4F", "#F46D43", "#FDAE61", "#FEE08B", "#FFFFBF", "#E6F598", "#ABDDA4", "#66C2A5", "#3288BD"]
```

### Viridis

``` r
viridis <- viridis(9)
plot(viridis)
```

![](color_palettes_files/figure-gfm/unnamed-chunk-4-1.png)<!-- -->

``` js
var viridis = ["#440154", "#472D7B", "#3B528B", "#2C728E", "#21908C", "#27AD81", "#5DC863", "#AADC32", "#FDE725"]
```

### Magma

``` r
magma <- viridis(9, option = "magma")
plot(magma)
```

![](color_palettes_files/figure-gfm/unnamed-chunk-6-1.png)<!-- -->

``` js
var magma = ["#000004", "#1D1147", "#51127C", "#822681", "#B63679", "#E65164", "#FB8861", "#FEC287", "#FCFDBF"]
```

### Wes Anderson; The Life Aquatic with Steve Zissou (2004)

``` r
zissou <- wes_palette("Zissou1")
plot(zissou)
```

![](color_palettes_files/figure-gfm/unnamed-chunk-8-1.png)<!-- -->

``` js
var zissou = ["#3B9AB2", "#78B7C5", "#EBCC2A", "#E1AF00", "#F21A00"]
```
