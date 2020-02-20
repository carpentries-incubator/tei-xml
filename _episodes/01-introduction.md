---
title: "Introduction to TEI"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "Understand the key features of a simple TEI record"
- "Explain the ways in which TEI can be used to describe special collections material"
- "Explain some of the key jargon used in TEI cataloguing"
- "Complete a simple TEI template"
- "Find information about cataloguing in TEI"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

# What is TEI?

Text Encoding Initiative

- Guidelines
- Organisation
- Community of practice

TEI logo and link

- Markup language based on XML (eXtensible Markup Language)
- Flexible and diverse
- A mechanism for structuring information

Photo by Ashkan Forouzani on Unsplash


# XML examples
## XML content and elements

```xml
<layout>
	<p>1 column, 25 lines</p>
</layout>
<pb/>
```

## XML attributes with values

```xml
<layout columns="1" writtenLines="25">
  	<p>1 column, 25 lines</p>
</layout>
```

# How is TEI constructed?

```xml
<TEI "http://www.tei-c.org/ns/1.0">
	<teiHeader>...</teiHeader>
	<facsimile SAMPLE>...</facsimile>
	<text>SAMPLE...</text>
</TEI>
```

## Header



{% include links.md %}

