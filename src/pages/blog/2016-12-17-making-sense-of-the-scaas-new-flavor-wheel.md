---
templateKey: blog-post
title: Introduction to Treemaps
date: 2016-12-17T15:04:10.000Z
description: 'Treemaps are wonderful, this article explains why.'
featuredpost: false
featuredimage: /img/screenshot-2019-08-20-at-13.41.09.png
tags:
  - flavor
  - tasting
---
![A treetop](/img/screenshot-2019-08-20-at-13.41.09.png)

Treemaps display hierarchical (tree-structured) data as a set of nested rectangles. Each branch of the tree is given a rectangle, which is then tiled with smaller rectangles representing sub-branches. A leaf node's rectangle has an area proportional to a specified dimension of the data \[1]. Often the leaf nodes are colored to show a separate dimension of the data.

When the color and size dimensions are correlated in some way with the tree structure, one can often easily see patterns that would be difficult to spot in other ways, such as if a certain color is particularly relevant. A second advantage of treemaps is that, by construction, they make efficient use of space. As a result, they can legibly display thousands of items on the screen simultaneously.

## Tiling algorithms

To create a treemap, one must define a tiling algorithm, that is, a way to divide a region into sub-regions of specified areas. Ideally, a treemap algorithm would create regions that satisfy the following criteria:

1. A small aspect ratio—ideally close to one. Regions with a small aspect ratio (i.e, fat objects) are easier to perceive.\[2]
2. Preserve some sense of the ordering in the input data.
3. Change to reflect changes in the underlying data.
4. Unfortunately, these properties have an inverse relationship. As the aspect ratio is optimized, the order of placement becomes less predictable. As the order becomes more stable, the aspect ratio is degraded.\[example needed]
