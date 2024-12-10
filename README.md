# BCTS-conformance-reports

## Overview

Welcome to the BCTS-conformance-reports repository. This page serves as a tool to automate the filtering and generation of the following bi-weekly conformance reports: 
- Annual Development Ready (DR) Conformance Summary
- Annual Developed Volume (ADV) Confromance Summary
- Development In Progress (DIP) Timber Inventory Conformance Summary
- Ready to Develop (RTD) Timber Inventory Conformance Summary
- Ready to Sell (RTS) Timber Inventory Conformance Summary

This repository leverages GitHub Actions CI (Continuous Integration) to automatically execute the scripts in a virtual environment, where Python and all necessary dependencies are pre-installed. This setup eliminates the need for users to install anything on their local machines. To generate the desired reports, simply upload the base report to the data folder. The actions will run automatically, and the generated reports will be available in the artifacts section.

## File Structure

This repository has the following structure:

```bash
project-folder/
├── data/
│   ├── .gitkeep
│   └── input_data.xlsx                        
├── scripts/                
│   ├── ADV_script.py
│   ├── DIP_script.py
│   ├── DR_script.py
│   ├── RTD_script.py
│   └── RTS_script.py
├── requirements.txt 
```

The base report (input data) should be placed in the `data` directory, while the five scripts in the `scripts` folder are responsible for generating the corresponding reports. Each script reads the base report from the `data` folder and processes it to produce its respective output.

## Usage 

**Important**: Please ONLY modify the base report within the data folder when necessary. DO NOT make changes to or delete any other files in any directories. Altering the scripts or the `requirements.txt` file could disrupt the automation process and result in errors.

