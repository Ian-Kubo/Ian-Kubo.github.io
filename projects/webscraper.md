---
layout: project
type: project
image: img/webscrape.png
title: "Webscraper"
date: 2026
published: true
labels:
  - AI
  - Python
  - Data Science
summary: "I Developed a Small Scale Webscraper Using Scrapy and Spiders."
---

<div class="text-center p-4">
  <img width="200px" src="../img/micromouse/micromouse-robot.png" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-robot-2.jpg" class="img-thumbnail" >
  <img width="200px" src="../img/micromouse/micromouse-circuit.png" class="img-thumbnail" >
</div>

Webscraping is the automated method of extracting, cleaning, and structuring large amounts of data from websites. I created a simple webscraper using scrapy, an open-source python webcrawling and data-extraction framework. Webcrawling specifically was done by creating custom python classes, called spiders, to define how a website gets crawled and what information is collected. This project started by just watching tutorials on scrapy and reading needed documentation to understand how the framework worked. I then used what I learned to create a scraper that could navigate a website, such as nbcnews.com, and collect information from its pages.  

My main role in this project was setting up and programming the web scraper in VScode. I was responsible for creating the spider, determining what information I wanted to extract, and figuring out how to organize the collected data. Since I was actively learning Scrapy along the way, I did run into some problems. One issue was creating code for processing data from a website since I wanted the spider to return both a headline and the link to a certain page. I was responsible for the majority of the project, including writing the Python code and troubleshooting problems that came up during development.

Through this project, I learned how web scraping and web crawling operates and gained more experience using Python. I learned that a web scraper needs to be carefully designed because websites can have different structures, and the information I want may not always be located in the same place. I also became more comfortable reading documentation and using tutorials to learn a new programming framework. Overall, this project helped me understand how programs can automatically collect and organize information from websites instead of having to manually gather the data myself. 

Here is some code that shows a Scrapy spider class:

```python
class NewSpider(scrapy.Spider):
    name = "news"
    allowed_domains = ["nbcnews.com"]
    start_urls = ["https://www.nbcnews.com"]

    def parse(self, response):
        headlines = response.css('article a, .headline a, h2 a, h3 a')
        seen_links = set()

        for headline in headlines:
            item = NewsCrawlerItem()
            link = headline.css('::attr(href)').get()

            if link:
                link = urljoin(response.url, link)

            if not link or link in seen_links:
                continue
            seen_links.add(link)

            title = headline.css('span::text').get() or headline.css('::text').get()

            if not title:
                title = headline.xpath('./ancestor::article//h2/text() | ./ancestor::article//h3/text()').get()

            if title and link and 'nbcnews.com' in link:
                item['title'] = title.strip()
                item['link'] = link
                item['source'] = "NBC News"

                yield scrapy.Request(
                    link,
                    callback=self.parse_article,
                    meta={'item': item}
                )

    def parse_article(self, response):
        item = response.meta['item']
        date = response.css('time::attr(datetime)').get() or response.css('time::text').get()
        summary = response.css('p.lede::text, .article-body p:first-child::text').get() or response.css('article p::text').get()

        if date:
            item['date'] = date.strip()

        if summary:
            item['summary'] = summary.strip()

        yield item
```

You can read more at [UH Micromouse News Announcement](https://manoa.hawaii.edu/news/article.php?aId=2857).
