Visual Analytics Module 12 - Graphing a Network
================

For this assignment, I will be using datasets containing the relationships found in media. I will first import the data into R and then create a matrix in order to plot the data.

``` r
#import data

net_nodes = read_csv("https://www.dropbox.com/s/ieaoo7efx87etyk/Dataset1-Media-Example-NODES.csv?dl=1")
net_edges = read.csv("https://www.dropbox.com/s/s4mli5l6j30gc5n/Dataset1-Media-Example-EDGES.csv?dl=1")
#Create an adjacency matrix for net_edges
net_edges_mat = as.matrix(net_edges)
```

``` r
p1 = plot(netgraph1_wo_loops, main = "Time Series Plot (Media)", frame = TRUE, edge.arrow.size=.5, vertex.color = "salmon", vertex.label=net_nodes$media, vertex.label.color="black", vertex.size = 7, edge.curved = .5, edge.width=2, shape='sphere')
```

![](Visual-Analytics-Module-12_files/figure-markdown_github/graph%20paramaters-1.png)

``` r
tkplot(netgraph1_wo_loops, main = "Network Graph Ex", frame = TRUE, edge.arrow.size=.5, vertex.color = "salmon", vertex.label=net_nodes$media, vertex.label.color="black", vertex.size = 7, vertex.label.family = "Times", edge.curved = .5,)
```

    ## [1] 1

``` r
#edge.curved range is 0-1, TRUE sets to .5
```
