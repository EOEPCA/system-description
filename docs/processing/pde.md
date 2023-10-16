# PDE - Processor Development Environment

> The purpose of this section is to identify the building-block, its role in the architecture, and its relationship to the other building-blocks expressed through the interfaces it provides and consumes. The idea is to provide a singular entrypoint to the EOEPCA building-blocks.<br>
> In the first instant, gather relevant information from existing docs/wikis where it exists, and collate here.<br>
> Use dedicated markdown files to separate the sub-section content if needed.<br>
> Use diagrams where useful.

The Processor Development Environment (PDE) provides integrated web tooling to perform interactive analysis and to develop, test and package apps for ADES execution. It provides an environment that seeks to replicate the conditions an application experiences when running in the ADES on a platform.

## Description

> Description to include:
> 
> * role in the architecture
> * functional capabilities

The PDE comprises two main parts:

* **JupyterHub Instance**<br>
  Provides the multi-user entrypoint through which the user logs-in and from where their interactive environment is spawned.
* **PDE Container**<br>
  Provides the interactive environment, an instance of which is spawned for each authenticated user.

### JupyterHub

The entry-point to the PDE service is provided through an instance of [JupyterHub](https://jupyter.org/hub) - as described at [https://jupyterhub.readthedocs.io/en/stable/](https://jupyterhub.readthedocs.io/en/stable/).

For EOEPCA, the PDE is designed for deployment to Kubernetes via the [PDE helm chart](https://github.com/EOEPCA/helm-charts/tree/main/charts/pde-jupyterhub), that is based upon the ['Zero to JupyterHub with Kubernetes'](https://zero-to-jupyterhub.readthedocs.io/en/latest/) distribution that is provided at [https://zero-to-jupyterhub.readthedocs.io/en/latest/](https://zero-to-jupyterhub.readthedocs.io/en/latest/).

At the core of the distribution is the JupyterHub `jupyterhub/jupyterhub` container image - see DockerHub [https://hub.docker.com/r/jupyterhub/jupyterhub](https://hub.docker.com/r/jupyterhub/jupyterhub). In the `jupyterhub/jupyterhub` image, the JupyterHub service is configured via the file `/srv/jupyterhub/jupyterhub_config.py`.

JupyterHub spawns a service instance for each user that logs in to the hub. Instances can be spawned as containers using the `DockerSpawner` or `KubeSpawner`. In the case of EOEPCA the `KubeSpawner` is used. The spawner is configured via the `jupyterhub_config.py` file.

Access to the spawned 'single-user servers' is proxied via the JupyterHub entry-point. Thus, all access to the hub and the associated user PDE sessions is made through the hub and its proxy.

More details regarding the [JupyterHub architecture](https://jupyterhub.readthedocs.io/en/stable/reference/technical-overview.html) are available at [https://jupyterhub.readthedocs.io/en/stable/reference/technical-overview.html](https://jupyterhub.readthedocs.io/en/stable/reference/technical-overview.html).

### PDE Container

The PDE container is an implementation of the so-called 'single-user notbook servers' that are designed to be spawned by JupyterHub for each authenticated user. Typically these single-user-servers are based-upon a JupyterLab instance. For the PDE a base JupyterLab container is enriched to provide additional tooling - for example the Theia IDE.


## Interfaces

> Specification of interfaces provided by the component.<br>
> Link to external specifications if applicable.

### JupyterHub Configuration

The JupyterHub service is configured via the file `/srv/jupyterhub/jupyterhub_config.py`:

* **Basics:** [https://jupyterhub.readthedocs.io/en/stable/getting-started/config-basics.html](https://jupyterhub.readthedocs.io/en/stable/getting-started/config-basics.html)
* **Detailed:** [https://jupyterhub.readthedocs.io/en/stable/reference/](https://jupyterhub.readthedocs.io/en/stable/reference/)

### PDE Container Configuration

> TODO

## Dependencies

> Describe links with other eoepca components - e.g. interfaces consumed.

## Additional Information

> Include descriptions of anything that is relevant to help users of the component.<br>
> Links to other relevant information.
