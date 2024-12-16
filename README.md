# TraumaCB

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## Overview

**TraumaCB** is a cutting-edge AI-powered diagnostic tool designed to enhance trauma radiology workflows by integrating advanced Retrieval-Augmented Generation (RAG) with OpenAI's GPT-4 Turbo. Developed as part of a proof-of-concept study, TraumaCB aims to improve the accuracy, transparency, and efficiency of diagnosing, classifying, and grading traumatic injuries from radiological findings.

The system significantly outperforms generic chatbots, achieving high accuracy in classification and grading while providing detailed explanations with references to scientific literature, fostering trust and accountability.

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [Example Workflow](#example-workflow)
- [Repository Structure](#repository-structure)
- [How It Works](#how-it-works)
- [Technical Implementation](#technical-implementation)
- [Performance](#performance)
- [Research and Development](#research-and-development)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgments](#acknowledgments)
- [Contact](#contact)

## Key Features

- **Enhanced Diagnostic Accuracy**: Achieved high accuracy for correct diagnosis, correct classification, and correct grading.
- **Transparency**: Provides references and explanations for each decision, enabling easy verification and fostering trust.
- **Two-Step Workflow Integration**: Mimics clinical workflows as a chain-of-thought process, offering primary diagnoses, classification, and grading with concise and targeted explanations.
- **Custom Knowledge Integration**: Leverages curated datasets, such as the RadioGraphics Top 10 Reading List, but can be extended with further PDFs for task-specific contextual understanding.
- **Flexibility**: Capable of adapting to new scientific resources and customizable for various clinical settings.

## Getting Started

### Prerequisites

- Python 3.10 or later
- OpenAI API Key
- Required Python Libraries: `pandas`, `pypdf`, `openai`, `llama_index`, and others listed in the code.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/maxrusse/TraumaCB.git
   cd TraumaCB
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Configure your OpenAI API key:
   Obtain your API key from [OpenAI's platform](https://platform.openai.com/signup/) and set it as an environment variable:
   ```bash
   export OPENAI_API_KEY='your-api-key'
   ```

## Usage
**Run TraumaCB**:
   Use the provided Jupyter Notebook or script to create a vector store, run single case analysis, generate predictions, and output results in a structured format.

1. **Data Preparation**: Create data folder.
2. **Run Prediction**: Input radiology case descriptions directly into the Jupyter Notebook cell.
3. **Analyze Results**: Generated outputs include:
   - Primary diagnosis
   - Classification system
   - Grading with explanations
   - Referenced scientific literature

## Example Workflow

- Input:
  ```plaintext
  Case/Report: Description of findings of a X-RAY, CT/MR-Scan
  ```
- Output:
  ```plaintext
  - Diagnosis: 
  - Classification: 
  - Explanation: 
  - References: 
  ```

## Repository Structure

- `TraumaCB-notebook`: Jupyter notebooks for reproducing paper results

## How It Works

- **Knowledge Database**: Builds a searchable knowledge base from curated datasets (e.g., RadioGraphics).
- **Vector Store**: Uses Llama Index to convert knowledge into dense vectors for efficient retrieval.
- **Retrieval-Augmented Generation (RAG)**: Fetches relevant content based on semantic similarity to the user query.
- **-4 Turbo Integration**: Generates answers using pre-trained models with task-specific prompts.
- **Two-Step Workflow**: Implements a two-step workflow mimicking clinical processes:
  1. **Primary Diagnosis**: Based on radiological findings, the system provides an initial diagnosis.
  2. **Classification and Grading**: After receiving the initial diagnosis, the system retrieves additional context to assign a classification system and grading, accompanied by concise yet comprehensive explanations.
- **Transparent Outputs**: Provides detailed source references for verification.

## Technical Implementation

- **Embedding Model**: Leverages `text-embedding-ada-002` for high-quality vector representation.
- **Semantic Search**: Retrieves relevant data using cosine similarity.
- **Custom Prompts**: Ensures contextual accuracy with domain-specific -4 Turbo templates.
- **Source Metadata**: Tracks filenames and pages for verification.

## Performance

- Outperformed generic -4 Turbo in trauma diagnosis, classification, and grading.
- Demonstrated higher trust ratings from expert reviewers for its detailed explanations and source transparency.

## Research and Development

This project is based on the original research article:

> *Will be inserted on publication*

The study highlights the potential of combining RAG with -4 Turbo to address challenges in trauma radiology.

## Contributing

This repository is fixed as Code for paper. For further collaboration, contact us directly.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Acknowledgments

- The TraumaCB team
- Contributors to the RadioGraphics Top 10 Reading List for Trauma Radiology
- OpenAI for providing the -4 Turbo platform
- Llama Index Team for their framework

## Contact

For further information, visit our research group:
[University Hospital Freiburg Radiology Research](https://www.uniklinik-freiburg.de/radiologie/forschung/ag.html)

[LinkedIn Profile]([https://www.linkedin.com/in/maximilian-russe-3a83a42a6](https://www.linkedin.com/in/maximilian-russe-3a83a42a6))
[maxrusse](https://github.com/maxrusse)
