## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)
* [Test Scenarios Covered](#Test-Scenarios-Covered)

## General info
This project is for Muesum API automated tests to run in the Jenkins using scripted pipeline.

## Technologies
Project is created with:
* Maven
* Karate 1.3.0
* Junit 5
* Java 17

## Setup
Run this command to buid the project in local:  
&emsp; &emsp; **mvn clean install**

Run this maven command to run the automation tests  using maven profile:\
&emsp; &emsp;  **mvn clean verify  -P regressiontests**

To run automation tests  in Jenkins:  
&emsp; &emsp;  **Configure Jenkins to create pipeline from script in jenkins-pipeline file**

## Test Scenarios Covered
Collections API:

    1. Default Search
    2. Search without API Key
    3. Search results in languages (culture - nl and en)
    4. Search results in file formats ( json and xml)
    5. Search Filters (Single and multiple)
    6. Search with Query parameters
    7. No of search results per page (Default –10, 0-100,101)
    8. Navigating to page in search results
    9. Sort Order for search results (‘relevance’, ‘objecttype’, ‘chronologic’, ‘achronologic’, artist, artistdesc)
    10. Facets based on dating period and normalized32Colors

Collection Object API:

    1. Get collection Object details
    2. Search without API Key
    3. Collection object details in languages (culture - nl and en)
    4. Collection object details in file formats (json and xml)

Issues Observed in the collections API

    1. Filters are not working when page and no of records per page is selected
    2. Image only and toppieces filters are not working 

