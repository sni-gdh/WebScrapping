---

# HuggingFace Vision Models Web Scraper

This project contains a Python script that **scrapes documentation for vision models from the HuggingFace Transformers documentation website** and organizes the extracted information locally in a structured folder format.

The script automatically navigates through the documentation, identifies available vision models, and stores the scraped content for each model in a separate folder.

---

# Project Objective

The goal of this project is to:

1. Start from the **Transformers documentation homepage**
2. Navigate to the **Models section**
3. Identify **Models**
4. Scrape documentation for each model
5. Save the extracted content locally in an organized structure

---

# Features

* Automatically navigates documentation pages
* Extracts model names and URLs dynamically
* Creates a structured folder hierarchy
* Scrapes model documentation content
* Saves documentation into `.txt` files
* Uses lightweight scraping with `requests` and `BeautifulSoup`

---

# Project Structure


Each model gets its own directory containing the scraped documentation.

---

# Technologies Used

* Python
* requests
* BeautifulSoup
* urllib
* os

---

# How the Script Works

### 1. Load Base Documentation Page

The script starts from:

```
https://huggingface.co/docs/transformers/index
```

It downloads the HTML content of the page.

---

### 2. Locate the Models Section

The script parses the page and finds the **Models** section link using HTML anchor tags.

---

### 3. Extract Vision Model Links

Inside the models page, the script searches within the `<main>` section and extracts:

* model names
* model documentation links

These links are stored in a dictionary.

---

### 4. Create Local Folder Structure

A main folder is created:

```
Vision Models
```

For each discovered model, a subfolder is created.

Example:

```
Vision Models/vit
Vision Models/detr
```

---

### 5. Scrape Model Documentation

The script visits each model page and extracts text content from the `<main>` section of the page.

The extracted text is saved in:

```
info.txt
```

inside each model folder.

---

# Example Output

Example console output when running the script:

```
model page: https://huggingface.co/docs/transformers/model_doc/index
Number of models: 10

Scraping: vit
Scraping: detr
Scraping: swin
Scraping: clip
```

---

# Running the Script

Simply run:

```bash
python scraper.py
```

or execute the notebook cells if using the provided Jupyter Notebook.

---

---

# Learning Outcomes

This project demonstrates:

* Practical **web scraping techniques**
* HTML parsing using BeautifulSoup
* Navigating structured documentation websites
* Automating data extraction
* Organizing scraped data programmatically

---
