# DISC
DISC: A Dataset for Information Security Classification

## Dataset
The Digital National Security Archive (DNSA) is a comprehensive document archive, comprising over 100,000 declassified records that document historic United States policy decisions. The DNSA contains electronic copies of both previously classified and unclassified government documents related to U.S. foreign policy from the post-World War II era to the present day. The DISC dataset was curated by ingesting documents form the following DNSA domains:
* AF, Afghanistan: The Making of U.S. Policy, 1973-1990
* CH, China and the United States: From Hostility to Engagement, 1960-1998
* PH, The Philippines: U.S. Policy during the Marcos Years, 1965-1986.

The statistics of the documents contained within the initial release of the DISC dataset are listed in the table below.

| Domain | UNCLASSIFIED | SECRET | TOP SECRET | TOTAL |
|:----------:|:----------:|:----------:|:----------:|:----------:|
| AF | 401 | 206 | 13 | 620 |
| CH | 151 | 666 | 132 | 949 |
| PH | 411 | 469 | 1 | 881 |
| **TOTAL** | **963** | **1,341** | **146** | **2,450**|

## DISC Schema

The documents in the DISC dataset have the attributes as listed in the table below. 


| Attribute | Description | 
|----------|----------|
| DocID | Unique DISC Document ID | 
| Title | Document Title | 
| Abstract | Brief Summary of the document | 
| OCRText | Text extracted via OCR from the PDF document | 
| Text | Text reconstructed via LLM from the OCR output | 
| Classification | Document classification events (each document may have mutliple classification events | 
| Database | References to the database the document was extracted | 
| Domain | Domain within the database the document was extracted | 
| Author | Authorship information | 
| StoreID |Database assigned unique document ID | 

Documents in the DISC dataset may have multiple classification events.   Classification events attributes are listed in the table below.

| Attribute | Description | 
|----------|----------|
| ClassID | Unique classification event ID | 
| Label | Classification level (UNCLASSIFIED, SECRET, or TOP SECRET) | 
| Date | Classification date | 

## DISC Dataset Access
The DISC dataset JSON file can be downloaded at the following link:
https://github.com/maxalbanese/DISC.git