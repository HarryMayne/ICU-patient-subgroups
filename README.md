# Identifying-Intensive-Care-Unit-Patient-Subgroup
Code repository for the paper "The Generalisability of Unsupervised Learning Approaches to Identify Intensive Care Patient Subgroup"

## Data Requirements
Since the MIMIC-IV data is confidential, users of this code must first access the data and put it into the relevant directories. The files required are the following:
* MIMIC-IV v2.2 dataset (mimic-iv-v2.2)
* Derived files from the MIMIC-IV Code Repository. These can be installed directly from GoogleBigQuery or you can find the raw SQL code [here](https://github.com/MIT-LCP/mimic-code/tree/main/mimic-iv).
    * Glasgow Coma Scale (gcs.csv) - NOTE: this is not the same as first_day_gcs
    * Charlson Comorbidity Index (cci.csv)
    * Code Status (codestatus.csv)
    * SAPS II (sapsii.csv)

## Required Directory Structure
Once you have downloaded MIMIC-IV you should put the contents of the `mimic-iv-v2.2' directory into the `data' directory. Derived files from the MIMIC-IV Code Repository/GoogleBigQuery should be put into the directory called `queried_data'. The finished set up should look like this:
![directory_setup](https://github.com/HarryMayne/Identifying-Intensive-Care-Unit-Patient-Subgroup/assets/115154632/7fda6c76-8e56-4638-8984-f417661840f4)
Note that the license is the MIMIC-IV licsense.

