# Assignment A1 for DATA 512

#### Goal
The goal of the project is to is to construct, analyze, and publish a dataset of monthly traffic on English Wikipedia from January 1 2008 through August 30 2019. The purpose of the assignment is to demonstrate that we can follow best practices for open scientific research in designing and implementing your project, and make our project fully reproducible by others: from data collection to data analysis.
#### Wikimedia
Content accessed via this (https://wikimedia.org/api/rest_v1/#/) API is licensed under the CC-BY-SA 3.0 and GFDL licenses, and you irrevocably agree to release modifications or additions made through this API under these licenses. See https://www.mediawiki.org/wiki/REST_API for background and details.
Wikimedia Foundation REST API terms of use: https://www.mediawiki.org/wiki/REST_API#Terms_and_conditions
#### API Documentation
The Legacy Pagecounts API (https://wikitech.wikimedia.org/wiki/Analytics/AQS/Legacy_Pagecounts) provides access to desktop and mobile traffic data from December 2007 through July 2016.
The Pageviews API (https://wikitech.wikimedia.org/wiki/Analytics/AQS/Pageviews) provides access to desktop, mobile web, and mobile app traffic data from July 2015 through last month.
#### Final Data
The csv file en-wikipedia_traffic_200712-201809.csv consists of the following fields
year: year of the pagecount value
month: month of the page count value
pagecount_all_views: taken from legacy page counts wikimedia, these are pagecounts of all site views from December 2007 through July 2016
pagecount_desktop_views: taken from legacy page counts wikimedia, these are pagecounts of all desktop views from December 2007 through July 2016
pagecount_mobile_views: taken from legacy page counts wikimedia, these are pagecounts of all mobile views from December 2007 through July 2016
pageview_all_views: taken from pageview wikimedia, these are pagecounts of all views from July 2015 to September 2019, calculated as a sum of the pageview_mobile_views and pageview_desktop_views 
pageview_desktop_views: taken from pageview wikimedia, these are pagecounts of all desktop views from July 2015 to September 2019
pageview_mobile_views: taken from pageview wikimedia, these are pagecounts of all mobile views from July 2015 to September 2019
#### Special Considerations
Data from the Pageview API excludes spiders/crawlers, while data from the Pagecounts API does not as the Pageview API (but not the Pagecount API) allows you to filter by agent=user.
pageview_all_views in the final csv is a derived field as a sum of pageview_desktop_views and pageview_mobile_views
