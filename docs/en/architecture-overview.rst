.. include:: ../common/common_definitions.rst


Architecture Overview
=====================

The IT-Wallet System is a federated ecosystem that enables secure Digital Identity management and Digital Credential exchange for citizens and organizations. 
The IT-Wallet ecosystem operates through a multi-layered architecture where governance bodies establish and maintain the foundational trust infrastructure, Primary Actors implement and operate the technical solutions, and external systems provide essential supporting services.

The following diagram depicts the IT-Wallet architecture overview.

.. plantuml:: plantuml/architecture-overview.puml
    :width: 99%
    :alt: The image illustrates the IT-Wallet architecture overvew.
    :caption: `IT-Wallet architecture overvew. <https://www.plantuml.com/plantuml/svg/fLXlZnktyNwlJy6V4i0wG6V_ahE3Cr07aIKvKUlQmfrS8q01WSiThLXJv8RawhmnyjtBuSvHN4c-NbEzC7pSuIpvpFFCd_t9UMvzirDiiRhyo9K2lxvjdOVTUcB5LdeGlh4m-3-fXMfAO7-PFdysVRwUcbrjD6Z_u-2NnMo-lbtDR-RlLxykvwEBmHFcFabTSyjtJ4aDlgs16UktPl1syklx3wlrs_cRrVfcyVClgsXEgwlto_Ni_STtSMq6cx2LtIvl5glvRNO0tzIyj5VFXDdjZFxnp9EDqVwItu4pExXyyKo0zN8Z1VVm2EkIUrvm1uznR2ht23DPhWMtvICiuRFOSbt1cYl_2FCxZDT_D7mcjVFIDruYMW7PQUEysJ7dMmLkC2dBkO8TQB_YrMW8dprOpTLmpBujggbHnhuQVlCo_d0DFTFg7T8ZsXbRWgNLoa8xl3XsMrkvuxRjU_tkkn-kY_9HNh_v_-BvzVNpKySUnBRlzGTHN5rj7kVrER---lxbgTVAx145BQ3l-tfozVBwpUDyltZn_TMBIV0zyD8hE0YCTG9ZkS0mBZ-dbxA9yCQwmMlJw3B0DZgSPyo69uvEDWuls9S12xybM6VqY0iTzhtZI06ksBGjmZg8nahViaaJX1d_DvfCtrqCSqkUdlajzmpsN3NSWsFJoMjceJRMEyProQHpJLWEcgoLZ2VXFjZvwCWzPNFj6ei6lLURJV2R8mF2k7Ydw3JSAkWM7EFb5YoWLs-OfiD5atbZJGrSi-JJUOwObUufXiJpohtgXVDRLmSxU3NCP851ok4gSWmcGbWePNSLzjgKRH-YtcDZAwxbx_6F3ZFAFk3YLP6kMWgk8bJWuwNC1l5qU3dk73YN8UACYaVy7wxZYZvfcXhiNZfZstIRVAq8Qyo2gursib30DiOoemiJG9Mw2g7qqkDzfFRcA7uRAC76oyVe21DiTMCQntP6IsziS41HbvPnuUK--dhA5fxjkEOLE5PpwwMGDTUUARa1qGe5qHyGYpAQtKc_PGT0c6qK_0ciI4eZmGiNy9WQ7MwzY_A84S7CW6ZXlKSXM54czym0l6dQm0yRYcv3v44062qE31WpNkwabiuZOljumqJZp8iBu9yb15jjeUr4qlObajvnK4FVkuNV6ca1tNyDB9RGokfdG0l1Yl-yvUtw0se5CRl8bYA6NEXy3JEGAou6Vs2YMtR5u2JBKP48o985HUKugwKDc9v0UodMpZHMWCEWtA-nssujHehoM0Sq6ICHFpYmJnmhPHKUAeR5FoB5lRUoQ3o4jtw938c_rFQCk5lpMWRNSEbGEkXlibpWosxcjwjDezWjhUFQHoXOieFFjN5GCh-rfgcsR3bxDuiguo8yTgYHT3CwR3nPL8aCrEy2bu8hVm_EQcky4KQvw4bg3vWPBI-ameYdy0EgPzSWFIADEWNH-sXnJ8cV4bc7I5DApxpbKkMKePZbVCcx69BNANXbSIPMR4RD5qAM__ysdZnM72SzPYb7oQJf1J2B6zjOisFyRE175YhKdGGtHk0sY7hCvjq3iEuYW7r0kh9SDuhVHoWcDejO8p8HveYJCbM5X_A6KbKCMmn6PIaA2A402ai696esHx6aw-S8te1Qp-wfru5u3msQq-b8f4ceVnmq-uHDbAnqHvUzBC5YTeb9tF4TC0LxK7sDTKtc-juUkKnrX18HMzAZI7GKQHPnxRdKO4TtxdHZjF-x2KZ0CzJ7fAuFAn6gkx3AwrebhYRo8yfPsMcqwCenLHFCZ5HFYFMHCBoAnNP6P9bQAD4NLsvyeW3GvQKtbn3BZh1jdPJGE221RRY8vJ7HJqP_djuTJtfEAod84LmKIHwd7FrIvCWV3imMpZKFGevR7I5zTci_3hY8eEP9QtKe8sHAoQMp7NUtn5q8YuMz-OH_d86N8h8DTWeIMavMcdkiw6FqG3g9-7TPwIINFmWcpLaPcdqiRPrZ6RJKuccNs6t0Gq3QEW5vkk-hRFv7rxpQcBvo-AXYVmKfXgr2KoWf8YIrbNlk8TMEB2lrqtzqIkGzr88nYymr0TLw6rpkkP8b4HpZHVPY2-AJExnGj9T5Ura21kYnLCPX-04YUuw4ietpRA4tbZjlcpZvfFJHHU3BcNBX-Vh-_i7cFRMYHBitgUNyfqRSSm8Vddsz61zrjnhk_fiEDod0nwjPKF6PsyewZvNBzkNHoLgh3EVeEU-2dUU-rqE7I9olltaaw7SEK3picefWsviERcXncCALhyoae_fQCjgEkKv6gI0C29RWdYiJ-to-vrBnGi7vd9ibfLknXHrtXyuZhr482CqC2J7gWOazs04uWUrhcq8RTn7kmHjbPi8orykVgi8vAO_m77wempvm2QAaYwmZfYgU9VYyNyxpVbw1-sOdnTdMPytop9UTczhnENtoEUd7WHw4m2SR7csODvackf6Tz9jFdaB2-30fBwWuvefFJqzAQ8e-G_nBR5EcYpaRpHK8RusMuk1mocrvyJHHmU7pwgYYzsYHfl8olIzl7MDEAEuvpTboCOkxui3AZvgFXSP4BE3fa94eUn_HpbUdGL-GTQdB32aIIso7sL9n7oV74Su95yFCJlOpAHwRQWVozcG8oDIIrmwSMzpH_B6SiCJkD9Zt0Os8zEU40lmTW6P02NISJojf-AovHtXe9Dro2sKyRpR69qNcM3uqO6HOuf7MVYjjkOuvD4s5b5LM-2Wl-tzjIYam1nbx_7544btUGXMUavFxVM_v7GCS-mLbxGgqYA_x5taaU0WB2rMZk4VN1Ra-dAfecGh-lA4WC5U3m0oLCIs2X75IU1mKY030gkN6Kk_1ULbHdsni_hRqkUGyhkpyTv4yMQ6GaQDvKecSFGMRaihVeErLGo9OzicJDRe4YqJ4AmnkGFLRrZHXty1l3JZlUaCvsiUf8j-3jW9aW8A9L5foutuhjxJWWisnyM205vpb7rsfobxG4_fpV8zXsFCJwBBPgNy3>`_


The governance level ensures that all participants in the ecosystem are compliant with security and technical standards and requirements. 

The primary operational layer implements the core Digital Credential lifecycle through coordinated interactions among specialized technical solutions. This layer operates within the trust framework established by governance actors, ensuring that all credential operations maintain security and privacy standards while enabling seamless user experiences.

External systems provide essential services that connect the IT-Wallet ecosystem to the national digital infrastructure. This ensures that the ecosystem is interoperable with existing government services and connected to authoritative identity and data sources.

The architecture enables four fundamental interaction processes:

  1. **Entity Onboarding and Federation**: This process ensures that only qualified and compliant Entities are registered within the IT-Wallet Federation. As a result of the registration process the Trust Registry is updated enabling all participants monitoring their ongoing federation status. This process may involve technical and security assessment and compliance checks to the requirements of the IT-Wallet ecosystem.

  2. **Credential Issuance**: Credential Issuers establish secure connections with Authentic Sources to request verified user attributes through standardized APIs exposed via the National Digital Data Platform. This interaction ensures that Digital Credentials are based on authoritative, up-to-date information from official registries and databases while maintaining proper authorization and audit trails.

  3. **Credential Storage and Management**: IT-Wallet Solutions receive issued Digital Credentials from authorized providers and manage them securely on user devices. This relationship enables users to obtain verified Digital Credentials from multiple sources while maintaining full control over them.

  4. **Credential Presentation and Verification**: When users need to prove their identity or specific attributes, IT-Wallet Solutions present appropriate Digital Credentials to Relying Party verification systems. This interaction enables them to validate user claims through cryptographic verification and status checks, supporting both public and private sector use cases.

The Trust Infrastructure manages the onboarding/revocation status of new Entities (with their technical solutions) and provides available Digital Credentials and schemas. It enables all ecosystem participants to discover authorized Entities and verify their current federation status.

The trust infrastructure provides automatic trust chain validation, distributed trust anchoring, standardized metadata exchange protocols, and Federation API services that enable seamless federation operations while maintaining cryptographic verification of all participant relationships.
This approach ensures that users can trust the credentials they receive, Relying Parties can trust the credentials they verify, and all participants can trust that their counterparts have been properly vetted and remain in good standing within the federation.


.. toctree::
  :caption: Architecture Overview Table of Contents
  :maxdepth: 3

  functionalities.rst
  how-to-read-spec.rst
