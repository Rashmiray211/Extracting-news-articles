# Extracting-news-articles
Here, I have scraped around 2500 news articles with content . For this, I have used "the hindu" newspaper.
After data scraping, I created a csv file of the news articles with ids and content.( It was part of an assignment given by my instructor).


Scraping:

For this, firstly I looked at the url of a page, then ran a loop for 80 pages where each page shows headings of various news articles. I appended the urls.
Then, for a page, I :
#found all <"class":"Other-StoryCard"> tags in a page
#found all <h3> tags in the above tags
#found all <a> tags in those <h3> tags
#found all hrefs in those <a> tags and appended in page_href1. It contains hrefs of all the news articles in a particular page. But, some of the hrefs were problematic. So, I appended hrefs after removing all the problematic hrefs in a page.
Then I appended hrefs of all the pages in all_hrefs.
For each href/url , I extracted only the relevent content as every news content contains non-relevent text at the end, some in between and in the starting.So, it's important to remove those texts.( Please look at the code, it will help you to understand).
After all this cleaning, I stored ids(index) and the news content in a csv file.

  
