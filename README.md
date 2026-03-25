# Multivariate Methods Assignment 0

This repository contains my setup verification for R, GitHub, and AI-assisted coding.

AI reflection:

I used ChatGPT 5.3 to increase the correlation and add contour lines to the plot. 
It modified the covariance matrix (updating the correlation from 0.5 to 0.8) and added a line (stat_density_2d(color = "blue") +) to the ggplot. 
It also updated some comments in the code and changed the title of the plot. 
The code worked immediately without any problems.

I made the following changes:

- I changed the function to geom_density_2d() since it serves the same purpose for this task. After checking the documentation, I saw that most examples use geom_density_2d(), which made me think it would be better to continue with that. (Documentation link: https://ggplot2.tidyverse.org/reference/geom_density_2d.html)

- I changed the order of the plotting layers. The LLM placed stat_density_2d() after geom_point(), which caused the contour lines to be drawn over the data points, making them harder to see. I reordered the lines so that the data points remain clearly visible.

- Lastly, I found the “blue” color too strong, so I changed it to “salmon3” (used this reference to check color names in R: https://sape.inf.usi.ch/quick-reference/ggplot2/colour). I also adjusted the transparency of the data points by modifying the alpha parameter in geom_point() to improve the overall appearance of the plot.

I verified the output using my own knowledge and by checking documentation. To increase the correlation, it was obvious to me that I needed to change the covariance matrix, so I focused on that part and compared the plots before and after. I observed that the data points became more concentrated around the line y=x, which indicates a higher correlation (from 0.5 to 0.8). 
For the contour lines, I searched “how to add contour lines to a ggplot” and found the relevant documentation (https://ggplot2.tidyverse.org/reference/geom_density_2d.html). After a quick review, I did not find any issues.

Author: Busra Ekinci

Date: 2026-03-25