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

# Technologies Used By iDAAS
The iDAAS (Intelligent Data as a Service) Clinical platform is intended for usage for the healthcare market. It contains the following Red Hat technologies, (this platform will also will work with their upstream equivalents):

| Capabilty Area | Upstream Release | Red Hat Release |Requirement|
| -------------- | ---------------- | --------------- |---------- |
| Integration    | Apache Camel     | Red Hat Fuse   | Core of the Platform|
| Business Rules | Drools           | Red Hat Decision Mgr |Used by iDAAS Dream, can be optional if no DREAM components implemented|
| Data Streaming | Apache Kafka     | Red Hat A-MQ Streams |Requirement by platform for messaging |
| Containers     | K8               | OpenShift            |End User defined, platform can be run stand alone or at scale|

It contains the following non Red Hat technologies:

| Capabilty Area | Technologies |
| -------------- | ------------ |
| RDBMS    | SQL Server, Postgres or MariaDB     |
| Programming Language(s)     | Java 1.8 or higher (determined by software implementations. .NetCore 3 for APIs and UI Platforms|

# iDAAS Platform Components
Below is a breakdown of each of the components that make up the iDAAS Platform

## iDAAS Connect
The problem of healthcare connectivity and data enablement has been around for decades. Vendors have had long standing practices of limiting paying customers to the data within the systems they operate and manage. As healthcare organizations prepare for their digital experiences, or look to re-evaluate their current digital experience capabilities, this is no longer a practice that can be tolerated or endured. Within the iDAAS Connect platforms their is a wide breadth of supported transactions. Please <a href="https://github.com/RedHat-Healthcare/iDAAS/blob/master/IntegrationStandardsSupported.md" target="_blank">look here</a> for the supported transactions.

iDAAS Connect Family of Offerings (These are linked to the respective code repositories):
  
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Clinical-IndustryStandards" target="_blank">iDAAS Connect Clinical - Industry Standards</a>: This connects specifically to clinical integration standards and specific protocols that might be required. For this component it is designed to connect to HL7v2 and FHIR based transactions. From an integration connectivity and standards perspective it can demonstrates the processesing HL7v2 messages of the following types from any vendor and any specifc message version from 2.1 to 2.8: ADT (Admissions), ORM (Orders), ORU (Results), SCH (Schedules), PHA (Pharmacy), MFN (Master File Notifications), MDM (Medical Document Management) and VXU (Vaccinations). For FHIR, we have included over twelve of the commonly used Clinical Resources.
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Clinical-ThirdParty" target="_blank">iDAAS Connect Clinical - Third Party</a> : This connects iDAAS to receive data from almost two dozens connectors. The connectors include  JDBC (any jdbc compliant data source with a jar), Kafka, FTP/sFTP and sFTP, AS400, HTTP(s), REST and many more.
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Clinical-MiddleTier" target="_blank">iDAAS Connect Clinical Middle Tier</a>: This component is specifically implemented to help keep the iDAAS Connect Clinical Industry Standards component small by moving the data streaming and HCDD-EIP (Healthcare Data Distribution and Enterprise Integration Pattern). 
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Financial-IndustryStandards" target="_blank">iDAAS Connect Financial Industry Standards</a>: This connects specifically to financial integration standards and specific protocols that might be required. For this component it is designed to connect to FHIR based transactions. For FHIR, we have included six of the commonly used Financial Resources.
* <a href="https://github.com/RedHat-Healthcare/iDAAS-Connect-Financial-ThirdParty" target="_blank">iDAAS Connect Financial Third Party</a>: (Same as its Clinical counterpart above) This connects iDAAS to receive data from almost two dozens connectors. The connectors include  JDBC (any jdbc compliant data source with a jar), Kafka, FTP/sFTP and sFTP, AS400, HTTP(s), REST and many more.

## iDAAS DREAM
* <a href="https://github.com/RedHat-Healthcare/iDAAS-DREAM/" target="_blank">iDAAS DREAM</a>:DREAM's design intent is to enable Red Hat, partners, SIs and developers to implement iDAAS and/or other capabilities internal or external to iDAAS in a dynamic manner without the need for stopping the platform and needing to restart it to work with data while adding new features.
 
## iDAAS Event Builder
* <a href="https://github.com/RedHat-Healthcare/iDAAS-EventBuilder/" target="_blank">iDAAS Event Builder</a>: iDAAS Event Builder is what enables Red Hat, partners, SIs and developers to develop, extend or enhance the platform's ability to process data into any type of needed custom format for any type of needed processing. iDAAS Event Builder is designed to call out and invoke needed events and can be customized based on business needs very quickly. The only thing past cloning the source code is setting up the appropriate way to include iDAAS Event Builder jar files so that it can be included. If you do not wish to leverage the existing code, enhance or extend it developers are able to add their own custom code for processing and object building.

## iDAAS Data Hub
<a href="https://github.com/RedHat-Healthcare/iDAAS-DataIntegration-DataHub/" target="_blank">iDAAS Data Hub</a>: iDAAS Data Hub is where data relative to the platform is stored. Like the rest of iDAAS it is intended to be extensibile. iDAAS Data Hub is a platform to enable processing of data into the various components and data models included. The key things Data Hub is meant to ensure resources have data driven insights from ANY activity the iDAAS platform will do. A key thing to note in the data model and events the system focuses on is a way to associate one organization to many healthcare entities and to many applications and within each application any components wished to be defined. This is ALL up to the implementation. Because of this data enablement iDAAS focuses on enabling a detailed eventing model to iDAAS Data Hub for any activities the system does, this specifically is done through a transaction event which has a rich set of data attributes to track:
* The iDAAS action being leveraged 
* The iDAAS component that is leveraging the action
* The date and time of the action
* The data involved within the component
* A subset of other attributes depending upon the action type: sending application, transactions processed, transactions generated, processing times, response times, and several more.

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
### TestData
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

## Platform Scripts
General Platform scripts area. These are uplifted from various projects based on market types.
### Clinical
Clinical centric components Kafka topics
### Financial
Financial centric components Kafka topics

# Building and Running iDAAS
iDAAS is a series of components so building it is a simple step, running it involves configuring several iDAAS components and running them together. Within each iDAAS component there is an implementation/running specific set of instructions. Since the platform leverages Maven the commands are very well published and known.

## Building
To build you will need to go to the main directory after cloning, or pulling the respective repositories, and run the following command where the pom.xml file is located (or configure an IDE):

mvn clean build

## Running
To run any component run the following command from where the pom.xml file is located (or configure an IDE):

mvn package

It will create a jar with the version defined in the pom.xml file within the /target directory. from the /target directory you can run the component by running: java -jar <jarfilename.jar>

# Practical Implementation: Partnering Organization
In order to address the healthcare market needs Red Hat’s healthcare team needed to ensure they had a real world market focus to build out relevant market demonstrations and workshops for the platforms it was creating. To help achieve this Red Hat Healthcare created a fictitious healthcare company named Care Delivery Corp US, it’s acronym is CADUCEUS (the medical symbol). The intent of doing this is to have a healthcare enterprise that resonates within the healthcare market. 

Here are all the various areas of healthcare the Care Delivery Corporation US will help Red Hat healthcare demonstrate its relevant platform(s).
* Healthcare provider service(s)
  * Hospitals
  * Physicians
  * Clinics
  * Same day surgery centers
  * Various ancillary such as radiology services
  * Cancer treatment and chronic disease management
* Provide healthcare support services they provide for themselves and some other healthcare organizations. 
  * Billing
  * Staffing
* Provide support for their healthcare services IT needs.
  * Operations teams to implementing and supporting COTS products
  * Data Organization supporting reporting and analytics needs
  * Integration Organization to support their data integration needs
  * Develop some customized business driven solutions 
  * Security organization to ensure compliance 
* Life sciences space to support their healthcare needs around Cancer treatment and chronic disease management

## Scenario: IT Digitization 
As  with any organization, irrespective of industry or market, Care Delivery Corp is re-evaluating its overall IT capabilities as a by product of needing to move into the digital realm. This re-evaluation is also being heavily influenced by their need to also prepare for upcoming government mandates around interoperability requirements specific to data access, not only for their patients but also their other businesses as well. Through the journey of their re-evaluation of capabilities they have identified some very consistent challenges they are having: lack of ability to innovate, vendor lock in, data interoperability incapabilities, without waiting for numerous vendors, experience problems from partner to customer to patient to clinician to technologist. As they took these common findings to their enterprise integration team the leadership team realized that also have a debt problem: technical, operational and functional in the way they deliver integration. So they decided to look at the overall application development and integration market landscape in general and quickly realized that they wanted to focus mostly on the Open Source market versus a series of COTS products. As they looked at the Open Source space Red Hat emerged as the leader. The technical leadership team realized that Red Hat had a very solid set of technologies to provide them the greatest range of capabilities for their current and future needs. From that decision came the details around what platform and capabilities can Red Hat provide? Red Hat has dozens of products that build massively extensive capabilities for some of the largest corporations in the world from their operating system to automation to integration to business rules to complex event processing to application development to API management. 

Based on all these findings, Care Delivery Corp has decided to start their digital transformation and implement a home grown platform, myEMR. myEMR is intended to be a platform for all Care Delivery US to leverage for its go forward digital needs, the intent is to have it drive all clinical data needs. In order to start their work efforts they wanted to start integration for their enterprise standard clinical management information systems, Major Medical Systems (MMS) platform called Care Kiosk. 

Enterprise Organization        CareDelivery US
Facility                Medical Center TN (MCTN)
Sending Application         Major Medical System (MMS) - Care Kiosk

## Scenario: Existing Implementation Scenario(s) 
As Care Delivery Corp US talked with their enterprise integration team they asked for a general architecture for their digital implementation needs. The plan is for one medical facility Medical Center TN (MCTN) and getting the following industry standard transactions processing:
* HL7 v2: Admissions, Orders, Results, Schedules, Master File Notifications, Medical Document Management, Scheduling and Vaccinations. 
* FHIR: All FHIR resources to provide the CMS Final Interoperability Rule compliance and help start them towards building out modern integration capabilities.
<br>
What they realized is they could not approach this effort like implementing clinical systems and knew they needed to develop an innovative approach to address their current and future data needs for this transformation.  

