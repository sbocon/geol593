For Loops & RMarkdown
================
Sam Ocon
3/22/2021

### For Loops and Conditionals

For loops allow you to repeat a task as many times as you want,
basically.

    iris <- iris
    sum <- 0
    for(i in 1:nrow(iris)){
      sum <- sum+1
    }
    print(sum)

    ## [1] 150

You can also use i to reference specific rows, for example,

    for(i in 1:5){
      print(iris$Species[i])
    }

    ## [1] setosa
    ## Levels: setosa versicolor virginica
    ## [1] setosa
    ## Levels: setosa versicolor virginica
    ## [1] setosa
    ## Levels: setosa versicolor virginica
    ## [1] setosa
    ## Levels: setosa versicolor virginica
    ## [1] setosa
    ## Levels: setosa versicolor virginica

So conditionals check to see if a statement is true, then act on that.

For example

    numsetosa <- 0
    numother <- 0
    for(i in 1:nrow(iris)){
      if(iris$Species[i] == 'setosa'){
        numsetosa <- numsetosa+1
      }
      else{
        numother <- numother+1
      }
    }

### Functions

You can build your own functions in r for streamlining!!

    addition <- function(x,y){
      sum <- x+y
      return(sum)
    }

    addition(3,4)

    ## [1] 7
