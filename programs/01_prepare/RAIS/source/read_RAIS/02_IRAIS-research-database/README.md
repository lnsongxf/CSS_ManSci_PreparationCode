# Code to prepare IRAIS research database

25 November 2020
Ian Schmutte
`schmutte@uga.edu`

Code in this folder must be run in a specific sequence to generate the IRAIS research database.

## Steps

1. Edit `./lib/header.sas` to point to local locations of the `irais&yr..sas7bdat` files generated in `01_build_integrated_RAIS`.
2. In `./01_make_db_files` execute the following programs in order
    1. `01.01.clean_contracts.sas`
    2. `01.02.harmonize_db.sas`
    3. `01.03.make_contents.sas` (optional)
3. In `./02_modal_characteristics` execute in order
    1. `02.01.extract_personchars.sas`
    2. `02.02.fixed_plantchars.sas`

The output files generated by this code are

* `rais_match_uniq_&year..sas7bdat` for each year 2002-2017
* `rais_plant_uniq_&year..sas7bdat` for each year 2002-2017
* `educ_best.sas7bdat`
* `race_gender_age_best.sas7bdat`