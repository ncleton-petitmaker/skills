# French Invoice Analyzer

Professional automated invoice processing skill for French accounting with Pennylane integration.

## Overview

This skill automates the complete workflow of processing French invoices for accounting purposes, saving up to 85% of manual data entry time.

## Features

### Intelligent Extraction
- Multi-format OCR (PDF, JPG, PNG)
- French language recognition (Tesseract)
- Automatic extraction of:
  - Supplier name
  - Invoice number
  - Date
  - Amounts (HT, TVA, TTC)
  - SIRET number
  - VAT details

### Automatic Classification
- French Chart of Accounts (Plan Comptable Général)
- 30+ classification rules
- Expense accounts (Class 6)
- Customizable rules

### Intelligent File Naming
- Standardized format: `YYYYMMDD_Supplier_Amount_InvoiceNumber.pdf`
- Automatic chronological sorting
- Optimized organization

### Pennylane Export
- Excel format compliant with Pennylane
- 3 accounting entries per invoice (expense, VAT, payable)
- Balanced entries
- Ready for direct import

## Files Included

### Main Skill File
- `french-invoice-analyzer.skill` (27 KB) - Complete packaged skill for Claude.ai

### Documentation
- `README.md` - This file
- `GUIDE_UTILISATION.md` - Complete installation and usage guide
- `RECAPITULATIF.md` - Skill overview and summary

### Reference Materials
- `Plan-de-comptes-pcg-2025.pdf` - French Chart of Accounts 2025

### Embedded Resources (inside .skill file)
- Python scripts (3 files)
- Accounting references (3 files)
- Excel template (1 file)
- Complete skill documentation

## Quick Start

### Installation

**Option 1: Claude.ai**
1. Upload `french-invoice-analyzer.skill` to Claude.ai
2. Activate in your project
3. Ask Claude: "Process invoices in this folder for Pennylane"

**Option 2: Local Scripts**
```bash
# Extract skill
unzip french-invoice-analyzer.skill

# Install dependencies
pip install pdfplumber pytesseract pillow openpyxl pdf2image

# Run processing
python scripts/process_invoices.py ./invoices
```

## Usage Examples

### With Claude.ai
```
"Analyze all invoices in ./invoices and prepare Pennylane import"
```

### Direct Script Usage
```bash
# Complete workflow
python scripts/process_invoices.py ./my_invoices

# Step by step
python scripts/analyze_invoices.py ./my_invoices
python scripts/generate_pennylane_import.py ./analyzed/invoices_data.json
```

## Output Files

- `pennylane_import.xlsx` - Ready to import into Pennylane
- `invoices_data.json` - All extracted data
- `summary_report.txt` - Processing summary
- `renamed_invoices/` - Renamed and organized invoices

## Automatic Classification Examples

| Supplier Type | Account | Label |
|--------------|---------|-------|
| EDF, Engie | 6061 | Energy |
| Orange, SFR, Free | 6262 | Telecommunications |
| Accountant, Lawyer | 6226 | Professional fees |
| Restaurants | 6257 | Meals & entertainment |
| Hotels | 6251 | Travel & accommodation |
| SaaS software | 651 | Software licenses |
| Google Ads, Facebook | 6231 | Advertising |
| Shipping companies | 6242 | Transport |
| Insurance | 6161 | Multi-risk insurance |
| **Unrecognized** | **6288** | **Other expenses** |

30+ automatic classifications included!

## ROI (Return on Investment)

### Before
- 7 minutes per invoice (manual entry)
- 50 invoices = 6 hours
- Repetitive and error-prone

### After
- 40 seconds per invoice (with verification)
- 50 invoices = 35 minutes
- Fully automated

**Result: 85% time saved - 5h30 saved for 50 invoices**

## Technical Details

### Technologies
- Python 3
- pdfplumber - Native PDF extraction
- pytesseract - OCR recognition
- Pillow - Image processing
- openpyxl - Excel generation
- French Chart of Accounts
- Pennylane format specifications

### Dependencies
```bash
pip install pdfplumber pytesseract pillow pdf2image openpyxl
apt-get install tesseract-ocr tesseract-ocr-fra poppler-utils
```

## Use Cases

### For Accounting Firms
- Monthly client invoice processing
- Pennylane import preparation
- Organized document archiving

### For SMEs
- Simplified accounting data entry
- Reduced classification errors
- Time savings on administrative tasks

### For Freelancers
- Autonomous bookkeeping management
- Preparation for accountant
- Document organization

## Future Enhancements

Possible extensions:
- Direct Pennylane API integration
- Analytics dashboards
- Machine learning classification
- Automatic email processing
- Duplicate detection
- Custom expense reports

## Support

- 📖 Complete guide: See `GUIDE_UTILISATION.md`
- 📋 Summary: See `RECAPITULATIF.md`
- 🔧 Customization: Modify Python scripts inside .skill file
- 💡 Questions: Open an issue on GitHub

## Version

- Version: 1.0.0
- Created: October 2025
- Format: .skill (Claude.ai compatible)

## License

Provided as-is for professional and educational use.

---

**Transform your accounting workflow today!**
