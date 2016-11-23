# bookscraper

This is a Scrapy project to scrape information about books at http://books.toscrape.com/

This project is only meant for educational purposes.
<h2>Extracted data</h2>

This project extracts all data including title, price, product type etc...
<br>A sample item:
<pre><code>
{
    'title': 'A Light in the Attic',
    'upc': '£51.77',
    'product_type': 'Books',
    'price': '£51.77',
    'tax': '£0.00',
    'stock': 'In stock (22 available)',
    'reviews': '0',
    'rating': '3'
}
</code></pre>

<h2>Spiders</h2>

This project contains two spiders: bookscraper-css and bookscraper-xpath. Both work the same way the first one is implemented with Css selectors the other one is implemented with xpath.

You can learn more about web scraping with Scrapy by going through the <a href="https://doc.scrapy.org/en/latest/intro/tutorial.html">original Scrapy Tutorial</a> or <a href="http://www.scrapingauthority.com/tutorials/scrapy/">Scrapy Tutorial Series</a> on <a href="http://www.scrapingauthority.com">ScrapingAuthority.com</a>.

<h2>Pipelines</h2>
This project contains four pipelines. One processes the "rating" field. The second one filters out books that have a stock number of more than five. The other two pipelines are meant to show you how to create json and csv files from the scraped data. You can disable pipelines in settings.py.

<h2>Running the spiders</h2>

You can run a spider using the <i>scrapy crawl</i> command:

<pre><code>
$ scrapy crawl bookscraper-css
$ scrapy crawl bookscraper-xpath
</code></pre>
