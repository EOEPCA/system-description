# Application Hub

The Application Hub provides integrated web tooling to perform interactive analysis, to develop, test & package apps for ADES execution, and to provide a user-extensible capability for interactive dashboards. This includes a web IDE (Code Server) that provides an environment that seeks to replicate the conditions an application experiences when running in the ADES on a platform.

## Description

The Application Hub is a comprehensive and modular platform delivering SaaS products, designed to cater to the diverse and multifaceted needs of the EO community. It is crafted to support a wide array of stakeholders, from developers and service providers integrating cutting-edge algorithms to researchers harnessing computational power, and analysts requiring clear and concise visualizations. At the heart of the Application Hub is the ability to manage the delivery of work environments and tools for a wide range of user tasks, such as develop, host, execute, and perform exploratory analysis of EO applications, all managed within a single, unified Cloud infrastructure.

The Application Hub, leveraging Kubernetes and JupyterHub, creates a robust, scalable, and user-centric platform for Earth Observation (EO) applications and analytics. Kubernetes ensures scalable operation of containerized applications by managing deployment, operation, and traffic distribution, while JupyterHub orchestrates the launching, scaling, and management of application instances, acting as the primary gateway for user requests. The Hub uses dedicated namespaces for each application pod, ensuring organization, security, and isolation. It also dynamically configures application pods based on the task, and personalizes the experience based on user profiles through Kube Spawner. This design ensures the Application Hub remains modular, scalable, and capable of catering to the dynamic requirements of EO tasks.

Typically, the Application Hub provides access to platforms and web apps in a Software-as-a-Service mode. Users can engage with containerized Interactive Graphical Applications (IGAs), specialized geospatial data exploration web apps, and customizable dashboards. This allows users not only to explore and analyze results but also to execute new applications or analyses and customize their computing experiences, all accessed from the same integrated Hub interface. Ultimately, this enhances user experience, optimizes software usage costs, and promotes ease of use, making it more accessible to the broader EO community.

## Interfaces

The ApplicationHub configuration is documented [https://eoepca.github.io/application-hub-context/](https://eoepca.github.io/application-hub-context/)

## Dependencies

The ApplicationHub can interact with other EOEPCA building blocks but has no dependencies.

## Additional Information

* Application-Hub-Context: 
  * [Software Repository](https://github.com/EOEPCA/application-hub-context)
  * [Documentation](https://eoepca.github.io/application-hub-context/)

* Apps:
  * [PDE with Code Server](https://github.com/EOEPCA/pde-code-server)
  * [JupyterLab](https://github.com/EOEPCA/iat-jupyterlab)
  * [Linux Remote Desktop](https://github.com/EOEPCA/iga-remote-desktop)
  * [QGIS on Remote Desktop](https://github.com/EOEPCA/iga-remote-desktop-qgis)
  * [SNAP on Remote Desktop](https://github.com/EOEPCA/iga-remote-desktop-snap)
  * [STAC Browser](https://github.com/EOEPCA/iga-stac-browser)
  * [Dashboard using Streamlit - demo](https://github.com/EOEPCA/iga-streamlit-demo)