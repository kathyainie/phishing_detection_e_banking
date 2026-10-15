# Detecting Phishing in E-Banking Websites

## Overview

Phishing websites imitate legitimate banking or financial websites to trick people into sharing sensitive information such as usernames, passwords, card details, or bank account information. This project explores a phishing-detection approach for e-banking websites using **associative classification and data-mining techniques**.

The proposed workflow takes a URL as input, extracts relevant features, preprocesses those features, applies classification, and presents a result indicating whether the URL is potentially phishing or legitimate.

> **Project status:** The accompanying presentation describes the project proposal, design, requirements, testing scenarios, and interface snapshots. The screenshots below are taken from that presentation and are illustrative of the shown interface; they do not independently verify that every feature or model is implemented or production-ready.

## Objectives

- Identify potentially phishing e-banking URLs.
- Extract useful URL, website-content, and security-related features.
- Explore association-rule mining, including the FP-Growth algorithm, for finding patterns in phishing data.
- Classify URLs as phishing or legitimate.
- Evaluate detection using metrics such as accuracy, precision, recall, and F1-score.
- Support a user-facing interface and, as described in the presentation, explore browser-extension-based detection.

## Proposed Workflow

1. **Data collection** – Gather labelled examples of phishing and legitimate websites.
2. **Preprocessing** – Clean, encode, and prepare the data for analysis.
3. **Feature extraction** – Examine indicators such as URL length, special characters, subdomains, IP-based domains, HTTPS/SSL status, redirects, HTML elements, and domain information.
4. **Pattern discovery and classification** – Use association-rule mining (FP-Growth is named in the presentation) and classification methods to identify suspicious patterns.
5. **Evaluation** – Measure model performance with suitable test data and evaluation metrics.
6. **Detection output** – Display a phishing/legitimate prediction to the user.

The presentation also discusses machine-learning classification, behavioral analysis, and model options. These are design concepts from the presentation, not a claim that all listed algorithms are integrated in one final implementation.

## Interface Screenshots

The following screenshots are extracted from the project presentation.

### Dashboard
![Dashboard](assets/dashboard.png)

### Search and Analyze
![Search and Analyze](assets/search-and-analyze.png)

### Analysis Results
![Analysis Results](assets/analysis-results.png)

### Detection Details
![Detection Details](assets/detection-details.png)

### Analysis History
![Analysis History](assets/analysis-history.png)

### URL Analysis Score
![URL Analysis Score](assets/url-analysis-score.png)

### URL Information
![URL Information](assets/url-information.png)

### Security Analysis
![Security Analysis](assets/security-analysis.png)

### Browser Extension
![Browser Extension](assets/browser-extension.png)

## Functional Requirements Described

- Accept a URL as input.
- Extract URL, domain, HTML, JavaScript, and other relevant features.
- Classify a URL as phishing or legitimate.
- Display the classification result.
- Keep a history/log of analyzed URLs and outcomes.
- Allow an administrator to upload datasets and view reports.
- Support batch detection from uploaded datasets.

## Requirements Mentioned in the Presentation

### Hardware
- Intel i5 (8th generation) or equivalent processor
- 8 GB RAM
- 256 GB SSD
- Optional NVIDIA GTX 1050 GPU for machine-learning training
- Internet connection (1 Mbps or higher)

### Software and Tools
- Windows 10/11, Ubuntu 20.04+, or macOS
- Python 3.8+
- Python libraries listed in the presentation: scikit-learn, pandas, NumPy, Matplotlib, Seaborn, and FP-Growth tooling
- Potential web stack: HTML, CSS, JavaScript, React.js, Flask/Django, and MySQL/MongoDB
- Jupyter Notebook

These are the requirements and candidate tools stated in the presentation; the exact stack used by a final implementation should be documented once confirmed.

## Example Test Scenarios

The presentation proposes testing cases including:

- A normal HTTPS banking URL.
- An HTTP URL instead of HTTPS.
- Lookalike domains (for example, a domain using `1` in place of `l`).
- Suspicious subdomains and verification-related keywords.
- URLs that use an IP address rather than a domain.
- Punycode/homoglyph domains.
- Shortened URLs.
- URLs that place a bank name before an unrelated real domain.



## Future Enhancements

The presentation suggests exploring stronger authentication, user-awareness efforts, multilingual support, secure email practices (DMARC, SPF, and DKIM), and other identity-verification approaches.


4. A. Arshad, A. Ur Rehman, S. Javaid, and T. M. Al, “A Systematic Literature Review on Phishing and Anti-Phishing Techniques,” 2021.

---

*Academic project presentation prepared by the Department of Information Science and Engineering, Sai Vidya Institute of Technology.*
