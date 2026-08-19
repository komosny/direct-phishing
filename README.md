# Extracting Direct Data-Harvesting Phishing from the PhishTank Baseline for Reliable Datasets, Benchmarks, and Detection

Research paper under review

## Data and source code

- [result-ground-truth](result-ground-truth) – processed direct data-harvesting phishing ground truth derived from PhishTank

- [direct-phishing.ipynb](direct-phishing.ipynb) – Jupyter notebook containing the source code

- [dataset-original](dataset-original) – original PhishTank database snapshot

- [dataset-sample](dataset-sample) – manually verified sample of the original PhishTank-reported phishing

The source code generates the following fields:

* `phishtank_id` – original PhishTank ID

* `phishtank_url` – original URL reported by PhishTank

* `phishtank_online` – original PhishTank online status (`True` for all records)

* `phishtank_verified` – original PhishTank verification status (`True` for all records)

* `crawl_date` – date on which the webpage was crawled

* `crawl_final_url` – final URL reached by the crawler; it may differ from the original PhishTank URL

* `crawl_screen` –  filename of the captured full-page screenshot (after scrolling)

* `crawl_page_input` – parsed metadata for input fields on the webpage

* `crawl_page_text` – raw text extracted from the webpage

The source code generates all fields listed above. Full-page screenshots and raw rendered text of the processed webpages are excluded from the publicly released data because they may contain third-party copyrighted text and graphics, trademarks and logos, personal data, or other sensitive information. Subject to applicable legal, ethical, data-protection, and institutional requirements, these materials may be made available by the author upon reasonable request.

## Examples

The following examples show a non-data-harvesting webpage and a direct data-harvesting phishing webpage reported by PhishTank.

---

**PhishTank-reported webpage:** This is not a direct data-harvesting phishing webpage because it contains no input fields requesting confidential information. The actual phishing webpage may be reached after following the link presented on this page.

This webpage is **NOT** included in the direct data-harvesting phishing ground truth.


<kbd>
<img src="front-figures/invalid-direct-data-harvesting.png" width="500" alt="">
</kbd>

---

**PhishTank-reported webpage:** This is a direct data-harvesting phishing webpage because it contains input fields requesting confidential information.

This webpage **IS** included in the direct data-harvesting phishing ground truth.


<kbd>
<img src="front-figures/valid-direct-data-harvesting.png" width="500" alt="">
</kbd>

---

The raw data source used in this work was provided by [PhishTank](https://www.phishtank.com/).