# Bear
Code for the analysis of an ancient bear proteome

Bits of code developed for the analysis of a rich ancient proteome

The notebook `Compile_FASTAs.ipynb` appears to be a script designed to install necessary libraries, mount Google Drive, and fetch and process FASTA files, likely from a database such as UniProt. Below, I will detail the functionalities based on the provided code snippet and overall structure.

### Key Functionalities

1. **Library Installation and Imports**:
   - Installs the Biopython library, which is essential for bioinformatics operations.
   - Imports several libraries including `requests`, `sys`, `pandas`, and `SeqIO` from Biopython.
   - Mounts Google Drive to access and save files within a Google Colab environment.

2. **Google Drive Integration**:
   - Utilises Google Colab's drive mounting feature to access files stored in Google Drive.

3. **Fetching Data from UniProt**:
   - There are references to `requests` and `SeqIO` which indicate the use of web requests to fetch data from UniProt and process it into FASTA format.

4. **Processing and Displaying Data**:
   - Uses `pandas` to handle and display data, making it easier to work with tabular data within the notebook.

### Code Analysis

Below is a breakdown of the extracted code:

```python
# Install the Biopython library
!pip install biopython

# Import necessary libraries
from google.colab import drive
import requests, sys, json, os, time
import pandas as pd
from IPython.display import display
from Bio import SeqIO

# Mount Google Drive
drive.mount('/content/drive')

# Documentation: https://www.uniprot.org/help/api
WEBSI
```

### Detailed Explanation

1. **Library Installation**:
   ```python
   !pip install biopython
   ```
   Installs the Biopython library, which is crucial for parsing and handling biological sequence data.

2. **Library Imports**:
   ```python
   from google.colab import drive
   import requests, sys, json, os, time
   import pandas as pd
   from IPython.display import display
   from Bio import SeqIO
   ```
   - `drive`: Used for mounting Google Drive.
   - `requests`: For making HTTP requests to fetch data from the web.
   - `sys`, `json`, `os`, `time`: Standard libraries for various system operations, JSON handling, OS interactions, and time-related functions.
   - `pandas`: For data manipulation and analysis.
   - `display`: To display data in a readable format within the notebook.
   - `SeqIO`: From Biopython, used for reading and writing sequence file formats.

3. **Mounting Google Drive**:
   ```python
   drive.mount('/content/drive')
   ```
   Mounts the user's Google Drive to the Colab environment to facilitate file operations between local storage and cloud.

### README.md

Here's a proposed `README.md` for the notebook:

---

# Compile_FASTAs

This Jupyter notebook is designed to fetch and compile FASTA files from UniProt, process them, and save the results to Google Drive. The notebook uses Biopython for handling biological sequence data and integrates with Google Drive for file storage.

## Features

- **Library Installation**: Installs Biopython for bioinformatics operations.
- **Google Drive Integration**: Mounts Google Drive to read and write files directly from your Drive.
- **Data Fetching**: Utilises the `requests` library to fetch data from UniProt.
- **Data Processing**: Uses Biopython's `SeqIO` to parse and manipulate sequence data.
- **Data Display**: Employs `pandas` for data manipulation and `IPython.display` for rendering data within the notebook.

## Requirements

- Google Colab
- Google Drive account
- Internet access for fetching data from UniProt

## Usage

1. **Install Required Libraries**:
   The notebook begins by installing the necessary Biopython library.
   ```python
   !pip install biopython
   ```

2. **Mount Google Drive**:
   Ensure your Google Drive is mounted to access files.
   ```python
   from google.colab import drive
   drive.mount('/content/drive')
   ```

3. **Run the Notebook**:
   Execute each cell in the notebook sequentially to install libraries, mount Google Drive, fetch data, and process the FASTA files.

## Notes

- Make sure to provide necessary permissions for Google Drive access.
- The script fetches data from UniProt using web requests. Ensure you have an active internet connection.

---
