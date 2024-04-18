# Data-Cruisers
## Contributors
Summer Chalmers, Yanet Gezu, and Patrick Mayer
## Introduction
We collected data from a speed detection radar located on 30th St and 24th Avenue in Rock Island IL. The data we collected was the type of car, speed of the car, time of the car passing by, and the weather all between the hours of 9 am to 6 pm. With this data, we will find the maximum speed, minimum speed, and median of all the speeds and will include a brief analysis of our scholarly articles' findings.

## Dictionary
1. Car Number (each car had a label to it)
2. Time of day
3. Weather (degree)
4. Type of car( Yruck, SUV, Van, Ambulence, and Sedan)
5. Speed
6. Name(person who collected the data)

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
![Max_Value](https://github.com/ygezu/Data-Cruisers-/assets/159511253/c12b1034-e12a-4bcc-8af8-1ef806accdd3)

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
<img src ="https://github.com/ygezu/Data-Cruisers-/blob/main/Images/Min.png"  width = "700">
</div>

## Median
This is the code to find the median of all the speeds in the dataset.

`output$median_value <- renderText({`

`req(input$Y)`

`median_val <- median(dataset[[input$Y]])`

`median_text <- paste("Median value in", input$Y, "is:", median_val)`

`return(median_text)`

 This returns the median value that allows the output to be displayed in the shiny window. 
<div align = "center">
<img src = "https://github.com/ygezu/Data-Cruisers-/blob/main/Images/MaxMinMedianCars.png" width = "700">
</div>

## Average speed
In our data, we found that the average speed was over 30 miles per hour for any type of vehicle, as shown in the graph below.
<div align = "center">
<img src = "https://github.com/ygezu/Data-Cruisers-/blob/main/Images/AverageSpeed.png" width = "700">
</div>
This is the code to find the average speed of all the cars collected:

 `output$plot_avg_speed <- renderPlot({`
 
 `avg_speed <- aggregate(dataset()[["Speed..mph."]], by=list(dataset()[["Type.of.Car"]]), FUN=mean, na.rm=TRUE)`
 
 `colnames(avg_speed) <- c("Type.of.Car", "Average Speed")`

## Analysis

Included in this project was a short essay on the findings of scholarly research articles that possibly correlate with our data's story. 
A brief synopsis of the essay is as follows:



Traffic safety technology has undergone continuous advancement, now integrating solar-powered speed radar displays. Drawing upon research conducted at Southern Illinois University and Morgan State University, the study investigated the efficiency of these speed radar displays at various times of the day and their impact on drivers' speeding behavior. According to the findings, while solar speed radars show promise in encouraging compliance with speed limits, dynamic speed display signs may lose effectiveness over time. The integration of cameras with speed detectors could enhance their impact on promoting compliance and improving road safety. These findings correlate with our collected data, showing higher speeding rates during the afternoon compared to the morning. 
