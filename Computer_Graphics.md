Course CMU Computer Graphics https://www.youtube.com/watch?v=W6yEALqsD7k&list=PL9_jI1bdZmz2emSh0UQ5iOdT2xRHFHL7E&index=1

<b>Lecture 01 Course Overview</b>

Computer Graphics: The use of computers to synthesize visual information, the use of computation to turn digital information into sensory stimuli. Perspective projection: Objects look smaller as they get further away. Represent a line(Rasterization: process of converting a continuous object to a discrete representation on a raster grid(pixel grid). Diamond rule(used by model GPUs): light up pixel if line passes through associated diamond). Line incremental rasterization. SVG: standard vector graph. 

<b>Lecture 02 & 03 Linear Algebra Review</b>

Linear Map-Algebraic Definition: A map f is linear if it maps vectors to vectors, and if for all vectors u, v and scalars a we have f(u+v) = f(u) + f(v), and in other words, if it does not matter whether we add the vectors and then apply the map, or apply the map and then add the vectors(and likewise for scaling). Affine function is not a Linear function. Span: is the set of all vectors that can be written as a linear combination of u and v. The image of any linear map is the span of some collection of vectors. Orthonormal Basis: basis vectors(unit length and mutually orthogonal).  Determinant encodes(signed) volume of parallelepiped with edge vectors u, v, w —> triple product formula. If a matrix A encodes a linear map f, det(A) measures the change in volume, and the sign of the determinant tells us whether orientation was reversed. 

Medium, A new algorithm for finding a visual center of a polygon, https://blog.mapbox.com/a-new-algorithm-for-finding-a-visual-center-of-a-polygon-7c77e6492fbc ,GitHub: https://github.com/mapbox/polylabel
