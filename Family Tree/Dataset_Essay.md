# Summary Information: 
* Selected Cope Family Tree

* Anna Smith, Haverford College Anne T. and J. Morris Evans Post-Baccalaureate Fellow

* Developed as part of the Cope Evans Project

* Adapted from the 2014 version of the project created by Cormac Quinn Rada ('17), Brandon Smith ('16), and Andrew Kafker ('17)

* Updated January 2024

* CSV, GEDCOM

* English

# Data Overview
The Selected Cope Family Tree showcases the ancestors and descendants of Thomas Pym Cope (1768-1854) and Gilbert Cope (1840-1928), beginning with the first emigrant to the now United States, Oliver Cope (-1697). The primary purpose of this family tree is to assist in deciphering the relationships evident in the Cope Evans Family papers (HC.MC.1170 and HC.MC.1242) and to differentiate between people of the same name. As such, this tree is not fully inclusive but rather is centered around those people represented in the collections, especially in the nineteenth century. The data represents 248 people, 72 marriages, and 177 parent/child relationships, and spans from the late seventeenth century to the late twentieth century. The data is represented in three linked CSV files: people, marriages, and families, along with a GEDCOM file to allow import into genealogical programs. 

# Dataset Creation
This tree is an adaptation of that developed by Cormac Quinn Rada, Brandon Smith, and Andrew Kafker as part of the original Cope Evans Project in 2014. However, as the source of the data was unclear, there were numerous known errors, and the 2023 project team did not have access to the data set, it was necessary to recreate the data set using the family tree visualization as a guide for the individuals to include. Data was hand-transcribed from the most recent published genealogical text on the Cope family, [*Cope, Emlen, Evans, Stokes Families: 1682-2002*](https://tripod.haverford.edu/permalink/01TRI_INST/14s7maf/alma991017277569704921), compiled and edited by Elizabeth Emlen, Walter Cope Evans, Kate Flynn, Eliza Cope Harrison, and Will Lewis (Baltimore: Gateway Press, 2005), into the [Gramps](https://gramps-project.org/blog/) genealogical research software over the course of about a week and subsequently edited by hand for typographical errors and complex relationships such as stepparent/stepchild. Though additional genealogical links and discoveries may have been made since the 2005 publication due to the prevalence of genealogy companies such as Ancestry.com that may enhance or contradict the information presented, it is often difficult to verify those claims, and they have been excluded in the name of consistency. 

The primary focus of the tree is the members of the Cope family present in the Cope Evans Family papers. Thomas Pym Cope is the father of Henry Cope, who established the Awbury residence in Germantown, Philadelphia, where many of the letters presented in the map visualization were addressed. Some names were not included in the source text but were present in the Rada et al. tree and the archival collections –primarily the ancestors and descendants of Gilbert Cope (1840-1928). Their information was verified through Gilbert Cope’s A Record of the Cope Family: As Established in America, by Oliver Cope, Who Came from England to Pennsylvania, about 1682, With the Residences, Dates of Births, Deaths and Marriages of his Descendants as Far as Ascertained (Philadelphia: King & Baird, 1861) and the Records of Births, Deaths, Etc., 1724-1935, from Birmingham Monthly Meeting, Chester, Pennsylvania.

When a child of a parent is listed due to their presence in the Cope Evans Family papers, all children of that parent will also be listed, even if they are not represented in the collections. However, not all parents will have children listed, even if they are known to have existed, as the exponential growth of people unrelated to the collections would result in an unwieldy data set and visualization. Additionally, while we recognize the fluid nature of gender, it is used here as a binary variable and determined by familial relationship, pronouns in the 2005 text, and usual gender of the given name, except in the case of the ethical considerations noted below. 

# Data Structure
The data is contained within three linked spreadsheets: People, Marriages, and Families, with a total of 247 unique individuals. Each person is assigned a person Gramps ID (I0000). The fields are as follows:

* Person: person Gramps ID, assigned sequentially in order of entry

* Surname: Last name

* Given: First and, if applicable, Middle name or Initial. If unknown, use the value “???.” If restricted, use the value “xxx.” 

* Suffix: Jr., II, etc., as represented in the 2005 text 

* Gender: Male, Female, Unknown

* Birth date: Date of birth (exact, between, about)

* Death date: Date of death (exact, between, about)

Subsequently, individuals are linked into a marriage event and assigned a family Gramps ID (F0000). The fields are as follows:

* Marriage: Gramps family ID, assigned in order of entry

* Husband: Gramps person ID

* Wife: Gramps person ID

* Date: Date of marriage (exact, between, about)

That family unit is then assigned children, linking the family Gramps ID to individual person Gramps IDs. The fields are as follows:
Family: Gramps family ID

* Child: Gramps person ID

* Where any information was unavailable, the field was simply left blank.

# Ethical Considerations 
Many of those included in this data set are still living, and while much of the information is available elsewhere both online and in print, it nonetheless constitutes personally identifying information. The project team decided that people born after 1990 likely did not personally consent to their information being published in the 2005 source text, while other members of the family likely did as it was begun at a family reunion. As such, people who were minors in 2005 have had their given names, birth dates, and genders restricted. 

# Bibliography 
Cope, Gilbert. A Record of the Cope Family: As Established in America, by Oliver Cope, Who Came from England to Pennsylvania, about 1682, With the Residences, Dates of Births, Deaths and Marriages of his Descendants as Far as Ascertained. Philadelphia: King & Baird, 1861.

Emlen, Elizabeth, et al., ed. Cope, Emlen, Evans, Stokes Families: 1682-2002. Baltimore: Gateway Press, 2005.

Records of Births, Deaths, Etc., 1724-1935. Birmingham Monthly Meeting, Chester, Pennsylvania. U.S. Quaker Meeting Records, 1681-1935, Ancestry.com. 


