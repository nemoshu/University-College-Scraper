# Univesity College Scraper Project Specification

## Explanatory Note

This document defines the high-level architecture of the project, serving as a vision of what should be built.

Developers are also advised to create additional specifications for each module, and for communication between modules.

## Section 1: Project Architecture

(1) The project should contain the following modules:

    (a) Scraping. 

    (b) AI Filtering.

    (c) Databases.

    (d) ICS / Subscription Manager.

    (e) Frontend.

    With additional requirement for each module defined in Sections 1A-1E.

(2) Modules should be independent to each other as far as possible, with interfaces clearly specified.

## Section 1A: Requirements for Scraping Module

(1) **Presentation of Data**

    (a) An event must contain the following information when passed through the calendar:

        (i) Time and Date of Message

        (ii) AI generated title

        (iii) Description

        (iv) Tags: Known Metadata about Organiser - the society or standalone; SU or non-SU
    
    (b) In addition to fields defined in (a), an event may have the following:

        (i) Time and Date of Event
        
        (ii) Location

(2) **General Scraping Workflow**

    Steps:

    1. Extract text data. (If source is an image then the scraper is responsible for OCR)

    2. Extract mandatory data, namely: (a)(i)(iv), and pass through the message to the AI component.

    3. The AI component would return (a)(ii)(iii), and if available, (b).

    4. Check database for duplications, merge / updates where appropriate. 

    5. Persist.

## Section 1B: Requirements for AI Filtering Module

## Section 1C: Requirements for Database Module

## Section 1D: Requirements for the ICS / Subscription Manager Module

## Section 1E: Requirements for the Front-end


