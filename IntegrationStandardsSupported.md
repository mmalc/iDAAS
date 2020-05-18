# iDAAS Industry Standards Support

Within the clinical integration space HL7.org is the group that manages and oversees the industry standards and has for 
several decades. For specifics and details on all the specifications they manage in healthcare, please feel to visit 
<a href="https://www.hl7.org/" target=_blank> HL7 Web Site</a>. HL7 is the oldest standards in healthcare for enabling systems integration, their focus is the clinical care side of 
the industry and they only handle specific billing related transactions as part of supporting the clinical services 
they support. HL7 is a very legacy based standards specific to the way communications occur. The HL7 v2 message 
standard has been a long standard for the clinical industry and vendor platforms to communicate for decades. 
It is often known as quasi standard throughout the healthcare industry due to its lack of hard and fast rules 
and openness for vendor augmentation. It has evolved from version 2.1 to its most current version 2.8 and 
is still being very actively enhanced. HL7 v2 communication involves a client-server based communication model 
known as MLLP (Minimal Lower Layer Protocol), the expectation is that the server is running one hundred percent 
of the time to receive transactions. As part of its communication it requires that every transaction is specifically 
acknowledged or negatively acknowledged during processing. Finally, healthcare systems and integrations typically 
involve a FIFO based messaging pattern, every message must be processed in order.

The iDAAS Platform has been tested and has the following HL7 v2 support.

## HL7
|Message Trigger| Message Trigger Desc. | Message Details | Total Msg Triggers |
|---------------| --------------------- | --------------- | ------------------ |
|ADT | Admissions, Discharges, Transfers | A01 to A61 Any v2 message version release | 60
|ORM | Orders | Any v2 message version release | 4
|ORU | Results| Any v2 message version release | 4
|MDM | Master Data Management | Any v2 message version release | 5
|MFN | Master File Notifications | Any v2 message version release | 5
|SIU | Schedule | Any v2 message version release | 15 
|SIU | Schedule | Any v2 message version release | 15 
|VXU |Vaccinations | Any v2 message version release |1
|||Total Message Support | 95
<br>

## FHIR
FHIR, Fast Healthcare Interoperability Resources, is the modern current healthcare industry standardization approach to
move healthcare from the dark ages of client-server connectivity towards a REST based set of capabilities. 
Unlike other attempts to modernize clinical integration standards FHIR is the future. It has been around for several years 
and already has a very large vendor community supporting and adopting it. The industry adoption from 2020 going forward 
adoption will dramatically increase with government mandates from CMS directly naming it as the means of compliance. From 
a simplification perspective are a set of modules and within the modules there are resources. Here is the latest version 
of FHIR, please feel free to look. 

We have decided to focus on what CMS has defined as the standard for Interoperability and Patient Access final rule. 
This includes comprehensive FHIR transaction processing requirements including detailed parsing capabilities for growth 
and extensibility.  Also, we wanted to ensure we could support multiple third party vendor based solutions, so we are 
implementing this in a repeatable manner.


