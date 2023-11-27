# ADES

## Description

The Application Deployment & Execution Service (ADES) forms a critical component within the Earth Observation Exploitation Platform Common Architecture (EOEPCA) functioning as a hosted execution engine, empowering users to initiate and manage processing jobs efficiently. By enabling the use of applications either self-developed or sourced from the platform community, ADES serves as a versatile tool for data processing and management.

Within the broader EOEPCA ecosystem, ADES plays a pivotal role. It aligns with the overarching goal of the EOEPCA to facilitate advanced Earth observation technologies and data exploitation. By providing a robust and user-friendly platform for deploying and executing applications, ADES enhances the capacity of users to process, analyze, and utilize Earth observation data effectively. This alignment with the EOEPCA's objectives underscores the importance of ADES in advancing Earth observation technology and its applications.

The ADES utilizes the Common Workflow Language (CWL) to describe and manage EO application packages. CWL offers a standardized, flexible way to define and execute workflows across various computational environments. 
In ADES, CWL is used to create detailed blueprints of EO applications, outlining parameters, dependencies, and required computational steps. This approach ensures that EO applications, whether written in Python, R, Java, or other programming languages, are packaged and executed consistently and reproducibly across different platforms. The use of CWL in ADES simplifies the process of deploying complex workflows and ensures that these workflows are portable and adaptable to various execution contexts, such as local machines, cloud resources, or high-performance computing environments.

## Functionalities 

The ADES has two distinct functionalities, one for deployment and another for execution that work in tandem to provide a streamlined process for deploying and executing EO applications. 

* Deployment: Used for deploying EO applications by handling the submission of application packages, which are described using CWL. This involves specifying parameters, software items, executables, dependencies, and metadata. The deployment interface is responsible for setting up these applications in the ADES environment, ensuring they are ready for execution.

* Execution: Once the applications are deployed, the execution is used to initiate and manage the processing jobs. Users interact with this functionality to execute the deployed EO applications, providing necessary input parameters and initiating the processing tasks. The execution interface manages the running of these applications, handling task scheduling, monitoring, and the retrieval of outputs.


## Interfaces

OGC API - Processes Part 1 and Part 2 are critical components of the Open Geospatial Consortium (OGC) standards, providing guidelines for the execution and deployment of computational processes in geospatial and EO applications. While OGC API Processes Part 1 addresses the execution of processes, Part 2 delves into the deployment of these processes. This includes the standards and protocols for uploading and managing process descriptions, setting up new processes, and configuring process environments within a service like ADES. By defining a consistent and interoperable approach, Part 2 ensures that the deployment of processing tasks in geospatial and Earth Observation contexts is streamlined, efficient, and compatible across different platforms and services.

The ADES follows specific standards for its deployment and execution interfaces as defined by the OGC API Processes:

* Deployment Interface: The ADES deployment interface is defined in the OGC API Processes Part 2. This part of the standard outlines the protocols and methods for deploying Earth Observation applications within the ADES framework.

* Execution Interface: The execution interface of ADES is aligned with the guidelines set in OGC API Processes Part 1. This section specifies the standards for executing the deployed applications, detailing how users can initiate and manage processing jobs within the ADES environment.


## Dependencies

The ADES can interact with other EOEPCA building blocks but has no dependencies 

## Additional Information

* [Zoo-Project](https://www.zoo-project.org/)
* ZooCalrissianRunner:
  * [Software Repository](https://github.com/EOEPCA/zoo-calrissian-runner)
  * [Documentation](https://eoepca.github.io/zoo-calrissian-runner/)
* [Default processing service template](https://github.com/EOEPCA/proc-service-template)

