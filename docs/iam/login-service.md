# Login Service

> The purpose of this section is to identify the building-block, its role in the architecture, and its relationship to the other building-blocks expressed through the interfaces it provides and consumes. The idea is to provide a singular entrypoint to the EOEPCA building-blocks.<br>
> In the first instant, gather relevant information from existing docs/wikis where it exists, and collate here.<br>
> Use dedicated markdown files to separate the sub-section content if needed.<br>
> Use diagrams where useful.

## Description

> Description to include:
> 
> * role in the architecture
> * functional capabilities

## Interfaces

> Specification of interfaces provided by the component.<br>
> Link to external specifications if applicable.

### OpenID Connection (OIDC)

Interface for the authentication of end-users.

Ref. https://gluu.org/docs/gluu-server/4.1/api-guide/openid-connect-api/

* **Discovery**
    * `/.well-known/openid-configuration`
        * `GET`: Get configuration
* **Authorization**
    * `/oxauth/restv1/authorize`
        * `GET`: Request end-user authentication
        * `POST`: Request end-user authentication
* **Token Endpoint**
    * `/oxauth/restv1/token`
        * `POST`: Obtain access token, ID token, refresh token
* **Client Info**
    * `/oxauth/restv1/clientinfo`
        * `GET`: Request info regarding client claims
        * `POST`: Request info regarding client claims
* **Client Registration**
    * `/oxauth/restv1/register`
        * `GET`: Retrieve client metadata
        * `POST`: Register new dynamic client
        * `PUT`: Update client metadata
* **End Session**
    * `/oxauth/restv1/end_session`
        * `GET`: Request end session
* **User Info**
    * `/oxauth/restv1/userinfo`
        * `GET`: Retrieve claims about the authenticated end-user
        * `POST`: Retrieve claims about the authenticated end-user

### User Managed Access (UMA)

Interface for the protection of resources by resource servers.

Ref. https://gluu.org/docs/gluu-server/4.1/api-guide/uma-api/

* **Discovery**
    * `/.well-known/uma2-configuration`
        * `GET`: Get configuration
* **Token Endpoint**
    * `/oxauth/restv1/token`
        * `POST`: Request RPT
* **Resource Registration**
    * `/oxauth/restv1/host/rsrc/resource_set`
        * `GET`: List resources
        * `POST`: Create resource
    * `/oxauth/restv1/host/rsrc/resource_set{rsid}`
        * `GET`: Get resource
        * `PUT`: Update resource
        * `DELETE`: Delete resource
* **Permission Registration**
    * `/oxauth/restv1/host/rsrc/resource_set`
        * `POST`: Register resource permission
* **Token Introspection**
    * `/oxauth/restv1/rpt/status`
        * `POST`: Token introspection

### System for Cross-domain Identity Management (SCIM)

Interface for retrieving and manipulating user data.

Ref. https://gluu.org/docs/gluu-server/4.1/api-guide/scim-api/

* **Users**
    * `/identity/restv1/scim/v2/Users`
        * `GET`: Search users based on filter criteria
        * `POST`: Create user
    * `/identity/restv1/scim/v2/Users/.search`
        * `POST`: Search users based on filter criteria
    * `/identity/restv1/scim/v2/Users/{id}`
        * `GET`: Retrieve a user by ID
        * `PUT`: Update a user
        * `PATCH`: Modify a user
        * `DELETE`: Delete a user
* **Groups**
    * `/identity/restv1/scim/v2/Groups`
        * `GET`: Search groups based on filter criteria
        * `POST`: Create group
    * `/identity/restv1/scim/v2/Groups/.search`
        * `POST`: Search groups based on filter criteria
    * `/identity/restv1/scim/v2/Groups/{id}`
        * `GET`: Retrieve a group by ID
        * `PUT`: Update a group
        * `PATCH`: Modify a group
        * `DELETE`: Delete a group
* **FIDO Devices**
    * `/identity/restv1/scim/v2/FidoDevices`
    * `/identity/restv1/scim/v2/Fido2Devices`
        * `GET`: Search FIDO devices based on filter criteria
    * `/identity/restv1/scim/v2/FidoDevices/.search`
    * `/identity/restv1/scim/v2/Fido2Devices/.search`
        * `POST`: Search FIDO devices based on filter criteria
    * `/identity/restv1/scim/v2/FidoDevices/{id}`
    * `/identity/restv1/scim/v2/Fido2Devices/{id}`
        * `GET`: Retrieve a FIDO device by ID
        * `PUT`: Update a FIDO device
        * `PATCH`: Modify a FIDO device
        * `DELETE`: Delete a FIDO device
* **Bulk Operations**
    * `/identity/restv1/scim/v2/Bulk`
        * `POST`: Apply bulk operation
* **Search**
    * `/identity/restv1/scim/v2/.search`
        * `POST`: Search resources based on filter criteria
* **Service Metadata**
    * `/identity/restv1/scim/v2/ServiceProvider`
        * GET: Retrieve information about the capabilities of the server
    * `/identity/restv1/scim/v2/ResourceTypes`
        * GET: Retrieve information about the types of resources available in the service
    * `/identity/restv1/scim/v2/Schemas`
        * GET: Retrieve the schemas in use by available resources

## Dependencies

> Describe links with other eoepca components - e.g. interfaces consumed.

## Additional Information

> Include descriptions of anything that is relevant to help users of the component.<br>
> Links to other relevant information.
