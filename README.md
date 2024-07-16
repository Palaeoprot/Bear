# Bear
Code for the analysis of an ancient bear proteome

Bits of code developed for the analysis of a rich ancient proteome
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
