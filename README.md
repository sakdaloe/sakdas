# Sakdas
## Beta Version !!!
Sakdas is a data profiling and auditing package based on statistical methods.

Its primary goals are to provide self-service data profiling to understand the data via statistical and visualization and data auditing to audit the data via a predefined condition.
## Features
1. Analyze the data profile based on statistical methods and visualization
2. Audit the data by using a predefined condition.
3. Provide audited dataset(CSV) with auditing result tag or without tag, duplicated dataset.
4. Generate data profiling and auditing reports.

## Install
```
pip install sakdas
```
## Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<your data path>/restaurant-and-market-health-inspections.csv")

auditConfig = {'audit':{
    'audit_duplication': True,
    'audit_missing_value': True,
    'define_custom_missing_value': ['.','999'],
    'audit_data_range':[
                {'column_name':'program_element_pe', 'min': 1700, 'max': 1900}
                
            ],
    'audit_data_pattern':[
                {'column_name':'service_description', 'regex_pattern': '(.*)'}
            ],
    'audit_outlier': False,
    'audit_primary_key': True
    }
} 

dataset.audit(auditConfig)
```
