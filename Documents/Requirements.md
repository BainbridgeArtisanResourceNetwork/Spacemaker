# Product Requirements
This document breaks down the initial, high-level requirements for Studio Shares's feature offerings. These requirements are based on discussions around [BARN](https://bainbridgebarn.org/)'s needs for maker space management software.

These requirements are the product of brainstorming, and are likely to change over time.

## Open Source
The goal of Studio Share is to provide open-source management software for makerspaces. There are many offerings for this type of software, but most require a paid subscription.

With the goal of sharing the code for Studio Share with other organizations in mind, we will aim to:
- Create software that is generic and flexible for use at other makerspaces.
- Publish a public roadmap with upcoming features and bug fixes.
- Provide documentation to enable the community to self-serve.
- Maintain an agnostic approach to deployment.

## Users
People are the core of any shared community space, and so the Studio Share data model must start with users. A user account in the Studio Share ecosystem needs to provide:
- Profile customization.
- Account creation, modification, and deletion.
- Association with fine-grained authorization roles.
- Password changes.
- Association with mailing lists.
- Qualifications based on event participation or other criteria.
- Membership enrollment and changes.

## Resources
Since makerspaces are managed in different ways depending on the goals of the organization, it is important that Studio Share remains flexible around what types of resources are being managed. This means that a "resource" could be scoped to something as large as a space or as small as an individual tool. With that flexibility in mind, Studio Share resource management should handle:
- Resource creation, modification, and deletion.
- Ownership associated with a user or a user role.
- Fields for description, images, specifications, etc.
- Reservation creation, modification, and deletion.
- Association with a calendar for scheduling.
- Reservation requirements based on user qualifications.

## Events
As makerspace resources are often reserved for a specific period of time, we need to be able to schedule events. These events might be classes, open studio time, or reservations for a specific resource like a tool. In order to keep the scope of Studio Share specific to makerspaces, events must be associated with a specific resource. However, they may be created as a draft to help with planning. 

Requirements for events include:
- Event creation, modification, and deletion.
- Draft events which do not block out time on specific resources.
- User registration for events.
- View and export of event data with flexible scope, for example:
	- All events in a time period.
	- Events associated with a specific resource.
	- Events associated with a specific user.
- Event costs, if any.

## Payment and Billing
As an all-in-one solution for makerspaces, Studio Share should integrate with payment processing providers to handle membership dues, event registration fees, and material costs. Ideally this integration should be generic and modular, allowing the organization to customize the payment process to suit their needs. Features should include:
- Generic internal model for billing data.
- Modular integration with third-party payment services.
- Authorize.net module (for BARN).

## Administration and Reporting
Users with adequate administrative roles should gain direct access to query and modify Studio Share data as needed. These administrative tools should include:
- Accommodate one or more data instrumentation tools such as Metabase
- SQL queries of database.
- Backup and import of database.
- Security access system synchronization with user roles.