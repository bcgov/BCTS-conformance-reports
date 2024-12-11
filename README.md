[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

# BCTS-conformance-reports

## Overview

Welcome to the BCTS-conformance-reports repository. This page serves as a tool to automate the filtering and generation of the following bi-weekly conformance reports: 
- Annual Development Ready (**DR**) Conformance Summary
- Annual Developed Volume (**ADV**) Confromance Summary
- Development In Progress (**DIP**) Timber Inventory Conformance Summary
- Ready to Develop (**RTD**) Timber Inventory Conformance Summary
- Ready to Sell (**RTS**) Timber Inventory Conformance Summary

This repository leverages GitHub Actions CI (Continuous Integration) to automatically execute the scripts in a virtual environment, where Python and all necessary dependencies are pre-installed. This setup eliminates the need for users to install anything on their local machines. To generate the desired reports, simply upload the base report to the data folder. The actions will run automatically, and the generated reports will be available in the artifacts section.

## File Structure

This repository has the following structure:

```bash
project-folder/
├── data/
│   ├── .gitkeep
│   └── QA_DR_DIP_RTS_HICurrentFiscal-Or-Planned_with_CFSSvrLine_YYYY_MM_DD.xlsxxlsx                        
├── scripts/                
│   ├── ADV_script.py
│   ├── DIP_script.py
│   ├── DR_script.py
│   ├── RTD_script.py
│   └── RTS_script.py
├── requirements.txt 
```

The base report (`QA_DR_DIP_RTS_HICurrentFiscal-Or-Planned_with_CFSSvrLine_YYYY_MM_DD.`) should be placed in the `data` directory, while the five scripts in the `scripts` folder are responsible for generating the corresponding reports. Each script reads the base report from the `data` folder and processes it to produce its respective output.

## Usage 

**Important**: Please ONLY modify the base report within the data folder when necessary. DO NOT make changes to or delete any other files in any directories. Altering the scripts or the `requirements.txt` file could disrupt the automation process and result in errors.

### 1. Have your base report ready 
- Prepare the base report you want to use on your local machine. Ensure that the report follows the exact naming format: `QA_DR_DIP_RTS_HICurrentFiscal-Or-Planned_with_CFSSvrLine_YYYY_MM_DD.` where `YYYY_MM_DD` should be replaced with the report date. 

### 2. Replace with the old base report with the new one you hope to use
- Enter the `data` directory: 
![](img/data_folder.png)

- Click on the old base report file that's currently in the directory:
![](img/old_base_report.png)

- Click on the three dots on the top right and select "Delete file"
![](img/three_dots.png)

- Click on the "Commit changes" on the top right
![](img/commit_deletion.png)