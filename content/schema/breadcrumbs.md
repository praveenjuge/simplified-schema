---
title: "Breadcrumbs Schema"
description: "Details about Breadcrumbs Schema."
date: 2019-01-01 12:23:42 +0000
schema: "Breadcrumbs"
---

## Microdata
---

```html
<nav aria-label="breadcrumb">
  <ol itemscope itemtype="http://schema.org/BreadcrumbList">
    <li itemprop="itemListElement" itemscope itemtype="http://schema.org/ListItem">
      <a itemprop="item" href="https://example.com/books"> 
        <span itemprop="name">All Books</span>
      </a>
      <meta itemprop="position" content="1" />
    </li>
    <li itemprop="itemListElement" itemscope itemtype="http://schema.org/ListItem">
      <a itemprop="item" href="https://example.com/books/fiction"> 
        <span itemprop="name">Fiction</span>
      </a>
      <meta itemprop="position" content="2" />
    </li>
  </ol>
</nav>
```

## Json-ld
---

```html
<script type="application/ld+json">
  {
   "@context": "http://schema.org",
   "@type": "BreadcrumbList",
   "itemListElement":[{
     "@type": "ListItem",
     "position": 1,
     "item":
     {
      "@id": "https://example.com/books",
      "name": "Books"
     }
    },{
     "@type": "ListItem",
     "position": 2,
     "item":
     {
       "@id": "https://example.com/books/fiction",
       "name": "Fiction"
     }
    }]
  }
</script>
```

## Usage Guidelines
---

*Coming Soon!*