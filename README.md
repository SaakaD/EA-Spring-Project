# EA-Spring-Project
Prescription Management System 
Background
Prescription Management System (PMS) is designed to automate the management of prescriptions for a pharmacy named "Drugs for You." The system keeps track of customer information, prescription history, and medications stocked by the pharmacy. The goal is to facilitate efficient tracking of patient prescriptions and medication dispensing.
The system must track the following information:
Patient Information
i.	Patient’s name
ii.	Telephone number
iii.	Date of birth
iv.	Insurance provider
v.	Insurance policy number
vi.	A prescription history (detailed below)

Prescription History
i.	Unique prescription ID number assigned by the pharmacy
ii.	Medication prescribed
iii.	Prescribing physician’s name and telephone number
iv.	Date of issue
v.	Expiration date
vi.	Number of refills authorized

Medication Information
i.	Medication name
ii.	Unit by which it is prescribed (e.g., pills, teaspoons, ml)
iii.	Generic equivalents, if available
iv.	Common side effects of the medication

System Queries
The system must support several queries, which may result in either hard-copy reports or be viewed online:
i.	Prescription History Report: A report of all prescriptions ever issued to a given customer, as requested by the customer.
ii.	Side Effects Report: A report of all side effects associated with a given medication, to be enclosed with each dispensed prescription.
Access:
All of the above reports and queries must be accessible through a secure website to individual customers and in-store pharmacists.
Simplifying Assumptions
The following assumptions are made:
1.	No Billing Matters:
o	The system will not handle pricing or reimbursement from insurance companies.
2.	Single Pharmacy Location:
o	We assume there is only one "Drugs For You" pharmacy location, and it is not part of a chain.
3.	No Inventory Control:
o	The system assumes an infinite supply of all medications or that medications are available on demand from a warehouse.
4.	Consistent Refills:
o	Refills will always be fulfilled with the same medication as the original prescription.
o	A prescription will never be initially filled with a generic and later refilled with a non-generic equivalent (or vice versa).
Project Implementation, Domain Classes and Use Cases and Descriptions
The above problem statement highlights 3 domain classes (Customer/Patient, Prescription and Medication).  However, for the complete execution of this project, we will add 2 additional classes (Physician and Pharmacist). 
Below are the use cases identified to be focused on. 
1. Add Patient (by Physician)
•	Description: The physician adds a new patient to the system, capturing details such as the patient's name, telephone number, date of birth, insurance provider, and policy number.
•	Precondition: The patient does not already exist in the system.
•	Postcondition: The patient is added to the system, and their profile is ready for future prescriptions.
2. Add Pharmacist (by Physician)
•	Description: The physician adds a new pharmacist to the system, capturing details such as the pharmacist’s name, and phone number.
•	Precondition: The pharmacist does not already exist in the system.
•	Postcondition: The pharmacist is added to the system, and their profile is ready for dispense future prescriptions.
3. Prescribe Medicine (by Physician)
•	Description: The physician prescribes medication to a patient, including details such as medication name, dosage, number of refills, expiration date, and prescribing physician information.
•	Precondition: The patient must already exist in the system.
•	Postcondition: The prescription is added to the patient’s history and becomes available for the pharmacist to dispense.
4. View Prescription History (by Patient, Physician and Pharmacist)
•	Description: The patient, physician, and pharmacist can view the complete prescription history for a specific patient. The system retrieves all past and current prescriptions issued to the patient.
•	Precondition: The patient must be registered, and at least one prescription must exist.
•	Postcondition: A list of all prescriptions is displayed to the requesting actor (patient, physician, or pharmacist).
6. Dispense Medication (by Pharmacist)
•	Description: The pharmacist dispenses medication based on a valid prescription, updating the system to reflect that the prescription has been dispensed and adjusting the number of authorized refills if applicable.
•	Precondition: The prescription must exist, and it must not be expired or out of refills.
•	Postcondition: The prescription is marked as dispensed, and the number of refills is updated.
•	Postcondition: The system returns whether the prescription can be refilled, based on the remaining refills and the expiration status.
