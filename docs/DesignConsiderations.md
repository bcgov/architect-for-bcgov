Design Considerations for an Application

Notes : In this context, an "application" may be substituted by "service" and many consideration would still apply, though they could have different implementations (ie, of the similar capability).  A Privacy Impact Assessment (PIA) and a Strategic Threat and Risk Assessment (STRA) are assumed to be undertaken for all applications.

# Shaping your application

**Audience**	- metadata factors: where is the audience geographically?  what is the overall size of the audience?  what is the expected peak concurrent audience engaged with app?  On what devices?

**Application Redundancy** - Related to Business Continuity, this is an implementation detail that addresses continued availability of applications that are very important to the business in case of failure of one or more parts of either the underlying infrastructure, other applications or services upon which an applications depends, or parts of the application itself.

**Business Continuity** - How important is this application to its audience?  What expectations does its audience have of its availability?  How easily can the business purpose of the application be accomplished without it?  What contingencies are in place for business to continue when the application becomes unavailable?  See also Application Deployment.)

**Legislation, Policy, & Standards** - Population considerations like indigenous language support, methods for implementing a Data Register, consumption of Common Components (and other de facto standard ways of doing something.)

# Within Your Application

**Presentation** - Consider target devices and bandwidth.  Consider localizations, audience preferences, and special requirements (accommodations).

**Data Collection** - What inputs are required from users?  Which of them can be automated, or collected from other Systems of Record or an input platform (phone, eg)?  Is permission required?  Considering accessibility and audiences, what special requirements apply?  What localizations?  Are BLOBs acceptable?  Specific formats?

**Identify** - To what level must audience members be identified?  

**Authorize** - What different levels of access are identified in the application?  What standard method(s) can be used to implement?

**Master Data Authoring** - What master data is required by the application?  (i.e., what authoritative data is consumed by the application?  What authoritative data can be updated through the application - via a system of record?) For ehat datga does this application serve as the system of record?

**Integrations** - What other systems / applications can provide data or functionality?  What other applications can consume functionality provided by this application?  What events take place within this application that other applications could benefit from knowing about; can they be notified?  See also ETL, External and Internal Capability Consumption, Asynchronous Messaging, Master Data Access.

**Workflows** - What states need to be accommodated for "documents" (or records) in the application?  For events that change state, where human invervention is required, how might that intervention be handled?  Are notifications required?  Alarms?  Escalations?  Must workflow be audited to document events?  What other System(s) of Record might be leveraged to verify authorizations?

**Data Storage / Retrieval** - How is the data stored?  Is this the system of record for any of the data is hosts?  Is the data protected with read and write services for consistent access?  Are services written to allow other systems access to the data?  How are other systems advised of access methods?  What events are published?  

**Data Protection** - To what level is data required to be protected?  In transit?  At rest? How is this tested/proven?

**Application Administration** - What resources are required to maintain user lists and privileged access?  What data retention policies apply to the data housed by the application, and what maintenance is required of the data?  When is data purged?  Is this automated or manual?  

# Meta Application

**Application Development** - Are there "universal truths" related to this consideration in the local environment, or more globally?  These may be stated as standards, determined globally or locally, or adopted from other bodies like industry standards organisations.  What toolsets or individual technologies are encouraged, deprecated, "sunsetted", restricted, if any?  What methodologies?

**Application Monitoring** - Where are the choke-points in the system that may impact performance/usability? How frequently are measurements taken / written to logs?  When are notifications or alarms generated?  Who responds?  Does monitoring frequency or notifications change with time?

**Application Deployment** - Design the application and its deployment to ensure that service levels are addressed.  What are availability expectations?  Ensure that RTO and RPO are met with appopriate, cost-effective design.  The business must be consulted, the Business Impact Assessment (BIA) and Business Continuity Plan (BCP) will both influence deployment, as may a methodology and/or platform choice.

**Application Governance** - Is the application being used for what it is intended?  What restrictions, constraints, guidelines, and agreements are in place to determine how the application is to be used, when it is available, how its data is managed (within the application, and from without)?  Definition of roles and user groups, and their abilities,  also fall into this consideration.

# Consumed Services

**Backup-Recovery** - Are backups provided as an infrastructure service?  Does the restore service satisfy Return to Operations objectives?  Does Backup/Restore support RPO?  Is there an opportunity to reduce costs by moving aging backups to archive storage (longer recovery time in exchange for lower storage costs)?

**Export / Transform / Load** - What requirements are there for high-volume data import and/or export?  Is latency for high-volume transport a consideration?

**Historical Operational Transaction Store** - Would business decisions benefit from analysis of historical transaction trends?  This "store" is historically addressed with a "business intelligence" backend like a data warehouse.

**Business Intelligence** - Typically implemented to complement a backend store, this addresses analysis of large volumes of data to support decisions, presenting discoveries and trends in easily-consumed ways.  May feed "dashboards."

**Infrastructure Monitoring & Logging** - In addition to a heartbeat to determine an application's availability, what points of possible constraint or dependency ought to be monitored or measured for throughput compared to expected capacity?  Should there be a watch on response times throughout and between components?  What notification events are triggered and to where are they directed?  What logs are written and for how long are they kept?

**External Capability Consumption** - What functionality provided by other systems or external components are required?  These capabilities are in addition to accessing master data. Examples may be taking or making a payment, formatting a street address, and confirming an official BC business.

**Asynchronous Messaging** - Closely related to integration, this accommodates less time-dependant integration use cases such as publish-subscribe, batch processing, and others.

**Master Data Access** - What master data is required by the app (i.e., what authoritative data is consumed by the app?  What authoritative data must be updated via another system of record?)  For what data does this app serve as the system of record?

