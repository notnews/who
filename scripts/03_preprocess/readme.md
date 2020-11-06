## Preprocess Search List

### Installation

```
pip install -r requirements.txt
```

### Configuration file

There are three sections in the configuration file [`preprocess.cfg`](preprocess.cfg)

1) search

 This section contains patterns ---combination of field names---we want to search for:

```
    [search]
    pattern1 = FirstName LastName
    pattern2 = NickName LastName
    pattern3 = Prefix LastName
```

2) drop

 The `file` variable points to the file containing list of people to be dropped. Usually, this file is an ad hoc list of patterns that we want removed. For instance, patterns matching famous people not on the list.

```
    [drop]
    file = drop_patterns.txt
```

3) editlength

 This section contains minimum name length for the specific edit distance.

```
    [editlength]
    edit1 = 10
    edit2 = 20
```

### Usage

```
usage: preprocess.py [-h] [-o OUTFILE] [-c CONFIG] input

Preprocess Search List

positional arguments:
  input                 Input file name

optional arguments:
  -h, --help            show this help message and exit
  -o OUTFILE, --out OUTFILE
                        Output file in CSV (default:
                        deduped_augmented_clean_names.csv)
  -c CONFIG, --config CONFIG
                        Default configuration file (default: preprocess.cfg)
```

### Example

```
python preprocess.py  augmented_clean_names.csv
```

By default the output will be saved as `deduped_augmented_clean_names.csv`
Script adds a new column, `search_name` for unique search key.
