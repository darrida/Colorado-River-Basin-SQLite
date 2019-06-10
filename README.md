# SQLite Script for Colorodo River Basin Cooperation and Conflict Spreadsheet
This is a simple Python script I created to insert the Colorodo River Basin Cooperation and Conflict Database into a SQLite database. 

The spreadsheet I inserted from, as well as more information about it, can be found here: https://transboundarywaters.science.oregonstate.edu/content/collection-research-and-datasets-colorado-river-basin

Direction download link: https://transboundarywaters.science.oregonstate.edu/sites/transboundarywaters.science.oregonstate.edu/files/Database/ResearchProjects/Colorado/Final_WWIS_UC_Event_Database.xls

## SQL Script for SQLite table:
```
CREATE TABLE CO_River_Basin (
    Event            DECIMAL (10)   PRIMARY KEY
                                    UNIQUE
                                    NOT NULL,
    SearchSource     VARCHAR (100),
    Newspaper        VARCHAR (200),
    ArticleCitation  VARCHAR (1000),
    ArticleTitle     VARCHAR (1000) NOT NULL,
    File             VARCHAR (100),
    ReportDate       DATE,
    ReportYear       DECIMAL (10),
    Eventdate        VARCHAR (100),
    EventYear        VARCHAR (100),
    Basin            VARCHAR (100),
    LocatorWaterBody VARCHAR (200),
    IssueType        VARCHAR (500),
    EventSummary     TEXT (5000),
    Stakeholders     VARCHAR (500),
    IntensityValue   VARCHAR (6),
    WaterTitle       VARCHAR (200),
    Comments         VARCHAR (5000) 
);
```

## Source
“Product of the Transboundary Freshwater Dispute Database, College of Earth, Ocean, and Atmospheric Sciences, Oregon State University.  Additional information about the TFDD can be found at: http://transboundarywaters.science.oregonstate.edu.” 
