---
title: "Recipe Schema"
description: "If you have a cooking-based website then this schema is a must. This is widely used on assistant devices such as Google Home, so make sure your recipe is readable by a robot."
date: 2019-01-01 12:23:42 +0000
schema: "Recipe"
---

## Microdata

```html
<div itemscope itemtype="http://schema.org/Recipe">
  <meta itemprop="keywords" content="harry potter, beer, alcohal-free" />
  <meta itemprop="recipeCategory" content="Drinks" />
  <meta itemprop="recipeCuisine" content="British" />

  <h2 itemprop="name">Make a Harry Potter Themed Butterbeer</h2>
  By <span itemprop="author">Madam Rosmerta</span>, Written On
  <meta itemprop="datePublished" content="2019-02-10" />2019-02-10

  <img itemprop="image" src="https://example.com/butterbeer/photo.jpg" alt="Photo of Butterbeer" />
  <p itemprop="description">
    A simple brown sugar and butter syrup gets topped with cream soda and a dollop of cream in this wildly popular
    drink.
  </p>

  Prep Time:
  <meta itemprop="prepTime" content="PT10M" />10 Minutes, Cook time: <meta itemprop="cookTime" content="PT10M" />10
  Minutes, Yield: <span itemprop="recipeYield">2 Servings</span>,

  <div itemprop="nutrition" itemscope itemtype="http://schema.org/NutritionInformation">
    Nutrition facts:
    <span itemprop="calories">540 calories</span>,
    <span itemprop="fatContent">26 grams fat</span>
  </div>

  <p>
    Ingredients: - <span itemprop="recipeIngredient">1/4 cup evaporated milk</span> -
    <span itemprop="recipeIngredient">1/4 cup butterscotch sauce</span> -
    <span itemprop="recipeIngredient">2 tablespoons whipped butter, room temperature</span> -
    <span itemprop="recipeIngredient">1 1/2 cups vanilla cream soda</span>
  </p>

  Instructions:
  <span itemprop="recipeInstructions"
    >Combine evaporated milk, butterscotch topping, and butter in a glass heatproof measuring cup. Heat in microwave for
    1 minute. Remove and stir until butter has melted and incorporated into mixture. Meanwhile heat cream soda in
    another heatproof measuring cup for 1 minute 30 seconds. Divide butterscotch mixture between 2 (10 to 12-ounce)
    mugs. Fill mugs with heated cream soda and stir thoroughly.</span
  >

  <p itemprop="aggregateRating" itemscope itemtype="http://schema.org/AggregateRating">
    Rated <span itemprop="ratingValue">4.8</span>/5 based on <span itemprop="reviewCount">389</span> reviews
  </p>

  <!-- Video is Optional -->
  <div itemprop="video" itemscope itemtype="http://schema.org/VideoObject">
    <h2>Video: <span itemprop="name">Make a Harry Potter Themed Butterbeer</span></h2>
    <meta itemprop="duration" content="PT2M50S" />
    <meta itemprop="thumbnailUrl" content="https://example.com/butterbeer/photo.jpg" />
    Uploaded On
    <meta itemprop="uploadDate" content="2019-02-10" />2019-02-10
    <object ...>
      <param ... />
      <embed type="application/x-shockwave-flash" ... />
    </object>
    <span itemprop="description">This is how you make a Harry Potter Themed Butterbeer.</span>
  </div>

  140 comments:
  <div itemprop="interactionStatistic" itemscope itemtype="http://schema.org/InteractionCounter">
    <meta itemprop="interactionType" content="http://schema.org/CommentAction" />
    <meta itemprop="userInteractionCount" content="140" />
  </div>
  From Ron Weasley, May 5 - This butterbeer is delicious! ...
</div>
```

## Json-ld

```html
<script type="application/ld+json">
  {
    "@context": "https://schema.org/",
    "@type": "Recipe",
    "name": "Butterbeer",
    "image": ["https://example.com/butterbeer/photo.jpg", "https://example.com/butterbeer/photo2.jpg"],
    "author": {
      "@type": "Person",
      "name": "Madam Rosmerta"
    },
    "datePublished": "2019-02-10",
    "description": "A simple brown sugar and butter syrup gets topped with cream soda and a dollop of cream in this wildly popular drink.",
    "prepTime": "PT10M", // Period - Time 10 Minutes
    "cookTime": "PT10M",
    "totalTime": "PT20M",
    "keywords": "harry potter, beer, alcohal-free",
    "recipeYield": "2 Servings",
    "recipeCategory": "Drinks",
    "recipeCuisine": "British",
    "nutrition": {
      "@type": "NutritionInformation",
      "calories": "540 calories"
    },
    "recipeIngredient": [
      "1/4 cup evaporated milk",
      "1/4 cup butterscotch sauce",
      "2 tablespoons whipped butter, room temperature",
      "1 1/2 cups vanilla cream soda"
    ],
    "recipeInstructions": [
      {
        "@type": "HowToStep",
        "text": "Combine evaporated milk, butterscotch topping, and butter in a glass heatproof measuring cup."
      },
      {
        "@type": "HowToStep",
        "text": "Heat in microwave for 1 minute."
      },
      {
        "@type": "HowToStep",
        "text": "Remove and stir until butter has melted and incorporated into mixture."
      },
      {
        "@type": "HowToStep",
        "text": "Meanwhile heat cream soda in another heatproof measuring cup for 1 minute 30 seconds."
      },
      {
        "@type": "HowToStep",
        "text": "Divide butterscotch mixture between 2 (10 to 12-ounce) mugs."
      },
      {
        "@type": "HowToStep",
        "text": "Fill mugs with heated cream soda and stir thoroughly."
      }
    ],
    "review": {
      "@type": "Review",
      "reviewRating": {
        "@type": "Rating",
        "ratingValue": "4",
        "bestRating": "5"
      },
      "author": {
        "@type": "Person",
        "name": "Ron Weasley"
      },
      "datePublished": "2018-05-01",
      "reviewBody": "This butterbeer is delicious!",
      "publisher": "The butterbeer makery"
    },
    "aggregateRating": {
      "@type": "AggregateRating",
      "ratingValue": "5",
      "ratingCount": "18"
    },
    // Video is Optional
    "video": [
      {
        "name": "Make a Harry Potter Themed Butterbeer",
        "description": "This is how you make a Harry Potter Themed Butterbeer.",
        "thumbnailUrl": ["https://example.com/butterbeer/photo.jpg", "https://example.com/butterbeer/photo.jpg"],
        "contentUrl": "http://www.example.com/butterbeer.mp4",
        "embedUrl": "http://www.example.com/videoplayer.swf?video=butterbeer",
        "uploadDate": "2019-02-05T08:00:00+08:00",
        "duration": "PT2M50S",
        "interactionCount": "4000",
        "expires": "2020-02-05T08:00:00+08:00"
      }
    ]
  }
</script>
```

This amazing recipe is from [geekychef](http://www.geekychef.com/2008/12/butterbeer.html).


## Usage Guidelines

- Learn more about writing different time periods [here](https://en.wikipedia.org/wiki/ISO_8601#Durations).

*More Info Coming Soon!*


## How it might look

![Recipe Schema with search results for 'harry potter butterbeer recipe'](/images/schemas/recipe-schema.png "Recipe Schema with search results for 'harry potter butterbeer recipe'")
