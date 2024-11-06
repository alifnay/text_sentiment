<h1 align="center">Sentiment Analysis using Caikit and Hugging Face</h1>
<p align="center">Berisi tentang model sentiment analisis yang dibuat menggunakan Caikit dan Hugging Face</p>

<div align="center">
    <img src="https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54">
    <img src="https://img.shields.io/badge/SciPy-%230C55A5.svg?style=for-the-badge&logo=scipy&logoColor=%white">
    <img src="https://img.shields.io/badge/PyTorch-%23EE4C2C.svg?style=for-the-badge&logo=PyTorch&logoColor=white">
</div>

## Overview

The Text Sentiment Analysis project is designed to analyze and categorize the sentiment of text inputs as positive, negative, or neutral. This tool leverages machine learning and natural language processing to understand emotional undertones within text data, making it useful for applications like customer feedback analysis, social media monitoring, and more.

For example, given the input *"I don't love you, like I did yesterday."* the sentiment analysis detects a **negative** sentiment. In contrast, with the input *"You are so beautiful today"* the sentiment is identified as **positive**.

## Model Components

1. **Data Model**: The `data_model` module handles data preprocessing, transforming raw text into a format suitable for model ingestion. This module cleans, tokenizes, and prepares data, improving model accuracy by ensuring consistency in input formatting.

2. **Runtime Model**: The `runtime_model` module integrates with the Hugging Face library and leverages pre-trained language models fine-tuned for sentiment analysis. This component is responsible for predicting sentiment labels based on input text.

3. **Configuration Management**: Through the configuration files (`config.yml`), users can specify model parameters, data paths, and various runtime settings. This flexibility allows easy tuning of the model to suit specific sentiment analysis tasks or datasets.

## Prerequisites

To run this project, ensure the following are installed:

- **Linux/MacOS x86_64** - Skills Network Lab environment is compatible.
- **Caikit (v0.9.2)** - Installed as part of project setup.
- **Python (v3.8+)** - Python 3.8 is pre-installed in the Skills Network Lab environment.
- **pip (v23.0+)** - We will upgrade pip to the latest version in the project setup.

## Getting Started

**1. Clone the Repository**

First, clone this repository to your local machine and navigate into the project directory:
```bash
git clone https://github.com/alifnay/text_sentiment
cd text-sentiment
```

**2. Upgrade pip**

Ensure pip is upgraded to the latest version. This is necessary to install all required packages:
```bash
python3 -m pip install --upgrade pip
```

**3. Install Dependencies**

Install the required libraries listed in requirements.txt. This will include Caikit (v0.9.2) and any other necessary packages:
```bash
pip install -r requirements.txt
```

**4. Start the Runtime**

To initialize the runtime environment, run the start_runtime.py script. This script sets up and prepares the environment for text sentiment analysis:
```bash
python start_runtime.py
```

**5. Run the Client**

Use client.py to interact with the text sentiment model. This script allows you to input text data and get sentiment predictions:
```bash
python client.py
```

## Project Structure

The repository is organized as follows:

```plaintext
text-sentiment/
├── start_runtime.py               # Script to initialize the runtime environment
├── client.py                      # Client script for interacting with the sentiment model
├── requirements.txt               # Lists dependencies for the project
├── models/                        
│   └── text_sentiment/
│       └── config.yml             # Configuration file for model settings
└── text_sentiment/                
    ├── config.yml                 # Main configuration file
    ├── __init__.py                # Package initialization
    ├── data_model/                # Data model submodule
    │   ├── classification.py      # Classification logic
    │   └── __init__.py            
    └── runtime_model/             # Runtime model submodule
        ├── hf_module.py           # Hugging Face model integration
        └── __init__.py
```
