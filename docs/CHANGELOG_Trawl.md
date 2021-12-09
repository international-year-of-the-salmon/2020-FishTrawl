# CHANGELOG

All notable changes to this project will be documented in this file. This document outlines all the changes made to the original data files: `2020-01 Specimen file.v21.1c_FINAL SUBMIT_jan18_2021.xlsx` (for specimen data), and `JuvSalmon_2020-01_Catch_v2021.1C_FINAL SUBMIT_jan18_2021.xlsx` (for bridgelog and overall catch data). To preserve the original files, the changes made were done in their respective working files (`2020_GoA_Fish_Specimen_data.xlsx` and `2020_GoA_Fish_Trawl_data.xlsx` respectively) to facilitate standardization of the data. The original data files are still in a secure Google Drive folder, and will be moved to the open IYS GitHub repository once approved and finalized. The working files - those that are being standardized to DwC standards - are saved locally. The standardization script also includes changes made to facilitate publication of the Standardized Data to the Ocean Biodiversity Information System (OBIS), however those changes were NOT made to the original file or working files, and are documented in the .Rmd file (`data_wrangle_trawl.Rmd`). 

## Changes to JuvSalmon_2020-01_Catch_v2021.1C_FINAL SUBMIT_jan18_2021.xlsx 

The following are the changes made to the original data to get to the working file (2020_GoA_Fish_Trawl_data.xlsx):

For Set_number 16 - the catch of Aurelia labiata is removed. The reason for this is that in the overall catch data the species was identified to a species level, but in the specimen data it was listed as _Aurelia sp._. Until verified that these Aurelia sp. are indeed Aurelia labiata, for consistency purposes the Aurelia labiata observation is removed. 

### Added

For Set_number 10 - Diaphus theta catch_number is changed to 62 as per comm. with CN. A comment was added that other pieces accounted for 11 grams.


## Changes to 2020-01 Specimen file.v21.1c_FINAL SUBMIT_jan18_2021.xlsx

In Set_number 1 the specimen information for _Citharichthys stigmaeus_ is removed (_rows: #... - #...). This is likely information associated with a record of Paralichthydidae in the overall catch data, which was removed from the standardized dataset as it was not identified to species level. In addition, there is a note in the specimen file indicating that _Citharichthys stigmaeus_ ID needs to be verified. Until such time, it is excluded from the standardized data. 

In Set_number 1 _Pasiphaea pacifica_ is included in the specimen data but not in the overall catch data, and therefore removed from the specimen data for consistency. As per CN: _This is another UBC question or possibly the Russians.  This was not on the hard copy catch sheets. It was either on the flat file from UBC or in the Russian database.  Since UBC took samples for species ID, I would refer to them first as sometime, unverified names ended up in Russian database. _

Rows _#123 - #131_ for 9 Diaphus theta individuals were removed. These rows were duplicates and indivated the fatty acid sample # for UBC. For the purposes of standardization this information is not required and therefore these rows are removed to avoid duplication of catch.

Rows _#214 - #263_ were removed. These were duplicates of Tarletonbeania crenularis - the rows with species information and measurements were retained.

Rows _#687 - #692_ were removed. These were duplicates of Symbolophorous californiensis - the rows with individual information and measurements were retained.

For set 4, 300 excess rows for Tarletonbeania crenularis were removed as these were a merging error when combining Russian and or UBC data. The number of rows retained include the individual measurements and align with the catch numbers and individuals measured as reported in the overall catch data. As per CN: _This is inputting error from trying to merge UBC and or Russian data into master datafile.  There is only 301.  The rows with 672 as tracking should be deleted.  These are rounded numbers and not the individual measurements taken.  The data on hard copies start with tracking 1994 with fish 75mm._

Removed rows _#3536 - #3567_, in the specimen file these are listed as Sebastes melanops, but in the overall catch data they are listed as Sebastes sp. (rockfish larva). As they were not identified to the species level in the overall catch they were omitted from the standardized data. As such, I have also omitted these from the standardized individual data for consistency purposes, until such time that the data provider can verify that Sebastes sp. in the overall catch data should be changed to Sebastes melanops. As per CN: _This will need to be confirmed by UBC. I do not believe we had anyone on board with expertise in juvenile rockfish ID._

For Set_number 22, _Phacellophoroa camtschatica_ is included in the specimen file, but in the overall catch file, it was recorded as _Phacellophoroa sp._. As there it was not identified to a species level it was excluded from the overall standardized catch data. For consistency purposes, it has therefore been removed from the specimen data as well until verified and aligned between overall and specimen catch data. As per CN: _This is a question for UBC.  I believe the P. camtschatica came from the Russians but I would question if this would be correct species for eastern pacific.  Could be.  I have no idea.  Since UBC took samples they should be able to confirm._

For Set_number 32, the overall catch data makes mention of Citharichthys sordidus (n=1) and Citharichthys stigmaeus (n=4) caught, and in the specimen data there is only Citharichthys stigmaeus (n=5). In the overall catch data, for Citharichthys stigmaeus there is a comment saying that genetic sample #1715 was taken to confirm the species. For Citharichthys sordidus (n=1) there was a genetic sample #1716 taken. In the specimen file it was indicated under a Citharichthys stigmaeus individual that the genetic sample #1715 was taken; however in the specimen file there's only Citharichthys stigmaeus included, _not_ Citharichthys sordidus. This seems to not be properly aligned. Until verified, Citharichthys stigmaeus records in Set_number 26 have been removed from the specimen file, and both Citharichthys sordidus (n=1) and Citharichthys stigmaeus (n=4) have been removed from the overall catch data file. 

### Added

For Set_number 36, four lengths (rows) are added for _Microstomus pacificus_. As per CN: _This is an error. The lengths for the four specimen are 35mm, 45mm, 30mm, and 50mm_. Added these lengths to `Length (total)` column (as per other Microstomus pacificus measurements).

For Set_number 47, two lengths (rows) are added for _Hormiphora cucumis_, with individual lengths. No individual weights were recorded. As per CN: _this is error. There are two lengths that need to be added to specimen file.  30mm and 20mm.  total weight of the two was 4g._  

#### Species names changes

The following species names were changed in the standardization script, NOT in the original file or working file:

Working file: 2020_GoA_Fish_Trawl_data

Original Name			            OBIS / WoRMS
--------------------------------------------------------
Paralichthydidae              Paralichthyidae
Paralepidadae                 Paralepidapedon
Sergestes similus             Sergestes similis
Salps                         Salpa
Abraliopsis Felis             Abraliopsis felis
Gooseneck barnacle            Pollicipes pollicipes
Chiroteuthis calix            Chiroteuthis calyx
Glycptocephalus zacharius     Glyptocephalus zachirus
squid                         Teuthida
Fish eggs                     Pisces
jellyfish                     Cnidaria
gonatidae                     Gonatidae

The following species names were changed in the standardization script, NOT in the original file or working file:

Working file: 2020_GoA_Fish_Specimen_data.xlsx

Original Name			OBIS / WoRMS
----------------------------------------------------------
Abraliopsis Felis             Abraliopsis felis
Oncorhynchus gorbusha         Oncorhynchus gorbuscha
Phacellopphoroa camtschatica  Phacellophora camtschatica
Chiroteuthis calix            Chiroteuthis calyx
Glycptocephalus zacharius     Glyptocephalus zachirus
Unknown jelly                 Cnidaria
Flatfish larvae               Pleuronectiformes
