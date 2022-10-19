# CHPL Filled Holds Data Set
<img src="https://raw.githubusercontent.com/cincinnatilibrary/collection-analysis/master/misc/CHPL_Brandmark_Primary.png" alt="CHPL" title="CHPL" width="250"/>

This is a set of data representing items placed on hold shelves and some related metadata

This data set consists of two .csv files:

1. `filled_holds_2019-01-01_to_2019-03-01.csv` (`filled_holds_2019-01-01_to_2019-03-01.zip`)
1. `branch_location_codes.csv`

The first file, filled_holds.csv contains columns that describe a “filled hold”–meaning an item has been placed on a hold shelf at a branch location at the request of a patron who placed a hold on that title (the catalog system software automatically matches an item from the list of items records attached to a title record). Columns in this file are described below:

* **hold_id** : unique id for the hold placed
* **item_record_id** : matched item record selected to fill the hold
* **patron_record_id** : unique id for the patron placing the hold
* **hold_placed_datetime** : the timestamp the hold was placed in the catalog system
* **hold_filled_datetime** : the timestamp the item was placed on the hold shelf at the location requested by the patron
* **source_location_code** : the coded location of the origin where the item came from
* **pickup_location_code** : the coded location’s hold shelf where the patron will pickup the item

The second file, branch_location_codes.csv contains some metadata about the branch codes referenced from the filled_holds.csv file. Columns in this file are described below:

* **location_code** : coded location
* **branch_code_num** : branch coded location
* **is_public** : boolean value indicating if the location is available to the public
* **branch_name** : branch name
* **branch_street** : street address
* **branch_city_state** City, State ZIP for the branch location

Some possible things to do with this data set:

* Can you identify trends in where items tend to come from in relationship to where they are sourced from?
* If you were to plan a delivery route based off of this data, what things may you consider in this data? What other types of data sources might you want to look at?
* Can you identify any trends around the time frames that holds are placed and filled?
