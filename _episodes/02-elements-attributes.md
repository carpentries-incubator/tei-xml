---
title: "Elements and Attributes"
teaching: 60
exercises: 60
questions:
- "How do I mark up a description?"
- "How do I validate my markup?"
objectives:
- "Describe what content, elements and attributes are in TEI."
- "Mark up a description with TEI by hand and in an editor."
keypoints:
- "You can mark up a manuscript using fewer than 20 different elements. FIXME"
- "OTHER KEY POINTS? FIXME"
---

Building on first workshop, getting stuck in to manuscript description.

We will work together at the start, working on paper. When we get to Oxygen, you may work at your own pace.

## Discuss homework from previous exercise

> ## Discussion
> Look back at the two homework exercises in Episode 1:
>
> - Find `msDesc` (manuscript description)
> - Find `extent`
>
> FIXME -- MAYBE INCLUDE THE DISCUSSIONS 'SOLUTIONS' FROM LAST EPISODE HERE INSTEAD?
{: .discussion}


## Marking up descriptions (on paper)

### Common elements to use
- `<idno>` - Reference number
- `<title>` - Title
- `<material>` - Page/support material
- `<dimensions>` - Page dimensions
- `<measure>` - Number of folios
- `<layout>` - Page layout
- `<origDate>` - Date of manuscript
- `<origPlace>` - Place of origin
- `<collation>` - Collation
- `<binding>` - Binding description
- `<provenance>` - Provenance

> ## Activity: marking up
> 
> Here is some information from Latin MS 6 to be entered into elements in TEI. 
> Enter the correct information from here into the corresponding TEI elements.
>
> - Latin MS 6 
> - Petrus Lombardus super Psalmos 
> - Parchment 
> - Page height and width 355 x 240mm 
> - 197 folios
> - Double columns of 48 lines
> - 12th century
> - Written in Germany
> - i8 ii8 (wants 1) iii-xxiv8 xxv4, xxvi2
> - The front cover is plated with gilt metal, apparently, of 13th century. 
> It is thus arranged. The border is composed of six oblong plates of enamel (at the corners and in the middle of the sides) 
> bearing decorative designs: 
> the intervals between these are occupied by six longer strips of filagree work, each of which is set with four stones. 
> The central plate of gilt metal has an incised design of foliage partially surrounding a crucifix. 
> The figure on the cross is in relief, crowned, with loin-cloth, and is fastened by four nails. 
> The cross is set with small turquoises. The head (bearded) inclines to left. The title of the cross bears the letters IHS: 
> above it is the Divine Hand. The interior angles of the cross are filled in, so that there is a disk at the intersection. 
> The field or body of the cross is enamelled. At each extremity are two stones; two more are on the right of the lower part of the cross, 
> and one is opposite to them on left. Nail holes (seven in number) are in various parts of the field. 
> At the angles of the panel are four disks of enamelled metal, bearing decorative designs. 
> The second cover is of wood, covered with green-brown velvet. 
> It can hardly be supposed that the metal plate originally belonged to the manuscript now associated with it. 
> There is some doubt as to whether the binding originally belonged originally to this MS
> - From the Cistercian Abbey of Hunnerode
> - Bought by Lord Lindsay in October 1861 from the London bookseller Thomas Boone of New Bond St. for £80
>
> We will use the following elements and colours:
> - `<msContents>` (intellectual content): blue
> - `<physDesc>` (physical description): red
> - `<history>` (history of the manuscript): green
{: .challenge}


## Transfering markup into TEI XML (in Oxygen)

We have provided some tips and tricks for marking up text in Oxygen. See the bottom of this page.

> ## Activity
> 
> Now you have marked up a document by hand, it is time to put it into a text editor. 
> Start with the template we have provided, replace the blanks with your markup.
> 
{: .challenge}

## Validating markup

To check that your markup is valid (in other words, there are no syntax errors), tick the "Validate" box. 
Look for any red lines under markup to identify invalid code. 
Look for a message at the bottom of screen to say "Validation Successful".


## Homework: Adding attributes

If you are comfortable working in Oxygen, you should add these attributes to the XML file you created at the workshop (for Latin MS 6). 
If you have less experience with Oxygen and XML, use the partially completed version in the homework folder (Latin MS 6_template_attributes). 
You might find it helpful to look at the XML for Latin MS 98 (from the homework for workshop 1) 
or the Draft Style Guide for Cambridge Digital Library (pdf).

FIXME: links above

> ## Replace attribute values
> 
> The element `<msDesc>` has three attributes. 
> For the attribute `xml:id`, replace the value `"UkMaJRU-Latin-MS-00"` with `"UkMaJRU-Latin-MS-06"`
{: .challenge}

> ## Add attributes and values to elements
>
> For `<supportDesc>`:
>
> - add attribute name: `material`
> - add attribute value: `parchment`
>
> For `<measure>`:
>
> For `<height>` and `<width>`:
> 
> - add attribute `quantity="nnn"` (i.e. `355` and `240`).	
>	
> For `<binding>`:
> 
> - add attribute `calendar` with value `gregorian`
> - attributes `notBefore` and `notAfter` with years (`YYYY`)
> - add certainty (attribute `cert` choose value from drop-down list).
>
> For `<origPlace>`:
>
> - add attribute `ref` (value isURL of the VIAF entry - find Germany in VIAF, or see LatinMS98)
> 
> For `<origDate>`:
>
> - add dating attributes as for binding
> `<item><ref target="http://id.loc.gov/authorities/subjects/"/>Religion</item>`{:.language-xml}
{: .challenge}


> ## Extra bits
>
> In `<provenance>`, markup Lord Lindsay within a `<persName>` element within a `<name>` element. 
>
> Add to the `<persName>` element the attribute `type=”display”`. 
> 
> Add to the `<name>` element the attributes `type` (`person`) and `subtype` (`fmo` – i.e. former owner), 
> and `ref` (value is URL of the VIAF entry)
>
> Within `<profileDesc>` add a suitable subject index term from the Library of Congress Subject Headings (within `<item>`)
> `<ref target=”http://id.loc.gov/authorities/subjects/sh9999”>term</ref>`
{: .challenge}


## Tips and tricks for working with Oxygen

> ## Oxygen shortcut keys
>
> To insert a £ sign, click on "Edit" > "Insert from Character Map" and select "£", "Character Entity: Decimal" then click "Insert".
>
> Oxygen has dozens of keyboard shortcuts, under "Options / Menu Shortcut Keys". These are some of the most useful ones: 
>
> Select some text, and press <kbd>Control</kbd> + <kbd>E</kbd>. You can choose an element to put around the text. 
>
> Place the cursor in an element, press <kbd>Alt</kbd> + <kbd>Shift</kbd> + <kbd>D</kbd>. 
> This splits the element in two (e.g. to turn a long paragraph into two paragraphs, or one list item into two).
>
> Put the cursor in an element and press <kbd>Control</kbd> + <kbd>Alt</kbd> + <kbd>X</kbd>. 
> The tag disappears leaving its contents. 
> 
> Put your cursor in an element, and press <kbd>Control</kbd> + <kbd>Shift</kbd> + <kbd>,</kbd>. 
> The tag will be commented out. Press the same thing again, and the comment will disappear.
> 
> Press <kbd>Control</kbd> + <kbd>Shift</kbd> + <kbd>V</kbd> to validate your file. 
>
> Press <kbd>Control</kbd> + <kbd>Shift</kbd> + <kbd>W</kbd> to check well-formedness. 
>
> Press <kbd>Control</kbd> + <kbd>Shift</kbd> + <kbd>Y</kbd> to toggle Line Wrap. 
> Mostly, when editing TEI documents, we want to have line wrap turned on, but it’s off by default in Oxygen. 
>
> There are lots of things that you can set up a keyboard shortcut for. Here's an example: 
>
> - Go to "Options / Menu Shortcut Keys". 
> - Type ‘maximize’. You should see Maximize/Restore Editor Area.
> - Click on the description, and then on Edit. 
> - Type the <kbd>F11</kbd> key, and press OK. 
> - Now hit <kbd>F11</kbd> a couple of times while you’re editing. It hides then restores all the surrounding panels. 
> This can be very handy if you’re editing a large document on a small screen. 
>
{: .callout}


> ## Other useful features in Oxygen
>
> Oxygen has a very rich feature set, but here are a couple of features you’ll find useful:
>
> Find All. Press "Find / Find Replace" (or <kbd>Control</kbd> + <kbd>F</kbd>) to see the find box. 
> Try Find All. You get a list of hits in the window at the bottom. Clicking on each hit will take you to it in the document. 
>
> Tip: If you’re using this to make changes, then make your changes from the bottom up. If you make changes from the top of the document, the other hits will no longer point at the right location in the document, because the offsets have changed. 
>
> Find / Replace in Files. Right-click on a folder in your Project panel and click on Find / Replace in Files. 
> You can search the entire folder, and get back a list of results just like Find All, but grouped into files. 
> Double-click on a hit to open the file and jump to the hit location. 
>
> The XPath box. In the top left, near the "File" menu, is a text box labelled "XPath 2.0". 
> Type ``//p`` in this box and press <kbd>Return</kbd> to find all the tags, or ``//@type`` to find all the type attributes.
>
{: .callout}


{% include links.md %}
