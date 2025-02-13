IIM-Amritsar-Grading-System/
│── grading_conversion.py    # Python script for DCP calculations
│── README.md                # Documentation on academic integrity & grading policies
│── .gitignore               # Git ignore file (optional)
└── LICENSE                  # MIT License (optional)

# grading_conversion.py
class DCPSystem:
    def __init__(self):
        # Mapping of grades to DCP values
        self.dcp_mapping = {
            "F": 6.00,  # Any credit unit results in 6 DCP for an 'F' grade
            "D": {1.25: 5.00, 1.00: 4.00, 0.75: 3.00, 0.50: 2.00, 0.25: 1.00}
        }

    def calculate_dcp(self, grade, credits):
        """
        Calculate the Deficit Credit Points (DCP) based on grade and credit units.
        """
        if grade == "F":
            return 6.00  # Fixed for any course unit
        
        if grade == "D" and credits in self.dcp_mapping["D"]:
            return self.dcp_mapping["D"][credits]

        return 0.00  # No DCP for other grades

# IIM Amritsar: Academic Integrity, Grading, and Deficit Credit Points (DCP) System

## Overview
This repository provides a structured **Grading Conversion System** along with documentation on **IIM Amritsar’s academic integrity policies, grading structure, and the DCP system**.

---

## 📜 Academic Integrity & Examination Conduct
- **Plagiarism and Cheating**: Strictly prohibited; may lead to penalties.
- **Attendance Requirement**: Minimum attendance is mandatory to sit for exams.
- **Examination Rules**: No unauthorized material allowed.
- **Grading Transparency**: Students can request re-evaluation under policy guidelines.

---

## 🎓 Grading System & DCP Calculation
### **Deficit Credit Points (DCP) Table**

| **Grade** | **Credits** | **DCP Earned** |
|----------|------------|---------------|
| **F**    | Any        | **6.00**      |
| **D**    | 1.25       | **5.00**      |
| **D**    | 1.00       | **4.00**      |
| **D**    | 0.75       | **3.00**      |
| **D**    | 0.50       | **2.00**      |
| **D**    | 0.25       | **1.00**      |

python3 grading_conversion.py



