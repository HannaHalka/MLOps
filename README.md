# MLOps - Customer support query classification

Customer support services always receive a lot of different types of issues. 
And separating each of them manually, for each team is simply unrealistic. 
So in terms of this course, we will use **machine learning** for analyzing customer issues `issue_description` and we will route them to support team `assigned_team`. 
Customer support requests arrive regularly therefore, 
the system must analyze them quickly in real time. 
After analysis, the request will be forwarded to the appropriate support team.
If the system makes an incorrect prediction the receiving team/support manager
can reassign a request to another team.

##  Data Version (DVC)

**Dataset:** https://huggingface.co/datasets/s2pidape/support-ticket-dataset \
**Sample size:** 400 000 records\
**File:** `data/raw/support_tickets.csv` \
**File size:** 194 MB \
**Versioning:** DVC 3.67.1 \
**Remote storage:** MinIO (S3-compatible) \
**Bucket:** `mlops-data` \
**SHA-256:** _b13add4425a9827808c187829d8f7ca853f5b6f6906b9425f92d13971a8a6992_

We download the full dataset, then we sort it by `created_at` and took only first 400 000 observation.

## Maturity Scorecard

| Property                                   | Evidence a reviewer checks                                                                 | Added in |
|--------------------------------------------|--------------------------------------------------------------------------------------------|----------|
| Repository reproducible from a clean clone | CI is green; `make setup` and `make lint` succeed on a fresh clone                         | Lab 1    |
| Design document exists and is current      | `docs/design.md` follows the template, every section filled or marked as an assumption     | Lab 1    |
| Data versioned                             | the documented pull command retrieves the raw data on a clean clone                        | Lab 2    |
| Pipeline idempotent                        | the same interval run twice gives identical row counts, both pasted in the README          | Lab 2    |
| Quality gate present                       | one bad batch fails the run on purpose, shown                                              | Lab 2    |
| Experiments tracked                        | every training run in the tracking server has parameters, metrics, data version and commit | Lab 2    |
| Model registered with lineage              | a registered version tagged with data version and commit, reproducible by one command      | Lab 2    |


