: Policy-Phi-Fighter Description: Open-source tool to generate structured, evidence-based rebuttals to unfair insurance claim denials. License: CC0 1.0 Universal (Public Domain) — free to use, modify, and distribute.
### GitHub Repo: Policy-Phi-Fighter

**Repo Name:** `Policy-Phi-Fighter`  
**Description:** Open-source tool to generate structured, evidence-based rebuttals to unfair insurance claim denials.  
**License:** CC0 1.0 Universal (Public Domain) — free to use, modify, and distribute.

**Repo URL (example):** `https://github.com/[your-username]/Policy-Phi-Fighter`

#### Repo Structure
```
Policy-Phi-Fighter/
├── README.md                  # Main documentation (below)
├── LICENSE                    # CC0 license text
├── prompts/
│   └── system_prompt.txt      # Core LLM prompt
├── examples/
│   ├── denial_example.txt     # Sample denial letter text
│   └── rebuttal_example.txt   # Generated rebuttal
├── tools/
│   └── pdf_extractor.js       # Simple PDF text extractor (Node.js)
└── CONTRIBUTING.md            # How to add jurisdiction-specific rules
```

#### README.md Content (Copy-Paste Ready)

```markdown
# Policy-Phi Fighter

**A practical, open-source tool to challenge unfair insurance claim denials**

Insurance companies often use high-volume, automated denial processes that rely on claimants giving up due to time and effort required to appeal.

**Policy-Phi Fighter** helps level the playing field by generating clear, professional, evidence-based rebuttals.

### How It Works

1. **Legal Audit**  
   Identifies inconsistencies between the denial reason and the policy wording or applicable law (e.g., UK Insurance Act 2015).

2. **Structured Rebuttal**  
   Produces concise responses citing specific clauses, statutory obligations, and escalation options (Financial Ombudsman Service, bad faith liability).

3. **Evidence Guidance**  
   Suggests documents or information that strengthen the case.

The tool applies the insurer's own rules and obligations systematically — no emotional appeals, just facts and law.

**UK Focus** (easily extensible):  
Leverages Section 13A of the Insurance Act 2015 (reasonable payment timeframe) and the duty of utmost good faith.

### Quick Start

1. Copy the system prompt from `prompts/system_prompt.txt`.
2. Paste into your preferred LLM (ChatGPT, Claude, Grok, local model).
3. Provide the denial letter text (or extracted PDF content).
4. Review and send the generated rebuttal.

### Files

- `prompts/system_prompt.txt` — Core prompt for LLMs
- `examples/` — Sample denial and generated rebuttal
- `tools/pdf_extractor.js` — Basic Node.js script to extract text from denial PDFs
- `CONTRIBUTING.md` — Guide for adding rules from other countries/jurisdictions

### Disclaimer

This tool provides general guidance and templates. It is not legal advice. Always consult a qualified professional for individual cases.

### License

CC0 1.0 Universal — Public Domain. Use, modify, and distribute freely.

### Contribute

- Add jurisdiction-specific legal references
- Improve PDF parsing
- Share successful (anonymised) case outcomes

Goal: Reduce information asymmetry in consumer-insurer disputes.

Feedback welcome.

#Insurance #ConsumerRights #OpenSource #LegalTech
```

#### LICENSE (CC0 Text)
Standard CC0 text — copy from https://creativecommons.org/publicdomain/zero/1.0/legalcode.txt

#### prompts/system_prompt.txt
```
You are Policy-Phi Fighter, an expert system for analysing insurance claim denials and generating professional rebuttals.

Task:
1. Identify inconsistencies between the denial reason and the policy wording or applicable law.
2. Produce a clear, concise rebuttal letter citing specific clauses and statutory obligations.
3. Highlight escalation options (e.g., Financial Ombudsman Service, bad faith liability).
4. Suggest supporting evidence the claimant could provide.

Tone: Professional, factual, unemotional. Use precise legal language.

UK-specific references (where applicable):
- Insurance Act 2015 Section 13A (reasonable time for payment)
- Duty of utmost good faith
- Financial Ombudsman Service jurisdiction

Structure the response as a draft letter ready for the user to customise and send.
```

#### tools/pdf_extractor.js (Basic Node.js)
```javascript
const fs = require('fs');
const pdf = require('pdf-parse');

let dataBuffer = fs.readFileSync('denial.pdf');

pdf(dataBuffer).then(function(data) {
    console.log(data.text);
});
```

(Requires `npm install pdf-parse`)



The balance shifts.

Ready to create it? I can refine any file. 🚀
