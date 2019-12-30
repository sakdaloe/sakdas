# Acknowledgment
This package is a part of the Master of Science Program in Applied Statistics (Business Analytics and Intelligence: BA&I), National Institute of Development Administration(NIDA), Thailand

## Beta Version !!!
Sakdas is a data profiling and auditing package based on statistical methods.

Its primary goals are to provide self-service data profiling to understand the data via statistical and visualization and data auditing to audit the data via a predefined condition.
## Features
1. Analyze the data profile based on statistical methods and visualization
2. Audit the data by using a predefined condition.
3. Provide audited dataset(CSV) with auditing result tag or without tag, duplicated dataset.
4. Generate data profiling and auditing reports.

## Installation
```
pip install sakdas
```
## Upgrade
```
install sakdas --upgrade
```
## Dataset Methods
|Methods|Return|
|---|---|
|dataset = Dataset(Path to CSV file)|dataset object and profiling report|
|dataset.audit(audit_config)|data profiling and auditing report|
    
## Dataset Attributes
## Attrubutes: dataset.fileName
#### Return type: String
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.fileName)
```
#### Output
```
/.../.../.../appleStore_description.csv
```
## Attrubute: dataset.dataframe
#### Return type: pandas.core.frame.DataFrame
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.dataframe)
```
#### Output
```
--
```
## Attrubute: dataset.duplicatedData
#### Return type: pandas.core.frame.DataFrame
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.duplicatedData)
```
#### Output
```
--
```
## Attrubute: dataset.header
#### Return type: bool
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.header)
```
#### Output
```
True
```
## Attrubute: dataset.schema
#### Return type: list
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.schema)
```
#### Output
```
[{'columnName': 'id', 'dataType': 'int64'}, {'columnName': 'track_name', 'dataType': 'object'}, {'columnName': 'size_bytes', 'dataType': 'int64'}, {'columnName': 'app_desc', 'dataType': 'object'}]
```

## Attrubute: dataset.printSchema
#### Return type: string
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.printSchema)
```
#### Output
```
===Schema===
id: int64
track_name: object
size_bytes: int64
app_desc: object
```

## Attrubute: dataset.profile
#### Return type: dict
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.profile)
```
#### Output
```
{'profile_engine': 'sakdas beta version 0.1.5', 'profile_id': '19774b02-eef0-4b08-b946-610299a98df9', 'file_name': 'appleStore_description.csv', 'profile_datetime': '30/12/2019 16:22:59', 'total_record': 7197, 'total_record_after_deduplication': 7197, 'duplicated_data': '0', 'primary_key': 'id', 'total_column': 4, 'completed_record': '7197', 'completed_record_ratio': '1.0', 'blank_column': '0',....
```
## Attrubute: dataset.printProfile
#### Return type: string
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.duplicatedData)
```
#### Output
```
{
    "profile_engine": "sakdas beta version 0.1.5",
    "profile_id": "2651fe71-7fd1-44fc-b377-72718829f23d",
    "file_name": "appleStore_description.csv",
    "profile_datetime": "30/12/2019 16:32:05",
    "total_record": 7197,
    "total_record_after_deduplication": 7197,
    "duplicated_data": "0",
    "primary_key": "id",
    "total_column": 4,
    "completed_record": "7197",
    "completed_record_ratio": "1.0",
    "blank_column": "0",
    "missing_condition": "null",
    "missing_data": "0",
    "missing_data_ratio": "0.0",
    "schema": [
        {
            "columnName": "id",
            "dataType": "int64"
        },
        {
            "columnName": "track_name",
            "dataType": "object"
        },
        {
            "columnName": "size_bytes",
            "dataType": "int64"
        },
        {
            "columnName": "app_desc",
            "dataType": "object"
        }
    ],
    "column_profile": {
        "id": {
            "dataType": "int64",
            "is_primary_key": "True",
            "distinct_value": "7197",
            "ratio_distinct_value": "1.0",
            "missing_value": "0",
            "ratio_missing_value": "0.0",
            "data_lenght_min": "9",
            "data_lenght_max": "10",
            "min_value": "281656475",
            "max_value": "1188375727",
            "mean": "863130997.45",
            "median": "978148241.0",
            "mode": "281656475",
            "variance": "7.356937774731443e+16",
            "std": "271236755.89",
            "first_quartile": "600093661.0",
            "third_quartile": "1082309664.0",
            "iqr": "482216003.0",
            "minimum": "358985659.5",
            "maximum": "1323417665.5",
            "negative_outliner_datapoint": "0",
            "positive_outliner_datapoint": "342",
            "top_5_data_value": [
                {
                    "data_value": "281656475",
                    "count_data_value": "1",
                    "value_ratio": "0.0001"
                },
                {
                    "data_value": "1058526204",
                    "count_data_value": "1",
                    "value_ratio": "0.0001"
                },
                {
                    "data_value": "1061661355",
                    "count_data_value": "1",
                    "value_ratio": "0.0001"
                },
                {
                    "data_value": "1061610336",
                    "count_data_value": "1",
                    "value_ratio": "0.0001"
                },
                {
                    "data_value": "1061572575",
                    "count_data_value": "1",
                    "value_ratio": "0.0001"
                }
            ],
            "top_5_data_pattern": [
                {
                    "pattern": "XXXXXXXXX",
                    "count_pattern": "3844",
                    "pattern_ratio": "0.5341"
                },
                {
                    "pattern": "XXXXXXXXXX",
                    "count_pattern": "3353",
                    "pattern_ratio": "0.4659"
                }
            ]
        },...
```

## Attrubute: dataset.columnProfile
#### Return type: dict
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.columnProfile)
```
#### Output
```
{'id': {'dataType': 'int64', 'is_primary_key': 'True', 'distinct_value': '7197', 'ratio_distinct_value': '1.0', 'missing_value': '0', 'ratio_missing_value': '0.0', 'data_lenght_min': '9', 'data_lenght_max': '10', 'min_value': '281656475', 'max_value': '1188375727', 'mean': '863130997.45', 'median': '978148241.0', 'mode': '281656475', 'variance': '7.356937774731443e+16', 'std': '271236755.89', 'first_quartile': '600093661.0', 'third_quartile': '1082309664.0', 'iqr': '482216003.0', 'minimum': '358985659.5', 'maximum': '1323417665.5', 'negative_outliner_datapoint': '0', 'positive_outliner_datapoint': '342', 'top_5_data_value': [{'data_value': '281656475', 'count_data_value': '1', 'value_ratio': '0.0001'}, {'data_value': '1058526204', 'count_data_value': '1', 'value_ratio': '0.0001'}, {'data_value': '1061661355', 'count_data_value': '1', 'value_ratio': '0.0001'}, {'data_value': '1061610336', 'count_data_value': '1', 'value_ratio': '0.0001'}, {'data_value': '1061572575', 'count_data_value': '1', 'value_ratio': '0.0001'}], 'top_5_data_pattern': [{'pattern': 'XXXXXXXXX', 'count_pattern': '3844', 'pattern_ratio': '0.5341'}, {'pattern': 'XXXXXXXXXX', 'count_pattern': '3353', 'pattern_ratio': '0.4659'}]},...
```

## Attrubute: dataset.printColumnProfile
#### Return type: string
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.printColumnProfile)
```
#### Output
```
{
    "id": {
        "dataType": "int64",
        "is_primary_key": "True",
        "distinct_value": "7197",
        "ratio_distinct_value": "1.0",
        "missing_value": "0",
        "ratio_missing_value": "0.0",
        "data_lenght_min": "9",
        "data_lenght_max": "10",
        "min_value": "281656475",
        "max_value": "1188375727",
        "mean": "863130997.45",
        "median": "978148241.0",
        "mode": "281656475",
        "variance": "7.356937774731443e+16",
        "std": "271236755.89",
        "first_quartile": "600093661.0",
        "third_quartile": "1082309664.0",
        "iqr": "482216003.0",
        "minimum": "358985659.5",
        "maximum": "1323417665.5",
        "negative_outliner_datapoint": "0",
        "positive_outliner_datapoint": "342",
        "top_5_data_value": [
            {
                "data_value": "281656475",
                "count_data_value": "1",
                "value_ratio": "0.0001"
            },
            {
                "data_value": "1058526204",
                "count_data_value": "1",
                "value_ratio": "0.0001"
            },
            {
                "data_value": "1061661355",
                "count_data_value": "1",
                "value_ratio": "0.0001"
            },
            {
                "data_value": "1061610336",
                "count_data_value": "1",
                "value_ratio": "0.0001"
            },
            {
                "data_value": "1061572575",
                "count_data_value": "1",
                "value_ratio": "0.0001"
            }
        ],
        "top_5_data_pattern": [
            {
                "pattern": "XXXXXXXXX",
                "count_pattern": "3844",
                "pattern_ratio": "0.5341"
            },
            {
                "pattern": "XXXXXXXXXX",
                "count_pattern": "3353",
                "pattern_ratio": "0.4659"
            }
        ]
    },...
```

## Attrubute: dataset.auditConfig
#### Return type: dict
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.auditConfig)
```
#### Output
```
{'audit': {'audit_duplication': False, 'audit_missing_value': False, 'define_custom_missing_value': [], 'audit_data_range': [], 'audit_outlier': False}}
```

## Attrubute: dataset.auditResult
#### Return type: dict
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.auditResuls)
```
#### Output
```
{'audit_result': {'file_name': 'appleStore_description.csv', 'audit_datetime': '30/12/2019 16:32:07'}}
```

## Attrubute: dataset.auditPrintResult
#### Return type: string
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.auditPrintResult)
```
#### Output
```
{
    "audit_result": {
        "file_name": "appleStore_description.csv",
        "audit_datetime": "30/12/2019 16:32:07"
    }
}
```

## Attrubute: dataset.auditedDatasetWithTag
#### Return type: pandas.core.frame.DataFrame
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.auditedDatasetWithTag)
```
#### Output
```
--
```

## Attrubute: dataset.auditedDataset
#### Return type: pandas.core.frame.DataFrame
#### Example
```ruby
from sakdas import Dataset

dataset = Dataset("/<path to csv file>/restaurant-and-market-health-inspections.csv")
print(dataset.auditedDataset)
```
#### Output
```
--
```

 

## Auditing Example
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
    'audit_outlier': False
} 

dataset.audit(auditConfig)
```
