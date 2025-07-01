## camed_results

The `camed_results` project provides a Python-based solution to quantitatively compare the CAMED and NoCEP approaches. It automates the extraction and calculation of various performance indicators from raw experimental data stored in CSV files. This includes resource utilization metrics (CPU and Memory usage) and classification performance metrics (F1-score, accuracy, specificity, false positives, precision, recall). The processed results are then used to generate informative plots and text-based summaries, facilitating a clear understanding of each approach's efficiency and effectiveness.

## Project structure

```
camed/
├── CAMED/:                           # CSV result files
│   └── i.cpu_overall.csv
│   └── i.memory_data.csv
│   └── i.model_output.csv
├──NoCEP/:                            # CSV result files
│   └── i.cpu_overall.csv
│   └── i.memory_data.csv
│   └── i.model_output.csv
├── process_result.ipynb              # Process the CSV Data
├── requirements.txt                  # Required python 
├── README.md                         # This file
```

## Installation and Setup
To set up and run this project, follow these steps:


1. <b>Clone the Repository (if applicable)</b>:

    ```
    git clone <repository_url>
    cd camed_results
    ```

2. <b>Create a Virtual Environment</b>: It is highly recommended to use a virtual environment to manage project dependencies.

    `python3 -m venv venv`

3.  <b>Activate the Virtual Environment</b>:

    * On Linux/macOS: `bash source venv/bin/activate`
    * On Windows: `bash .\venv\Scripts\activate`

4.  <b>Install Required Dependencies</b>: Navigate to the project root directory (where `process_results.py` and `requirements.txt` are located) and install the necessary Python packages using pip.

    `bash pip install -r requirements.txt`

    [!NOTE]  
    (Note: If you don't have a requirements.txt file, you will need to create one with the following content:)
    pandas scikit-learn matplotlib

5.  Install Jupyter Lab: If you don't have Jupyter Lab installed globally or within your virtual environment, install it:
    `bash pip install jupyterlab`

## How to Use

1. <b>Ensure Data is in Place</b>: Make sure your experimental result folders (CAMED and NoCEP) are correctly structured as described in the Data Structure section.

2. <b>Start Jupyter Lab</b>: Activate your virtual environment (if not already active) and launch Jupyter Lab from the project's root directory:

    `jupyter lab`

3. Open and Execute Notebook: In the Jupyter Lab interface, open the process_results.py notebook. Execute all cells within the notebook in sequential order.

## Output

Upon successful execution of all cells in `process_results.py`, the project will generate:

- <b>Text Results</b>: Printed statistical summaries (mean values) of all calculated metrics for both CAMED and NoCEP approaches, along with their comparative differences, displayed directly in the Jupyter Lab output cells.
- <b>Figures</b>: Image files representing the plots, typically saved as .png files (e.g., resources.png for CPU/Memory, metrics.png for F1-Score/Specificity/False Positives) in the project's root directory.


## License
This project is open-source. It is released under a license that grants all permissions commonly associated with open-source software, similar to the permissive nature of licenses often used with Linux distributions. You are free to use, modify, and distribute this code.
