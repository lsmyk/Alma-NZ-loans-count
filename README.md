# Alma CF Holdings Sorter

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/lsmyk/Alma-NZ-loans-count/blob/main/sorting_by_numbers_of_OCUL_copies.ipynb)

A Python utility designed to streamline the library weeding and retention process. 

## Purpose
To facilitate a collaborative weeding/retention process, this script helps our library quickly identify if books targeted for weeding are already held by our Consortium/Cooperative Facilities (CF) library partners. 

## How It Works
The script processes an **Alma CF Analytics report** containing CF holdings data and automatically categorizes all titles into two distinct groups based on scarcity:
* **High Retention:** Titles with **3 or more copies** across CF partners.
* **High Scarcity:** Titles with **fewer than 3 copies** across CF partners.

## Prerequisites
This script requires the **`pandas`** library. If you are running this in Google Colab, `pandas` is already pre-installed and ready to use.

## Required Input Format
The script expects a file named **`NZ_report.csv`** exported from Alma Analytics. The file must include the following columns:
* `MMS Id`
* `OCLC Call number (035$a)`
* `Resource Type`
* `Material Type`
* `Network Id`
* `Institution Name`
* `Title`
* `Lifecycle`
* `Linked to CZ`

## How to Run in Google Colab
1. Open a new notebook in [Google Colab](https://google.com).
2. Copy and paste the script code into a code cell.
3. Click the **Files** icon (folder shape) on the left sidebar of Colab.
4. Upload your **`NZ_report.csv`** file directly into that file area.
5. Click the **Play** button on the code cell to execute the script.

## Output Files
After running, the script will generate and save two separate CSV files in your Colab files sidebar for you to download:
1. **`books_with_3plus_copies.csv`** – Titles that are safely backed up by 3 or more partner copies.
2. **`books_with_less_than_3_copies.csv`** – Scarce titles with fewer than 3 partner copies that may require high retention priority.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request if you want to add features (such as customizable copy thresholds, Excel support, or direct Alma API integration).
