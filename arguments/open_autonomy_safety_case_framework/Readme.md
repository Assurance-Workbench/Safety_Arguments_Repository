# Open Autonomy Safety Case Framework

The goal of the Open Autonomy Safety Case Framework (OASCF) is to support safety engineers in developing a safety case in compliance with UL 4600 that argues that the system is developed in compliance with relevant standards mentioned by UL 4600, such as ISO 26262 and ISO 21448.  

OASCF is open, meaning that it is implementation agnostic and can be used in different projects, implementing AVs for different use cases. 

## Application Domains

Whereas the framework scopes automotive systems, UL 4600 also recommends following best practices from other industries, such as aerospace (Federal Aviation Administration (FAA) documents) and military (MIL-STD-882E). OASCF establishes how to implement a safety management system, communicate risks to stakeholders, and navigate relevant standards and regulations. 

## Argumentation Strategy

The top-level claim of the templated high-level structured argumentation strategy is “The autonomous driver is safe enough to operate in the considered operational design domain”. An autonomous driver is a system embedded in a vehicle, which navigates and operates the vehicle without human intervention. An autonomous driver uses various sensors, such as cameras, radars, and lidars, to perceive the operating environment of a vehicle, make decisions, and perform driving tasks without human input. Autonomous drivers can have different levels of automation, ranging from Level 0 (no automation) to Level 5 (full automation). Implementing the PTB approach, the OASCF relies on three pillars of argumentation (see figure below). 

- Arguing about having confidence in the safety argument given the employed processes in the organisation;

- Arguing that the system is safe by design, namely that the system was engineered and tested using rigorous processes while considering the identified hazards;

- Arguing that the hazards uncovered during system operation are appropriately addressed.

![OASCF top-level diagram](./figures/oascf_g1.jpg)

## Read more

More about OASCF can be found [here](https://arxiv.org/abs/2404.05444).
