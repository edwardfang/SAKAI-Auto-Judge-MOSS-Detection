# SAKAI-Auto-Judge-MOSS-Detection

Some useful scripts for SAKAI code extraction and plagiarism detection

## Installation

Install all extracting support packages.

### Ubuntu/Debain

```bash
sudo apt-get update
sudo apt-get install p7zip-full rar
```

## Usage

```bash
# Eaxmple
./extract.py bulk_download.zip
./moss.sh -l java -m 20 -d $(find ./judge -type f \( -iname "*.java" ! -iname "._*" \) )
# Another formation of find
find . -type f -not -path "*/\.*" -name "*.java"
```

Also, for the usage of the `MOSS` Please refer to the web site of MIT `MOSS` or the content of `moss.sh`.

Useful Option for `moss.sh`: 

-n 600

where `600` is number of matching files to show in the results.


## TODO

 - [ ] Integrate with [mosspy](https://github.com/soachishti/moss.py)
 - [ ] Auto ditinguish different language
 - [ ] Move one students' code into the root of the same directory
 - [x] Remove code/report records from OJ when there exists code from SAKAI
 - [x] Generate table from the HTML result
