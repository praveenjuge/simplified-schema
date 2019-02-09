---
title: "Organization Schema"
description: "Details about Organization Schema."
date: 2019-01-01 12:23:42 +0000
schema: "Organization"
---

## Microdata
---

```html
<div itemscope itemtype="http://schema.org/Organization">
  <meta itemprop="url" content="http://www.example.com" />
  
  <h2 itemprop="name">Night's Watch</h2>
  <img itemprop="logo" src="https://www.example.com/images/brand/logo.png" alt="Night Watch Logo">
  <p><strong>Tel: </strong><span itemprop="telephone">(331) 4268 5300</span></p>
  <p><strong>E-mail: </strong><span itemprop="email">jon@example.com</span></p>
  
  <p itemprop="founders" itemscope itemtype="http://schema.org/Person">
    <strong>Founded By: </strong>
    <span itemprop="name">Jon Snow</span>
  </p>
  
  <p>
    <strong>Address:</strong>
    <span itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
        <span itemprop="streetAddress">38 avenue de l'Opera</span>
        <span itemprop="postalCode">F-75002</span>
        <span itemprop="addressLocality">Paris, France</span>
    </span>
  </p>
</div>
```

## Json-ld
---

```html
<script type="application/ld+json">
  {
    "@context": "http://schema.org",
    "@type": "Organization",
    "name": "Night's Watch",
    "legalName" : "Elite Strategies Llc",
    "url": "http://www.example.com",
    "logo": "https://www.example.com/images/brand/logo.png",
    "foundingDate": "1765",
    "email": "jon@example.com",
    "telephone": "(331) 4268 5300",
    "address": {
      "@type": "PostalAddress",
      "addressLocality": "Paris, France",
      "streetAddress": "38 avenue de l'Opera",
      "postalCode": "F-75002"
    },
    "sameAs": [
       "http://www.twitter.com/nightwatch",
       "http://www.linkedin.com/company/nightwatch"
     ],
    "founders": {
      "@type": "Person",
      "name": "Jon Snow"
    }
  }
</script>
```

## Usage Guidelines
---

*Coming Soon!*