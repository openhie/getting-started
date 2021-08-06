---
description: Component Level Project and Exchange Level Project
---

# Document Requirements

## \*\*\*\*![](../../.gitbook/assets/papers.svg) **Document Requirements**                          

**Document Data Specifications** 

A data specification document is a technical tool describing the data elements or the information to be managed in one or more registries.  This is a similar concept to a data dictionary where the representations, meaning, and format of data elements in the system are documented.   It is recommended one consider the appropriate [FHIR Resources](https://www.hl7.org/fhir/resourcelist.html) and [FHIR Implementation Guides](https://www.fhir.org/guides/registry/) for registries such as the Facility Registry, Client Registry, Health Worker Registry and Product Catalogue.   In addition, you will want to consider inclusions of any key local attributes.  Other considerations include alternate representations, i.e., “mappings”, that may be required for reporting to external authorities, sharing data with other eHealth systems, or alternate stakeholder needs.   ****

{% hint style="success" %}
![](../../.gitbook/assets/book.png) **Resources and Examples:**

* **Job aids:**[ ****Facility Registry Data Specification Guide](https://docs.google.com/document/d/1V1nw2aLUUdDHJk_C36GRpiPAcRW1n89WaYZtFTWp4mE/edit?usp=sharing);[ Draft WHO MFL Guide](https://docs.google.com/a/instedd.org/file/d/0B_RUEKy5Lc7BS2swR3ZDTjZZeTQ/edit?usp=sharing) 
* **Tanzania Example:**[ ****TZ Facility Registry Data Specification](https://docs.google.com/document/d/1X_3unJ6v3ZOgmXHQ4W98zKXzy7uifi9h_ZLUyULX88M/edit?usp=sharing) 
* **Rwanda Example:**[ ****RW Registry Specifications \(See Page 17\)](https://drive.google.com/file/d/0B_RUEKy5Lc7Bd0tuYzVmcFdiY1E/edit?usp=sharing) 
{% endhint %}

**Document Component Functional Requirements** 

Each OpenHIE component will have both data exchange needs including the ability to support specific standards and APIs and needs for functional requirements.  You should start your journey by looking at the  [OpenHIE Architecture Specification](https://ohie.org/framework/).  This will outline some of the key requirements for each type of component.  For functional requirements, you may want to additionally document them using user stories.

User Stories are a mechanism to gather user requirements and/or core requirements describing the desired registry functionality.  They are a short and simple description of how a particular user needs to interact with the system.  They tell who, what and why the person is interacting with the system. The following are two short examples of user stories from different projects.  ****

* **Example User Story – Other Clinic Visits:**
  * A pregnant woman enters the clinic for her first appointment.  The healthcare worker collects the patient’s name and demographic information.  The worker wants to see if the woman has had visits at other clinics so the worker enters in the demographic information and asks for data from other institutions.  The system will determine if the patient has visited other point-of-care facilities and return the references to those visits. ****
* **Example User Story – Insurance Verification:**
  * A man walks into a clinic he has not visited before.  The health worker needs to verify the man’s insurance. The health worker asks for his name and geographic information.  The man provides the information.  The health worker enters in his information and asks for insurance verification.  The system will use the information entered to check with insurance providers and verifies that the man has insurance. 

**Document Data Exchange Requirements** 

The data exchanges are the processes for sharing data between OHIE components.  We recommend drawing out the data exchange required using interactions diagrams.  The [OpenHIE Specification](https://ohie.org/architecture-specification/) can provide a foundation for recommending the standards and processes for data exchange.  Along with the typical technical expertise required to develop and implement a technology solution, the registry requires technical knowledge of healthcare transactions standards such as IHE PIX/[PDQ](https://wiki.ohie.org/display/documents/Patient+Demographics+Query+IHE+ITI-21+Transaction). The [OpenHIE Architecture Specification](https://ohie.org/architecture-specification/) outlines the recommended standards for each transaction.  ****

If you need to implement a data exchange that is not already outlined in the [OpenHIE Architecture Specification](https://ohie.org/architecture-specification/), please contact the [OpenHIE Architecture Community](https://wiki.ohie.org/display/resources/Architecture+Subcommunity+Call) to gain alignment, ensure that any work your team is doing can be used by others and get any help needed for creating FHIR IGs and/or IHE profiles if they do not already exist.  

{% hint style="success" %}
\*\*\*\*![](../../.gitbook/assets/book.png) **References:**  

* \*\*\*\*[OpenHIE Standards and Profiles](https://wiki.ohie.org/display/documents/OpenHIE+Standards+and+Profiles)
*  [OpenHIE Architecture Specification](https://ohie.org/architecture-specification/)
{% endhint %}

**Document Data Privacy Impact and Requirements**

If the project component\(s\) or information exchanges contain patient demographic data that is used to identify a person, it is important to understand any national and/or local data privacy laws that apply to this data.  The role of the governance structure and content owner is to understand privacy laws and ensure policies, procedures and processes are in place to protect patient privacy.  

Based upon applicable privacy and electronic records regulations for your context, an implementation team may need to address privacy and the appropriate management of electronic healthcare records through measures such as:  

* Guidelines for granting access to the component
  1. _\(Who approves access?  Who can access the registry and when is access allowed?\)_ The guidelines may need to consider:
     * Physical access to servers and data
     * Database access via DBA \(Database Administrator\) or technical resource and perhaps a client registry application
     * Exchange access _\(What systems can provide data to or receive data from the registry?\)_
* Documented annual or regular privacy training for those with access to the component
* Process for annually reviewing data access
* Privacy and security incident management processes.  _\(How are potential breaches of security or privacy to be handled?\)_

{% hint style="success" %}
\*\*\*\*![](../../.gitbook/assets/book.png) **Resource:**  [Guidelines on Protecting the Confidentiality and Security of HIV Information](http://data.unaids.org/pub/manual/2007/confidentiality_security_interim_guidelines_15may2007_en.pdf)  - While aimed at HIV patient data, this resource can be used to help understand privacy, confidentiality and security concerns for patient information.  

\*\*\*\*![](../../.gitbook/assets/book.png) **Reference:** [OpenHIE Privacy and Security](https://wiki.ohie.org/display/SUB/OpenHIE+Privacy+and+Security) 
{% endhint %}

**Agile and Iterative Development**

After the identification and prioritization of requirements and user stories is complete, agile and iterative development takes the prioritized lists and applies the project team to resolve the prioritized requirements and user stories.  Additional requirements and user stories will continue to be generated throughout the lifetime of the implementation and should be prioritized and similarly addressed by the team.  Initially, the goal of this activity will be to address the user stories that will result in a viable and operational OpenHIE component\(s\) or data exchanges.  Additional, development will continue to occur and will also be informed through routine testing and re-prioritization among the team.  A GitHub or similar repository to track this process can help to keep both technical and non-technical stakeholders engaged and accountable. 

