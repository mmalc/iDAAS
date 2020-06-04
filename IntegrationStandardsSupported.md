# iDAAS Industry Standards Support

Within the clinical integration space HL7.org is the group that manages and oversees the industry standards and has for 
several decades. For specifics and details on all the specifications they manage in healthcare, please feel to visit 
<a href="https://www.hl7.org/" target=_blank> HL7 Web Site</a>. HL7 is the oldest systems integration standard in healthcare. It focuses on the clinical care side of 
the industry, and they only handle specific billing related transactions as part of the clinical services they support. It is often known as quasi standard throughout the healthcare industry due to its lack of hard and fast rules 
and openness for vendor augmentation.

It has evolved from version 2.1 to its most current version 2.8, and it
is still being actively enhanced. HL7 v2 communication involves a client-server based communication model known as MLLP (Minimal Lower Layer Protocol), and the expectation is that the server is always available to receive transactions. Its communication protocol requires that every transaction is positively or negatively acknowledged. Finally, healthcare systems and integrations typically involve a FIFO based messaging pattern where every message must be processed in order.

The iDAAS Platform has been tested with the following HL7 v2 messages.

## HL7
|Message Trigger| Message Trigger Desc. | Message Details | Total Msg Triggers |
|---------------| --------------------- | --------------- | ------------------ |
|<a href="https://datica.com/academy/hl7-201-the-admission-discharge-transfer-adt-message/" target="_blank">ADT</a> | Admissions, Discharges, Transfers | A01 to A61 Any v2 message version release | 60
|<a href="https://datica.com/academy/hl7-203-the-hl7-orm-order-entry-message/" target="_blank">ORM</a> | Orders | Any v2 message version release | 4
|<a href="https://www.lyniate.com/knowledge-hub/hl7-oru-message/" target="_blank">ORU</a> | Results| Any v2 message version release | 4
|<a href="https://datica.com/academy/hl7-205-the-hl7-mdm-medical-document-management-message/" target="_blank">MDM</a> | Master Data Management | Any v2 message version release | 5
|<a href="http://www.hl7.eu/refactored/dom07.html" target="_blank">MFN</a> | Master File Notifications | Any v2 message version release | 5
|<a href="https://www.lyniate.com/knowledge-hub/hl7-siu-message/" target="_blank">SIU</a> | Schedule | Any v2 message version release | 15 
|<a href="https://hl7-definition.caristix.com/v2/HL7v2.3/TriggerEvents/VXU_V04" target="_blank">VXU</a> |Vaccinations | Any v2 message version release |1
|||Total Message Support | 95
<br>

## FHIR
FHIR, Fast Healthcare Interoperability Resources, is the newest universal systems integration standard in healthcare. It's attempting to move healthcare from the dark ages of client-server connectivity, towards a modern REST based set of capabilities. 
Unlike other failed attempts to modernize clinical integration standards such as HL7 v3, FHIR appears to be widely accepted as HL7 v2's successor. It's been around for several years and has a large vendor community supporting and adopting it. 

From 2020, industry adoption in the United States will dramatically increase with government mandates from the Centers for Medicare & Medicaid Services (CMS) directly naming it as the means of compliance. 
We have decided to focus on what the CMS have defined as the standard for Interoperability and Patient Access final rule. 

### Clinical

|Resource| 
|----------| 
|<a href="https://www.hl7.org/fhir/adverseevent.html" target="_blank">Adverse Event</a>|
|<a href="https://www.hl7.org/fhir/allergyintollerance.html" target="_blank">Allergy Intollerance</a>|
|<a href="https://www.hl7.org/fhir/appointment.html" target="_blank">Appointment</a>|
|<a href="https://www.hl7.org/fhir/appointmentresponse.html" target="_blank">Appointment Response</a>|
|<a href="https://www.hl7.org/fhir/careplan.html" target="_blank">Care Plan</a>|
|<a href="https://www.hl7.org/fhir/careteam.html" target="_blank">Care Team</a>|
|<a href="https://www.hl7.org/fhir/codesystem.html" target="_blank">CodeSystem</a>|
|<a href="https://www.hl7.org/fhir/clinicalimpression.html" target="_blank">Clinical Impression</a>|
|<a href="https://www.hl7.org/fhir/communicationresponse.html" target="_blank">Communication Response</a>|
|<a href="https://www.hl7.org/fhir/communication.html" target="_blank">Communication</a>|
|<a href="https://www.hl7.org/fhir/condition.html" target="_blank">Condition</a>|
|<a href="https://www.hl7.org/fhir/consent.html" target="_blank">Consent</a>|
|<a href="https://www.hl7.org/fhir/detectedissue.html" target="_blank">Detected Issue</a>|
|<a href="https://www.hl7.org/fhir/device.html" target="_blank">Device</a>|
|<a href="https://www.hl7.org/fhir/devicerequest.html" target="_blank">Device Request</a>|
|<a href="https://www.hl7.org/fhir/diagnosticresult.html" target="_blank">Diagnostic Result</a>|
|<a href="https://www.hl7.org/fhir/encounter.html" target="_blank">Encounter</a>|
|<a href="https://www.hl7.org/fhir/episodeofcare.html" target="_blank">Episode of Care</a>|
|<a href="https://www.hl7.org/fhir/goal.html" target="_blank">Goal</a>|
|<a href="https://www.hl7.org/fhir/healthcareservice.html" target="_blank">Healthcare Service</a>|
|<a href="https://www.hl7.org/fhir/imagingstudy.html" target="_blank">Imaging Study</a>|
|<a href="https://www.hl7.org/fhir/immunization.html" target="_blank">Immunization</a>|
|<a href="https://www.hl7.org/fhir/location.html" target="_blank">Location</a>|
|<a href="https://www.hl7.org/fhir/deviceusestatement.html" target="_blank">Device Use Statement</a>|
|<a href="https://www.hl7.org/fhir/medicationadministration.html" target="_blank">Medication Administration</a>|
|<a href="https://www.hl7.org/fhir/medicationdispense.html" target="_blank">Medication Dispense</a>|
|<a href="https://www.hl7.org/fhir/medicationrequest.html" target="_blank">Medication Request</a>|
|<a href="https://www.hl7.org/fhir/observation.html" target="_blank">Observation</a>|
|<a href="https://www.hl7.org/fhir/organization.html" target="_blank">Organization</a>|
|<a href="https://www.hl7.org/fhir/organizationaffiliation.html" target="_blank">Organization Affiliation</a>|
|<a href="https://www.hl7.org/fhir/patient.html" target="_blank">Patient</a>|
|<a href="https://www.hl7.org/fhir/person.html" target="_blank">Person</a>|
|<a href="https://www.hl7.org/fhir/practitioner.html" target="_blank">Practitioner</a>|
|<a href="https://www.hl7.org/fhir/procedure.html" target="_blank">Procedure</a>|
|<a href="https://www.hl7.org/fhir/questionaire.html" target="_blank">Questionaire</a>|
|<a href="https://www.hl7.org/fhir/questionaireresponse.html" target="_blank">Questionaire Response</a>|
|<a href="https://www.hl7.org/fhir/schedule.html" target="_blank">Schedule</a>|
|<a href="https://www.hl7.org/fhir/servicerequest.html" target="_blank">Service Request</a>|
|<a href="https://www.hl7.org/fhir/specimen.html" target="_blank">Specimen</a>|
|<a href="https://www.hl7.org/fhir/substance.html" target="_blank">Substance</a>|
|<a href="https://www.hl7.org/fhir/supplydelivery.html" target="_blank">Supply Delivery</a>|
|<a href="https://www.hl7.org/fhir/supplyrequest.html" target="_blank">Supply Request</a>|
|<a href="https://www.hl7.org/fhir/verificationresult.html" target="_blank">Verification Result</a>|

### Financial

|Resource| 
|----------| 
|<a href="https://www.hl7.org/fhir/account.html" target="_blank">Account</a> | 
|<a href="https://www.hl7.org/fhir/chargeitem.html" target="_blank">Charge Item</a> | 
|<a href="https://www.hl7.org/fhir/chargeitemdefinition.html" target="_blank">Charge Item Defintion</a> | 
|<a href="https://www.hl7.org/fhir/claim.html" target="_blank">Claim</a> |
|<a href="https://www.hl7.org/fhir/claimresponse.html" target="_blank">Claim Responses</a> | 
|<a href="https://www.hl7.org/fhir/contract.html" target="_blank">Contract</a> | 
|<a href="https://www.hl7.org/fhir/coverage.html" target="_blank">Coverage</a> | 
|<a href="https://www.hl7.org/fhir/coverageelibilityrequest.html" target="_blank">Coverage Eligibility Request</a> |  
|<a href="https://www.hl7.org/fhir/coverageeligibilityresponse.html" target="_blank">Coverage Eligibility Response</a> | 
|<a href="https://www.hl7.org/fhir/enrollmentrequest.html" target="_blank">Enrollment Request</a> | 
|<a href="https://www.hl7.org/fhir/enrollmentresponse.html" target="_blank">Enrollment Response</a> | 
|<a href="https://www.hl7.org/fhir/explanationofbenefits.html" target="_blank">Explanation of Benefits</a> | 
|<a href="https://www.hl7.org/fhir/insuranceplan.html" target="_blank">Insurance Plan</a> | 
|<a href="https://www.hl7.org/fhir/invoice.html" target="_blank">Invoice</a> | 
|<a href="https://www.hl7.org/fhir/paymentnotice.html" target="_blank">Payment Notice</a> | 
|<a href="https://www.hl7.org/fhir/paymentreconcilliation.html" target="_blank">Payment Reconcilliation</a> | 

### Public Health

|Resource| 
|----------| 
|<a href="https://www.hl7.org/fhir/researchstudy.html" target="_blank">Research Study</a> | 
|<a href="https://www.hl7.org/fhir/researchsubject.html" target="_blank">Research Subject</a>| 

### Evidence Based Medicine

|Resource| 
|----------| 
|<a href="https://www.hl7.org/fhir/researchdefinition.html" target="_blank">Research Definition</a> | 
|<a href="https://www.hl7.org/fhir/researchelementdefinition.html" target="_blank">Research Element Definition</a>| 
|<a href="https://www.hl7.org/fhir/evidence.html" target="_blank">Evidence</a>| 
|<a href="https://www.hl7.org/fhir/evidencevariable.html" target="_blank">Evidence Variable</a>| 
|<a href="https://hl7.org/fhir/R4/effectevidencesynthesis.html" target="_blank">Effect Evidence Synthesis</a>| 
|<a href="https://hl7.org/fhir/R4/riskevidencesynthesis.html" target="_blank">Risk Evidence Synthesis</a>| 

### Quality Reporting

|Resource| 
|----------| 
|<a href="https://www.hl7.org/fhir/measure.html" target="_blank">Measure</a> | 
|<a href="https://www.hl7.org/fhir/measurereport.html" target="_blank">Measure Report</a> | 
|<a href="https://www.hl7.org/fhir/testscript.html" target="_blank">Test Script</a> | 
|<a href="https://www.hl7.org/fhir/testreport.html" target="_blank">Test Report</a> | 

### FHIR Server
A FHIR Server is not required for our implementation or CMS compliance; however, these servers can help organizations with capabilities they might need. The iDAAS Connect component is designed to connect to multiple vendor implementations of FHIR servers in a repeatable manner. 

