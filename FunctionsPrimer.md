## <h1>Rprog

add2<- function(x,y){
  x+y;
}

above10 <- function(x){
  use <- x > 10
  x[use] 
}

## <h6>finding the mean in a matrix
columnmean <- function(x)
{
  nc<- ncol(x);
  means<- numeric(nc);
  for (i in 1:nc){
    means[i]<-mean(x[,i])
  }
  means
}

mydata <- rnorm(100)
sd(mydata)
sd(x=mydata, na.rm=FALSE)

## <h6>Extending an existing function - pass arguments to other functions
myplot <- function(x,y,type="1",...){
  plot(x,y,type=type,...)
}


## <h6>scoping
#search() on command prompt: R checks globalenv.. then tries to find it in the packages
#the base package is the last

## <h6>Scoping Rules and difference from S
R uses lexical scoping or static scoping.
F<- function(x,y)
{
  a<- x/y +z
  #Z is free variable. A environment is a collection of (symbol,value) pairs
}

#functions can return functions to variables
make.power<-function(n){
  pow<-function(x){
    x^n
  }
  pow
}

cube<-make.power(3)
square<- make.power(2)
cube(3)
square(2)

#Lexical scoping vs dynamic scoping difference
y<-10
f<- function(x){
  y<-2
  y^2+g(x)
}
#lexical scoping
#The value of y is looked into the environment in which the parent function is defined
#here y=10 will be invoked as it isdefined as the variable in the parent env. 
#All scheme, perl, python, Lisp use lexical scoping

g<-function(x){ 
  
  x*y
}
#f(3) = 34


## <h6>
#R stored objects in memory


#Lexical scoping is typically used in optimization routines. Build your own constructor functions

#Strptime() is the function for datetime
#as.Date() , as.PoSIXct(), as.POSIXlt()
