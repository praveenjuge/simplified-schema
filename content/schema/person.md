---
title: "Person Schema"
description: "This schema is focused on an individual person on webpages, like team members, artist details, etc. You can also use this to get on search engine's knowledge panel but it's hard unless the person is well known."
date: 2019-01-01 12:23:42 +0000
schema: "Person"
---

## Microdata

```html
<div itemscope itemtype="http://schema.org/Person">
  <h2 itemprop="name">
    <a href="http://www.example.com" itemprop="url">Gandalf</a>
  </h2>
  
  <img itemprop="image" src="https://www.example.com/images/gandalf.jpg" alt="Photo of Gandalf">
  <p itemprop="disambiguatingDescription">Wizard sent by the West in the Third Age to combat the threat of Sauron.</p>
  <p><b>Email: </b><span itemprop="email">info@example.com</span></p>
  <p><b>Job Position: </b><span itemprop="jobTitle">Wizard</span></p>
  <p><b>Phone Number: </b><span itemprop="telephone">(123) 456-6789</span></p>
  
  <div itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
    <span itemprop="streetAddress">501 Buckland Rd</span>
    <span itemprop="addressLocality">Hinuera, Matamata</span>,
    <span itemprop="addressRegion">NZ</span>
  </div>
</div>
```

## Json-ld

```html
<script type="application/ld+json">
  {
    "@context": "http://schema.org",
    "@type": "Person",
    "name": "Gandalf",
    "disambiguatingDescription": "Wizard sent by the West in the Third Age to combat the threat of Sauron.",
    "url": "http://www.example.com",
    "image": "https://www.example.com/images/gandalf.jpg",
    "email": "info@example.com",
    "gender": "Male",
    "jobTitle": "Wizard",
    "height": "82 inches",
    "telephone": "(123) 456-6789",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "501 Buckland Rd",
      "addressLocality": "Hinuera, Matamata",
      "addressRegion": "NZ",
      "postalCode": "3472"
    }
  }
</script>
```

## Usage Guidelines

*Coming Soon!*

## How it might look

![Person Schema with search results for 'chris coyier'](/images/schemas/person-schema.jpg "Person Schema with search results for 'chris coyier'")
