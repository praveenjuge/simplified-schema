---
title: "Product Schema"
description: "This can be useful for any physical or virtual product that is available on your webpage. You can give a lot of information about your product to display on search engines. A must-have for E-commerce based websites."
date: 2019-01-01 12:23:42 +0000
schema: "Product"
---

## Microdata
---

```html
<div itemscope itemtype="http://schema.org/Product">
  <meta itemprop="sku" content="123456"> <!-- Stock Keeping Unit - Optional -->
  
  <h2 itemprop="name">The One Ring</h2>
  <img itemprop="image" src="https://example.com/onering/photo.jpg" alt='A Golden Ring with Engraving on its sides.' />
  <p>
    Product description: <span itemprop="description">The One Ring was one of the most powerful artifacts ever created in Middle-earth. It was crafted by the Dark Lord Sauron in the fire of Orodruin.</span>
    Brought to you by: <span itemprop="brand">Mount Doom Corporation</span>
  </p>
  
  <p itemprop="offers" itemscope itemtype="http://schema.org/Offer">
    <span itemprop="priceCurrency" content="USD">$</span><span itemprop="price" content="600.00">600.00</span>
    <link itemprop="availability" href="http://schema.org/InStock" />In stock
    <meta itemprop="priceValidUntil" content="2020-11-05">
    <a itemprop="url" href="http://www.example.com/onering/buy-onering/">Buy Now!</a>
  </p>
  
  <p itemprop="aggregateRating"
    itemscope itemtype="http://schema.org/AggregateRating">
   Rated <span itemprop="ratingValue">4.8</span>/5
   based on <span itemprop="reviewCount">389</span> customer reviews
  </p>

  Customer reviews:
  <p itemprop="review" itemscope itemtype="http://schema.org/Review">
    <span itemprop="name">Apparently I shouldn't wear it</span> -
    by <span itemprop="author">Frodo Baggins</span>,
    <meta itemprop="datePublished" content="2019-04-01">April 1, 2019
    <span itemprop="reviewRating" itemscope itemtype="http://schema.org/Rating">
      <meta itemprop="worstRating" content = "1">
      <span itemprop="ratingValue">1</span>/
      <span itemprop="bestRating">5</span>stars
    </span>
    <span itemprop="description">This ring sucks, it's not even good to look at, maybe I should try it on...</span>
  </p>
  <p itemprop="review" itemscope itemtype="http://schema.org/Review">
    <span itemprop="name">Best thing I got on this journey</span> -
    by <span itemprop="author">Bilbo Baggins</span>,
    <meta itemprop="datePublished" content="2019-03-25">March 25, 2019
    <span itemprop="reviewRating" itemscope itemtype="http://schema.org/Rating">
      <meta itemprop="worstRating" content = "1"/>
      <span itemprop="ratingValue">5</span>/
      <span itemprop="bestRating">5</span>stars
    </span>
    <span itemprop="description">This ring makes me invisible! 5/5 would steal again!</span>
  </p>
  
</div>
```

## Json-ld
---

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org/",
    "@type": "Product",
    "name": "The One Ring",
    "image": ["https://example.com/onering/photo.jpg", "https://example.com/onering/photo2.jpg"],
    "description": "The One Ring was one of the most powerful artifacts ever created in Middle-earth. It was crafted by the Dark Lord Sauron in the fire of Orodruin.",
    "mpn": "925872", // Manufacturer Part Number - Optional
    "sku": "123456", // Stock Keeping Unit - Optional
    "brand": {
      "@type": "Thing",
      "name": "Mount Doom Corporation"
    },
    "aggregateRating": {
      "@type": "AggregateRating",
      "ratingValue": "4.8",
      "reviewCount": "389"
    },
    "offers": {
      "@type": "Offer",
      "url": "http://www.example.com/onering/buy-onering/",
      "priceCurrency": "USD",
      "price": "600",
      "priceValidUntil": "2020-11-05",
      "itemCondition": "https://schema.org/NewCondition", // Full List Below
      "availability": "https://schema.org/InStock",
      "seller": {
        "@type": "Organization",
        "name": "Mount Doom Corporation"
      }
    },
    // Review is Optional
    "review": [
      {
        "@type": "Review",
        "author": "Frodo Baggins",
        "datePublished": "2019-04-01",
        "description": "This ring sucks, it's not even good to look at, maybe I should try it on...",
        "name": "Apparently I shouldn't wear it",
        "reviewRating": {
          "@type": "Rating",
          "bestRating": "5",
          "ratingValue": "1",
          "worstRating": "1"
        }
      },
      {
        "@type": "Review",
        "author": "Bilbo Baggins",
        "datePublished": "2019-03-25",
        "description": "This ring makes me invisible! 5/5 would steal again!",
        "name": "Best thing I got on this journey",
        "reviewRating": {
          "@type": "Rating",
          "bestRating": "5",
          "ratingValue": "5",
          "worstRating": "1"
        }
      }
    ]
  }
</script>
```

## Usage Guidelines
---

For offers `itemCondition` you can choose one of the values below. The value should be case sensitive if you want it to work on Google.

- https://schema.org/NewCondition
- https://schema.org/DamagedCondition
- https://schema.org/RefurbishedCondition
- https://schema.org/UsedCondition

*More Info Coming Soon!*