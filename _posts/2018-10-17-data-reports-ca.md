---
layout: post
title: Digitized Newspapers from the National Digital Newspaper Program, USA
tags: [dh, DiD, data reports]
author: rccordell
---

[Chronicling America](https://chroniclingamerica.loc.gov/) provides an aggregated, public portal to historical newspapers from the United States, collected under the [National Digital Newspaper Program](http://www.loc.gov/ndnp/), a collaboration between the National Endowment for the Humanities and the Library of Congress. Newspapers have been digitized from the years 1789-1963, though the bulk of the collection comes from the nineteenth century—indeed, especially from around 1850 on—to around 1922, the date commonly considered the US copyright boundary. Indeed, of the 2,576 titles available in Chronicling America as of April 2018, only 8 titles include issues from the decades 1780-1790, and only 24 titles reach into the decades 1930-1960.

Newspaper Overview as of April 2018:

+ 2,576 distinct historical newspaper titles (which can, however, include multiple title changes in a largely stable paper as separate titles)
+ 13,286,065 historical newspaper pages
+ Page images are provided in PDF and JPG2 through the web interface. Additionally, archive-quality TIFF facsimiles can be requested from the Library of Congress
+ OCR-derived, page-level text data is provided in both TXT and XML formats
+ Titles available at <http://chroniclingamerica.loc.gov/newspapers.txt>

## Data quality

The images digitized through the NDNP and made available through Chronicling America (see “Collection History” below) are the highest-quality images that could be made given the technical restrictions at the time of digitization and the quality of the original microfilm scanned. The highest-resolution images are the archive-quality TIFF files, which are large and must be requested directly from the Library of Congress. The PDF and JPG files served through the project’s web interface are derivatives from the TIFF files.

The OCR data varies widely by state awardee, date of digitization, quality of source pages (or the source microfilm of those pages), and title. In some cases, however, OCR quality varies widely even within a given title, possibly due to changes in the source newspapers, which themselves changed rapidly over the course of the nineteenth century, and possibly due to other factors such as the quality of the original preserved materials. The quality of the OCR data is so variable, in fact, that it is nearly impossible to summarize here.

## Data Availability & Legal Restrictions Concerning the Data

Chronicling America’s data and metadata can be accessed through [the site’s API](https://chroniclingamerica.loc.gov/about/api/). The Library of Congress also provides [access to bulk data](https://chroniclingamerica.loc.gov/about/api/#bulk-data), which can be retrieved through web crawling tools. Chronicling America includes Atom and JSON feeds to assist in retrieving bulk data.

## Metadata Structure

Chronicling America's data uses a variant of  METS/ALTO . Files are held within subdirectories with the following format: 

	https://chroniclingamerica.loc.gov/data/batches/[Batch Name]/data/[Library of Congress Title ID/[Processing ID]/[YYYMMDDEE]/[File ID].xml
	
Which can be seen in the examples:

	https://chroniclingamerica.loc.gov/data/batches/batch_me_allagash_ver02/data/sn83009571/00279523891/1860022401/1860022401.xml [METS]
	https://chroniclingamerica.loc.gov/data/batches/batch_me_allagash_ver02/data/sn83009571/00279523891/1860022401/0035.xml [ALTO]

The METS/ALTO format stores issue metadata separately from page content data. 

The **METS** file, contains the following basic data, with some variants depending on the issue:
 
+ The container element containing information about the METS file and the software used to create the OCR text
	+ A header, containing information on the creator of the file
	+ Descriptive metadata for the issue, including
		+ The title ID, the volume number, the issue number the edition number, corresponding to the YYYYDDMMEE of the directory structure
		+ The date of the issue
		+ Additional notes of the issue's status
	+ Descriptive metadata for each page, including
		+ The page number
		+ The type of physical item being digitized
		+ The reel and sequence numbers, if microfilm, and its physical location
		+ The institution responsible for the reproduction / digitisation of the item
	+ A listing of the files included in the digitized issue and their provenance
	+ A structural map of the files included in the digitized issue
	
 
The **ALTO** file contains the following basic data:
 
+ The container element containing information about the ALTO file and the software used to create the OCR text
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
	+ The information for the printed area of the page, including the same attributes as above.
		+ A container for the content for a single text block on the page, including the same attributes as above.
			+ A container for a single line of text within the text block, including the same attributes as above.
				+ A container for a single word within the text line, including the same attributes as above as well as information on OCR confidence and the text itself.
				+ Containers for any whitespace characters, detailing the height and width of those spaces between words. 

The Library of Congress Title ID corresponds directly to its record in the standard library catalogue, providing additional bibliographic information. It can be accessed with the base url `https://www.loc.gov/item/` followed by the title ID. 

Combined, the *Chronicling America* database and Library of Congress Catalogue provides direct data on the content, layout, and origin of the digitized newspaper as well as providing a detailed map of the file structure containing the OCR and image data. This allows for the material to be recombined in different ways to suit different needs.

## Collection History

Chronicling America is a portal that provides access to newspapers digitized under the [National Digital Newspaper Program](http://www.loc.gov/ndnp/) or NDNP, which is in turn an outgrowth of the United States Newspaper Program. The USNP worked from 1982-2011 to identify, describe, and preserve historical newspaper collections, often through microfilming. The NDNP builds on this work and is, in essence, a grant program through which groups can apply for funding to select and digitize “approximately 100,000” newspaper pages representing that state. These papers are mostly scanned from the microfilm editions created under the USNP, which can be scanned more quickly than paper copies. In each NDNP grant, the applicants develop a plan for digitization that determines what a representative group of newspapers might comprise for their state. In some cases states strive for geographic spread (i.e. a selection of newspapers drawn from different geographic parts of the state) and in other cases states focus on digitizing papers that reflect aspects of population such as race, ethnicity, or language. To date, not all states have participated in the NDNP, so there are notable geographic gaps in coverage state-by-state across the US. Other states have received 2 or 3 rounds of funding through the NDNP and thus have significantly more than 100,000 total pages from their states digitized. Until July 2016, the NDNP helped states digitize newspapers published between 1836-1922, but [they now allow digitization of papers between 1690-1963](https://www.neh.gov/news/expanding-our-current-scope-ndnp).


## <a name="sources"></a>Sources

Ryan Cordell, ““‘Q i-jtb the Raven’: Taking Dirty OCR Seriously,” *Book History* 20 (2017), [available online](http://ryancordell.org/research/qijtb-the-raven/).

“About Chronicling America,” <https://chroniclingamerica.loc.gov/about/>

“National Digital Newspaper Program,” <http://www.loc.gov/ndnp/>
