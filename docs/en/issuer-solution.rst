.. include:: ../common/common_definitions.rst

.. _issuer-solution:

Issuer Solution
+++++++++++++++

An Issuer, as an Organizational Entity participating in the IT-Wallet ecosystem, MUST provide technical Solutions (Issuer Solution) that combine software, hardware, services, settings, and configurations to issue Digital Credentials to User Wallet Instances in a secure and trusted manner.

Logical architecture is composed of the following elements:

- **Trust Anchor**: It represents the root of trust for the entire IT-Wallet Federation and allows Issuers to federate in the ecosystem. The Trust Anchor has PKI capabilities and issues Digital Certificates during the Issuer onboarding process.
- **Digital Credential Issuer Solution**: Organizational Entity that provides the services and components required for issuing Digital Credentials to Users through their Wallet Instances. This solution includes:
   
  - **Frontend Component**: Provides additional services through a Web User interface, allowing Users to view, verify, manage, and request Digital Credentials.
   
  - **Credential Issuer Component**: Creates and issues Digital Credentials to Wallet Instances following the Issuance Flow as defined in Section :ref:`pid_eaa_issuance.rst`.
   
  - **Authorization Server**: Handles authentication and authorization flows as specified in OAuth 2.0, managing access tokens, refresh tokens and authorization codes required during the Digital Credential issuance process.
   
  - **Relying Party Component**: Authenticates Users either with National eID systems (for PID issuance) using OIDC, or SAML protocols, or with PID (for (Q)EAA issuance) using `OpenID4VP`_ protocol (see Section :ref:`Remote Flow` for technical details).
   
 - **PDND e-Services**: Authorized digital services accessing/exchanging data through national interoperability platform.
   
  - **Credential Lifecycle Management**: Handles Digital Credential registration, status tracking, and revocation processes.
   
  - **Trust & Security Component**: Manages keys, certificates, and security monitoring to ensure the integrity of the issuance process.

The following diagram depicts the Issuer Solution High Level Architecture.

.. figure:: ../../images/issuer-solution.svg
   :width: 100% 
   :alt: The image illustrates the Issuer Solution and its relations and interactions within the ecosystem.
   :target: https://www.plantuml.com/plantuml/svg/lLTlRzj63t_lJy6g3vucG5CtVr8a0mhKiTFDGzfuSTAzDCuIBHyYwRIxanDls7SVJtUA99-I2XsmlB748t_yaI9vp2UbcTH5cWpUmFW4nYBDHOQPXeYpMB8KLaB2LAa29Sn5KcWkCXZ9SCqrXhgGE7Z5ip0f8eIrrhdwQJYKxE5TpFMwM1OAPIWoJNZlGf4EyuHbnjU1qb72byFnoS7CYEw-N0rJfZHA4YqS1xB93IyYDi4Lpn3civlfxULyy2goxzFnzTUxcwiUZdMHiqWUrmGudHwiIED0vP92KSv_7Oq37v9vAZ9BnJii4TW3Af7YmUamHAdvYeTCOp-3Y6csPAgdTYB2-twQ9dxLaxE8UseIvWPbFzrxtFPdsa-JHukGoQYVCZw6QvR5k629xlafKDrhaVTJVc19Wds0XpnJckkoRPxAULmeBL9GUfkW6eoYw3B153Dzo-Az01yroembmLlutp8UYqJ8Zy7hy_BFo0owapwO9YprX8nGEcaiSHlixy9IbQTCRjkeXuSVpfPHBzJNxvSdPsSdFh32K6IH1_qXN1uVh_f1dx2puwDpWdu37hZSy11L6nlFbyIy7pOxEZiyVE_Jrh9GkWrxDZe-F_lS3_RqzEZuT4ImzNJIQmGMQY4Li2o2wZk2sYgDgHhCK2gHxPc2Vml17Vq4z6kbi1P9nBCO9Zpccep64YEYobbIncw7rCV062loEYyn5vUFUi-MuiBK6Sj29CZVImbCdIHmtjuecDuUs4E3gLciFhRAhVBYEgtj9sEcXbcoG1uHubVt2ZYTW5KBckB81SBBCFJMfU5bnpGrsavPeTV6FbmeKSWokb4bWdafKe4J2i8Wxni4CrL1kTCN7LRpj-srh8q5vOum2VpMlCAeV3NEReJG85PGgfNt8p6gSmkVCK9Pvk5bvutRmezweTTSHekSaGwgEiG_CO9RSmGpUsGOmQz5n4FE4Y0oyo8tNQE4tCA5Y3ZQUhp2cCwPInJ_NcOQSwkptd8fDfpYhEjjvYH1csnL25Kh0mj3L8gAlHhIz6W_cLvBKSHhg4eDU4R418N3bZmnHPGdJ5F2qtSlaxSSYNUxFRqzPYcASdGDBjp37Yyr5iffK2X-H-x21Flmrm3eh-KhPJo3i5fbb56ejwlApqgMIuffgC_kiLOAJ6vnsSWSdPfEXihCQBYqqsaKSPktsgBAA0C3P6njJbSiHDWpfOkFBCqJXFbQFAZXDvHKaQY6NrZ6OlgzmJyALBfhBktNty1TBirFuAxJOByCtAN79Uw2XVSkqkxiX4zU5ZPH5AUV_rQYhdFCffEJR-DfO9MPTXah4LHN1A05s581DpwRNU4kjdPOTWToKLK4NCVQiqRrbsKCSsjYE9g38_Fq2n5B3Bzgc5bLGvUrZ5U9UFX1JXAJBRLMEKAsPcpPTvYPz-xapM08rzF9c7xceozNGNFSblaixnzuu7eDhGl0tN6sf6RJoJu8QTNenKhtVjk_78tsVooMFCgY1LPbRQf-ydK2U31tafBfR0hL-tyyWpf3QQwWTK1-XITyXU4sJB1Tv5UL66mlfkvRkH2RLLI3WSIOAosP7LvACrrGkaYFJZOYRDzARWbgNaaYLXvNUnrIZ0KfRPyknF_3t8cSha_GJH6WUvrODEuxnwd2X5HaN0j9N-45SkRV7oBtzyvGbvYKOQarpzM0gjojMFvYHFFFH5UhU5FOLsckFLuxc0ftsfwthXdcfgbo7oH4ldbcCXMcEA4UQizvQG-UwwLcTBOpGnoMeKum1cTtDlX1-ZtlGlMDFKxViszntfrItrZ2eoUxf_NHcNf9tSs0ky1sKg2UD-zinBfoIxMeunEz0EdrYocgSayCvJRN8fOiN_CGp53nwFbSlDbNmcrie96TMbJ1gGFnQlhVH7Z13UGkWuwj_0QrvBXf4ZFVhyMk6ypV9wTcuh9GDujcSTUv5U-2-RO3P-qjTZjBlblQtSuWN2CrnsbpVhcGp2JwMOeYfmfMG0OKmSwIGng6mAGYiBJYxlam5bdfbv2xpThbtiV0Qx3Q19wpyTBQmqztcVMmzFgbPVE9D8eq-GS0
      Issuer Solution High Level Architecture

Issuer Solution Requirements
============================

This section lists the requirements to be met by Digital Credential Issuer Solutions.

- The Issuer Solution MUST register with the Federation Authority to obtain a Registration Certificate that explicitly authorizes which Digital Credential types and specific attributes may be issued.
- The Issuer Solution MUST implement secure mechanisms for creating and issuing Digital Credentials, ensuring the integrity and confidentiality of the issuance process.
- The Issuer Solution MUST communicate with Authentic Sources to obtain verified User data for Digital Credential issuance through secure, trusted and reliable API Services.
- The Relying Party Component MUST be properly federated within the national eIDAS digital identity ecosystem when acting as a PID Provider.
- For PID issuance, the Relying Party Component MUST authenticate Users with LoA High using the national Digital Identity Providers.
- For (Q)EAA issuance, if User authentication is required, the Relying Party Component MUST authenticate Users by verifying a valid PID from the User's Wallet Instance using `OpenID4VP`_, as defined in Section :ref:`Remote Flow`.
- The Credential Lifecycle Management Component MUST implement proper procedures for Digital Credential management, including issuance, status tracking, revocation, and renewal (see :ref:`Digital Credential Lifecycle` for more technical details).
- The Trust & Security Component MUST maintain an audit trail of Digital Credential issuances while respecting privacy requirements and data protection regulations.
- The Credential Issuer Component MUST issue Digital Credentials that support Selective Disclosure.
- The Issuer Solution MUST periodically renew its trust with the Federation to maintain its ability to issue Digital Credentials.
- The Issuer Solution MUST authenticate to Wallet Instances during the issuance flow to prove the legitimacy and authorization of its issuance capabilities.
- The Credential Issuer Component MUST support immediate issuance flow and MAY also support deferred issuance flow to accommodate various operational scenarios.
- The Issuer Solution MUST implement appropriate error handling and User notifications for all Digital Credential issuance processes.
- The Frontend Component MAY provide additional web services to allow Users to view, verify, manage, and request Digital Credentials through a Web User interface.
- The Frontend Component MUST implement User authentication with a Level of Assurance (LoA) at least equal to that used to obtain the Digital Credential being issued.
- The Frontend Component MUST provide appropriate security measures to protect User data and Digital Credential information displayed in the web interface.

.. _issuer-components:

Digital Credential Issuer Solution Components
=============================================

Frontend Component
------------------

The Frontend Component SHOULD provide a web-based User interface that allows for additional services related to Digital Credentials, such as:

- Display issued Digital Credentials and their status.
- Verify that the issued Digital Credentials are valid and authentic.
- Manage Digital Credential lifecycle (i.e. revocation).
- Initiate Digital Credential issuance through User interfaces by generating Credential Offers to be scanned by Wallet Instances.
- Provide user support and documentation for Digital Credential usage.

The Frontend Component MUST implement User authentication with a Level of Assurance (LoA) at least equal to that used to obtain the Digital Credential itself. For instance, if a Digital Credential was issued after authentication with LoA High, any subsequent access to manage that Digital Credential through the Frontend Component must also require authentication with LoA High.


Credential Issuer Component
---------------------------

The Credential Issuer Component MUST be based on the OpenID for Verifiable Credential Issuance specification [`OpenID4VCI`_] following the implementation profile defined in Section :ref:`pid_eaa_issuance.rst`, and it MUST be responsible for:

- Creating and issuing Digital Credentials to Wallet Instances.
- Implementing the Credential Issuance protocols and flows (see Section :ref:`pid_eaa_issuance.rst` for technical details).
- Processing Digital Credentials requests from Wallet Instances.
- Requesting and obtaining User Data from the Authentic Source through secure, trusted and reliable API Services.
- Generating properly formatted and signed Digital Credentials.
- Supporting different Digital Credentials formats, i.e. SD-JWT-VC, mDoc-CBOR, (see Section :ref:`pid_eaa_data_model.rst` for more details).


Authorization Server
--------------------

The OAuth2-based Authorization Server MUST handle:

- Authentication and authorization flows for Digital Credential issuance.
- Managing access tokens and authorization codes.
- Validating User identity confirmed by the Relying Party Component.


Relying Party Component
-----------------------

When the User authentication is required, the Credential Issuer MUST provide a Relying Party Component. This component MAY handle User authentication through multiple protocols (OpenID4VP, OIDC, SAML) and has dual functionality:

- For PID issuance: It MUST authenticate Users with the national Digital Identity Providers, based on OpenID Connect Core 1.0 or SAML2 protocols.
- For (Q)EAA issuance: It MUST authenticate Users by requesting presentation of a valid PID from their Wallet Instance. This component acts as a web Relying Party Instance by sending a presentation request to the Wallet Instance, according to [`OpenID4VP`_].


PDND e-Services
----------------------------

This component MUST: 

- Establish secure connections with Authentic Sources.
- Implement appropriate authentication and authorization for these connections.
- Format and prepare the retrieved data according to Digital Credential schemas.
- Retrieve verified User data from authoritative registries and databases.
- Provide the Authentic Source with cryptographic evidence of User authentication, when required by the Authentic Source.

.. note::
   In case of public Authentic Sources, a Credential Issuer MUST use PDND according to the rules defined in Section :ref:`e-Service PDND <e-service-pdnd>` and in Section :ref:`Status Update by Authentic Sources <Status Update by Authentic Sources>`. See also Section :ref:`Authentic Source Catalogue <authentic_source_catalogue>` for additional details.

.. _issuer-solution-credential-lifecycle-management:

Credential Lifecycle Management
-------------------------------

This trust-related component MUST handle the entire lifecycle of issued Digital Credentials, including:

- **Credential Status Management**: Maintaining and updating the validity status of Digital Credentials
- **Revocation Processes**: Implementing mechanisms to revoke or suspend Digital Credentials when necessary, according to Section :ref:`Digital Credential Lifecycle`.
- **Renewal Workflows**: Managing the renewal of Digital Credentials according to the mechanisms defined in Section :ref:`pid_eaa_issuance.rst`.

Trust & Security Component
--------------------------

This component MUST ensure the security and trust of the Issuer Solution by:

- Managing cryptographic keys and certificates.
- Implementing audit logging for security events.
- Monitoring for and responding to security incidents.
- Ensuring compliance with security requirements of the IT-Wallet Federation.


Interaction Patterns
============================================

The Digital Credential Issuer Solution supports several interaction patterns between its components and external entities:

1. **User to Frontend Component**: Direct web-based interactions where Users can request Digital Credentials, view status, and manage their Digital Credential portfolio.

2. **Frontend Component to Credential Issuer Component**: Internal interactions that convert User requests into proper `OpenID4VCI`_ protocol messages, including the generation of Credential Offers.

3. **Wallet Instance to Credential Issuer Component**: Direct protocol-based interactions following the Issuance Flow as defined in Section :ref:`pid_eaa_issuance.rst`.

4. **Relying Party Component to National eID/Wallet Instance**: Authentication interactions that verify the User's identity either through national eID systems (for PID issuance) or by verifying the User's PID (for (Q)EAA issuance).

5. **PDND e-Services to Authentic Sources**: Backend API calls to retrieve verified User data from Authentic Sources.

The implementation of these flows and interaction patterns MUST adhere to the security considerations outlined in Section :ref:`pid_eaa_issuance.rst`, including proper handling of tokens, proofs, and cryptographic materials.

.. _issuer-endpoints:

Digital Credential Issuer Solution Endpoints
============================================

The Digital Credential Issuer Solution MUST expose a predefined set of endpoints supporting all the features required for trust evaluation and Digital Credential issuance. 

Federation Endpoints
--------------------

The Issuer Solution MUST provide a Federation Endpoint at the well-known location `/.well-known/openid-federation` that serves the Entity Configuration document as specified in Section :ref:`Entity Configuration of PID/(Q)EAA Providers`. This endpoint enables the establishment of trust relationships within the IT-Wallet Federation and allows Wallet Instances to discover and verify the Issuer.

.. include:: pid-eaa-entity-configuration.rst

Credential Issuer Component Endpoints
-------------------------------------

Credential Issuer Component Endpoints MUST implement the protocols described in the PID/(Q)EAA Issuance Sections (see in Section :ref:`Low-Level Issuance Flow` for technical details).


Frontend Component Endpoints
----------------------------

The Frontend Component MAY implement additional endpoints to support its User interface functionalities:

- User authentication and session management endpoints.
- Digital Credential management endpoints.
- Digital Credential request initiation endpoints.
- Digital Credential offer generation endpoints.
- User profile and preference management endpoints.

These endpoints are meant for direct User interaction through web interfaces and are separate from the `OpenID4VCI`_ protocol endpoints used by Wallet Instances.


