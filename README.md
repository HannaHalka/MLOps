# MLOps - Customer support query classification

Customer support services always receive a lot of different types of issues. 
And separating each of them manually, for each team is simply unrealistic. 
So in terms of this course, we will use **machine learning** for analyzing customer issues `issue_description` and we will route them to support team `assigned_team`. 
Customer support requests arrive regularly therefore, 
the system must analyze them quickly in real time. 
After analysis, the request will be forwarded to the appropriate support team.
If the system makes an incorrect prediction the receiving team/support manager
can reassign a request to another team.

## Maturity Scorecard

| Property                                   |  Evidence a reviewer checks                                                            | Added in |
|--------------------------------------------|----------------------------------------------------------------------------------------|----------|
| Design document exists and is current      | `docs/design.md` follows the template, every section filled or marked as an assumption | Lab 1    |
| Repository reproducible from a clean clone | CI is green; `make setup` and `make lint` succeed on a fresh clone                     | Lab 1    |


