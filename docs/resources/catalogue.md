# Resource Catalogue [TODO]

> The purpose of this section is to identify the building-block, its role in the architecture, and its relationship to the other building-blocks expressed through the interfaces it provides and consumes. The idea is to provide a singular entrypoint to the EOEPCA building-blocks.<br><br>
> This section describes the Resource Catalogue building-block. The relationship of the Resource Catalogue to other components is described in the <a href="../../system/overview/">System Overview</a>.



## Description

> The Use Cases for the Resource Catalogue are described below.

![EOEPCA Resource Catalogue Use Cases](../../img/resources/EOEPCA-Resource-Cat-Use-Cases.drawio.png)

> * Publish Metadata. Metadata can be an input or output for the ADES ( Application Deployment & Execution Service).
> * Publish Product. Metadata relating to a product and containing a reference to that product.
> * Publish Processing Service. Metadata describing a Processing Service.
> * Publish Interactive Application. Metadata describing the needs of an Application.
> * Publish Collection.  Metadata describing a collection of Metadata.
> * Compliance. Metadata compliance required before it is published. 
> * Search Metadata.  Find desired Metadata.
> * Search Temporally. Time based search. 
> * Search by AOI. Area of Interest based search. 
> * Search Input for Data Processing. Input required by a process in the ADES.
> * Search Parameters for Processing. Parameters required to help configure a process in the ADES.
> * Authorisation. This may be requites to perform Publish and Search based Use Cases.

## Interfaces

> The following interfaces are used by the Resource Catalogue.
> 
> * Publishing and Search
>     * OGC CSW 3.0.0 and 2.0.2 interfaces
>     * Certified OGC Compliant and OGC Reference Implementation for both CSW 2.0.2 and CSW 3.0.0
> * Search
>     * OpenSearch
>     * OGC API Records
>     * OGC OpenSearch Geo and Time Extensions
>     * OGC OpenSearch EO Extensions
>     * STAC (SpatioTemporal Asset Catalog)
>     * Federated catalogue distributed searching
> * Metadata
>     * Implements ISO Metadata Application Profile 1.0.0
>     * Support for ISO-19115-1 and ISO-19115-2  (Geographic information)
> * Ingestion
>     * Harvesting support for WMS, WFS, WCS, WPS, WAF, CSW, SOS

## Dependencies

> The Resource Catalogue is designed to support the ADES component.

## Additional Information

> Please refer to the latest <a href="https://github.com/EOEPCA/eoepca/tree/develop/release-notes">EOEPCA release notes</a> for more information. 
> 
> The Use Cases above were derived from the EOEPCA <a href="https://eoepca.github.io">Use Case Analysis Document</a>.

