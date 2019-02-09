---
title: "Website Schema"
description: "Details about Website Schema."
date: 2019-01-01 12:23:42 +0000
schema: "Website"
---

## Microdata
---

```html
<div itemscope itemtype="http://schema.org/WebSite">
  <link itemprop="url" href="http://www.example.com/" />
  <p itemprop="name">Example Site Name</p>
  <form itemprop="potentialAction" itemscope itemtype="http://schema.org/SearchAction">
    <meta itemprop="target" content="http://example.com/search?q={query}" />
    <input itemprop="query-input" type="text" name="query" /> 
    <input type="submit" />
  </form>
</div>
```


## Json-ld
---

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "WebSite",
    "url": "https://www.example.com/",
    "name": "Example Site",
    "potentialAction": [{
      "@type": "SearchAction",
      "target": "https://query.example.com/search?q={search_term_string}",
      "query-input": "required name=search_term_string"
    },
    // Optional - For Android App
    {
      "@type": "SearchAction",
      "target": "android-app://com.example/https/query.example.com/search/?q={search_term_string}",
      "query-input": "required name=search_term_string"
    }]
  }
</script>
```

## Usage Guidelines
---

*Coming Soon!*