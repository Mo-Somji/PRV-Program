# PRV Designer
PRV Designer is a Windows-based Python application for designing pressure relief valves (PRVs) in accordance with the API 520 standard. Built using PyQt5, it integrates with NIST REFPROP to perform accurate thermodynamic calculations and PRV sizing. The tool generates editable Excel datasheets that can be shared with vendors for procurement and documentation.

## Features
* GUI-based tool built with PyQt5
* PRV sizing calculations compliant with API 520 (2014 version)
* Integration with NIST REFPROP for thermodynamic property data if fluid present in NIST database
* Exportable Excel datasheet using openpyxl
* Save-as feature for custom datasheet naming and location

## Requirements
* Windows OS (due to REFPROP DLL dependency)
* Python 3.8+
* NIST REFPROP installed at ```C:/Program Files (x86)/REFPROP```

## Folder Structure
```
PRV Program/
├── Datasheets/
│   ├── Datasheet Template.xlsx    # Excel template used for generating outputs
│   └── Datasheet.xlsx             # Example or previously generated datasheet
├── KSH Values.xlsx                # Standard values obtained from API 520
├── PRV_Designer.py                # Main application script
├── PRV_Designer.ui                # PyQt5 UI layout file
├── Requirements.txt              # Python dependencies
├── .gitignore                    # Git ignored files
├── .gitattributes                # Git attributes for cross-platform compatibility
└── .git/                         # Git repository metadata folder
```

## Installation Instructions
1) Clone this repository:
   ```
   git clone https://github.com/Mo-Somji/PRV-Program.git
   cd PRV-Program
   ```

2) Set up a virtual environment (optional but recommended):
   ```
   python -m venv 'VENV NAME'
   .\'VENV NAME'\Scripts\activate
   ```

3) Install required packages
   ```
   pip install -r Requirements.txt
   ```

4) Make sure REFPROP is installed and accessible at the path defined in the script:
   ```
   os.environ['RPPREFIX'] = r'C:/Program Files (x86)/REFPROP'
   ```

## Usage
1) Run the application:
   ```
   python PRV_Designer.py
   ```

2) Use the GUI to:
   * Input process parameters
   * Perform sizing calculations
   * Save the datasheet using the built-in Save As functionality

## Notes
* This application is Windows-only due to the use of ctREFPROP, which relies on the REFPROP DLL.
* Ensure REFPROP is correctly installed and licensed.
* ```.DS_Store``` and ```xlsx``` are excluded using ```.gitignore```











