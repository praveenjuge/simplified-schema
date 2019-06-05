---
title: "Event Schema"
description: "An event schema can be added to anything such as sports, concerts, lectures. You can come on search results for 'Events near me' if proper data is given. But don't self promote, just report the event."
date: 2019-01-01 12:23:42 +0000
schema: "Event"
---

## Microdata

```html
<div itemscope itemtype="http://schema.org/Event">
  <h2 itemprop="name">Superhero Running Race</h2>
  <p itemprop="description">Who is faster, The Flash or Superman? Well you can find the answer this Sunday!</p>
  <img itemprop="image" src="https://example.com/images/race.jpg" alt="A side by side image of Flash and Superman" />

  <p>
    <span itemprop="startDate" content="2019-01-30T13:35:03+0200">Wed, 30-Jan-19 13:35</span> -
    <span itemprop="endDate" content="2019-01-30T19:35:03+0200">19:35</span>
  </p>

  <p>
    Performed by:
    <span itemprop="performer" itemscope itemtype="http://schema.org/Person">
      <a href="https://en.wikipedia.org/wiki/Flash_(Barry_Allen)" itemprop="url">
        <span itemprop="name">The Flash</span>
      </a>
    </span>
    and
    <span itemprop="performer" itemscope itemtype="http://schema.org/Person">
      <a href="https://en.wikipedia.org/wiki/Superman" itemprop="url"> <span itemprop="name">Superman</span> </a>
    </span>
  </p>

  <p itemprop="location" itemscope itemtype="http://schema.org/Place">
    <link href="http://www.example.com/flash-museum/" itemprop="url" />
    <span itemprop="name">Flash Museum, Central City</span>
    <span itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
      <span itemprop="streetAddress">32, Flash Museum</span> <br />
      <span itemprop="addressLocality">Town Square</span>, <span itemprop="addressRegion">CC</span>
      <span itemprop="postalCode">123456</span> <meta itemprop="addressCountry" content="US" />
    </span>
  </p>

  <p itemprop="offers" itemscope itemtype="http://schema.org/Offer">
    <span itemprop="price" content="50.00">$50.00</span>
    <a itemprop="url" href="http://www.example.com/events/superhero-race/offers/">Tickets</a>
    <meta itemprop="priceCurrency" content="USD" />
    <meta itemprop="availability" content="http://schema.org/InStock" />
    <meta itemprop="validFrom" content="2019-01-27T13:35:03+0200" />
  </p>
</div>
```


## Json-ld

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Event",
    "name": "Superhero Running Race",
    "image": "https://example.com/images/race.jpg",
    "url": "http://www.example.com/events/superhero-race/",
    "description": "Who is faster, The Flash or Superman? Well you can find the answer this Sunday!",
    "startDate": "2019-01-30T13:35:03+0200",
    "endDate": "2019-01-30T19:35:03+0200",
    "location": {
      "@type": "Place",
      "name": "Flash Museum, Central City",
      "sameAs": "http://www.example.com/",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "32, Flash Museum",
        "addressLocality": "Town Square",
        "postalCode": "123456",
        "addressRegion": "CC",
        "addressCountry": "US"
      }
    },
    "offers": {
      "@type": "Offer",
      "url": "http://www.example.com/events/superhero-race/offers/",
      "price": "30",
      "priceCurrency": "USD",
      "availability": "https://schema.org/InStock",
      "validFrom": "2019-01-27T13:35:03+0200"
    },
    "performer":  [{
      "@type" : "Person",
      "name" : "The Flash",
      "sameAs" : "https://en.wikipedia.org/wiki/Flash_(Barry_Allen)"
    },{
      "@type" : "Person",
      "name" : "Superman",
      "sameAs" : "https://en.wikipedia.org/wiki/Superman"
    }]
  }
</script>
```

## Usage Guidelines

*Coming Soon!*


## How it might look

![Events in action with search results for 'events in new york'](/images/schemas/events-schema.png "Events in action with search results for 'events in new york'")
