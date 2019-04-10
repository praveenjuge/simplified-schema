---
title: "Job Posting Schema"
description: "An organization can post a job opening using this schema that would tell Google to list everything when an applicant searches for it. For example, 'IBM Jobs' would list all the available jobs on IBM's website."
date: 2019-01-01 12:23:42 +0000
schema: "Job Posting"
---

## Microdata
---

```html
<div itemscope itemtype="http://schema.org/JobPosting">
  <h2 itemprop="title">Defence Against the Dark Arts Teacher</h2>

  <p>
    <strong>Description:</strong>
    <span itemprop="description">In this class you will teach students how to magically defend themselves against Dark Creatures, the Dark Arts, and other dark charms.</span>
  </p>
  
  <p itemprop="jobLocation" itemscope itemtype="http://schema.org/Place">
    <strong>Location:</strong>
    <span itemprop="address" itemscope itemtype="http://schema.org/PostalAddress">
    <span itemprop="streetAddress">445, Mount Road</span>
      <span itemprop="addressLocality">Scotland</span> 
      <meta itemprop="addressRegion" content="GB-SCT" />
      <meta itemprop="postalCode" content="G34" />
    </span>
  </p>

  <p>
    <strong>Hours:</strong>
    <span itemprop="employmentType">Full-time</span>,
    <span itemprop="workHours">40 hours per week</span>
  </p>

  <p itemprop="baseSalary" itemscope itemtype="http://schema.org/MonetaryAmount">
    <strong>Salary:</strong> 
    <span itemprop="currency">EUR</span> 
    <span itemprop="value" itemscope itemtype="http://schema.org/QuantitativeValue">
      <span itemprop="value">50000</span> / <span itemprop="unitText">Month</span>
    </span>
  </p>
  
  <p itemprop="hiringOrganization" itemscope itemtype="http://schema.org/Organization">
    <strong>Hiring by:</strong>
    <span itemprop="name">Hogwarts School of Witchcraft and Wizardry</span>
    <span itemprop="logo" itemscope itemtype="http://schema.org/ImageObject">
      <img itemprop="url" src="https://www.example.com/images/brand/logo.png" alt="Example Site">
    </span>
  </p>

  <p>
    <strong>Date Posted:</strong>
    <span itemprop="datePosted">2019-01-30</span>
  </p>
  
  <p>
    <strong>Position Available Till:</strong>
    <span itemprop="validThrough">2019-02-28</span>
  </p>
  
</div>
```

## Json-ld
---

```html
<script type="application/ld+json">
   {
    "@context" : "https://schema.org/",
    "@type" : "JobPosting",
    "title" : "Defence Against the Dark Arts Teacher",
    "description" : "In this class you will teach students how to magically defend themselves against Dark Creatures, the Dark Arts, and other dark charms.",
    "datePosted" : "2019-01-30T13:35:03+0200",
    "validThrough" : "2019-02-28T13:35:03+0200",
    "employmentType" : "FULL_TIME", // Case Sensitive, Full List Below
    "hiringOrganization" : {
      "@type" : "Organization",
      "name" : "Hogwarts School of Witchcraft and Wizardry",
      "sameAs" : "http://www.example.com",
      "logo" : "https://www.example.com/images/brand/logo.png"
    },
    "jobLocation": {
      "@type": "Place",
      "address": {
        "@type": "PostalAddress",
        "streetAddress": "445, Mount Road",
        "addressLocality": "Some Mountain Area, Scotland",
        "addressRegion": "SCT",
        "postalCode": "G34",
        "addressCountry": "GB"
      }
    },
   "baseSalary": {
      "@type": "MonetaryAmount",
      "currency": "EUR",
      "value": {
        "@type": "QuantitativeValue",
        "value":  50000.00,
        "unitText": "MONTH"
      }
    }
  }
</script>
```

## Usage Guidelines
---

For `employmentType` you can choose one of the values below. The value should be case sensitive if you want it to work on Google.

- FULL_TIME
- PART_TIME
- CONTRACTOR
- TEMPORARY
- INTERN
- VOLUNTEER
- PER_DIEM
- OTHER


*More Info Coming Soon!*