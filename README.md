# HealthOutcomesandParkAmenities
TLDR: This repository holds the data, code, and final report for my Capstone project for the MS in Informatics and Analytics program at the University of North Carolina at Greensboro.

###################################################################################################################

Title: Relationships Between Health Outcomes and State Park Amenities in Counties in New York State: 2020-2021 Data
                                                   Author: Anne Miller
                                                     Date: May 2023

###################################################################################################################

                                                        Abstract:
The goal of the project was to analyze relationships between health outcomes and the availability of amenities at state parks in the state of New York. Data for almost 200 state parks and 
health outcomes in the parks' corresponding counties was collected frpm www.ny.gov and www.census.gov. The analysis was conducted at the county level to see if health outcomes in counties 
where the park amenities were present differed from health outcomes in counties where the park amenities were not present. The project was divided into the two following questions, and both
questions were analyzed using R:

1: Do mean health outcomes change based on the state park amenities available and, if so, what is the magnitude and direction of the relationship(s)?
2: Does that relationship vary between groups of counties with different ranges of health outcomes and, if so, what is the magnitude and direction of the relationship(s) within each group?

These questions were first answered for all counties as a whole. Then, the counties were grouped into clusters based on their health outcomes, and the questions were again analyzed withineach cluster.

###################################################################################################################

                                                          Method:
Because there were multiple health outcomes to be analyzed, a MANOVA was chosen as the most appropriate method of analysis. The assumptions of MANOVA were checked on both the full dataset
and the clustered data, and health outcomes that did not meet these assumptions were dropped from the analysis. In addition to the MANOVA, an ANOVA was also conducted on the overall health
rating for each county, a variable that was created as a ranking system based on the other health outcome variables.

###################################################################################################################

                                                          Results:
-------------------------------------------------------------------------------------------------------------------
1: Do mean health outcomes change based on the state park amenities available and, if so, what is the magnitude and direction of the relationship(s)?

When all counties were considered, there was statistically significant evidence (p-value=0.04) of an estimated 0.0001% decrease in the age-adjusted percentage of adults who received one or 
more buprenorphine prescriptions for opioid use disorder, an estimated 1.65% decrease in adults who smoke cigarettes, an estimated 0.25% decrease in adults diagnosed with depression, an 
estimated 0.29% decrease in adults diagnosed with cardiovascular disease, and an estimated 2.76% decrease in obese adults in a county that has state parks with playgrounds compared to a county 
that does not.

When all counties are considered, there was also statistically significant evidence (pvalue=0.04) of an estimated increase of 0.76% in adults who participate in physical leisure activity
in a county that has state parks with playgrounds compared to a county that does not. 

When all counties are considered and the family-wise error is controlled, there is statistically significant evidence of an estimated increase of 4.56 in overall health rating in a county 
that has state parks with trails compared to a county that does not (95% confidence interval 0.76-8.36, p-value=0.02).

-------------------------------------------------------------------------------------------------------------------
2: Does that relationship vary between groups of counties with different ranges of health outcomes and, if so, what is the magnitude and direction of the relationship(s) within each group?

When the counties were clustered into three groups based on their combined health outcomes, there was statistically significant evidence (p-value=0.0002) in counties contained in 
Cluster 3 that the presence of waterfalls is associated with an estimated decrease of 0.48% in adults who smoke cigarettes, an estimated decrease of 1.85% in obese children, 
and an estimated decrease of 2.40% in adults with a regular healthcare provider. 

There is also statistically significant evidence (p-value=0.04) in counties contained in Cluster 3 that the presence of food amenities is associated with an estimated increase of 0.55% in 
of adults who smoke cigarettes, an estimated increase of 0.06% in in obese children, and an estimated 1.31% decrease in adults with a regular healthcare provider. Overall, the presence of 
food amenities in counties contained in Cluster 3 both decreased health outcomes that are considered negative indicators of health and increased health outcomes that are considered positive 
indicators of health. 

Although there was no statistically significant evidence of a relationship between any of the park amenities and health outcomes in Clusters 1 and 2, the presence of waterfalls in counties 
within all three clusters was associated with a decrease in the percentage of obese children in these clusters as well (estimated 0.84% decrease in Cluster 1 and estimated 3.20% decrease in Cluster 2). 

When counties are clustered into 3 groups but only the overall health rating is considered and the family-wise error rate is controlled for, there is no statistically significant evidence of an 
association between any of the state park amenities and overall health rating in any of the clusters.
