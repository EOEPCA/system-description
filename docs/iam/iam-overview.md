# Overview

The User Management components are illustrated by the following deployment diagram:

* PROVIDED interfaces above
* REQUIRED interfaces below

![User Management Building Blocks](../../img/iam/iam-deployment-overview.png)

The [Login Service](login-service.md) provides an [OpenID Connection (OIDC)](login-service.md#openid-connection-oidc) interface for end-user authentication, a [User Managed Access (UMA)](login-service.md#user-managed-access-uma) interface for resource protection, and a [System for Cross-domain Identity Management (SCIM)](login-service.md#system-for-cross-domain-identity-management-scim) interface for management of user data.
