<h1>Summary Information:</h1> 

Cope-Evans Correspondence, 1820-1920

Anna Smith, Haverford College Anne T. and J. Morris Evans Post-Baccalaureate Fellow

Developed as part of the Cope Evans Project

Adapted from the 2019 version of the project created by Aleena Maryam ‘21

Updated January 2024

CSV

English

<h1>Data Overview</h1>
The Cope-Evans Correspondence, 1820-1920, data set showcases 100 years of correspondence of the Cope-Evans family, as represented in the Cope-Evans Family papers. The primary purpose of this data set and its accompanying visualizations is to demonstrate the epistolary network of the family, particularly as it relates to the family’s movements and relationships across time and changing political, economic, technological, and religious landscapes. The data is represented in a CSV file.

<h1>Dataset Creation Abstract</h1>
The data set was created through the manual cleaning, update, and enhancement of the metadata associated with the digitized correspondence of two collections in the Haverford College Quaker & Special Collections, the Cope-Evans Family papers (HC.MC.1170 and HC.MC.1242), hosted on the [TriCollege Libraries Digital Collections](https://digitalcollections.tricolib.brynmawr.edu/collections/cope-evans-family-papers) site. In addition to the metadata fields available on the site, origin and destination fields were added through the comparison of the individual letter with Library of Congress geographic headings, except in the cases of Awbury (Philadelphia, Pa.) and Woodbourne (Susquehanna County, Pa.) due to their specific significance to the Cope-Evans family. When additional information, such as a street address, was provided, the information was entered into a “Precise” origin or destination column. 

<h1>Data Set Creation</h1>
This data set relies on the digitized correspondence and associated metadata from two collections in the Haverford College Quaker & Special Collections, the Cope-Evans Family papers (HC.MC.1170 and HC.MC.1242), hosted on the Islandora-based [TriCollege Libraries Digital Collections](https://digitalcollections.tricolib.brynmawr.edu/collections/cope-evans-family-papers) site. TriCollege Libraries Digital Collections uses the Drupal-based Islandora 2.0 and requires administrative privileges for metadata creation and editing. While a CSV can be freely downloaded from any of the collection pages using a Collection Search Data Export, administrative privileges are required to add exported values beyond Title, Description, Date Created, Member of ≫ Content ≫ Title (indexed field), Identifier, and Local Identifier.
<br>
The preliminary data set was assembled by combining three separate CSV files. Following [instructions from Mark Jordan](https://mjordan.github.io/islandora_workbench_docs/generating_csv_files/), a REST view was created to identify published parent objects in the Cope-Evans Family papers collection. A CSV file was then created using a Workbench get_data_from_view task containing all metadata fields for each of the 5109 objects along with the node ID necessary to update the metadata through a Workbench task. However, this method did not allow for the export of item URLs, necessitating a Collection Search Data Export with Local Identifier and Item URL fields. The third CSV was first created in 2019 as part of the second iteration of the project and contains the Origin and Destination fields that were no longer distinguishable from geographic subjects due to Haverford’s migration from its previous CONTENTdm-based digital collections site, Triptych, to the Islandora-based TriCollege Libraries Digital Collections. 

These three CSVs were then imported into OpenRefine, with the REST-based CSV serving as the primary sheet. Cell crossing was performed using the Local Identifier column as the key value in order to add Item URLs and Origin and Destination data from the other two sheets The Local Identifier was chosen as the key rather than the persistent identifier (PID) as only migrated records had been assigned PIDs at that time. The Genre column was then faceted to include only “letters (correspondence)” and “business letters.” The Linked Agent column, which relies on MARC relator codes, was separated into Author and Recipient columns based on their respective “aut” and “rcp” codes. 

This process established a data set consisting of 4000 letters dated between 1732 and 2009 that would serve the needs of the visualization. However, numerous errors were known to exist, as the metadata had been created over a period of over 20 years, across three digital collections platforms, and by approximately a dozen different people operating with different cataloging and metadata procedures. In an effort to minimize these errors, each digital surrogate was hand-checked against its metadata. 

When errors were found, usually related to mistyped dates or misidentified authors or recipients, the metadata was corrected in the working spreadsheet and the edited metadata and node ID was added to a separate spreadsheet to be run as part of a Workbench replace task. A total of 190 records were updated using this method. A total of 17 duplicate digital surrogates were identified; each pair was evaluated and the record with less-accurate metadata was unpublished. Additionally, several records were found to be transcriptions of letters that were also in the collection or to not fit their assigned genre. These records were marked from exclusion from the final data set, but not edited for the digital collections site. 

Origin and destination data was also found to be missing for many of the records, likely because their metadata was created after the move away from Triptych. This data was gleaned from the letter’s header, envelope, or back. In an effort to maintain consistency, Library of Congress geographic headings were chosen as the source schema, except in the cases of Awbury (Philadelphia, Pa.) and Woodbourne (Susquehanna County, Pa.) due to their specific significance to the Cope-Evans family. When additional information, such as a street address, was provided, the information was entered into a “Precise” origin or destination column. Though not used in any of the visualizations, it was determined that the information could be useful for future explorations such as the family’s movements across Philadelphia. 
Uncertain or assumed location information–determined either through the content of the letter or knowledge of the author or recipient’s whereabouts during a specific period–was added in brackets. In some cases, the name by which the author knew a certain location has since changed, as in the case of Mauch Chunk, Pennsylvania, now Jim Thorpe. The previous name was added in the relevant “Precise” origin or destination column, while the current name used in Library of Congress subject headings was added in the standard origin or destination column. 

In order to transform the Library of Congress geographic headings into mappable data, each term was manually compared against the GeoNames database, where the latitude and longitude was then copied into the spreadsheet. When a suitable match could not be found in GeoNames, the Mapbox Geocoding API was used to find the coordinates. Finally, the data was faceted to include only letters dated between 1820 and 1920. 
Despite these efforts, numerous errors are still assumed to exist. Backs of letters containing address information and envelopes were frequently not scanned, resulting in a loss of some location information, particularly related to destination. Some location names were indecipherable or unable to be confidently associated with a specific place. The shelf locator for many of the records refers to the incorrect box, and some letters in the collections either were not scanned or were lost in migration processes. Errors may still remain in other columns. 
 
<h1>Data Structure</h1>
The final data set consists of 3064 letters between 1820 and 1920. All fields except Precise Origin, Origin, Precise Destination, Destination, Author, and Recipient are derived from the metadata schema developed by the TriColleges. Multiple entries within a cell are delimited by a pipe (|).  

Title	

Description

Date Created	

Genre	

Precise Origin	

Origin

Precise Destination	

Destination

Geographic Subject

Author	

Recipient	

PID \[Persistent Identifier]	

Subjects (Name)	

Subjects (Topic)	

Shelf Locator	

Local Identifier	

Note

Item URL

Where any information was unavailable, the field was simply left blank.

<h1>Ethical Considerations</h1> 
The project team decided to limit the data set to 1820-1920 not only to limit the scope of the project but also to avoid issues of privacy and public domain, as still-living authors wrote other letters in the collections. The use of Library of Congress geographic headings rather than full addresses also minimizes the use of identifying information.
Geography is always political. Even those place names and geographic boundaries that are internationally recognized often reflect violent histories of colonization. For example, the majority of the letters in the data set have either origins or destinations in Philadelphia, which lies in an area also known as Lenapehoking, the traditional homelands of the Lenape. One letter in the data set (hsc0028) was written off the coast of what was, to the author, Palestine but since 1948 has been known as Israel. Other places within the United States have changed administrative boundaries. 
Though imperfect, the Library of Congress geographic headings were chosen as the taxonomy schema for origin and destination fields as they most commonly matched the names the authors themselves used. In cases where the creator-supplied name did not match the name in the Library of Congress taxonomy, the former was placed in the relevant “precise” column while the latter was placed in the Origin or Destination column. The project team felt that it was important to retain the original historic and geographic contexts of the letters in the data set while also acknowledging the names currently recognized by the Library of Congress as an accessibility measure.   

<h1>Bibliography</h1> 
Cope-Evans Family papers, HC.MC.1130 and HC. MC.1242. Quaker & Special Collections, Haverford College, Haverford, Pennsylvania. TriCollege Libraries Digital Collections, accessed 29 January 2024, https://digitalcollections.tricolib.brynmawr.edu/collections/
cope-evans-family-papers. 
