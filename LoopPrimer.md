
*********Loop functions*************
lapply sapply apply mapply tapply split

#lapply 
> returns a list irrespective of the input vector. Usually used for functions not part of the original list

lapply can be used for anonymous functions in the list
lapply(x, function(elt) elt[,1])

sapply adjust according to the output and gives a list/matrix/vector


#apply generally applied to rows and cols of a matrix
x <- matrix(rnorm(200), 20, 10)
apply(x, 2, mean)
rowSums = apply(x, 1, sum)
rowMeans = apply(x, 1, mean)
colSums = apply(x, 2, sum)
colMeans = apply(x, 2, mean)

tapply is used for functions over a subset of the vector. (Mean of Numeric vector with Men/ Women in a set)
x <- c(rnorm(10), runif(10), rnorm(10, 1))
f <- gl(3, 10)
tapply(x,f,mean)
