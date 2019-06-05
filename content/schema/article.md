---
title: "Article Schema"
description: "An article schema could be used on many types of written content such as News Article, Blog Post, Scholarly Paper and much more. If done properly on a blog, this could improve your SEO results immensely."
date: 2019-01-01 12:23:42 +0000
schema: "Article"
---

## Microdata

```html
<article itemscope itemtype="http://schema.org/Article">
  <link itemprop="mainEntityOfPage" href="https://www.example.com/articles/proof-superman-clark-kent/" />
  <meta itemprop="description" content="Why does everyone think that Clark Kent might be Superman? He is not and here is proof."/>
  
  <h1 itemprop="headline">Definite Proof that Clark Kent isn't Superman</h1>
  
  <time datetime="2019-01-29T21:29:21-0800" itemprop="datePublished" pubdate>January, 29 2019</time>
  <meta itemprop="dateModified" content="2019-01-29T21:29:21-0800">
  
  <span itemprop="author" itemscope itemtype="http://schema.org/Person">by 
    <a itemprop="sameAs" rel="author" href="https://www.example.com/authors/lois-lane/">
      <span itemprop="name">Lois Lane</span>
    </a>
  </span>
  
  <figure itemprop="image" itemscope itemtype="http://schema.org/ImageObject">
    <meta itemprop="representativeOfPage" content="true">
    <meta itemprop="url" content="https://www.example.com/images/articles/clark-superman.jpg">
    <meta itemprop="width" content="1000"> <!-- Atleast 700px Recommended -->
    <meta itemprop="height" content="700">
    <meta itemprop="description" content="Side to Side Picture of Clark Kent and Superman.">
    <picture>
      <img src="https://www.example.com/images/articles/clark-superman.jpg" alt="Side to Side Picture of Clark Kent and Superman." itemprop="contentUrl">
    </picture>
  </figure>
  
  <div itemprop="articleBody">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Provident molestiae iure unde? Aliquid officia earum nemo velit ab doloribus accusantium molestias quae quam. Soluta quibusdam eos qui totam sit iure?</div>
  
  <div itemprop="publisher" itemscope itemtype="http://schema.org/Organization">
    <a href="https://example.com" title="Example Site" tabindex="-1" itemprop="url">
      <span itemprop="logo" itemscope itemtype="http://schema.org/ImageObject">
        <img itemprop="url" src="https://www.example.com/images/brand/logo.png" alt="Example Site">
      </span>
    </a>
    <span class="screen-reader" itemprop="name">Example Site</span>
  </div>
</article>
```

The above markup is a little opinionated but it's a very good starting point for article schema. If for some reason you can't use the microdata format described above, I recommend you to use the JSON-LD below.

## Json-ld

```html
<script defer type="application/ld+json">
  {
    "@context": "http://schema.org",
    "@type": "Article",
    "headline": "Definite Proof that Clark Kent isn't Superman", // 100-110 Characters Recommend 
    "description": "Why does everyone think that Clark Kent might be Superman? He is not and here is proof.",
    "datePublished": "2019-01-29T21:29:21-0800",
    "dateModified": "2019-01-29T21:29:21-0800",
    "wordCount": "200",
    "author": {
        "@type": "Person",
        "name": "Lois Lane"
    },
    "mainEntityOfPage": {
      "@type": "WebPage",
      "@id": "https://www.example.com/articles/proof-superman-clark-kent/"
    },
    "image": {
      "@type": "imageObject",
      "url": "https://www.example.com/images/articles/clark-superman.jpg"
    },
    "publisher": {
      "@type": "Organization",
      "name": "Example Site",
      "logo": {
        "@type": "imageObject",
        "url": "https://www.example.com/images/brand/logo.png"
      }
    }
  }
</script>
```

## Usage Guidelines
*Coming Soon!*

## How it might look

![Article Schema in action with Search Results for 'taylor swift'](/images/schemas/article-schema.png "Article Schema in action with Search Results for 'taylor swift'")
