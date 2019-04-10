---
title: "Local Business Schema"
description: "Search engines now have a knowledge graph of all the relevant information like address, phone number, open hours about a business or an organization, this schema can get your business there."
date: 2019-01-01 12:23:42 +0000
schema: "Local Business"
---

## Microdata
---

```html
<div itemscope itemtype="http://schema.org/LocalBusiness">
  <h2 itemprop="name">Avengers Tower</h2>
  <span itemprop="description">A high-rise building complex located in Manhattan, New York City. Owned and constructed by Tony Stark.</span>
  <img itemprop="image" src="https://example.com/photos/1x1/photo.jpg" alt="Interior Image">
  <div itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
    <span itemprop="streetAddress">148 W 51st St</span>
    <span itemprop="addressLocality">Manhattan</span>,
    <span itemprop="addressRegion">NY</span>
  </div>
  Phone: <span itemprop="telephone">850-648-4200</span>
  <meta itemprop="priceRange" content="Not Applicable" />
</div>
```

## Json-ld
---

```html
<script type="application/ld+json">
  {
    "@context": "http://schema.org",
    "@type": "LocalBusiness",
    "name": "Avengers Tower",
    "description": "A high-rise building complex located in Manhattan, New York City. Owned and constructed by Tony Stark.",
    "telephone": "850-648-4200",
    "priceRange": "N/A",
    "image": [
      "https://example.com/photos/1x1/photo.jpg",
      "https://example.com/photos/4x3/photo.jpg",
      "https://example.com/photos/16x9/photo.jpg"
     ],
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "148 W 51st St",
      "addressLocality": "New York",
      "addressRegion": "NY",
      "postalCode": "10019",
      "addressCountry": "US"
    }
  }
</script>
```


## Microdata (For Restaurants)
---

```html
<div itemscope itemtype="http://schema.org/Restaurant">
  <h2 itemprop="name">Avengers Shawarma Palace</h2>
  <img itemprop="image" src="https://example.com/photos/1x1/photo.jpg" alt="Interior Image">
  
  <p itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
    <span itemprop="streetAddress">148 W 51st St</span>
    <span itemprop="addressLocality">Manhattan</span>,
    <span itemprop="addressRegion">NY</span> <span itemprop="postalCode">10019</span>
  </p>
  
  <p itemprop="telephone">(121) 2245-9600</p>
  <a itemprop="url" href="http://www.example.com">example.com</a>
  
  <p>Hours:
    <meta itemprop="openingHours" content="Mo-Sa 11:00-14:30">Mon-Sat 11am - 2:30pm
    <meta itemprop="openingHours" content="Su 17:00-22:00">Sun 5pm - 10:00pm
  </p>
  
  <p>Categories:
    <span itemprop="servesCuisine">Middle Eastern</span>,
    <span itemprop="servesCuisine">Levant</span>
  </p>
  
  <p>Price Range: <span itemprop="priceRange">$$$</span></p>
  
  <p>Takes Reservations: Yes
    <meta itemprop="acceptsReservations" content="True" />
  </p>
</div>
```

## Json-ld (For Restaurants)
---

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "Restaurant",
    "@id": "http://www.example.com",
    "name": "Avengers Shawarma Palace",
    "url": "http://www.example.com/restaurant-locations/manhattan",
    "telephone": "+12122459600",
    "menu": "http://www.example.com/menu",
    "acceptsReservations": "True",
    "priceRange": "$$$",
    "servesCuisine": [
      "Middle Eastern",
      "Levant"
    ],
    "image": [
      "https://example.com/photos/1x1/photo.jpg",
      "https://example.com/photos/4x3/photo.jpg",
      "https://example.com/photos/16x9/photo.jpg"
     ],
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "148 W 51st St",
      "addressLocality": "Manhattan",
      "addressRegion": "NY",
      "postalCode": "10019",
      "addressCountry": "US"
    },
    "geo": {
      "@type": "GeoCoordinates",
      "latitude": 40.761293,
      "longitude": -73.982294
    },
    "openingHoursSpecification": [
      {
        "@type": "OpeningHoursSpecification",
        "dayOfWeek": [
          "Monday",
          "Tuesday",
          "Wednesday",
          "Thursday",
          "Friday",
          "Saturday"
        ],
        "opens": "11:30",
        "closes": "22:00"
      },
      {
        "@type": "OpeningHoursSpecification",
        "dayOfWeek": "Sunday",
        "opens": "16:00",
        "closes": "22:00"
      }
    ]
  }
</script>
```

## Usage Guidelines
---

*Coming Soon!*