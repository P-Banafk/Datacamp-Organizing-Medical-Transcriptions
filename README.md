# Datacamp-Organizing-Medical-Transcriptions

## Overview

This project uses the OpenAI API to automatically extract structured medical information from unstructured medical transcription records. The extracted information is then matched with the appropriate ICD-10 code to support medical documentation, insurance processing, and healthcare data analysis.

The project demonstrates how Large Language Models (LLMs) can be used to transform free-text clinical notes into structured datasets suitable for downstream healthcare applications.

## Features

* Extracts patient age from medical transcriptions
* Identifies the associated medical specialty
* Extracts recommended treatments from clinical notes
* Maps extracted information to ICD-10 diagnostic codes
* Converts unstructured medical text into a structured pandas DataFrame
* Uses OpenAI GPT models for accurate information extraction

## Dataset

The project uses an anonymized dataset of medical transcriptions.

### Dataset Columns

| Column            | Description                                                       |
| ----------------- | ----------------------------------------------------------------- |
| medical_specialty | Medical specialty associated with the transcription               |
| transcription     | Detailed medical transcription text describing patient encounters |

## Technologies Used

* Python
* Pandas
* OpenAI API
* JSON

## Project Workflow

1. Load medical transcription records from a CSV file.
2. Send each transcription to the OpenAI API.
3. Extract:

   * Patient age
   * Medical specialty
   * Recommended treatment
   * ICD-10 code
4. Parse the model response into structured JSON.
5. Store results in a pandas DataFrame for analysis and reporting.

## Example Output

| age | medical_specialty | recommended_treatment   | icd_code |
| --- | ----------------- | ----------------------- | -------- |
| 45  | Cardiology        | Beta-blocker therapy    | I10      |
| 32  | Dermatology       | Topical corticosteroids | L30.9    |

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/medical-transcription-extraction.git
cd medical-transcription-extraction
```

Install dependencies:

```bash
pip install pandas openai
```

Set your OpenAI API key:

```bash
export OPENAI_API_KEY="your_api_key"
```

For Windows:

```powershell
set OPENAI_API_KEY=your_api_key
```

## Usage

Run the notebook or Python script to process the transcription dataset and generate a structured output DataFrame containing extracted medical information.

## Learning Outcomes

This project demonstrates:

* Information extraction with Large Language Models
* Structured data generation from unstructured text
* Healthcare NLP applications
* ICD-10 code mapping
* OpenAI API integration in Python

## Disclaimer

This project is intended for educational and research purposes only. The extracted information and ICD-10 mappings should not be used for clinical decision-making without professional medical review.
