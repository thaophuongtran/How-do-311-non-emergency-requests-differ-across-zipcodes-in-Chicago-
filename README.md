Project 2 Write-Up
================

\#Project 2 Write-up

\#\#Kamran Ahmed, Kaylah Thomas, Thao Tran (Rosy Eeve) \#\#5/11/2022

## Introduction

In this project, we utilize interactive and animated spatio-temporal
visualization to illustrate how the composition of non-emergency
requests differ across communities with varying sociodemographic
characteristics in the Chicago 311 Service Requests data.

The 311 system is a non-emergency response system where people can make
a request to find information about services, make complaints, or report
non-emergency problems, such as potholes and trash collection. While the
system was initially designed to reduce call volume on the overloaded
911 system, 311 request systems have become an integral part of the
e-government movement in which technological innovations are deployed to
help local governments deliver more efficient and effective services to
residents. Thus, we employ the 311 data in Chicago to provide insights
on the variation of communities’ needs and assist the city to better
allocate resources accordingly. We are also interested in incorporating
demographic measures into this analysis. Examining the distribution of
requests for areas with varying sociodemographic characteristics can
possibly help to show where more resources should be allocated, or other
trends in requests.

We focus on two measures of interest regarding the 311 data: number of
requests and the amount of time it takes to complete a request. While
the first measure informs the demand of non-emergency services, the
second measure reflects the quality of responses from the city to its
residents, where longer requests may be lower quality since there is a
delay in serving the community. We use zip codes to identify our
geographical areas and merge in sociodemographic information from the
American Community Survey (ACS) 2019. (see the [data]() folder of this
repository for information about the variables of interest used in this
analysis.

Our project will include spatial visualizations of varying 311 service
request types, as well as other plots that will aid in illustrating the
characteristics of a selected area. This will help to show the
correlation between trends, for example, an influx of a graffiti
cleaning service request and the education level of those who reside in
that area. We plan to implement Shiny apps to show each type of 311
request. We would also like to consider using the package `rayshader` to
develop interactive 3-D maps to represent the frequency of service
requests in a given area. Basic `ggplot2` visualizations will be
developed in order to aid our 3-D interactive visualizations, such as
density plots, line plots, or bar charts.

We intend to add an element of interactivity to this analysis using
Shiny app. The app will include the ability to toogle certain categories
of service requests, as well as select a community area in order to see
the distribution of service requests and the demographic patterns
associated with the frequency of requests in the area.

## [Data](proj2-rosy-eeve/Data)

[Chicago 311 Service
Requests](google%20drive%20link%20to%20dataset%20here)

The data on 311 Service Requests received by the City of Chicago are
publicly available on the Chicago Data Portal. The dataset includes
requests created after the launch of the new 311 system on 12/18/2018
and was last updated on May 11, 2022. Currently, it has 6 million rows
and 37 columns, where each row is a request. Useful features from the
data include request type, owner department, create date, closed date,
and zip code. Since we are interested in the response time, we restrict
observations to requests that have been completed. It is noted that the
address for requests of the type “311 INFORMATION ONLY CALL” is often
the address of the City’s 311 Center. See the codebook below for all
variables of interest.

[Demographic
Variables](proj2-rosy-eeve/Data/Chicago_zcta_subset_acs2019_clean.csv)

The American Community Survey (ACS) is a questionnaire conducted by the
United States Census Bureau yearly to collect information about American
citizens. Relevant sociodemographic elements were selected from this
survey in the year 2019, and converted into a workable dataset using
`tidyCensus`. Our subset of data includes 24 columns and 296 rows
correlating to Chicago and other outlying areas included in the Chicago
Metropolitan Statistical Area (MSA). Only zip codes included in the
Chicago 311 dataset will be selected from this dataset. Among the
selected variables include factors relevant to race, education, age,
gender, and socioeconomic status. While the already selected variables
are robust, the many questions included in the original survey allow for
us to add or reduce the number of variables included as necessary. See
the codebook below for all variables of interest.

## Repository Organization

  - [Data](proj2-rosy-eeve/Data/README.md)
      - Demographic data from the ACS via `tidycensus`
      - 311 data
  - [Presentation](proj2-rosy-eeve/Presentation/README.md)
  - [Proposal](proj2-rosy-eeve/Proposal/README.md)
  - [Write-up](proj2-rosy-eeve/README.md)

## Citations
