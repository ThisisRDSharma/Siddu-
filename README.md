Model Settings and Parameters
Model Settings:
The model generates a score between 100 and 899 for applicants, but certain special cases result in exception scores being assigned. These exception scores reflect specific conditions handled by the model:

9999: Missing or insufficient data for score calculation.
9992: Policy rule decline prior to score calculation. This score is used when the institution has elected to decline an account based on a specific rule (e.g., prior fraud closures on file). In such cases, the application is rejected before the credit bureau is assessed, thus reducing costs for accounts that would ultimately be declined.
9998: Deceased SSN. The applicant’s SSN matches an entry on the deceased SSN master list, and the application is not scored or processed further.
Key Parameters:

Score Range: The model generates scores ranging from 100 to 899. Scores above a certain threshold (e.g., 580 for risk-averse strategies) are accepted, and scores below are declined.
Special Scores:
9999: Missing or incomplete data.
9992: Policy rule decline (before score calculation) based on predefined conditions (e.g., prior fraud closures).
9998: SSN is flagged as deceased.
Accept Thresholds: The client can configure the model’s accept thresholds (e.g., accept scores above 580 for a risk-averse strategy).
Vendor Customizations:

The model is not customized for individual clients, but it is flexible for clients to adjust decision thresholds and implement their own business rules.
Clients can handle exception scores (9992, 9998, and 9999) as part of their custom decision-making process.
The model supports integration with client systems, enabling the use of business rules (e.g., 9992 for policy rule declines) to automate decisioning.
Client-Specific Customization Options:

Business Rules and Strategies: Clients can combine model scores with additional customer data (e.g., income, credit history) and create custom strategies tailored to their needs. Strategies can include risk-averse, risk-moderate, and risk-aggressive approaches, as well as the basic rules-only strategy.
Handling Special Scores: Clients can set up their system to manage special scores based on business policies. For example:
9992: Policy rule decline (e.g., prior fraud closures) can be implemented as a filtering mechanism before processing the credit bureau data, saving operational costs for accounts that are unlikely to be approved.
9998: If the model returns a 9998 score (deceased SSN), clients can route these applications for further review or reject them outright.
9999: Missing data cases can be flagged for additional data gathering or manual review.




