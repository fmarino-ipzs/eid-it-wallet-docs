.. include:: ../common/common_definitions.rst


Credential Issuer Solution
==========================

An Issuer, as an Organizational Entity participating in the IT-Wallet ecosystem, MUST provide Technical Solutions (Issuer Solution) that combine software, hardware, services, settings, and configurations to issue Digital Credentials to User Wallet Instances in a secure and trusted manner.

The following diagram depicts the Issuer Solution High Level Architecture.

.. plantuml:: plantuml/ci-solution-architecture.puml
    :width: 99%
    :alt: The image illustrates the Issuer Solution and its relations and interactions within the ecosystem.
    :caption: `Credential Issuer Solution High Level Architecture. <https://www.plantuml.com/plantuml/svg/fLPHRzis47xthxYfmve0pRmsIP42Qr7NIJ4FxUh5QVSeqEHP9Yg96aavyORzznqfAfOinH5QlrWYZzzzT_hkU6-DPTgMMGfJZG9pAraACsDArB1GQMcboc6Y-LfQvBRKEFf1vZmj1SAlqxFnz2oUggnGEPryCnezXKjSoHnXCR-UtLmj6iQsB9ZGfsEkiapbRtfsLYgt9-mMZShmv7pCKLkvafnP760jc6LBPeQOfef_7M1M6jHc24-L334Zj0tg0OPVSJkGtG0pAMBEj1XWYNTypV84OvRQ8Vb6yzMgOe3bBKjJV1HoB7DZfVLwyqAQbiQg38pTfcX64o6kKimmjpSiEOhmpgBEMHezWn-NoLIbIh-EdhpoFxVcaCFghLEkjrDQe0whYSPjTBmFMsYPCRrjepv__l9YAGQXFlbbUNPnSTO5DiXLBZhGB_doz7Gr3FgCNPo-UDM5jfeIrOQzc9o-kdW_3FRy_CNf-OHWTxLhrmYCMwKDi5n0dMimMsCnCwCvQgFo8wV0Pn1zfh-8_gjLMAjKo3o1Ivb8ovfTnJZdXb9iyNNaYukyBZncV7LdZogTn4u7BET8a7_v5PY5bIXuUsfWTdDIRJfConBpkYM9sajGVzjFpgnKP1YZ58JuHtW5d5r2PHOrbqK8HFemx3QauR1Zgk6sKrRQjJlFOwDAxQERr4kmy4ic2ekACCZx1i4rDJ1Xzw33klsrlNfjn9GxmYJm6_SA4__gd5qhPK6jm9l1IcaWHhlSmdiKg7qU3ZjlTEfkrB5TIotYWf4Dcbs8_w206xS5yshBCOBVIo6vkuA8pA8iK6-aKNeBxvIGMEdn0oQqpqAYv6EPQVILNhqLMcsaGBtJspoiH6sojH2C8yKT6SxH619xtJlfqN-odmypgXmJcNRDTMxTfIfzpnYz2mz7qbl49bWGlswPDM12qF3l2EXtVq_NC2kjSekvAuBtuN5d5BbyuB8HBUswweFwcBC8gQ9T8QJprioFNMjL9cjWG43LMKadzOfnX2CdDxnZMP4YBDRgreo_e2OLeHb_P3bBwFyQ_oxHsBvUShnBSMZQpGo7ooawze7lHS_lKU8g4HH7DtsjH7mgC9zTddsPpgBAcDcG4OzW-XY2LL1zQGWjhQdKS26qQLSZ0h5kCGvbL6qs9CcyI1P-sPDq6o_Sqs_4B7K4wmvJcJg-h7LubQhRRoMbCTsIu7rXRrqpgTvXxjxxqpU7CNoQNKxfRp7v-25gDa6VKNyhmAsqQsYrvN3pLAAPpowFGUdAZ5wgrQC_Zwyca-Dl3AOGkOYnLgxZDP_1h1Ph51RmfBRuZjPmc61p2klGR4etbIlaMvvYMxqVwcMeYYWBds1HCMkgOmS66XDfh6PLKp6MsPAIG7Qqir6yVGM4YQD1sat07RBXyZ78IxBQtby_Fy4YB0NRBiDG_q2tAD5et2w1L8q9cSgbLPgIUu2T6_U9tNzxtLPZwkCoQrcO4Qat33JTCOGw5uNNCEdqpwv9SyZeoDmfDrXtlFLrfz07JVWY7ENcWPvJEir1erqzuANTKJujBQEzTdEeiHpr0DCk-VuOkwNSVxX3wR7pBShxpUSBIwMuFtS_guMZdPpk9w2-UTePC0yVxol4Xd2zcUZvGWSWs-KIDEM7CgwtXLM9PiLQSb05wWwzBfTEH_DmcofGKKsM9E0iW7Ga_JqHlfCESfz1pmXyZLPBt3I9kU_NOjSFrXtUVBTct3P54t_k7K7RO0-UxOvRU_Dqc8_3AA125JMRQRDvrG6zfVoMMVe_>`_


.. .. figure:: ../../images/issuer-solution.svg
..    :width: 100%
..    :alt: The image illustrates the Issuer Solution and its relations and interactions within the ecosystem.
..    :target: https://www.plantuml.com/plantuml/svg/fLTjRzis4FxkNt5LXpK1chfvIP4CA537IJSFQUF5IVVHeAMpJ4GIDP9ouWtxxpk-A9PCnnFQVAWbykwvvquFZzTFIZEfgpphlO7X2Gn5Nee22mq9PwbaESo5X95I5KgOYApIN1GmaF62Qunr9R7tYXTnLYK82wrBzKk_BzdZkvJhHJMh5CfO59hmtiKYxvSPAqoi0wMJZC_wmvE3iLcw_tBTpvdIA6bfwZcGJsbu4R5BdFC2OJA-7TrTJNgl4lS-6jvylR-zxX1OLoLBvF6Q0AVTWpbP7AXIKYhAnrzduy7xv9wBmb49DYq2UqGbSZmuxSSeDP_pc6divf0mpMPCTRJEHFpGpTBahpfo5cb7Iy9Seknc-u2hxaoxMV9a6ZEPT3F6ftZ1YXIdBDCTFmMg1otARiQFBCkm2t2V5qfpRO_Divo7bT8Y1wLN6QhU84ckCionq7SitOlmIQCiM1QzXPzcwL1aGdwCNf_RFxDcqFtgepc4rax81ALVJIMkelrDM59vpkIgZNfu-E5ibdH2VVr-Td9sTX82AwIZb0JG7-BPyV6y6_G9Epi-EYVeDn20ooMFKRMnyNn6pBjXiwEpmyFt8MqjAwNRi6U3u_EppzrWJq-FZay71BlkJdg1m68jf09M951_Hr0hfJ5NlJ5A9Oez8_Yt4DtJJqI_RXKM8ajuaS8bJxacfw74XAXobjdSNPFw61bdHL4d5dDwzQJtd1IdHcUiY94W_xGhCF8haO_sHi7exi1j6apDKlMn9RSwYZzfxJW5CnfcsHHvGeXV_IlWw1ASMTHSJdmYtAQXLxuCkmDJrsW7PPLU6FzugaGbRNQ3UWacTab5Vb4G1aLV8fYk2ihlxWnOzzzsLAkDATMEC0dyphp2mBwQOBT2Q11pi6RsVYH6wzh2PqnGsZhi3jwuBSAifth1PJ8j6TcWMgVuDoPmPxPWxBOC8_YzIdXCOW4YCwbASsgKa2ku40b7fyThJ6cVEHJZk9jSeszjrLifnP9JdckzZVrAr2PR2w4-oi1Y-bUHsEicJO_saxtRpSW59ZBjCnSC9pDHsNxKk_0FUznQJ9Mt87xXCMl0-AJXdnxGNojMpdW1SJsVA6Em7fdgE7Df9mzpIZxxnxLHP0g6iqOvQDSSJwZTZ8Ml9Uqc2JTqcWNK2ocgT04C2CZvSlAKSnOZx1azuXFBomnXiX2FglyD9SaCLVyBArXAlxVuLuLARsis--jlu6-CvYVmTsIqRnFtvV65ks3nGpFJe3hnSvIfAnJb6TI_NQYR4elHvSctuIXonapxYba4jIq3q0ASLC3tnARK_MtLJiiDDfHLax0_Xcwl8MbcHJPnBeQZsJWoJxyHiSpmgpkKCpLqMSjvded7x-GaCLlHUR5zOMLwaNk7iNdVNhmnzE5cT3cadydWotNKxA6sdlPIWKUk5z3gwlxYSf8QZoxtGKXdHYzkTU-F_Ql1OF_xSYcJ8fbYBMj3Qpo2KQtao2_WGMtn0urbDx_ciDXW6SWsutECLt66RULUrylW3bZkFy344MjAOmq64bEkj6Ik8odDT4Kr83lQMOguVN_uSQN1sOpj0LTtSL6E5Hcjdg-kds7YbxnjID2t1g0Rc5WqRYRFgSQ4N1HS2qcbtK7E_4U5oFsxqQabPZOjjU2bwf5q_J0KZZ3Kr2YxXadGMaEJve0IQDp8rbi7qROr9jyYbVyWCVBb2-scCeg3HgTw8KgxczpCDAEzZSRWiGnrWZ4ucmS-J38yo3xLq3dWz7_-BSwRhUSRotZoxFSyw7dNeAYR5V2tqaO9rClksmvYGxdMBDdoYNP01kV5YCfETB5SbLgaafKB7eCeKORq0Yv1GxDmIvTeuiPIKd3kGG9D_qY65zn0RZBOCZ_VefOSbqrY5Jcqs6q72oS_swnPh9kYcTvldLytmKBVdlSEfhMDSToFrtuG4FuWDTjfit_vb4md-bMAgYG5Ao07oc1ZSY4BG-2o9Z1pozlxmr0KDYuXRtThoBsRGt306YxmeazGrjrnTiYiWsTmNfe-dyYYohF_0000
      
..    Issuer Solution High Level Architecture

Credential Issuer Requirements
------------------------------

The Digital Credential Issuer Solution MUST:

   1. Register with the Federation Authority to obtain proper authorization for issuing specific credential types.
   2. Implement secure creation and issuance mechanisms that ensure integrity and confidentiality.
   3. Communicate with Authentic Sources through secure and reliable API Services to obtain verified User data.
   4. Authenticate to Wallet Instances during issuance to prove its legitimacy.
   5. Support immediate issuance flow and MAY support deferred issuance for various operational scenarios.
   6. Implement appropriate error handling and User notifications for all processes.
   7. Maintain comprehensive audit trails while respecting privacy regulations.
   8. Issue Digital Credentials that support Selective Disclosure.
   9. Periodically renew its trust with the Federation.
   10. Register the Relying Party Component within the CIEid Digital Identity Federation ecosystem (for PID issuance), and within the IT-Wallet ecosystem (for (Q)EAA issuance, if required).
   11. For PID issuance, authenticate Users with LoA High using national Digital Identity infrastructure.
   12. For (Q)EAA issuance requiring authentication, verify a valid PID from the User's Wallet Instance via `OpenID4VP`_.
   13. Implement proper procedures for the entire Digital Credential lifecycle as detailed in Section :ref:`credential-revocation:Digital Credential Lifecycle`.

   For the Frontend Component (if implemented):

   14. Authenticate Users with a Level of Assurance (LoA) at least equal to that used to obtain the Digital Credential being issued or managed.
   15. Provide appropriate security measures to protect User data and Digital Credential information.

Component Details
-----------------

Frontend Component
^^^^^^^^^^^^^^^^^^

The Frontend Component, if provided by the Issuer, MUST provide a web-based User interface for Digital Credential management, offering functionality to:

   - Display and verify issued Digital Credentials and their status.
   - Manage Digital Credential lifecycle (e.g., revocation).
   - Initiate issuance through Credential Offers.
   - Provide User support and documentation.

Issuers MAY provide additional services to the User through the Frontend Component. These additional services MUST NOT conflict with any regulatory or technical requirements defined in this technical specification or in national/European security and privacy regulations.

Credential Issuer Component
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Following the `OpenID4VCI`_ specification and the implementation profile in Section :ref:`credential-issuance:Digital Credential Issuance`, this component MUST:

   - Issue Digital Credentials to Wallet Instances.
   - Process Digital Credential requests.
   - Obtain User data from Authentic Sources.
   - Generate properly formatted and signed Digital Credentials in supported formats (SD-JWT-VC, mDoc-CBOR). See Section :ref:`credential-data-model:Digital Credential Data Model` for more details.
   - Implement the Digital Credential issuance protocols and flows.

Authorization Server
^^^^^^^^^^^^^^^^^^^^

This OAuth2-based component MUST:

   - Handle authentication and authorization flows.
   - Manage access/refresh tokens and authorization codes.
   - Validate User identity confirmed by the Relying Party Component.

Relying Party Component
^^^^^^^^^^^^^^^^^^^^^^^

When User authentication is required, this component MUST authenticate Users:

   - For PID issuance, via national Digital Identity Providers.
   - For (Q)EAA issuance, requesting, obtaining and validating PIDs from User Wallet Instances using `OpenID4VP`_ in accordance with Section :ref:`credential-presentation:Digital Credential Presentation`.

API Interface
^^^^^^^^^^^^^

This component MUST establish secure connections with Authentic Sources to:

   - Retrieve verified User data.
   - Properly authenticate and authorize connections.
   - Format data according to Digital Credential schemas.
   - Provide cryptographic evidence of User authentication when required.

.. note::
   For public Authentic Sources, a Credential Issuer MUST use PDND according to rules in Sections :ref:`e-service-pdnd:e-Service PDND`, :ref:`credential-revocation:Status Update by Authentic Sources`, and :ref:`authentic-source-endpoint:e-Service PDND Authentic Source Catalogue`.

Credential Lifecycle Management
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

This component MUST handle:

   - Status management (maintaining and updating validity).
   - Revocation processes (implementing mechanisms to revoke or suspend Digital Credentials), according to Section :ref:`credential-revocation:Digital Credential Lifecycle`.
   - Renewal workflows (managing Digital Credential renewal processes), according to the mechanisms defined in Section :ref:`credential-issuance:Digital Credential Issuance`.

Trust & Security Component
^^^^^^^^^^^^^^^^^^^^^^^^^^

This component MUST ensure security through:

   - Key and certificate management.
   - Audit logging.
   - Security monitoring and incident response.
   - Compliance with IT-Wallet Federation security requirements.

Interaction Patterns
--------------------

The Digital Credential Issuer Solution supports these interaction patterns:

   1. **User to Frontend**: Web-based interactions for Digital Credential management.
   2. **Frontend to Credential Issuer**: Converts user requests into OpenID4VCI protocol messages.
   3. **Wallet Instance to Credential Issuer**: Direct protocol-based interactions following the issuance flow.
   4. **Relying Party to Identity Providers**: Authentication interactions with national eID systems or PID verification.
   5. **API Interface to Authentic Sources**: Secure API calls to retrieve verified User data.

All interactions must follow the security considerations in Section :ref:`credential-issuance:Digital Credential Issuance`, including proper handling of tokens, proofs, and cryptographic materials.

.. include:: credential-issuer-entity-configuration.rst
.. include:: credential-issuer-metadata.rst


