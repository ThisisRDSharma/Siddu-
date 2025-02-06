To ensure the accuracy and integrity of the data processed by the model, QualiFile incorporates several input verification checks. These checks help prevent errors, detect fraudulent information, and improve the reliability of automated decision-making.

SSN Validation Check:

The model verifies whether the provided Social Security Number (SSN) is valid.
If an SSN validation failure occurs, QualiFile displays a message, alerting the user to take corrective action.
While the model can process an inquiry without an SSN, this is not recommended, as missing SSN data may limit the availability of critical consumer history, potentially impacting the decisioning process.
Consumer Identity Theft Alert Check:

If a consumer has placed an identity theft alert with ChexSystems, the model automatically returns a "Review" recommendation instead of an automated approval or decline.
This ensures that institutions manually assess the case before proceeding, preventing fraudulent activity from influencing decisions.
Consumer Security Freeze Check:

If a consumer has implemented a security freeze on their third-party consumer reports, the model returns a "Review" recommendation rather than a standard decision.
The consumer must contact the relevant credit reporting agency to lift the freeze before the financial institution can proceed with the application.
Driver’s License Format Verification:

The model checks whether the driver’s license number, state ID, or military ID follows the correct alphanumeric format for all 50 states, U.S. territories, and military bases.
This helps detect improperly entered or potentially fraudulent identification details.
Invalid Telephone Number Check:

The model verifies whether the telephone number’s exchange/prefix exists within the specified area code.
This check ensures that input phone numbers are formatted correctly and belong to a valid area code, though it does not confirm whether the number is currently active.
Reconciliation of Final Modeling Dataset to Source Systems:

The final modeling dataset is reconciled against source systems to ensure data accuracy and completeness.
This process verifies that key attributes (e.g., SSN, identity alerts, and transaction history) are correctly populated and match source records, preventing data corruption or transformation errors.
Reconciliation helps maintain the integrity of model inputs, ensuring reliable decision-making.
