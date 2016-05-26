#How To Open Your Data: A Primer
##If you love your data, set it free.

**The aim of open data is to maximize the potential of your data, to help it find new users and new uses.** 

Your data may hold the answers to unexpected questions and enable other researchers to further knowledge in surprising ways (for more about this, see our “Why Open Data” Primer). To encourage reuse, you’ll need to save your data files and put them where lots of people can access them freely-- ideally on the world wide web. But before you rush off to do just that, you’ll need to take steps to prepare your data for its new life in the open. **In this second primer we’ll explore how you can make your data findable, accessible, comprehensible, and easily usable by others, before you share it widely.** 

As you read through this primer, keep two things in mind: 1) your own dataset, which you probably have spent time carefully and lovingly collecting, curating, and analyzing, and 2) an imaginary stranger, somewhere out there on the internet, who knows absolutely nothing about your dataset, but might have an exciting, novel use for it. **The process of opening your data is the process of bringing #1 and #2 together-- introducing your dataset to a complete stranger. Let’s get started!**

##A Data Blind Date
To introduce our dataset to a complete stranger who might want  to reuse it, we’ll need some really great metadata. Metadata is information about information. What does that mean? Let’s look at an example-- let’s meet some strange data on the internet, and try to get to know it better:

*insert image1*

This is a number, a value, and it certainly looks like a data point. It could be the most important value in a data set, the value that proves a groundbreaking theory... or the one that sinks it. But it’s obviously meaningless if we don’t know what it measures.  Here’s this data point, with a bit of context:

*insert image2*

From this expanded dataset we can begin to make out a story.  The first column seems to be date and time, so this is probably part of a time series.  In the last field, each entry is tagged as an “earthquake,” and there are locations listed, too-- we might guess that we’re looking at seismic data. It seems that our highlighted value is linked to an earthquake West of Anchor Point, Alaska, but we still don’t know what that “3.2”  value actually represents. **A researcher intimately acquainted with this dataset and collection methods might have no trouble reading and understanding it. But if we imagine that we’re newcomers to data and that this is all the information we have, the data set is unusable because we just don’t know enough about it.** What happens if we have access to a bit more information?

*insert image3*

Finally, labels for every column! These labels are metadata, or information that describes data. This is much better-- at last we see the highlighted value is labeled “mag,” since we’re talking earthquakes, perhaps that’s an abbreviation for magnitude. Some of the other labels are familiar: latitude and longitude, depth and place. We can infer that his data shows seismic events logged in early May of 2016. And yet, mysteries remain. For example, what is the unit of measure for depth? And what do “nst,” “dmin,” and “rms” stand for? What scale is used for “mag”? What is “mag type"? **Even if we had more familiarity with the terminology, we still don’t know the origins of the data, who collected it, and why and how.  Even with labels, we don’t have the whole picture.** 

##Metadata, A Love Note to the Future
**Our future users-- and even our future selves, who may eventually forget some of the finer details of even our own datasets months or years on-- need well-described, thoroughly documented data sets to ensure proper, responsible use and reuse.**  In the example above, we saw how baffling a dataset can be when we don’t have access to good metadata about it. The example data set we looked at was (...big reveal…) sourced from the United States Geographical Survey (USGS), which makes earthquake data available on its website, as downloadable CSV or comma separated values files, or even as live streams. The downloaded file we saw above was the result of a query to the USGS database for earthquakes detected within a certain time frame-- 24 hours in early May of 2016. 

Luckily for us, the USGS has carefully documented their data sets on their web site, and provides a terrific reference [guide to the CSV spreadsheet format](http://earthquake.usgs.gov/earthquakes/feed/v1.0/csv.php), including a glossary of terms to explain the metadata! Here are example definitions from that glossary:

*insert images 4-6*
 
The magnitude-- the data type of that initial highlighted value-- links to yet more information.

*insert image 7*

Anyone using this data will benefit from detailed documentation. **Even the researcher who collected this data years back will need this information, if collection methods, instrumentation, or scales have changed in the intervening time period.**  Note that some disciplines have rules for metadata called metadata schemas.  Check with someone in your department or at your library to determine if there is a standard metadata schema you should be using for your data.

Now we’ve got our metadata and good information about each data product,  yet there’s one more thing, something that could easily be missed if we downloaded this file and then shared it with others without any other descriptors.  If you look closely, you’ll see that none of the earthquakes in this data set (pictured here in its full glory) register less than a magnitude 2.5. USGS allows researchers to query a large database, and it’s request certain subsets of data that are pertinent to a particular question or study. When this CSV file was created, someone helpfully named it “USGSquery>2.5,” to indicate that these earthquakes that registered 2.5 magnitude or greater. But this information is not documented elsewhere in the actual file. **A newcomer who’s not clued in to this notation could very easily, mistakenly assume that this is the full set of data for all earthquakes, when it’s only a curated subset.**

*insert image 8*

**Our example data set highlights the need for external documentation that goes with your dataset wherever it goes.** We need to create supplementary data files that tell the full story of the data set-- what the data is about, who collected it, where it was collected, when, and how. This is your “love note to the future”-- your way of preparing your data with those future users (or your future self) in mind, so they can reuse it effectively and responsibly. 
##Creating a DATA_README
In the world of computer programing and the world wide web, a file that comes with a piece of software or code and contains critical information about its origins and how to use it is called a README file. The README’s all-caps title emphasizes how urgent it is that you read it carefully before you use the code or software. We can borrow this documentation convention when sharing our data, and bundle a README file with our data to ensure that new users have all the information they need to responsibly and effectively use the data.  README files (usually text files) are stored with the rest of your data files, frequently in a top-level folder so they can be easily found.  (For more information on different types of data documentation files, see the Additional Resources section at the end of this primer.)

We can think of our DATA_README file as a data reuse plan. Let’s look at creating a DATA_README for our USGS earthquake data, answering five key questions that new users of your data must know: what, who, when, where, and how. Our document will have five sections: data summary (what), source and contact details (who), location and access information (where), dates of collection and coverage (when), and collection methods (how). 

###1.Data Summary###
This first section of the DATA_README file tells users **what** the data is about. A good description is especially important when we’re sharing our data on the web., as sSome data repositories are indexed by search engines, such as Google, making it easier for new users to quickly find your data through a simple online search.  Include the following:

* A descriptive title, to help users know immediately if this data set is likely towill be useful to them.
* A brief yet detailed summary including origins, scope, limitations, and types of data included in the set.
* A list of previous publications, if any, resulting from this dataset, to provide context on research use.

#####*Example:*#####
**Title:**  USGS M2.5+ Earthquakes 2016-05-02  
**Description:** This is earthquake data collected by the United States Geological Survey in a 24-hour
period on May 2, 2016. This is a subset of that time period’s data, containing only earthquakes of 2.5
magnitude or greater.  Includes the date/time of the earthquake along with the following products:
latitude, longitude, depth, magnitude, magnitude Type, nst, gap, dmin, rms, net, id,updated, place, type,
horizontalError, depthError, magError, magNst, status, locationSource, magSource. See “Data
Collection Methods & Processing” (below) for more information on these data products. 

###2. Source & Contact Details###
This section of your DATA_README file tells users **who** was involved in creating or collecting the data set and **who** can be contacted if there are any questions about the data set. This information will enable new users to credit the appropriate people and institutions when using the data.  Include the following.  

* The name and affiliation of the person(s) or organization(s) who collected the data
* Contact information for a person or group who can answer questions about the data long into the futureof the above, so questions can be directed to the appropriate person.
* The names and affiliations of any collaborators on the research. 
* The name of the organization or institution that sponsored or funded the research. 

#####*Example:*#####
**Source:** This data was compiled by the United States Geologic Survey, a United States Federal
Agency. The data was collected at research stations registered in the International Registry of
Seismograph Stations (IR),  jointly maintained by the ISC and the World Data Center for Seismology
(NEIC/USGS).  Questions about this data set can be directed to: GS_Data_Management@usgs.gov.  

###3. Location & Access Information###
This section of your DATA_README covers locations **where** the data was collected and **where** it is stored and can be accessed again. For geographically-related data, the location info helps a new user determine whether the data’s geographic coverage falls in their area of interest.  By including info on where the data can be accessed, you enable anyone who downloads the file to to find it again later, and ensure the data is cited correctly in any future publications. Be sure to include: 

* Information on where the data was collected, and specify single or multiple sites of collection. Be as specific as possible (geographic coordinates provide most specificity). 
* DOI or other persistent URL that links to a landing page for your datadocument. Check with your data repository to see if they provide this service.

#####*Example:*#####
**Location:** Data collected internationally by registered seismograph stations: http://www.isc.ac.uk/registries/.  
**Place of Publication:** Published on USGS Earthquake Hazards Program Real-Time Feeds website:  http://earthquake.usgs.gov/earthquakes/feed/v1.0/csv.php 

###4. Date of Collection & Coverage###
This section of your DATA_README deals with all the time and/or date information about your data set. In this section, use the international standard date format (YYYY-MM-DD hh:mm.ss) and try to be as specific as possible. Be sure to include: 

* **When** the data was originally collected.
* **When** the data was published or made available in the repository or database.
The time periods covered by the dataset.  

#####*Example:*#####
**Date of Collection:** Data collected on 2016-05-02.  
**Date Published:** Published by USGS Earthquake Hazards Program in a real-time feed; each datapoint made available as it was collected on 2016-05-02.  
**Dates of Coverage:** This data covers the period from 2016-05-02 00:00:00 to 2016-05-02 23:59:59.  

###5. Collection Methods###
This section of your DATA_README should answer questions about **how** the data was collected and processed. This information is critical as these methods may constrain or alter how the data can be used and interpreted. Be sure to include:
* Collection methods, addressing issues such as what instruments were used to collect the data, how frequently data were collected, how data collection sites were selected, If there was a sample population, and if so, how it was selected, etc. If you are following a standard procedure or set of  methods, provide or link to documentation of those methods.
* Data pProcessing, addressing issues such as was the data cleaned, how were missing or null values handled, was code used to processing the data and, if so, where might it be found.
* File iIndex & fFormats, specifying what files are included in the data set (as a list), and how they are organized, any naming conventions that are used, and what formats and what software is required.
* Glossary, data dictionary, or other file of metadata definitions, which may be a separate file or linked file  (see example definitions above from USGS). 

#####*Example:*#####
**Collection Methods:** For information about collection methods for this data set, refer to the ANSS Comprehensive Earthquake Catalog (ComCat): http://earthquake.usgs.gov/data/comcat/, which contains earthquake source parameters and other products produced by contributing seismic networks.  
**Data Processing:** see documentation on ComCat.  
**File Index and Format:** This is a single CSV, or comma separated value file. It can be opened with any spreadsheet software such as Open Office, Microsoft Excel, etc.  
**Glossary:** For a comprehensive glossary related to data products, see ComCat.  

If you have a great DATA_README, your dataset will truly be free for proper, responsible re-use on the internet. There’s just one last thing, which is selecting the best format for release of your data. 

##File Formats FTW! 
Though it’s not the most thrilling of topics, file formats for data sharing is very, very important. You want to select a format that is accessible to as many people as possible. Avoid proprietary formats if you can! Make sure your file is readable by computers so no human is forced to re-enter your data into another document to use it. For example, the ever-popular PDF, while it can be opened on many systems, doesn’t allow other software programs to “read” the contents and extract data for analysis and re-use. Here are a few other data “don’ts” -- formatting issues related specifically to spreadsheet data-- that will make your data difficult for any machine to read:
* Don’t include data visualizations or summaries in the same worksheet as raw data. Raw data should be kept separately for easiest processing and readability.
* Don’t include multiple tables in the same worksheet.
* Don’t put special characters or values in field names; these will make it difficult for your data to be opened/loaded cleanly by a new user.
* Data contained in formatting rather than values Don’t use formatting to add meaning to your data.  For example, using fonts or text colors to identify certain values.  Machines won’t read the formatting when running analysis and that information will be lost.


**Most numeric and textual data can be reformatted to be communicated in text-based forms, like the comma separated value (CSV) format that can be opened with any text editor. This is the best possible format to enable wide, easy, reuse.**  For other sustainable format types, refer to the File Formats guide distributed by the Australian National Data Service in the “Information” section of the Additional Resources, below.

Now that you have a DATA_README and your data is in great shape to meet any potential new user,  take a look at the  third in our series of Open Data Primers, which will help you decide *where* to share your data. In that primer, we’ll take a whirlwind tour of the world of online data repositories.

####ADDITIONAL RESOURCES####

####Glossary:####

**Data dictionary** - a text file defining field names and values (sometimes used interchangeably with the term “codebook”). Includes: a list of all field names, a description of fields & values (e.g. units of measurement, formulas used for calculation, abbreviations, value ranges) as well as the relationship of fields to one another. Example of a data dictionary: http://www.utexas.edu/cola/redcap/_files/data_dictionary_example.jpg

**Metadata schema** - are sets of rules for how to describe a certain type of information.  There are many different metadata schema primarily organized by information format and/or discipline. 

**Permanent identifier** - A permanent identifier (or PID) is a set of numbers and/or characters, frequently in the form of a URL, that points to the location of a resource. PIDs are set up in such a way that even though the storage location of the resource may change over time (e.g. moving data from one university server to another), the PID will always point to the correct location. DOI (Digital Object Identifier) is a commonly known type of PID. 

####Trainings:####
* Mozilla Science Lab Open Data Module 2: How to Open Data - *insert link*
* [Mozilla Science Lab Working Open Workshop Presentation on “Open Data and Data Reuse Plans”](https://docs.google.com/presentation/d/1kZd-ZD5lru5a7jIbyi9q8cBYCCAKRnIBSRvixYFtoF0/edit?pref=2&pli=1#slide=id.g1088c5b110_0_183)
* [Mozilla Science Lab Working Open Workshop Exercise on “Open Data and Data Reuse Plans”](http://mozillascience.github.io/working-open-workshop/data_reuse/)

####Information:####
* Digital Curation Centre’s List of Disciplinary Metadata: http://www.dcc.ac.uk/resources/metadata-standards 
* Research Data Alliance Community-Maintained List of Metadata Schema: http://rd-alliance.github.io/metadata-directory/subjects/ 
* UK Data Archive Documenting Your Data Overview: http://www.data-archive.ac.uk/create-manage/document 
* Australian National Data Service Working-Level Metadata Guide: http://ands.org.au/guides/metadata-working 
* Northwest Environmental Data Network Best Practices for Data Dictionary Definitions and Usage: http://www.pnamp.org/sites/default/files/best_practices_for_data_dictionary_definitions_and_usage_version_1.1_2006-11-14.pdf
* Australian National Data Service File Formats Guide: http://www.ands.org.au/guides/file-formats
