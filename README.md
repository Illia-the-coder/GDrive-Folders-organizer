# GDrive-Folders-organizer
# File Organization in Google Drive

This Jupyter notebook helps organize files in a Google Drive directory based on their file extensions. Files will be sorted into predefined categories depending on their types (documents, multimedia files, code files, etc.).

## Requirements
This script uses Google Colab and requires the following libraries:
- `os` (built-in)
- `shutil` (built-in)
- `tqdm`

To install `tqdm`, run the following command:

```python
!pip install tqdm 
```

## Instructions

### Step 1: Mount Google Drive folder to Google Colab

Before starting file organization, mount your Google Drive folder to Google Colab by running the following code:

```python
from google.colab import drive
drive.mount('/content/drive')
```

### Step 2: Install `tqdm` library

We will use the `tqdm` library to display a progress bar during file iteration. Install and import the necessary libraries using this code:

```python
!pip install tqdm
import os
import shutil
from tqdm import tqdm
```

### Step 3: Get Unique File Extensions

The `get_unique_file_extensions` function walks through the directory structure of a given source folder and identifies unique file extensions.

```python
def get_unique_file_extensions(src_folder):
    # code block here
```

Run this function and print unique file extensions found in your Google Drive folder:

```python
source_folder = "/content/drive/MyDrive"
unique_extensions = get_unique_file_extensions(source_folder)
print(unique_extensions)
```

### Step 4: File Categories

Define a dictionary mapping file extensions to categories. This will serve as the guide for the categorization process.

```python
file_categories = {
    # list of categories here
}
```

### Step 5: Categorize Files

The `categorize_files` function goes through the directory structure, moving files into the appropriate category folders based on their extensions.

```python
def categorize_files(src_folder, file_categories=file_categories, go_through=True):
    # code block here
```

### Step 6: Implement File Sorting

Finally, run the `categorize_files` function to sort all files in your Google Drive:

```python
source_folder = "/content/drive/MyDrive"
categorize_files(source_folder)
```

This will sort files into category-specific directories within the source folder. Please note that any files with extensions not defined in the `file_categories` dictionary will be moved to an 'Others' directory. 

## Caution
Please backup your data before running this script, as moving files could result in data loss if not handled properly. We are not responsible for any data loss that may occur.

## Contributions
Suggestions and improvements are welcome. Feel free to submit a pull request.
