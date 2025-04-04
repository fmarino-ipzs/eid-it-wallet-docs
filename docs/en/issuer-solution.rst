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
   
  - **Authentic Source Integration**: Provides API Services to retrieve verified User data from authentic sources.
   
  - **Credential Lifecycle Management**: Handles Digital Credential registration, status tracking, and revocation processes.
   
  - **Trust & Security Component**: Manages keys, certificates, and security monitoring to ensure the integrity of the issuance process.


The following diagram depicts the Issuer Solution High Level Architecture.

.. figure:: ../../images/issuer-solution.svg
   :width: 100% 
   :alt: The image illustrates the Issuer Solution and its relations and interactions within the ecosystem.
   :target: https://www.plantuml.com/plantuml/svg/fLRVRzis47xtNt5LXoK6chhvaS8PKA2kdMu6qiQBa-vHeAMpJ4GIDPAoumtxttUaQCkqN4_e_2ABlFlkk-FTHtrKcabTPcdd18PNC1HP8NBCDSIS9P9bC1SInagLA64gqb9paSD0HWkkCTAbnCuhdaTf6ICij2xKBxsUPAkt2TUBSbOgb978DU6zZKJMArAMcrXdIiSfd_M6LsSJi_JqvQwNCQLHqbAuvV2sCBo8s0ZdF4UOJXx6ZxVJpgkuUXyFxxy-FTor2ApBWiNoiYR0QVTiJXPdgf1SetBnwsmSU8_SCv5RAirDYy1Mg4I6PzUz2ANcSnunZUqSOgRPZAcMrgc8djjPclnLIyuYQMb9c4kKxMoVSTsUQJjB7eSHat4xOto95YnFC6IfRdaKg9wrABOzDooL5XaelKvHTGPnV9jYXhb-PCbfW2yQPSxIu0tyD4k68XNoG_3wnlxCci5sgoipATPEo1YbMqqaheFkFYorOiRasaSzFt_VdyMjK5-_crtr-rTDO8NKxt43-dqqkxoSjuE-OltBYnk2Fe46k5po29MFZJSpOjuEcrtqpy_VDMbhMIhjm_O7bpVzp-rWhwylBgy715jBY5uWi4WBgO3bCMpE4THQQSnKPu9IYVpKTEKR29xe4T2pMeM5I6EU9p3Y2TVaD9GO4rNEKfjxfIGV0Zjy57LgCSFR5tswOccAEkIvqYoFa23_i2imTYk1YtQYOFnuLcqQJCqIzS5hjqqKDmv-d9nfBiWmH1uJubVt2ZWUGMKMx2x7BX5kqz1hLuRZWMcq_Q2ir0lZ7uLAbD9cDzWimTGkgS0j2iAWw4i48tsWtExHW1kHzAFQtWYfTeH9u8_c5GRsrGHx44A3c8CrivSOCQfh2vynHcdhS3puZgJlDrBZMfo9qWvPvvFxSygjHQYS1V5gziu-JD25lpj0FozMndWEqUPcLCQWlgmtSURItddcw3-xlxLHOBeEP-36jHe0qtEmSREjBiMInsOtZddL9hM7NaXH9WjWG42LBoTFEMSHmgafChwmh4WHfWknKhrlAAbsg7fVMCuIUZxWdoKgVMY2klKvE1dqUg1Ivw1h4tVbSONxnA9db-dXwaJRA65LACgpKN-_KFS5vkFHrRVXEAYCcNOLimZgK0QW1LI33jMWUvtj9DXFgxfIWwvFs4vKMEtLS_ENxLQOscNBqMnSc7-_4R4K5MmdqPfQkinpdgTYzOES9APh4h-mO5AlpO1Lxp0nxuUBDu4Ut8z7GtfC1r_kWbrXiFMqIWahhXVWIPLJuwgb9kDH5uIipEYbMZtzlNix67H_A9U6OeMcYvDA3Wwe5uphRPl4P0pJ-jAZKcZ9SUaIgfIDPYghpwCMkgDqTxzQQjBDBaxv7ADrbABVo7URPQZcBNFduRZkTaeD1X8JhlGcUQMPBjKRspiIboBQqqYhfvv0YaGrk5RYh30goMYzbUUVOUgMd6sJe5CAe5k6MEoeh-EqmOHCv5mBIIruX9pvOYPo_-m9jyJKfgKMl50TwcHtuJUlQT8uarrjqbJQXeb_2VijRxlOMJUY7T8ffvZA7KY4VFaTzIcL6STQkBuNnHUN-vbcjBUd4mvhK5go5iUV_-D9khbsgJQT6vp-oz_ZlAz4trZAuwtVzcF6kJQAkby1TqdjbK1zt_tW8DQTQytY0qTq1DAV5zTKzgibakj2YqIoOi4Z40NA1hqcbwFwvi2NLTfnBLSEygXp0zgJloschuER5chCpl-ff8KCdvgVM7iVXkv3pztUecftJ_HsLMRBzmH-bQ8igCyKa0EFSUzpWomCWT66mAnQFZp5Gv7Rk8HysCrloZOEZJ6eNU1ea2EDqIBguIDhu-dtkE_paIpABFqN
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


