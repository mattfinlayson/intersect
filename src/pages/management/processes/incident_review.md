---
title: incident review
---

Production Incident


From Google SRE book:

 It is better to declare an incident early and then find a simple fix and close out the incident than to have to spin up the incident management framework hours into a burgeoning problem. Set clear conditions for declaring an incident. My team follows these broad guidelines—if any of the following is true, the event is an incident:

    Do you need to involve a second team in fixing the problem?
    Is the outage visible to customers?
    Is the issue unsolved even after an hour’s concentrated analysis?

Incident management proficiency atrophies quickly when it’s not in constant use. So how can engineers keep their incident management skills up to date—handle more incidents? Fortunately, the incident management framework can apply to other operational changes that need to span time zones and/or teams. If you use the framework frequently as a regular part of your change management procedures, you can easily follow this framework when an actual incident occurs. If your organization performs disaster-recovery testing (you should, it’s fun: see [Kri12]), incident management should be part of that testing process. We often role-play the response to an on-call issue that has already been solved, perhaps by colleagues in another location, to further familiarize ourselves with incident management. 

Severities (SAAS from VMWare)

Critical (SaaS Severity 1) 	Critical production issue that severely impacts your use of the service. The situation halts your business operations and no procedural workaround exists.

    Service is down or unavailable.

    Data corrupted or lost and must restore from backup.

    A critical documented feature / function is not available.


Severity 1 issues require the customer to have dedicated resources available to work on the issue on an ongoing basis with VMware.

Major (SaaS Severity 2) 	Major functionality is impacted or significant performance degradation is experienced. The situation is causing a high impact to portions of your business operations and no reasonable workaround exists.

    Service is operational but highly degraded performance to the point of major impact on usage.

    Important features of the Software as a Service offering are unavailable with no acceptable workaround; however, operations can continue in a restricted fashion.


Minor (SaaS Severity 3) 	There is a partial, non-critical loss of use of the service with a medium-to-low impact on your business, but your business continues to function. Short-term workaround is available, but not scalable.

Cosmetic (SaaS Severity 4) 	Inquiry regarding a routine technical issue; information requested on application capabilities, navigation, installation or configuration; bug affecting a small number of users. Acceptable workaround available.

Software as a Service Support Policies


To Categorize:

- [Collaboration In Post-Incident Review](https://www.researchgate.net/publication/344166071_Collaboration_In_Post-Incident_Review_Skybrary_Hindsight_26)
- []()
- []()
- []()
- []()

