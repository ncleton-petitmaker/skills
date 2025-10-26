# Skills Collection

Professional skills for Claude AI, organized by category. Each skill provides specialized capabilities that Claude can load dynamically to perform domain-specific tasks.

## What are Skills?

Skills are folders of instructions, scripts, and resources that Claude loads dynamically to perform specialized tasks. They enable Claude to handle complex, domain-specific workflows with expert-level knowledge.

## Available Skills

### Finance & Accounting

#### French Invoice Analyzer
Automated French invoice processing for Pennylane accounting software.

**Capabilities:**
- OCR extraction from PDF/JPG/PNG invoices
- Automatic classification using French Chart of Accounts (Plan Comptable Général)
- Intelligent file renaming with standardized format
- Excel export ready for Pennylane import
- 85% time savings on accounting data entry

**Use cases:**
- Accounting firms processing client invoices
- SMEs simplifying accounting workflows
- Freelancers managing their own bookkeeping

**Tech stack:** Python, pdfplumber, pytesseract, openpyxl

📁 [View skill details →](./finance/french-invoice-analyzer/)

## Repository Structure

```
/
├── README.md                    # This file
├── finance/                     # Finance & accounting skills
│   └── french-invoice-analyzer/ # Invoice processing for Pennylane
└── .gitignore                   # Git ignore rules
```

## Installation & Usage

### Option 1: Claude.ai (Web Interface)

1. Download the `.skill` file from the skill folder
2. Go to [Claude.ai](https://claude.ai)
3. Navigate to Settings > Skills
4. Click "Upload Skill"
5. Select the `.skill` file
6. Activate the skill in your project or conversation

### Option 2: Claude Code (CLI)

Skills are automatically loaded when present in your project directory:

```bash
# Clone this repository
git clone https://github.com/ncleton-petitmaker/skills.git

# Navigate to a skill folder
cd skills/finance/french-invoice-analyzer

# Use with Claude Code
claude "Process all invoices in ./invoices folder"
```

### Option 3: Direct Script Usage

Each skill contains standalone Python scripts that can be used directly:

```bash
# Extract and run scripts locally
cd finance/french-invoice-analyzer
unzip french-invoice-analyzer.skill -d extracted
cd extracted
python scripts/process_invoices.py ./your_invoices
```

## Creating Your Own Skills

Want to add your own skill to this collection?

1. Create a category folder (e.g., `marketing/`, `development/`)
2. Add your skill folder with a descriptive name
3. Include:
   - `SKILL.md` - Main skill documentation
   - `.skill` file - Packaged skill for Claude.ai
   - Supporting scripts, references, and assets
   - Usage documentation

Structure:
```
category-name/
└── skill-name/
    ├── skill-name.skill      # Packaged skill
    ├── SKILL.md              # Skill documentation
    ├── GUIDE.md              # Usage guide
    ├── scripts/              # Python/shell scripts
    ├── references/           # Reference documentation
    └── assets/               # Templates, examples
```

## Skills Roadmap

Future skills planned for this repository:

- **Finance:** Financial statement analysis, expense categorization
- **Marketing:** Content calendar generation, SEO optimization
- **Operations:** Process documentation, workflow automation
- **Data:** CSV transformation, API integration helpers

## Contributing

Contributions are welcome! If you've created a skill that could benefit others:

1. Fork this repository
2. Add your skill following the structure above
3. Update this README with your skill description
4. Submit a pull request

## License

This repository and its skills are provided as-is for educational and professional use.

Individual skills may have their own licenses - check each skill folder for details.

## Support

- 📖 Documentation: Check each skill's folder for detailed guides
- 🐛 Issues: [Report issues on GitHub](https://github.com/ncleton-petitmaker/skills/issues)
- 💡 Suggestions: Open a discussion or pull request

---

**Built with Claude AI** | [Learn more about Claude Skills](https://docs.anthropic.com/)
