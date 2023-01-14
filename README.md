# data_collection-challenge
Week 11 Challenge

# Part 1: Scrape Titles and Preview Text from Mars News
Used Splinter and Beautiful Soup to scrape the article text from the website: https://static.bc-edx.com/data/web/mars_news/index.html

Stored each article title-and-preview pair in a Python dictionary with two keys: title and preview. An example is the following:
    {'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm", 
        'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."
    }

The dictionary of each article was added to a list of articles.    


# Part 2: Scrape and Analyze Mars Weather Data
A table was scraped from the website: https://static.bc-edx.com/data/web/mars_facts/temperature.html using a Beautiful Soup pbject and Splinter


A df was made with the following columns:
    id: the identification number of a single transmission from the Curiosity rover
    terrestrial_date: the date on Earth
    sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
    ls: the solar longitude
    month: the Martian month
    min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
    pressure: The atmospheric pressure at Curiosity's location

The df data was analyszed to answer the following questions: 
    (1) How many months exist on Mars?
        It was found that 12 months exist on Mars

    (2) How many Martian (and not Earth) days worth of data exist in the scraped dataset?
        It was found that there is 1867 Martian days worth of data.

    (3) What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
        a. Find the average the minimum daily temperature for all of the months.
        b. Plot the results as a bar chart.
        
        The coldest month of the year is the 3rd month with a temperature of -83.31.
        The warmest monthe of the year is the 8th month with a temperature of -68.38

    (4) Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
        a. Find the average the daily atmospheric pressure of all the months.
        b. Plot the results as a bar chart.

        The 6th month has the lowest average atmospheric pressure of 745.05.
        The 9th month has the highest average atmospheric pressure of 913.31

    (5) About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
        a. Consider how many days elapse on Earth in the time that Mars circles the Sun once.
        b. Visually estimate the result by plotting the daily minimum temperature.

        Using a for loop to track the month on mars, it was found that the number of Earth days in a Martian year is approxicately 687 days 00:00:00.
        A visual estimate for the number of earth days in a Martian year is 690 days, 0:00:00. Hot dang my estimate was good