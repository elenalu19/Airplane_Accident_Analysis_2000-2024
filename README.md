# USA Aviation Accident Data Analysis

## Project Overview

This project performs an in-depth analysis of USA aviation accidents from January 1, 2000, to the present day. While many public aviation accident datasets exist, this analysis focuses on previously unexplored factors by extracting information directly from the official NTSB (National Transportation Safety Board) accident reports. The primary goal was to answer questions related to pilot demographics, flight phase, and historical context, which are not readily available in the NTSB's queryable database.

## Key Questions & Hypotheses

The analysis was designed to explore the following factors:

* **Pilot Demographics:** What is the age and flight experience of pilots involved in accidents?

* **Historical Context:** Is there a correlation between the number of accidents and the U.S. presidential administration at the time?

* **Accident Phase:** At what point during the flight do most accidents occur?

## Data Sources & Methodology

The data for this project was compiled from two primary sources:

1. **NTSB Aviation Accident Data:** The initial dataset was sourced from the NTSB's public data query tool. A key step involved filtering for accidents with a "Complete" status and located in the United States, ensuring that final reports were available for analysis.

2. **NTSB Accident Report PDFs:** A custom Python script was developed to programmatically access and parse the final accident report PDFs. This was necessary to extract specific, granular details—such as pilot age and flight phase—that were not included in the main NTSB dataset.

3. **U.S. President Data:** A separate table containing a list of U.S. presidents and their terms was used to join with the accident data, enabling historical comparisons.

The raw data was cleaned and pre-processed using Microsoft Excel. The NTSB data and the U.S. president table were then joined using SQL in Google BigQuery to create a unified dataset.

## Key Findings

This analysis revealed several interesting insights, with more detailed findings available in the final Tableau dashboards:

* **Pilot Age:** Approximately **44%** of the accident reports analyzed involved pilots in the 47-57 age range. This aligns with broader industry data indicating that a significant portion of the pilot population falls within this demographic.

* **Geographical Hotspots:** The states with the highest number of aviation accidents were California, Illinois, Florida, Texas, Colorado, New York, and Alaska.

* **Alaska's Exception:** The high number of accidents in Alaska, disproportionate to its population, is primarily attributed to harsh weather conditions and rough terrain, which present unique challenges to aviation in the state.

## Tools & Technologies

The project utilized a combination of programming languages, libraries, and software for data extraction, analysis, and visualization.

* **Programming Language:** Python

* **Notebook Environment:** Google Colab

* **Data Extraction & Processing Libraries:** `pypdf`, `requests`, `pandas`, `re`

* **Cloud & Database Services:** Google BigQuery, Google Colab

* **Data Visualization:** Tableau

## Repository Structure
notebooks/

[Code_Aviation_Data_Collect&Clean.ipynb](Code_Aviation_Data_Collect&Clean.ipynb)

data/
[ext_far121_ntsb.csv](ext_far121_ntsb.csv)

[USA_pres_2000-2025.csv](USA_pres_2000-2025.csv)

[Joined_aviation_president.csv](Joined_aviation_president.csv)

visualizations/
[2000-2024 Airplane Accidents.twbx](2000-2024 Airplane Accidents.twbx)

README.md
