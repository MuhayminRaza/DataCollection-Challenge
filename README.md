# DataCollection-Challenge

This module had 2 parts: 
Part 1: Scrape Titles and Preview Text from Mars News
Part 2: Scrape and Analyze Mars Weather Data

After scraping and analyzing the data, the following questions were answered:
How many months exist on Mars?
How many Martian (and not Earth) days worth of data exist in the scraped dataset?
What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
Find the average minimum daily temperature for all of the months.
Plot the results as a bar chart.
Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
Find the average daily atmospheric pressure of all the months.
Plot the results as a bar chart.
About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
Consider how many days elapse on Earth in the time that Mars circles the Sun once.

The following code was written with the help of a TA during office hours and through ASKBCS. 

for element in text_elements:
    title = element.find('div', class_='content_title').text.strip()
    preview = element.find('div', class_='article_teaser_body').text.strip()
    article_dict = {'title': title, 'preview': preview}
    list.append(article_dict)

table = mars_soup.find_all("tr",class_="data-row")
