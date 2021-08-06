---
description: Component Level Project and Exchange Level Project
---

# Testing

## \*\*\*\*![](../../.gitbook/assets/instrument.svg) **Software Validation and Testing**                     

There are many components required to validate and test software that is used to manage healthcare records.  Some ministries of health like the United States FDA have specific guidance documents that need to be followed to ensure that healthcare software has been appropriately validated and tested and that electronic records requirements are being met. The purpose of this section is not to detail good software validation practices, but to highlight specific testing considerations for health software.    ****

### **Workflow Testing \(Integration Testing\)**

You will need to test to ensure that any components sharing data with other components  appropriately integrate with the Interoperability Layer and each of the point-of-care systems or other systems that will provide or receive data.  One approach for this testing could be to test various iterations of each workflow\(data exchange\) that will be used between each of the various components involved.   This testing would then be repeated for each system that is in scope. This approach paired with an approach that goes through the whole health care process is recommended. 

### **Performance and Load Testing**

There are at least two aspects of performance testing that will need to be addressed.  First is transaction through-put.  This can be tested by estimating the number of transactions \(data exchanges\) that will be expected during peak business times and ensuring that the network and hardware can support this volume of transactions.    
  
****The second aspect of testing that needs to be considered is ensuring that the registry/OpenHIE component\(s\) is configured to support the number of records required to be stored in the component at its peak usage for the given scope.  For component systems such as the client registry, facility registry and other OHIE components, hardware, databases, matching algorithms and key system functions will need to be tested to ensure that they are appropriately configured and tuned to handle the estimated number of records expected in the next two or three years. 

### **User Testing** 

A key component of the agile process initiated will be to conduct routine field testing of the system that should be completed to gain feedback from a subset of system users.  The goal of this activity is to obtain user feedback on the use of the component.  The testing should be a separate activity from augmented or decentralized processes to collect and standardize data that may also be desired as part of the governance and management of a facility registry system.  It is also likely that the formality of the testing may vary based on the availability of resources and at the request of the central stakeholders. 

{% hint style="success" %}
\*\*\*\*![](../../.gitbook/assets/book.png) **Examples and References:**

* **Example:**  [**User Testing Guide**](https://docs.google.com/document/d/1ZGqn_0XJYdzZLTE25sUjQEkeosM5lSV5xJ0GsmAjGzU/edit?usp=sharing) ****
* **Reference:**[ **INVEST in Good Stories, and SMART Tasks**](http://xp123.com/articles/invest-in-good-stories-and-smart-tasks/) ****
* **Reference:**[ **Examples of Rwanda User Stories for RHIE**](https://wiki.ohie.org/download/attachments/10486056/RHEA%20storyboard%20%284%29.pptx?version=1&modificationDate=1386949763329&api=v2)  ****
{% endhint %}

