---
title: "Relationships Between Pixels"
datePublished: Thu Dec 07 2023 13:03:07 GMT+0000 (Coordinated Universal Time)
cuid: clpv7kvpe000308lehxq6h8nl
slug: relationships-between-pixels
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1701954170921/c1ee9078-59c2-4061-84bb-6ed77e8a88f4.png

---

In image processing, a pixel represents a point in an image and has neighboring pixels surrounding it. For a pixel at coordinates (x, y), there are adjacent pixels arranged in different ways:

1. **4-Neighbors (Np4):** These are the immediate horizontal and vertical neighboring pixels. For a pixel at (x, y), the four neighboring pixels are at coordinates (x+1, y), (x-1, y), (x, y+1), and (x, y-1).
    
2. **8-Neighbors (Np8):** In addition to the 4-neighbors, this includes diagonal neighbors as well. For a pixel at (x, y), the eight neighboring pixels are at coordinates (x+1, y), (x-1, y), (x, y+1), (x, y-1), (x+1, y+1), (x-1, y+1), (x+1, y-1), and (x-1, y-1).
    

The collection of pixels around a particular pixel p is called its neighborhood. If this neighborhood includes the pixel p itself, it's termed a "closed" neighborhood. Conversely, if the neighborhood excludes the pixel p, it's considered an "open" neighborhood.

### Adjacency

In image processing, the concept of adjacency relates to how pixels are connected or considered neighbors based on their intensity values.

In a binary image (where pixels have values of 0 or 1), adjacency considers pixels with a value of 1 as connected. In a grayscale image (where pixels can have a range of values from 0 to 255), the idea remains the same, but the set of intensity values, denoted as V, includes more values.

There are three types of adjacency:

1. **4-adjacency:** Two pixels, p, and q, with values from V, are 4-adjacent if q is one of the immediate horizontal or vertical neighbors of p (as defined in the 4-neighbors concept described earlier).  
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701953616875/c6ffbed4-c187-4b11-ba0b-b016a4bf0c2c.png align="center")
    
2. **8-adjacency:** Here, two pixels, p and q, with values from V are 8-adjacent if q is one of the horizontal, vertical, or diagonal neighbors of p (as defined in the 8-neighbors concept described earlier).  
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701953569494/c7e2aed4-b534-449d-88fd-c0065979ecc1.png align="center")
    
3. **m-adjacency (mixed adjacency):** This adjacency type is introduced to resolve potential ambiguities that might occur with 8-adjacency. In m-adjacency, two pixels, p, and q, are considered adjacent if q is either a 4-neighbor of p or an 8-neighbor of p, but there are specific conditions:
    
    * q is in Np4 (one of the 4 neighbors of p), or
        
    * q is in NpD (one of the 8 neighbors of p, the diagonal neighbors), and the intersection of the 4 neighbors of p and the 4 neighbors of q (denoted as Np ∩ Nq4) contains no pixels with values from V.
        

The purpose of m-adjacency is to resolve ambiguity that might arise in 8-adjacency. For instance, certain pixel configurations might lead to multiple possible 8-adjacent connections, creating ambiguity. By using m-adjacency, these ambiguities can be eliminated, ensuring clearer definitions of pixel adjacency.

### Boundaries

If R happens to be an entire image, then its boundary (or border) is defined as the set of pixels in the first and last rows and columns of the image. This extra definition is required because an image has no neighbors beyond its border. Normally, when we refer to a region, we are referring to a subset of an image and any pixels in the boundary of the region that happens to coincide with the border of the image are included implicitly as part of the region boundary.

### Distance between two Pixels

There can be multiple distances that we can find between pixels. Let us take two pixels (x,y) and (u,v) and look at formulas to calculate different kinds of differences between them:

1. **Euclidean Distance**
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701953902020/141c45fa-ce0a-4cf4-9988-15c319e2f452.png align="center")
    
2. **City-Block Distance**
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701953915998/2f1a5fa6-e3b4-441c-8105-0c96c1178f49.png align="center")
    
3. **Chessboard Distance**
    
    ![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701953925166/e25ca444-7536-451b-a39b-f1078d21943b.png align="center")
    

Note that the D4 and D8 distances between p and q are independent of any paths that might exist between these points because these distances involve only the coordinates of the points. In the case of m-adjacency, however, the Dm distance between two points is defined as the shortest m-path between the points. In this case, the distance between two pixels will depend on the values of the pixels along the path, as well as the values of their neighbors. For instance, consider the following arrangement of pixels and assume that p, p2 , and p4 have a value of 1, and that p1 and p3 can be 0 or 1:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1701954016547/3a62203b-0137-4af8-9344-019dfc45887f.png align="center")

Suppose that we consider the adjacency of pixels valued 1 (i.e., V = {1}). If p1 and p3 are 0, the length of the shortest m-path (the Dm distance) between p and p4 is 2. If p1 is 1, then p2 and p will no longer be m-adjacent and the length of the shortest m-path becomes 3 (the path goes through the points pp1p2p4 ). Similar comments apply if p3 is 1 (and p1 is 0); in this case, the length of the shortest m-path also is 3. Finally, if both p1 and p3 are 1, the length of the shortest m-path between p and p4 is 4. In this case, the path goes through the sequence of points pp1p2p3p4.