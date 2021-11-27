# VBA Challenge

## Overview of Project

Cleaning and analyzing the provided stock data to evaluate environmentally friendly stock performance.

### Purpose

The purpose of the analysis was to refactor the solution code to loop through all the data one time in order to determine whether refactoring the code successfully made the VBA script run faster.

## Results

### Refactoring the Original Code

Refactoring code doesn’t add new functionality; rather, it makes the original code more efficient while still maintaining the original functionality.  Refactoring may include taking fewer steps, using less memory, improving the logic of the code, or making the code clearer and more readable for future readers.

For this particular code, the way to make it faster and more efficient was to have the code loop through all the date one time in order to collect all the necessary information, rather than having it loop multiple times.  The key was to change the nesting order of the loops to create one continuous loop.  To do this, I created three additional arrays to complement the first array, tickers.  The additional arrays were tickerVolumes, tickerStartingPrices, and tickerEndingPrices.  By creating a variable called tickerIndex, I was able to link each additional array to the ticker array.  

#### Original Code

![This is an image](https://github.com/amacancio/VBA_Challenge/blob/main/Resources/VBA%20Challenge%20Original%20Code.png)

![This is an image](https://github.com/amacancio/VBA_Challenge/blob/main/Resources/VBA%202017%20Original%20Code.png)
![This is an image](https://github.com/amacancio/VBA_Challenge/blob/main/Resources/VBA%202018%20Original%20Code.png)

The original code, while functional, looped through the dataset multiple times in order to obtain the necessary data and place it in the appropriate locations.  As you can see in the second and third images, the code ran in between .29 and .30 seconds for each year.

#### Refactored Code

![This is an image](https://github.com/amacancio/VBA_Challenge/blob/main/Resources/VBA%20Challenge%20Refactored%20Code.png)

![This is an image](https://github.com/amacancio/VBA_Challenge/blob/main/Resources/VBA_Challenge_2017.png)
![This is an image](https://github.com/amacancio/VBA_Challenge/blob/main/Resources/VBA_Challenge_2018.png)

The refactored code retains the same functionality, but loops through the dataset only once, making it more efficient.  As you can see in the fifth and sixth images, the code ran in about .06 seconds for both 2017 and 2018.

## Summary

### Thoughts on Refactoring Code in General

Refactoring is a powerful tool because it takes code that already functions and makes it better: faster, more efficient, and more adaptable.  It can make future improvements easier by increasing clarity and usability.  However, refactoring takes further time and money to complete, which a programmer may not have available to them.  Furthermore, there is a risk of taking code that was once usable and making it unusable.  

### Thoughts on the Refactored Code

While the difference between .29 or .30 seconds and .06 seconds seems arbitrary, in reality the refactored code is running in approximately 16.67% of the time it takes the original code to run.  The current dataset is relatively small and, as such, the time difference is seemingly negligible; however, with a larger data set, what would take the original code about 1 hour to execute would take the refactored code approximately ten minutes to execute.

As I experienced, the downside to refactoring code is how long it takes.  It was faster than creating the original code, but still took a significant amount of time to complete.  Also, refactoring is useless unless you know how to improve the functionality of the original code, something which isn’t always obvious.  In certain cases, it may be better to have code that works rather than code that could work.
