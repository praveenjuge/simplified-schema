---
title: "Microdata, RDFa or JSON-LD: Which should I choose for my Schema?"
description: "You have lots of choices when deciding the syntax that you use for Schema but Google, as always, has the last say."
date: 2019-05-26T03:06:32+00:00
author: "Praveen Juge"
category:
  - "Schema"
---

Here’s the tea,

- [Google](https://developers.google.com/search/docs/guides/intro-structured-data#structured-data-format) recommends you to use **JSON-LD**, probably because it’s easier to crawl through.
- Other search engines like [Yandex](https://yandex.ru/support/webmaster/schema-org/semantic-faq.html) and [Bing](https://www.bing.com/webmaster/help/marking-up-your-site-with-structured-data-3a93e731) also have JSON-LD, but they support all three equally.
- Wait, Yahoo has Search?
- Normal sane people like **Microdata** cause it’s easier to write within HTML markup.
- Web Performance Experts also like to use **Microdata.** Although JSON-LD won’t affect your page rendering, having lots of JSON-LD is frowned upon. (A E-Commerce site had 400 product’s JSON-LD info in the head tag)
- A general rule of thumb is to use **Microdata** when all the content is in the HTML markup (Like an [article](https://simplified-schema.netlify.com/schema/article/)) and to use **JSON-LD** when all the info is not available in the page itself (Like [JobPosting](https://simplified-schema.netlify.com/schema/job-posting/))
- Hipsters use **RDFa.**


## FAQ

<details>
  <summary>What’s the difference between Microdata and RDFa?</summary>
  They basically do the same job, except for different syntaxes.
</details>

<details>
  <summary>Can I use Microdata and JSON-LD in the same webpage like a mad man?</summary>
  Yeah
</details>

<details>
  <summary>Which is better for writing Semantic HTML? Microdata or RDFa?</summary>
  Both are almost the same so it doesn’t matter which you use, just write semantic HTML first and sprinkle Microdata later.
</details>

<details>
  <summary>Which do you use personally? </summary>
  I am so glad you asked dude, you know no one really asks me what I use and it’s really refreshing to know there are really people out there who care enough to ask me about my personal opinion. So thanks for asking.
</details>
