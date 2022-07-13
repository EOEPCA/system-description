# Data Access [TODO]

> The purpose of this section is to identify the building-block, its role in the architecture, and its relationship to the other building-blocks expressed through the interfaces it provides and consumes. The idea is to provide a singular entrypoint to the EOEPCA building-blocks.<br><br>
> This section describes the Resource Catalogue building-block. The relationship of the Resource Catalogue to other components is described in the <a href="../../system/overview/">System Overview</a>.



## Description

> The Use Cases for Data Access are described below.

![EOEPCA Resource Catalogue Use Cases](../../img/resources/EOEPCA-Resource-Data-Access-Use-Cases.drawio.png)

> * Get Data 


## Overview

> The high level design is described below.

![EOEPCA Resource Catalogue Use Cases](../../img/resources/EOEPCA-Resource-Data-Access-Deployment-Diagram.drawio.png)


## Interfaces

> The following interfaces are used by Data Access.
> 
> * Get Data
>     * OGC WMS 1.1 - 1.3 interfaces
>     * OGC WMTS 1.0 interfaces with automatic caching
>     * OGC WCS 2.0 interfaces with EO Application Profile

## Dependencies

> The Data Access component is dependent upon the Catalogue and the S3 bucket.

## Additional Information

> Please refer to the latest <a href="https://github.com/EOEPCA/eoepca/tree/develop/release-notes">EOEPCA release notes</a> for more information. 
> 
> The Use Cases above were derived from the EOEPCA <a href="https://eoepca.github.io">Use Case Analysis Document</a>.
