# Scraping-News

Given a topic (keyword(s)), scrape news articles from 6 of the largest media outlets in my country about that topic.
I have found two applications for the information that can be scraped from these sites and I will explain them below.

## Display the News on my own Site
1. Start a Flask server
2. Extract the news:
    A. For each news website:
        I. Program sends get request to keyword(s) search result page(s) on news website
        II. For each news on the search page:
            a. Scrape title (headlines) and link
            b. Send get request to page linked
            c. For each linked page:
                i. Scrape description, date, publisher (name of news outlet), and article body
3. Sort the articles by date
4. Use render_template to display HTML and execute Javascript code from HTML template on the server
5. Send get request from JavaScript code to obtain JSON article data from Python
6. Fetch and unpack JSON data on Javascript side
7. Generate new HTML elements and display data on server

## Generate Fake News
1. Extract the news:
    A. For each news website:
        I. Program sends get request to keyword(s) search result page(s) on news website
        II. For each news on the search page:
            a. Scrape title (headlines) and link
2. Output headlines to file
3. Read file from Hidden Markov Model script
4. Train algorithm with the headlines from the file
5. Generate and display new "fake news" headlines on command line
        