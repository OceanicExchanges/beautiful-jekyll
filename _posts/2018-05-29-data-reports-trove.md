---
layout: post
title: Trove, National Library of Australia
tags: [dh, DiD, data reports]
author: mhbeals
---
### History of the Collection

[Trove](https://trove.nla.gov.au/), originally known as the Single Business Discovery Service, was launched in August 2008 in order to create a single point of entry for online discovery services developed by the National Library of Australia between 1997 and 2008-2009, including Register of Australian Archives and Manuscripts, Picture Australia, Libraries Australia, Music Australia, Australia Dancing, PANDORA search service, ARROW Discovery Service and the Australian Newspapers Beta service. The digital newspaper collection, an extension of the Australian Newspaper Plan (ANPlan), was curated for digitisation from exisiting microfilm copies by the various state libraries of Australia with the aim of a providing a sample of historical newspapers evenly distributed across the various regions of the country.

The "Australian Newspapers Beta" service was launched in July 2008 as a standalone website and a year later became a fully integrated part of Trove. Since August 2008 the system has incorporated crowdsourced text-correction as a major feature, allowing the public to change the searchable text s well as more recent options for crowd-sourced tagging of materials. These features have allowed a high degree of community engagement and enrichment of the collection.

### Data Quantity

[Trove Digitised Newspapers](https://trove.nla.gov.au/newspaper/) provides access to over 20 million pages from over 1000 Australian newspapers from each state and territory and from the earliest published newspaper in 1803 to the mid-20th century, including some community language newspapers. 

The newspaper issues included in the collection, expanded daily, are selected under the National Library of Australia’s [Australian Newspaper Digitisation Program (ANDP)](http://www.nla.gov.au/australian-newspaper-plan) by the National, State and Territory libraries. The collection also includes newspapers selected identified and funded by individuals and institutions through a [contributor model](http://www.nla.gov.au/content/contributor-guidelines). Newspapers are selected based on use, historical significance, geographical and regional coverage and microfilm status. It is the ultimate aim of the ANDP to make freely available all Australian newspapers published prior to 1955, beginning with microfilmed issues and moving onto hardcopy material as time and funding allow.

A [list of newspaper titles already digitised](http://trove.nla.gov.au/ndp/del/titles) is available on Trove, as well as a [list of newspaper titles selected for digitisation for the current year](http://www.nla.gov.au/content/new-titles-coming).


### Data Quality

The majority of Trove newspapers were scanned from 35mm Master negative Silver gelatin microfilm reels or second-generation Silver gelatin microfilm reels into a pair of digital images, consisting of a 400 dpi Raw Greyscale TIFF and an Image Optimised Bi-tonal TIFF.  The digital images are converted into full-text searchable files through the use of Optical Character Recognition (OCR) with content analysis undertaken by human operators, who identified separate articles (zones) and created metadata for them. 

Apex Publishing LLC was responsible for OCR and content analysis in the initial phase while a panel of OCR and content analysis providers was established to cater for the expanding program. OCR contractors process page-level image files provided by National Library of Australia to create an XML file for each page, conforming to the ALTO schema, and an xml file for each issue, conforming to the METS schema. The latter contains most of the human supplied metadata for the issue. 

The overall OCR quality of the Trove Newspapers collection varies owing first to variations in the source materials and second to the non-systematic inclusion of contractor and end-user corrections. During the initial processing, titles, sub-titles, authors and the first four lines of each zoned article are re-keyed, resulting in 99% percent accuracy for these components.  Moreover, as of March 2014, over 120 million column-lines of the OCR text had been manually corrected by Trove users, though this represents only a small percentage of the overall collection. These latter changes are recorded, allowing users to retrieve the original OCR text as well as all subsequent corrections to it. Thus, any given article within Trove may have had a small or significant manual correction to the original OCR transcription, which itself varies considerably depending the condition and typography of the original item. As these corrections are updated daily, the OCR quality of the collection should be specifically tested for any sub-corpus used.

Most of the newspapers are in English but there are also some periodicals in Chinese, Estonian, French, German, and Italian, leading to a greater variance in OCR quality.

### Data Availability & Legal Restrictions Concerning the Data

The contents of the Trove digital archive, including digitised newspapers, up to 1954 are available as public domain images and machine-readable texts. Images, fully cited using the National Library of Australia stable article identifier, may be obtained from the Trove graphical user interface and reused without other restrictions.

Machin- readable texts, created from optical character recognition, are available to users either through the graphical user interface or through the Trove API, without special agreement or additional copyright conditions. A full technical description of the API is available at [http://help.nla.gov.au/trove/building-with-trove/api-technical-guide](http://help.nla.gov.au/trove/building-with-trove/api-technical-guide)

### Metadata Structure

The metadata for each newspaper page held by Trove is stored in standard ALTO format. However, as the data is largely retrieved by users via the API, the fields returned vary depending on the construction of the user's query. Below is the full metadata available for a given page, as described by Bronwyn Lee in "Use of METS and ALTO in the Australian Newspapers Digitisation Program (ANDP) at the National Library of Australia (NLA)"

+ The container element containing information about the ALTO file and the software used to create the OCR text.
  + The unit of measurement used in the ALTO file, expressed as contains the unit of measurement used in the ALTO file, expressed as “pixel”
  + The container element for the image used as the source for OCR text
    + The path and filename of the source image file
  + The container element for the software information used to create the OCRtext
    + The container element for each OCR processing step
	  + The date and time on which the OCR was processed
      + The name of the agency which performed the OCR processing
	  + The OCR processing software information
	    + The name of the creator of the OCR software, i.e. “Abbyy”
		+ The name of the OCR software, i.e. “FineReader”
		+ The software version number, i.e. “8.0”
      + Container element for post-processing steps
	    + Processing date and time
		+ Processing agency
		+ A description of the processing step performed
+ Container element for style information in the OCR file.
  + A unique ID for each text style used in the OCR file and the “fontsize” attribute contains the size of the font of the text style; there may be multiple entries.
  + A unique ID for each paragraph style used in the OCR file. The “align” attribute contains the alignment value for the paragraph style, i.e. “Left”
+ The content information in the OCR file.
  + Identification of the page area of the page in the OCR file. The “id” attribute contains a unique ID for the page and the “height” and “width” attribute contains the height and width measurements of the full page.
    + The information for the top margin of the page including the unique ID for the margin element, the horizontal position upper/left corner, the vertical position upper/left corner, the width and the height
	+ The information for the left margin of the page, including the same attributes as above.
	+ The information for the right margin of the page, including the same attributes as above.
	+ The information for the bottom margin of the page, including the same attributes as above.
    + Defines the boundaries of the OCR text on the page, including the unique ID for print space,  the confidence level of the OCR, a value between 0 and 1, the horizontal position upper/left corner, the vertical position upper/left corner, the width and the height.
	  + The top-level instance of the element <Composed Block> is used to contain the content for a single article on the page. Subordinate instances of this element within the article-level <ComposedBlock> represent each article zone within the page. Each zone-level <ComposedBlock> element will contain nested <TextBlock> to contain paragraph text. Additionally, a single <ComposedBlock> will be used to contain nested <ComposedBlock> for illustrations and associated caption text. The illustration and the caption text will be contained within separate zone-level <ComposedBlock> elements within a single parent <ComposedBlock>. This element has the following attributes: 
	    + ID: Unique ID for the element
		+ “ART#” for article-level blocks
		+ “ZONE#-#” for article-zone level blocks
		+ ”ILLBLOCK#” for blocks containing illustration and associated caption text. 
		+ ROTATION: Degree of rotation expressed in CCW°
		+ HPOS: Horizontal position upper/left corner
		+ VPOS: Vertical position upper/left corner
		+ WIDTH: Width
		+ HEIGHT: Height
	  + The paragraph-level text content or the text of a caption, associated within an illustration. This element has the following attributes and child elements:
	    + ID: Unique ID for the element
		+ STYLEREFS: Reference to paragraph style ID
		+ HPOS: Horizontal position upper/left corner
		+ VPOS: Vertical position upper/left corner
		+ WIDTH: Width
		+ HEIGHT: Height
	    + The information for a zone consisting of only an illustration. When associated within a caption, the <Illustration> is contained within a single <ComposedBlock> and the associated captions are contained with a separate <ComposedBlock>. Both of these, in turn, are contained within a single <ComposedBlock>. This element has the following attributes:
	      + ID: Unique ID for the element
	  	  + TYPE: One of the valid illustration types
		  + HPOS: Horizontal position upper/left corner
		  + VPOS: Vertical position upper/left corner
		  + WIDTH: Width
		  + HEIGHT: Height
	    +  A single line of text within the paragraph. This element has the following attributes and child elements:
          + ID: Unique ID for the element
		  + STYLEREFS: Reference to paragraph style ID
		  + HPOS: Horizontal position upper/left corner
		  + VPOS: Vertical position upper/left corner
		  + WIDTH: Width
		  + HEIGHT: Height
		  + A single string within a line of text. This element has the following attributes:
		    + ID: Unique ID for the element
			+ CONTENT: The character content of the string
			+ WC The word confidence level
			+ CC The character confidence level
			+ HPOS: Horizontal position upper/left corner
			+ VPOS: Vertical position upper/left corner
			+ WIDTH: Width
      + HEIGHT: Height
