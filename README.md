# TraumaCB

## Overview

**TraumaCB** is a cutting-edge AI-powered diagnostic tool designed to enhance trauma radiology workflows by integrating advanced Retrieval-Augmented Generation (RAG) with OpenAI's GPT-4 Turbo. Developed as part of a proof-of-concept study, TraumaCB aims to improve the accuracy, transparency, and efficiency of diagnosing, classifying, and grading traumatic injuries from radiological findings.

The system significantly outperforms generic chatbots, achieving high accuracy in classification and grading while providing detailed explanations with references to scientific literature, fostering trust and accountability.

## Key Features

- **Enhanced Diagnostic Accuracy**: Achieved high accuracy for correct diagnosis, correct classification, and correct grading.
- **Transparency**: Provides references and explanations for each decision, enabling easy verification and fostering trust.
- **Two-Step Workflow Integration**: Mimics clinical workflows as a Chain-of-thought approach, offering primary diagnoses, classification, and grading with concise and targeted explanations.
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

### Usage

1. **Data Preparation**: Input radiology case descriptions directly into the Jupyter Notebook cell.

2. **Run the Diagnostic Tool**:
   Use the provided Jupyter Notebook or script to load cases, generate predictions, and output results in a structured format.

3. **Analyze Results**: Generated outputs include:
   - Primary diagnosis
   - Classification system
   - Grading with explanations
   - Referenced scientific literature

### Example Workflow

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

## Research and Development

This project is based on the original research article:

> *Will be inserted on publication*

The study highlights the potential of combining RAG with GPT-4 Turbo to address challenges in trauma radiology.

## Contributing

This repository is fixed as Code for paper. For further collaboration, contact us directly.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## Contact

For further information, visit our research group:
[University Hospital Freiburg Radiology Research](https://www.uniklinik-freiburg.de/radiologie/forschung/ag.html)

## Acknowledgments

- The TraumaCB team
- Contributors to the RadioGraphics Top 10 Reading List for Trauma Radiology
- OpenAI for providing the GPT-4 Turbo platform
