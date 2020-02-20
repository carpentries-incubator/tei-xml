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

TEI stands for: the Text Encoding Initiative. It has been developed to describe text based objects (eg. manuscripts, archives, letters) but is also being used in some cases to describe visual materials. TEI (helpfully) is actually three things: 

- it is a set of **guidelines** for describing objects and structuring information
- it is an **organisation** which oversees the production of official guidelines (more on this later)
- it is a **community of practice** of people using the guidelines

IMG: TEI logo and link

TEI is one kind of **mark up language**.  Markup encodes information about text – so it could describe the structure, appearance and content of a text. Digital markup has to be explicit and unambiguous so that a computer can understand it.

TEI is **based on XML** (eXtensible Markup Language), which is a descriptive markup language. EAD (encoded archival description), used to describe archival materials, also uses xml. Markup can be presentational (it tells you about how the text appears on the page eg. line breaks, tabs etc.), procedural (it gives an output device, for example a printer, information about how it should deal with text) or descriptive (it encodes the structure of the text, but not what to do with it).
(Coombs, James H., Allen H. Renear, and Steven J. DeRose. 1987. "Markup Systems and the Future of Scholarly Text Processing." in (Landow and Delaney 1993))

TEI is very **broad and flexible** – it can be used in many ways. At the moment, at The Unversity of Manchester Library, we are using it primarily as a mechanism for **structuring** information.

IMG: Photo by Ashkan Forouzani on Unsplash


## XML examples
XML is made up of content, elements and attributes.


### XML content and elements

```xml
<layout>
	<p>1 column, 25 lines</p>
</layout>
<pb/>
```

Here you can see the ‘human readable’ content – “1 column, 25 lines” (it describes how a manuscript page is laid out) – this is what gets displayed on a viewer or online catalogue (or in a pdf version). This is surrounded by elements which structure the information. Like in html, the element also determine the formatting of the content.

The common element `<p>` for paragraph, is nested inside the element `<layout>`

Every element has an opening and closing ‘tag’. The beginning of the element is denoted by the element name in angled brackets. The end of the element has a slash before the element name. You can get ‘empty’ elements without content, like page break `<pb/>` (this functions as the beginning and end of an element).


### XML attributes with values

```xml
<layout columns="1" writtenLines="25">
  	<p>1 column, 25 lines</p>
</layout>
```
Elements can also contain ‘machine-readable’ content. This can be used to search and filter through large datasets.

Here, the number of columns and lines is also given in the attributes.

The attribute names are shown here in olive brown. This is followed by an equal sign, then the content in double quotes.



# How is TEI constructed?
Don’t worry, you don’t need to remember this!

```xml
<?xml version="1.0" encoding="UTF-8"?>
<TEI>
	<teiHeader>...</teiHeader>
	<facsimile>...</facsimile>
	<text>...</text>
</TEI>
```

There are three main elements in a TEI file: header, facsimile and text. All the other elements are nested in one of these.

- The `header` describes both the TEI file itself and its ‘source’ (i.e. the object which is being encoded)
- `facsimile` is where metadata about digital facsimiles (images) is provided
- `text` is where the text is transcribed
 
IMG: outline view from Oxygen

The images are from screenshots of the ‘outline’ view in the Oxygen editor – you can use this to navigate around a TEI document. XML enables linking between sections. For example, if you describe an illustration in the header, this can be linked to via the facsimile section. 

We’re not going to cover here how the facsimile section is arranged!


## Header

```xml
<TEI>
	<teiHeader>
		<fileDesc>
			<titleStmt>Catalogue of Latin Manuscripts</titleStmt>
			<publicationStmt>The University of Manchester</publicationStmt>
			<sourceDesc>...</sourceDesc>
		</fileDesc>
		<encodingDesc>...</encodingDesc>
		<profileDesc>...</profileDesc>
		<revisionDesc>...</revisionDesc>
	</teiHeader>
	<facsimile>...</facsimile>
	<text>...</text>
</TEI>
```

 - `fileDesc` – this describes the TEI file itself, for example its title, author and publication details (including rights statements), and contains the description of the source, such as the manuscript. We’ll cover this in more detail at the next workshop.
 - `encodingDesc` – this describes how the file has been encoded, including what taxonomies are used (for example states that Library of Congress Subject Headings are being used)
 - `profileDesc` – includes the subject headings themselves, information about language, and can contain correspDesc
 - `revisionDesc` – where you record any changes to the file (should have date and name, and can also include details of changes made)

## Text

```xml
<TEI>
	<teiHeader>...</teiHeader>
	<text xml:id="HAM/1/1/3/8">
		<body>
			<pb n="1"/>
			<lb/>...
			<opener>Dear ...</opener>
			<lb/>...
			...<choice>learnd</choice>...
			<lb/>...
```

The text can be divided into three main components:
 - `front` – for front matter – title, prefaces, contents page etc.
 - `body` is the main body of the text!
 - `back` is the back matter – indexes etc.
 
You can also ‘nest’ other texts within text

TEI is used to transcribe texts in a systematic and complex structure – called ‘scholarly apparatus’. We’re keeping it simple. For the exercise, we are only using `body`, which can be divided into divisions, and also by page breaks and line breaks.

> ## Try out a TEI puzzle
> 
> This puzzle will help you to put together your very first TEI record by filling in the blanks. 
> As you work through it, have a think about what some of these elements might mean.
> 
> Activity details FIXME
> > ## Solution
> > details of solution FIXME

(ROUGH:) To access this puzzle and the instructions, navigate to the LibraryConnect folder called ‘TEI Puzzle’ by clicking on the link in the ‘Activity’ box. 

# Jargon busting


{% include links.md %}

