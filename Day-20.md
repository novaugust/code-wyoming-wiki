# SEO

## SERP
Search Engine Result Page

## Search Algorithms
They are magical, and how they decide to rank different sites is proprietary, secret knowledge.

## Important tags
We do, however, know that the following tags are important in SEO.

* meta
* title
* header tags (h1, h2, ..)
* anchor tags
* alt attributes
* writing good, clean code

### Things that will negatively effect your SEO

* Incorrect / incomplete tags
* Duplicate code / tags
* Too much code
* Text hidden by code
* Unnecessary script code

## Keywords
Identify the key words that are important to you for getting found in search results. For example, for a fishing company in Jackson, WY,  `jackson`, `fishing`, `fishing guides` would be keywords.

## Title 
The title is what shows on search results. It also is used by many social media sites.
It influences both users interest and SEO rankings.

* Google shows a maximum of 70 characters. Longer titles are fine, but keep that in mind.
* Identify yourself in your title
* Make the title unique to each page
* Make the title tag match the h1
* Add keywords to the title
    Careful here! Don't get carried away with making it too long. Adding a location within your title is common practice.
    
Mostly, ask yourself, what will truly 


## Meta
Meta tags go in the head section, and help identify important information about the page.

### Description

```html
<meta name="description" content="My website that's all about stuff.">
```

This is the most important meta tag for SEO. Just like the `title` tag provides a title, `description` provides a description for the webpage.

**However, meta descriptions have no impact on SEO rankings**. So why bother with them?

Descriptions are seen prominently in two places.

1. Search results
    The description appears directly below the title.
2. Social media sharing
    The description is the text that will be seen on the share.

#### Description not shown
There are times when the description is **not** shown on the SERP. This is when the keywords searched for do not appear within your meta description. In that case, the user will be given an excerpt of the content on the page.
So, be sure to use the appropriate keywords in your description.

Limit your description to 160 characters. (SERPS will not go beyond that)
Like the title, each description should be unique.

### Keywords
This is falling out of use. It was a list of comma separated keywords.
Both google and bing are ignoring this meta property, as it was too easily abused.

So is it still worth adding? Perhaps, if you're working in countries where google and bing aren't the dominent search engines.


## Site Structure

Your homepage is a big deal here. If you can't get from your home page to important content, your need to rework you structure.
Typically, home pages will link to "category" pages, which contain yet more links to pages within a category.

### Breadcrumbs

These are nice for large, complex webpages.

### Subdirectories

Structure your website into subdirectories, and give the subdirectories names that make sense. Bonus points if you can use keywords in your URL.

```
http://www.sports.com/baseball/statistics
```

Some amount of SEO value is assigned to your naming of internal links.

If you're using a CMS that gives you URLs with strange numbers and codes you don't really understand... well, web spiders feel the same way.

A good CMS will allow you to construct sensible permalinks.

Content that is deep within other subdirectories receives a lower score from spiders, and users are less likely to click such a link.

## Canonicalization
If you have duplicate pages on your website, the search engine may penalize you for trying to cheat it. Or, the search engine may split your value between the two pages, giving you a lower ranking than you deserve.

Canonicalization allows you to specify "this is the **main** page for this content". In other words, when you have two urls that point to the same content, the canonicalization

So, to do so, add the following code to the *duplicate* page.

```
<link rel="canonical" href="http://myWebsite.com/the-real-url" >
```

## Page Structure
Have your main navigation menu come early in the code for your page structure.

### Headers

Headers (h1, h2, ...) are important markers that say "this content is important".

#### h1

The blog post name on your blog, or your product name on your product page.

In fact, try to make the h1 match the title.

### Fragment Anchors
For large, single page websites, be sure to use fragment anchors to help users find content.

### Footers
Use footers to provide links to content that is only occasionally need, but not necessarily important enough to make it into the header / nav. You can also repeat the important links down in the footer as well.

## Noindex and Nofollow
[Robots meta](http://www.robotstxt.org/meta.html)

By default, spiders will save and index just about every page they come to on a webpage.

You may have pages you don't want a spider to index, like promotion pages meant for customers provided through email links, or pages for employees only.

Whatever you don't want the public to see should not be indexed.

### Noindex
To keep a page from being indexed, add this meta tag.
```
<meta name="robots" content="noindex">
```
You may still get crawled and cached, but no longer appear on SERPs. 
Be careful. **This will kill your page from appearing on SERPS**
Do not add it to a template and accidentally kill your entire site.

### Robots.txt
[Robotstxt.org](http://www.robotstxt.org/robotstxt.html)

You can create a file which shuts down parts of your website to robots.
NPR's robots.txt:
```
User-agent: *
Disallow: /mpx/
Disallow: /cgi-bin
Disallow: /ramfiles/
Disallow: /*.smil
Disallow: /*.asx
Disallow: /*.ram
Disallow: /*.wav
Disallow: /*.rmm
Disallow: /*.js
Disallow: /*.au
Disallow: /stations/force/force_localization.php?
Disallow: /rundowns/segment.php?
```

### Nofollow

#### In Anchors
When you link to another page, search engines see it as a "vote" or endorsement for that website. If you have links on your webpage someone is paying for, or there are links on your website you didn't insert yourself (ie, comments), be sure to add the nofollow attribute to the link.

```
<a href="//usergeneratedlink.com" rel="nofollow">
```

This keeps us from looking like black hats to google.

#### In meta robots
No follow inside of a meta robots essentially sets the `rel="nofollow"` attribute on every link in the page.

## Sitemaps
[Sitemaps.org](http://www.sitemaps.org/protocol.html)

A modern sitemap is an xml file created specifically for robots to consume.

At its most basic, a sitemap looks like this
```xml
<?xml version="1.0" encoding="UTF-8"?>

<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">

   <url>

      <loc>http://www.example.com/</loc>

   </url>
  <url>

      <loc>http://www.example.com/some-page</loc>

   </url>

</urlset> 
```
#### Optional tags
Each `url` can have additional information specified with the following tags.

* lastmod
    When the file was last updated, in [w3c datetime format](http://www.w3.org/TR/NOTE-datetime) -- but just YYYY-MM-DD is fine.
* changefreq
    The frequence with which the url is updated, from the following list
    * always
    * hourly
    * daily
    * weekly
    * monthly 
    * yearly
    * never
* priority
    Values for priority range from 0.0 to 1.0.  By default, a page's priority is 0.5. This marks the priority of your pages *relative to one another*, not to external webpages.
    
    
### Example sitemap

```xml
<?xml version="1.0" encoding="UTF-8"?>

<urlset xmlns="http://www.sitemaps.org/schemas/sitemap/0.9">

   <url>

      <loc>http://www.example.com/</loc>

      <lastmod>2005-01-01</lastmod>

      <changefreq>monthly</changefreq>

      <priority>0.8</priority>

   </url>

   <url>

      <loc>http://www.example.com/catalog?item=12&amp;desc=vacation_hawaii</loc>

      <changefreq>weekly</changefreq>

   </url>

   <url>

      <loc>http://www.example.com/catalog?item=73&amp;desc=vacation_new_zealand</loc>

      <lastmod>2004-12-23</lastmod>

      <changefreq>weekly</changefreq>

   </url>

   <url>

      <loc>http://www.example.com/catalog?item=74&amp;desc=vacation_newfoundland</loc>

      <lastmod>2004-12-23T18:00:15+00:00</lastmod>

      <priority>0.3</priority>

   </url>

   <url>

      <loc>http://www.example.com/catalog?item=83&amp;desc=vacation_usa</loc>

      <lastmod>2004-11-23</lastmod>

   </url>

</urlset>
```


### Sitemap size
Sitemaps cannot have more than 50,000 URLS and be no larger than 10MB. If you exceed this limit, look into [sitemap index files](http://www.sitemaps.org/protocol.html#index)

### Alternate Sitemaps
You can also provide RSS feeds or text files.

IF you use a text file, it should have simply one URL per line.

### Sitemap location
Place your sitemap at the root directory of your webpage and name it `sitemap.xml`.

```
http://example.com/sitemap.xml
```

Specify this location in your `robots.txt`
```
...
Sitemap: http://www.example.com/sitemap.xml
...
```
Some search engines have webmaster tools that allow you to submit the sitemap directly to the search engine.





## Social Metas
Facebook, twitter, and other social media sites allow you to proactively specify how your content should look when it is shared.

Titles and descriptions should still be though of under the same constraints as normal titles and descriptions (70 characters and 160 characters, respectively).

### Facebook's open graph (OG)

[Open Graph description](https://developers.facebook.com/docs/opengraph/)

Facebook's open graph protocol uses the following meta tags.

* og:title
* og:description
* og:url
* og:image
* og:type

### Twitter Cards

[Twitter Cards API](https://dev.twitter.com/docs/cards)

When links are in tweets, users may see additional information in a nicely formatted display

* twitter:title
* twitter:description
* twitter:url
* twitter:image
* twitter:card

## Google places and authorship

* [Authorship](http://www.google.com/insidesearch/features/authorship/)
* [Places](http://www.google.com/business/placesforbusiness/)
If you're a content creator (blogger)''


# HTML5 Video & Audio
I just have a link. Sorry. [MDN Vid & Aud](https://developer.mozilla.org/en-US/docs/Web/Guide/HTML/Using_HTML5_audio_and_video)