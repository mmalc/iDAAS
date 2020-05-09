This is the iDAAS Platform central repository. It is designed to be a launch point for content and all the specific components and additional artifacts that make iDAAS an extensible platform can be found. For general awareness, any iDAAS components code IS ONLY intended to be run within resources that leverage the needed upstream software or equivalent licensed software as defined below within the content. In addition, this effort through its <a href="https://www.apache.org/licenses/LICENSE-2.0" target="_blank">open source licensing</a> selection ensures appropriate protection for all parties. Red Hat Healthcare is doing this to help the broader healthcare community and while a market within Red Hat this is an independant effort. 

# Background
For decades across the various markets within healthcare (clinical, financial, pharmacy and life sciences) integration has been a challenge for many differnt reasons. Within Red Hat there is a specific industry team dedicated to ensuring Red Hat's technologies meet the industry needs and ensuring its customers have meaningful platforms that demonstrate these capabilities, the Red Hat healthcare team. The focus of the team is enabling and empowering healthcare organizations to transform their organizations through infusing Red Hat's open organization, open source mindset and community based culture. As the Red Hat healthcare team started this journey they also wanted to ensure they could help showcase how Red Hat addressed the many variant and expansive needs of a healthcare organization. 

As the Red Hat healthcare team thought about potential ways to help the organizations they wanted to ensure there were a set of specific differentiators no matter for whatever platform would be built:

* Extensibility
* Reduce Proprietary Knowledge
* Open Source Enablement
* Modern Application Development/Delivery Capabilities
* Reduce Propritary Skillset(s)
* Innovative Disruption
* Deliver Consistentcy
* Polyglot Language Support

Here's how the differentiators are expressed in more detail:

* Extensibility: The focus has been on building an extensible platform based on need and usage. The platform is just a series of components that can be connected, extended or new components developed as developers and business teams work together. Within the platform it is developed to enable small to large and complex healthcare organizations to leverage this platform. The platform looks at ANY data as by the application, components, facilities, and overall organization associated with EVERY transaction. 
* Reduce Proprietray Knowledge: We have removed COTS or black box box software and gone with a very open approach. Our approach leverages the numerous Open Source and upstream Open Source products Red Hat is engaged in. Here are several of the technologies this platform leverages: Spring Boot, Red Hat Fuse, Red Hat Process Automation Manager (Business Rules, Workflow and Complex Event Processing), Red Hat A-MQ Streams (Kafka)  - (we also into an A-MQ release as well).
* Open Source Enablement: Provide the source code of the components to extend as needed.
* Modern Application Development/Delivery Capabilities: Where applicable everything is cloud native/container focused. Several of the platform components are based on SpringBoot for easy of deployment and running.
* Reduce Preprietary Skillsets: Removing COTS centric skillsets. This platform is about enabling industry best technologies to enable healthcare to build capabilities rapidly. 
* Disruption: This platform is absolutely designed to enable disruption and enable innovation at the speed of business and technologists.
* Deliver Consistency: Focus around industry standard design and integration patterns.
We don't require deep knowledge of the industry standards to get started, just common developer skillsets. 
* Polyglot Language Support: Enabling the use of many different programming languages. The focus here is to ensure by major capability area a programming language is supported.

As discussed in the introduction integration has been a challenge for decades in each market within healthcare. Within healthcare the challenges have been driven by many different factors, here are just a few common ones: industry standards (HL7) that aren't constrained enough, Clincal software vendor market constraints, COTS integration vendor lock-in, and government mandates that they cannot directly support without third party vendor engagement.

# Connected Health / iDAAS (Intelligent Data As A Service) Platform
When you think of all the needed areas of a healthcare organization, data/data integration must be very high on that list. For the Red Hat healthcare team it was a very logical place to start. Recalling back to earlier the healthcare team wanted to ensure a focus on several things extensibility, open source enablement, consistency, modern development approach, disruption and community enablement. As it was thought through since data powers applications and both of these are strong suits of Red Hat it became a great starting point. With a focus around data integration the Red Hat healthcare team wanted to ensure iDAAS platform was nimble, lightweight, and focused on capabilities to ensure healthcare maket(s) needs could be addressed in a consistent manner. To ensure proper direction the Red Hat healthcare team put together a capability matrix or set to ensure what iDAAS could and would address.

Here are some of the capabilities, the five R’s:

* Receive: receive data from various formats. We have branded this capability iDAAS Connect. From receiving data we focus on industry standards and then third party connectivity. Industry standards support include HL7 v2, FHIR, and EDI Claims. There are potential future plans for  NCPDP and HL7 v3 message support being discussed. From a third party connectivity perspective we focus on building an on-ramp for data to be leveraged within iDAAS for over 75 common protocols like JDBC data sources, File, FTP, SFTP, FTPS, APIs, WSDL, AS400,  Mongo, Kafka, numerous cloud platforms  and many more.
* Route: enable data to be routed to many sources. For this capability we have focused on building out several specific components such as healthcare event builder (both code and integration) to form the intelligent healthcare data router. In order to demonstrate this, our focus was on building a reusable repeatable enterprise application integration message pattern along with the ability for organizations to build and deliver healthcare even streaming.
* Run:  This is one of the most exciting capabilities we are enabling. This is done through our DREAM component. DREAM, Data Realtime Exchange Automated Management, is all about driving change in the healthcare community and building out a value exchange that can be used by anyone implementing iDAAS to add new capabilities in a low latency and very low risk. You would build a component that has the capability of acting on streaming information and being invoked in a real-time manner. These activities could include areas like event population and building, business rules enablement, third party application integration, AI, ML,  dynamic mapping of data sources, cross mapping codes and many other potential examples.
* Resolve: Enable error handling and insight to resolve potential processing issues. Also, the need to replay messages for new needs.
* Research: Enable access to information in a reusable auditable manner. This includes our ability to enable real time clinical information to be tagged as its passing through the platform.

Here are the technologies that drive the capabilities:

* Integration: Ties back to Red Hat’s Fuse and its upstream Apache Camel community. This technology is backed by one of the most active communities and continues to grow and expand this technology for well over a decade. As part of its commitment there are thousands of implementations of all sizes, types and scale levels in numerous industries with some of them growing to support 1 billion daily transactions. As part of its growth are the hundred plus connectors that it natively supports, this will be very beneficial for Red Hat’s healthcare team as the platform looks to grow and expand based on feedback and demand. 
* Business Rules: This capability is supported by Decision Manager and the upstream Drools community. This technology is very largely adopted and implemented throughout the community. Drools has a very large footprint in organizations all over the world delivering expert based solutions and capabilities.
* Data Streaming: A key effort for us is enabling and building a high end data streaming and distribution platform. This capability is being supported by AMQ-Streams and the upstream Kafka community. We are also looking at future implementations with other distributed queuing technologies. As a side note, within the codebase there is a codebase built atop Apache-MQ; however, we maintain the code ONLY for resources that would rather leverage that technology.
* APIs: we have developed all the APIs leveraging .Net Core v3. This will be in two seperate efforts, one is for the platform and one will be for the data tier.
* UX /User Interfaces: The UX experience for the platform is currently driven by .Net Core v3 based assets and a very modern, responsive application design. These applications are best run on the industry leading OpenShift platform for scale. The security model for these capabilities is currently being worked through to ensure the platform is demonstrable, the focus is on showcasing security and enabling the adopters to tie it to LDAP/AD or SAML based systems for the highest level of security.
* Data: We currently are moving to support DDLs for SQL Server, Maria DB (MySQL) and Postgres. This is because there is wide adoption of these within healthcare. The first few implementations with be SQL Server DDL centric as well finalize data model validation. We also intend to expand towards NoSQL standards quickly as we continue to implement new features.
Connected Health/iDAAS overall objective is to simplify data integration and interoperability needs. By establishing a platform initally this enabled the team to focus on the overall industry needs and work through them and establish capabilities for each. As the capabilities were worked through components have been developed to address these needs. 

Here is a general visual of how iDAAS fits in and can enable innovation and solving the problem of integration innovation in the clinical space:
<p align="center" >
<img src="content/images/iDAAS-Platform/iDAAS%20-%20High%20Level%20Solution%20Overview.png" alt="Healthcare Integration" width="500" height="350" />
</p>

Here is a visual on the iDAAS Platform and all its specific components:
<p align="center" >
<img src="content/images/iDAAS-Platform/iDAAS%20Platform%20-%20iDAAS%20Connect%20and%20Vendor%20FHIR%20Modules.png" alt="iDAAS Component Design" 
width="600" height="600" />
</p>

# iDAAS Platform Components
Below is a breakdown of each of the components that make up the iDAAS Platform

## iDAAS Connect
The problem of healthcare connectivity and data enablement has been around for decades. Vendors have had long standing practices of limiting paying customers to the data within the systems they operate and manage. As healthcare organizations prepare for their digital experiences, or look to re-evaluate their current digital experience capabilities, this is no longer a practice that can be tolerated or endured. Within iDAAS, this is the component responsible for providing connectivity to any systems is branded iDAAS Connect and then the market vertical and then the type of connectivity. Lets demonstrate that naming convention.

iDAAS Connect Family of Offerings (These are linked to the respective code repositories):
  
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Clinical-IndustryStandards" target="_blank">iDAAS Connect Clinical - Industry Standards</a>: This connects specifically to clinical integration standards and specific protocols that might be required. For this component it is designed to connect to HL7v2 and FHIR based transactions. From an integration connectivity and standards perspective it can demonstrates the processesing HL7v2 messages of the following types from any vendor and any specifc message version from 2.1 to 2.8: ADT (Admissions), ORM (Orders), ORU (Results), SCH (Schedules), PHA (Pharmacy), MFN (Master File Notifications), MDM (Medical Document Management) and VXU (Vaccinations). For FHIR, we have included over twelve of the commonly used Clinical Resources.
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Clinical-ThirdParty" target="_blank">iDAAS Connect Clinical - Third Party</a> : This connects iDAAS to receive data from almost two dozens connectors. The connectors include  JDBC (any jdbc compliant data source with a jar), Kafka, FTP/sFTP and sFTP, AS400, HTTP(s), REST and many more.
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Financial-IndustryStandards" target="_blank">iDAAS Connect Financial Industry Standards</a>: This connects specifically to financial integration standards and specific protocols that might be required. For this component it is designed to connect to FHIR based transactions. For FHIR, we have included six of the commonly used Financial Resources.
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Financial-ThirdParty" target="_blank">iDAAS Connect Financial Third Party</a>: (Same as its Clinical counterpart above) This connects iDAAS to receive data from almost two dozens connectors. The connectors include  JDBC (any jdbc compliant data source with a jar), Kafka, FTP/sFTP and sFTP, AS400, HTTP(s), REST and many more.

## iDAAS DREAM
* <a href="https://github.com/RedHat-Healthcare/iDAAS-DREAM/" target="_blank">iDAAS DREAM</a>:DREAM (Dynamic Runtime Extensible Automated Mgmt). Component for implementing features and capabilities withing iDAAS. 

## iDAAS Event Builder
* <a href="https://github.com/RedHat-Healthcare/iDAAS-EventBuilder/" target="_blank">iDAAS Event Builder</a>: Ability to build POJOs to represent data in any manner needed for integration and these cana be invoked dynamically against dat within DREAM. Start with over 100 basic POJOs and add your own 

## iDAAS Data Hub
<a href="https://github.com/RedHat-Healthcare/iDAAS-DataIntegration-DataHub/" target="_blank">iDAAS Data Hub</a>: Transactional insight and repository for all things ocuring within any iDAAS component.

## iDAAS UI
 <a href="https://github.com/RedHat-Healthcare/iDAAS-UI/" target="_blank">iDAAS UI</a> | User Interface for accesing iDAAS Data Hub.
 
## iDAAS API
 <a href="https://github.com/RedHat-Healthcare/iDAAS-DataHub-API/" target="_blank">iDAAS API</a>: APIs built from the data tier within iDAAS Data Hub.

# Supporting Materials and Details
Within each component of the platform the Red Hat Healthcare team wanted to try and ensure to help developers and provide common 
implementation direction as we get feedback and continue to expand the iDAAS platforms footprint across SIs (Systems Integrators) and organizations.

## Content
* content: Is a high-level directory intended to maintain any content published about the platform. 
### General
* images/general - This is where general images used in content or materials for iDAAS are maintained.
* images/general/iDAAS-Platform - Images specific to the iDAAS platform and components.
* published/PDFs - Published Content about the iDAAS Platform
### Testing Data
* testdata: is a base directory that has several sub-directories. Each sub-directory is intended to be specific to the type of data it contains.
 #### samples-bluebutton
 These are from the CMS Bluebutton site <a href="https://bluebutton.cms.gov/assets/ig/index.html" target="_blank">Blue Button CMS Site</a>
 #### samples-fhir
 These samples are from the HL7 FHIR community.
 #### samples-hl7
 These have come from merging some public sources. Here are a few examples: <br>
 <a href="https://asiis.azdhs.gov/phchub/help/SampleHL7Msgs.htm" target="_blank">Sample Source 1</a><br>
 <a href="https://blog.interfaceware.com/components-of-an-hl7-message/" target="_blank">Sample Message Source 2</a><br>
 <a href="https://help.interfaceware.com/getting-sample-hl7-data.html" target="_blank">Sample Message Source 3</a>
   
 
# Technologies Used By iDAAS
The iDAAS (Intelligent Data as a Service) Clinical platform is intended for usage for the healthcare market. It contains the following Red Hat technologies, (this platform will also will work with their upstream equivalents):

| Capabilty Area | Upstream Release | Red Hat Release |
| -------------- | ---------------- | --------------- |
| Integration    | Apache Camel     | Red Hat Fuse   |
| Business Rules | Drools           | Red Hat Decision Mgr |
| Data Streaming | Apache Kafka     | Red Hat A-MQ Streams |
| Containers     | K8               | OpenShift            |

It contains the following non Red Hat technologies:

| Capabilty Area | Technologies |
| -------------- | ------------ |
| RDBMS    | SQL Server, Postgres or MariaDB     |
| Programming Language(s)     | Java 1.8 or higher (determined by software implementations. .NetCore 3 for APIs and UI Platforms|

# Practical Implementation: Partnering Organization
To support ANY developed artifcats the Red Hat Healthcare team has created a fictious company named Care Delivery Corporation US (CADuCeUS). Care Delivery Corp. US is intended to help Red Hat Healthcare demonstrate its solutions across all areas of the healthcare market. While everything associated with Care Delivery Corp US is fictiotious including the software they leverage and are building the industry scenarios and platform usage is driven by real world healthcare ongoing use cases/scenarios and needs.
