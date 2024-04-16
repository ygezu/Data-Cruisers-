# Data-Cruisers
## Contributors
Summer Chalmers, Yanet Gezu, and Patrick Mayer
## Introduction
We collected data from a speed dection radar located on 30th St and 24th Avenue in Rock Island IL. The data we collected was type of car, speed of the car, time of the car passing by, and the weather all between the hours of 9 am to 6pm. With this data we will find the maximum speed, minimum speed, and median of all the speeds and will include a brief anaylsis on scholarly articles findings agains't the story our data tells us. 
## Maximum
This is the code to find the maximum value in the dataset collected

`output$max_value <- renderText({ `
   
    `req(input$Y) `
    
     `max_val <- max(dataset[[input$Y]]) `
     
    ` max_text <- paste("Maximum value in", input$Y, "is:", max_val) `
    
     `return(max_text)`
   
    This return the maximum value to allow the output to be displayed in the shiny window
 
  ## Minimum
  This is the code to find the minimum value in the dataset, similar to the maximum.
  
 `output$min_value <- renderText({ `
    `req(input$Y) `
    
    `min_val <- min(dataset[[input$Y]]) `
     
    ` min_text <- paste("Minimum value in", input$Y, "is:", min_val) `
 
    ` return(min_text)`

    This returns the minimum value to allow the output to be displayed in the shiny window.

## Median
This is the code to find the median of all the speeds in the dataset.

`output$median_value <- renderText({`

    `req(input$Y)`
    
    `median_val <- median(dataset[[input$Y]])`
    
    `median_text <- paste("Median value in", input$Y, "is:", median_val)`
    
    `return(median_text)`

    This returnt he median value to alllow the output to be displayed in the shiny window.
