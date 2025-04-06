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
   :target: https://www.plantuml.com/plantuml/svg/lLTjRzis4FxkNt5LXpK1chfvIP4CA537JZSFQUF5IVVHeAMpJ4GIDP9ouWtxxpk-AB9C9nCwOFbYYRnxxhdJSqVcaz9CwYhFUczWU093aPUYm493mbagMGuB8M6iL8KIfYAhD1S536Iyv1fZNKdilU95d5K9mbBhKltKxqlsy2xbUbdDAuKo5eKcl7UnoFjbnWeJwq3f9EFp_l3aO6AMxhvSzNEcD4fQcdaEv5CQNaHiX0jU84mdD-FRosdlLUBUnyFhhtStLnq2wwfaYJnk273QFLYGnO4g9QMYVFmc6m_U9_TS58vAi6aHs0CgaUF1QJz6gVc2nqnZDuU4QJPdggDr9kBxRfOcVzMHiqWxMXBc2cKtstjSTsVQpP8divZ9f9inFiPBLgGuOvdk-2bGtMjHTZD-O5c6NO3xl52QQzisJt8ULagB79HUPwXwWoIvp337Gj-oT2_2HusoO5dq5dwOfqEH2VanUdrk_yoQGVUh3wO9hPsG2Kg_cafSH_lRiAJodCbr6_NmyCFPFEc4-lhz_EJix2G4LXYB8WcWFyJpu-D5D-WJTdPyT4xGRo00boiUesfZu_cSc7V3PaTdXuVlGzfQLagtOSy6n-Tddxl1dfuU7PyE2BQPJdg9m68jf09M951_Hr1hfJ5NlGbA9Oez8_Yt4DtHJqI_RXMM8ajuaSA8froJqr1YGbGvospkRaXzZ8opegXJYpcxVDHxJeepepDMn4YGlziL6FkLo4Txes1yU-0s3QPcgVhOabiTnNTQEqx1Z8PPDaEU4E9N_meu7e4pYpQN4vy8jsdejI_3ou5fQhI3iaelZNyyKwAIDhj1lGHJkwGYloW8WwAl4CnK1ULtNmnOpzzsLAkD6TMEC0dyrhp2mBwQO3T2Q10Bi6RsV2H6JMtXCoOeRHrU3hvnMeHPp_IIosHMCh91rQJu9oPmQxPWuhOC8_YrIdZCMGP4PbgLfckKa6ku40b7fyShJ6cVEHJZ-3AvZRcrKs-b52jEUJPwc_YLg4ss5aBToi3Y69KYiTT3cXxT9zDBAQfq2RNKW1T4J50wRCup8w8oOveAdhzxcRpZIBpRxHdSO-QYigEhT-4VzhYrc2blGQc47RaD4-t3NpsWlrQidF42ulegeun1SxkguooalQIOXlhi7nkZoDGMvnkLertJoL2x6GjVTjfD4kxgrdZK5MLWW8olg-c2nGXxHhhuoF8oGvWknOFgVqD9YaJL_y8AbjBl3VvHeTAxvj9-ymtyuTBgB7USHlisSLyUNxWB5j_xJ7TN9twACdE5eZp3-hSATLrYCHwTV1kE8sVCjA-OHL2xCW0jm4a5_FZSx0f_iBNJSdSWdrLDm7UiszjGlvKnJ9sBuMWsZipJBqGiC_pgOUPC3LtMSbvauk4xEKdCrjHQTeIipTXoxp0nxxkBDu4-N8z7G_gP3hvSHPlZrjRJdZ_mmFKIMWU0F-ESf2RZqJu8wSpenQtk_RP_EHZiVrykPL8aCwnbRLG_-Ze2F9Zw5SjqCeRw_N-UGJjJsRo2DWc52i_u0kDrd65Rv5VrChXUpFstyYbkggW10uafLreoDxoKPhgYSf4TxQn4t3wL_2LeyqWIgGgukkEGSgp8QFrq8Fu8Kx_aRKE2Vee0dUl4OkEyyvngJCX5mRMGz1LU86V-_I5oVsyDTOcPJKijUQbwf79_nGelHZJ_J7QDIJ25GvFDQq_G3aRXtZg8jck6-Mcg_0U9aQ-UcKoL4ISqG-svAEt1SptNZFQsPeZ7CjG9nk1ipuOmoR3dVQgXSy3ft_nRdBUdr3UMyUJ9x-dww5t3ecvLm1zWMoLGpxllRCH6kTOisV69Ne0C-iM8ojuJOxakjKWbAvSy1ZDK0deXbs3sMRYLIpHnKuiKd7kGGDF_9SCBRY2t6UoubT-WbXnNcyJCzsknsmqMtYV7PkAoM6-B9hWJRqE5dbRjixlmMhTrnVTNTdzZ4BwDDeVfvlJo2PavzBCKLKdwLK0En7_hYaCMXi2e9Z1toxkdmr0KDYuXxtPhYRsBGzXUZGiywnEKjKESNIBhuXbqIyld4rbKUVOF
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


Authentic Source Integration
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

5. **Authentic Source Integration to Authentic Sources**: Backend API calls to retrieve verified User data from Authentic Sources.

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


