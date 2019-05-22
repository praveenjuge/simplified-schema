---
title: "Difference between itemscope and itemtype in Schema"
description: "Ever wondered what the itemscope and itemtype that you use in your Schema mean? Well, me too."
date: 2019-05-22T14:36:49+00:00
author: "Praveen Juge"
category:
  - "Schema"
---

**itemscope:** When you use it in an HTML tag, you say that this tag contains some type of Schema. It is an identifier that says, “Yo Google, I have a Schema in my webpage.”

**itemtype:** This has the URL to the schema that you are using. It says, “This is the type of Schema that I’m using.”

### Example

```html
<div itemscope itemtype="http://schema.org/Person"> 
  <h2 itemprop="name"> 
  	<a href="http://www.lotr.com" itemprop="url">Gandalf</a> 
  </h2> 
</div>
```

Here, by using the `itemscope` you are telling that the div tag has some kind of Schema. The `itemtype` is the one which specifies that this Schema is about a Person. 

### FAQ

<details>
  <summary>Should I always put `itemtype` immediately after `itemscope`?</summary>
  Yes
</details>

<details>
  <summary>Where can I find a more reliable source for this?</summary>

  - Hurtful but ok,
  - [Getting Started - schema.org](https://schema.org/docs/gs.html#microdata_itemscope_itemtype)
  - [itemscope - HTML: Hypertext Markup Language | MDN](https://developer.mozilla.org/en-US/docs/Web/HTML/Global_attributes/itemscope)
</details>
