---
title: "Descriptions and Cataloguing"
teaching: 60
exercises: 60
questions:
- "How do you mark up a locus?"
- "How do you link a locus?"
- "(something on manifests and authorities)"
objectives:
- "Work between records"
- "(catalogue)"
- "objective 1 (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---
Building on first workshop, getting stuck in to manuscript description.

## Discuss homework from previous exercise

> ## Discussion
>
> - Did you use the file you created, or the template?
> - Did you have any validation errors or other problems?
> - Did you try adding a subject index term?
>
{: .challenge}


## Enable browsing between items
### Loci (or locuses?)
A locus marks information of interest on a particular page. In MDC, this links directly to the correct image (demonstrate)

- Illustrations
- Annotations
- Physical evidence

MDC enables a live link between the description and the relevant image


> ## Activity: How do you mark up a locus?
> 
> - Navigate to MDC www.digitalcollections.manchester.ac.uk
> - Find Latin MS 8 (Beatus) in the Latin Manuscripts Collection
> - Download the metadata from MDC and take a look at the `<decoDesc>` section
>
> ```xml
> <decoDesc><decoNote type="illustration">
> 	<note>For a detailed discussion ... 
> 			see <ref target="http://www.worldcat.org/oclc/470899747">Peter K. Klein, Beato de Liebana… 2002).</ref>
> 	</note>
> 	<list>
> 		<item>Folio <locus from="1r" to="1r">1r</locus>: Porticus. 
> 			Uncoloured ground at the top, and from the upper border depend blank medallions...</item>
> 		<item>Folio <locus from="1v" to="1v">1v</locus>: Cross supported by the lamb. The ground is blue...</item>
> 	</list>
> </decoNote></decoDesc>
> ```
>
{: .challenge}

> ## How do you link a locus in Manchester Digital Collections?
> 
> In between `<teiHeader>` and `<text>` is the `<facsimile>` section. 
>
> This describes the object in terms of at least one `<surface>` element.
>
>  - `<surface>` contains the attribute `xml:id` and the attribute `n`.
>  - `n` enables `<locus>` to link to the correct image.
>  - `xml:id` enables linking between the image and transcription `<text>`.
> 
> ```xml
> <facsimile><surface xml:id="i9" n="1r">
> <graphic>…</graphic></surface></facsimile>
> 
> <text><div><pb n=“1r” xml:id="pb-1r" facs="#i9"/></text>
> ```
>
> Within `<surface>` the element `<graphic>` contains attributes for image metadata.
> 
> ```xml
> <surface xml:id="i1" n="Front_cover">
> 	<graphic n="JRL1316304" decls="#downloadImageRights #download" rend="portrait" 
> 	 height="5500px“ width="3797px" 
> 	 url="MS-LATIN-00008-000-00001.jp2"/>
> </surface>
> ```
> > ## Solution
> >
> > Show facsimile on MS 8. The `<facsimile>` section brings together information about the digital and physical objects in the TEI file. 
> > This programming enables the system/reader to link different pieces of information together in one relatively straightforward phrase.
> > 
{: .challenge}

## Authorities and index terms

.... MORE TO COME, FIXME

### Best practice: identifying and encoding

> ## Challenges: interoperability
> 
> ...
{: .challenge}





{% include links.md %}
