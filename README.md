## OpsGenie Alert Classifier
Helpful functions for analyzing an export of OpsGenie alerts and collecting useful data on them.

### Functions
* Clean
  * Specify rows from a *raw.csv file into a *clean.csv file
* Count
  * Count the number of alerts matching a specified column name (default Alias). If no column is specified, return the total count of alerts
* Time Interval Filtering
  * An interval to filter the "CreatedAtDate" hour of each alert. This can be added to count.
* Keyword matching
  * A keyword to filter the specified --count column against

### Future functionality
* Created to Updated (typically alert creation to close) duration

### Running
This requires Python3
```
pip install virtualenv
virtualenv -p python3 venv
source venv/bin/activate
```
Run commands:
```
python classify.py alert-data-raw.csv --clean Alias Message Teams
python classify.py alert-data-raw.csv --count Alias
python classify.py alert-data-raw.csv --count Alias --interval 4 13
python classify.py alert-data-raw.csv --count Alias --match gdpr
```