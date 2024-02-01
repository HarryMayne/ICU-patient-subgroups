# Identifying Intensive Care Unit Patient Subgroup
Code repository for the paper "The Generalisability of Unsupervised Learning Approaches to Identify Intensive Care Patient Subgroup"

## Data requirements
Since the MIMIC-IV data is confidential, we cannot share the data used for the project. Users of this code must first get access the data and then put it into the relevant directories. The code is designed that there is minimal effort required once the data is sourced.

We require the following datasets:

* MIMIC-IV v2.2 dataset (mimic-iv-v2.2). Details about getting access to this can be found [here](https://physionet.org/content/mimiciv/2.2/).
* Derived files from the MIMIC-IV Code Repository. These can be installed directly from Google BigQuery or you can find the raw SQL code [here](https://github.com/MIT-LCP/mimic-code/tree/main/mimic-iv). If there are python implementations of these derived tables then feel free to let us know or submit a pull request. 
    * Charlson Comorbidity Index (charlson.csv)
    * SAPS II (sapsii.csv)
    * Glasgow Coma Scale (gcs.csv). **NOTE:** this is not the same as first_day_gcs

## Required directory structure
Once you have downloaded MIMIC-IV you should put the contents of the `mimic-iv-v2.2' directory into the `data' directory. Derived files from the MIMIC-IV Code Repository/GoogleBigQuery should be put into the directory called `queried_data'.

The finished set up should look like the image below. Note that the LICENSE.txt and CHANGELOG.txt are part of the MIMIC-IV contents.

<img src="https://github.com/HarryMayne/Identifying-Intensive-Care-Unit-Patient-Subgroup/assets/115154632/7fda6c76-8e56-4638-8984-f417661840f4" alt="directory_setup" width="300" style="display:block; margin-left:auto; margin-right:auto"/>

## Generating the cleaned dataset 
To generate the dataset for clustering, you only need to run one file. This is `data_cleaning.ipynb'. This will create a csv file called `cleaned_data.csv' in the data directory. It is a long notebook and can take a while to run depending on your compute. The returned dataset contains all of the recreated features for all individuals. 
