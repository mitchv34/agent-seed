---
title: Public Data Sets Not On Snowflake (NCES & BLS)
description: Data sets collected but not yet uploaded to Snowflake, focusing on NCES and BLS data.
parent: index.md
max_lines: 250
source: slab
---

# Public Data Sets Not On Snowflake (Part 1: NCES & BLS)

These are some data sets which we have collected but not yet uploaded to Snowflake. They are available [here](https://us-east-2.console.aws.amazon.com/s3/buckets/intern-uploads-public-data?region=us-east-2&bucketType=general&tab=objects).

## 1. NCES Data

A. **School District Composites**
* **Prefix:** `School_District_Composites_SY_`
* **Years Available:** 2013–14 through 2023–24
* **Description:** Annual composite datasets combining geographic boundaries with district-level attributes such as identifiers and demographic stats for all U.S. public school districts.

B. **School District Office Locations**
* **Prefix:** `School_District_Office_Locations_`
* **Years Available:** 2015–16 through 2023–24, plus current
* **Description:** Geocoded datasets providing the physical locations and contact information of school district administrative offices in the U.S.

C. **School District Characteristics**
* **Prefix:** `School_District_Characteristics_`
* **Years Available:** 2017–18 through 2022–23, plus current
* **Description:** District-level demographic and operational data, including enrollment, staffing, and fiscal information for public school districts.

D. **Public School Locations**
* **Prefix:** `Public_School_Locations_`
* **Years Available:** 2015–16 through 2023–24, plus current
* **Description:** Geospatial datasets of public school locations, including name, address, coordinates, and basic school attributes.

E. **Public School Characteristics**
* **Prefix:** `Public_School_Characteristics_`
* **Years Available:** 2017–18 through 2022–23, plus current
* **Description:** Annual data on public school attributes including student demographics, teacher counts, and instructional offerings.

F. **Private School Locations**
* **Prefix:** `Private_School_Locations_`
* **Years Available:** 2017–18 through 2021–22, plus current
* **Description:** Geolocated information on private schools, including name, address, and basic classification details.

G. **School District Boundaries**
* **Prefix:** `School_District_Boundaries_`
* **Years Available:** Current only
* **Description:** Current-year shapefiles showing the geographic boundaries of public school districts nationwide.

H. **Postsecondary School Locations**
* **Prefix:** `Postsecondary_School_Locations_`
* **Years Available:** 2015–16 through 2023–24, plus current
* **Description:** Geocoded data on colleges and universities, including institutional characteristics and location info from the IPEDS system.

I. **ACS-ED: Children Enrolled in Public Schools**
* **Prefix:** `ACS-ED_XXXX-XXXX_Children-Enrolled_Public:`
* **Years Available:** 2013–2017 and 2014–2018
* **Description:** ACS 5-year estimates on students enrolled in public schools, detailing economic, social, demographic, and housing characteristics.

J. **ACS-ED: Total Population**
* **Prefix:** `ACS-ED_XXXX-XXXX_Total_Population:`
* **Years Available:** 2013–2017 and 2014–2018
* **Description:** ACS-based community context data on the general population, covering economic, housing, and social factors.

K. **School Attendance Boundary Survey**
* **Prefix:** `School_Attendance_Boundary_Survey_`
* **Years Available:** 2015–2016
* **Description:** Geographic files showing attendance zone boundaries, mapping which neighborhoods are assigned to which public schools.

L. **School Neighborhood Poverty Estimates**
* **Prefix:** `School_Neighborhood_Poverty_Estimates`
* **Years Available:** 2016–17 through 2021–22, plus current
* **Description:** Model-based estimates of poverty levels in neighborhoods surrounding schools, linked to school catchment areas.

## 2. NCES Longitudinal Surveys

A. **National Postsecondary Student Aid Study (NPSAS)**
* **Prefix:** `NCES_npsas_...`
* **Years Covered (in this batch):** 1999–2000 through 2015–16
* **Description:** NPSAS collects detailed financial aid and demographic data on undergraduate and graduate students across U.S. institutions.

B. **Beginning Postsecondary Students Longitudinal Study (BPS)**
* **Prefix:** `NCES_bps_...`
* **Description:** BPS tracks first-time postsecondary students over time to study persistence, degree attainment, major changes, employment outcomes, and financial aid history.

C. **Baccalaureate and Beyond Longitudinal Study (B&B)**
* **Prefix:** `NCES_b&b_...`
* **Description:** B&B follows students who earn bachelor’s degrees to examine graduate school enrollment, employment, loan repayment, and geographic mobility after graduation.

## 3. BLS State and Metro Area Employment, Hours, & Earnings Data

A. **sm.txt**: Master file containing series-level metadata.
B. **sm.area.txt**: Reference list of geographic areas.
C. **sm.industry.txt**: Industry classification codes.
D. **sm.supersector.txt**: Higher-level industry groupings.
E. **sm.data_type.txt**: List of data types available.
F. **sm.series.txt**: Complete index of all available series.
G. **sm.period.txt**: Time periods used in the data.
H. **sm.footnote.txt**: List of explanatory footnotes.
I. **sm.contacts**: Contact information for regional BLS offices.
J. **sm.state.txt**: Lookup table for state FIPS codes and BLS area codes.
K. **sm.data.X.StateName.txt**: State-specific employment, hours, and earnings data.
L. **Sector-Specific Aggregates**: Pre-aggregated datasets for high-level sectors.

## 4. BLS Local Area Unemployment Statistics

A. **la.txt**: Primary series metadata file.
B. **la.series.txt**: Detailed listing of all data series.
C. **la.measure.txt**: Definitions of the types of employment and earnings measures.
D. **la.period.txt**: Codes for time periods.
E. **la.footnote.txt**: Footnotes used in the dataset.
F. **la.contacts.txt**: Contact information for BLS regional staff.
G. **la.state_region_division.txt**: Maps states to U.S. Census regions and divisions.
H. **la.area.txt**: Lookup table for geographic codes.
I. **la.area_type.txt**: Identifies the type of each geographic area.
J. **la.map_info and la.areamaps.txt**: Geographic mapping support files.
K. **la.data.X.StateName.txt**: State-specific datasets with monthly employment and earnings data.
L. **la.data.60.Metro, la.data.62.Micro.txt, la.data.63.Combined**: Datasets for MSAs.
M. **la.data.64.County.txt, la.data.65.City.txt**: County and city level data.
N. **Aggregated Groups**: National subgroups summary statistics.
