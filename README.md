# Data-Cruisers
## Contributors
Summer Chalmers, Yanet Gezu, and Patrick Mayer
## Introduction
We collected data from a speed dection radar located on 30th St and 24th Avenue in Rock Island IL. The data we collected was type of car, speed of the car, time of the car passing by, and the weather all between the hours of 9 am to 6pm. With this data we will find the maximum speed, minimum speed, and median of all the speeds and will include a brief anaylsis on scholarly articles findings agains't the story our data tells us. 
## Maximum
This is the code to find the maximum value in the dataset collected

`output$max_value <- renderText({`

 `req(input$Y)`
  
 `max_val <- max(dataset[[input$Y]])`
 
 `max_text <- paste("Maximum value in", input$Y, "is:", max_val)`

`return(max_text)`

`})`

This returns the maximum value to allow the output to be displayed in the shiny window. 
Next is the graph of the maximum speed which you can see was 45 miles per hour. 
<div align = "center">
<img src = "https://github.com/ygezu/Data-Cruisers-/blob/main/Max.png" width = "700">
</div>

## Minimum
This is the code to find the minimum value in the dataset, similar to the maximum.
  
`output$min_value <- renderText({`

`req(input$Y)`
    
`min_val <- min(dataset[[input$Y]])`  

`min_text <- paste("Minimum value in", input$Y, "is:", min_val) `

`return(min_text)`

This returns the minimum value to allow the output to be displayed in the shiny window.
Next is the graph of minimum speed which you can see was 20 miles per hour. 
<div align = "center">
<img src ="https://github.com/ygezu/Data-Cruisers-/blob/main/Min.png"  width = "700">
</div>

## Median
This is the code to find the median of all the speeds in the dataset.

`output$median_value <- renderText({`

`req(input$Y)`

`median_val <- median(dataset[[input$Y]])`

`median_text <- paste("Median value in", input$Y, "is:", median_val)`

`return(median_text)`

 This return the median value to alllow the output to be displayed in the shiny window.
 At the very end of the shiny window median, along with maximum and minimum, have been displayed for the user to see. 
<div align = "center">
<img src = "https://github.com/ygezu/Data-Cruisers-/blob/main/MaxMinMedianCars.png" width = "700">
</div>

## Average speed
In our data we found that the average speed was over 30 miles per hour for any type of vehcile, as shown in grapg below.
<div align = "center">
<img src = "https://github.com/ygezu/Data-Cruisers-/blob/main/AverageSpeed.png" width = "700">
</div>
## Anaylsis
Included in this project was a short essay on the findings of scholarly research to either back up our findings or to argue agains't our data's story. 
