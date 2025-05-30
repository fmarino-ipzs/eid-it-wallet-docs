.. include:: ../common/common_definitions.rst

Flussi ad Alto Livello per l'Emissione di Attestati Elettronici
================================================================

Flusso ad Alto Livello per PID
-------------------------------

La :numref:`fig_High-Level-Flow-ITWallet-PID-Issuance` mostra un'architettura generale ed evidenzia le principali operazioni coinvolte nell'emissione del PID.

.. _fig_High-Level-Flow-ITWallet-PID-Issuance:

.. plantuml:: plantuml/pid-issuance-high-level-flow.puml
    :width: 99%
    :alt: La figura illustra l'architettura generale e il flusso ad alto livello per l'emissione del PID.
    :caption: `Emissione del PID - Architettura generale e flusso ad alto livello. <https://www.plantuml.com/plantuml/svg/ZLHnR-gs5_q_dy8_LEb7fLQqQz-RD57qU86kaTW3XNJLaof59huD5ecTsJUqsRJllcie45ZwbgfIyFNnESVNn_vYaHiiyypxdrH9LWfWVV-svz_6lbR8fG8pyBo7O3IEvz4u74-ZxxDnzzoR3BzF7wDuChwFuZ3uzI6YccTNKXNSy9nbj12h0fWskDIr2QK5M2ZOzTLLhMguMcsgFrzvtl_P25veFPlFmY0QpslEi2ouC3UzHEUvLeE6cHToVSbVmUeSBZ_r4Z0eNsJ24LgW1KU-uBODDDF9gWMij61i6vywRGCZjZMO5i0LL2tTjO194IVSY1P8U4kMNAKGympRz1li2dNH0ldAimp-ax8dbKM99KeN3cyeH0XPnDDkXzjA9PqBTeRmXhxEjBax6uRXz2c-dtwBOdywcOOqws9xD5kVc6ELmTs8soM82OsxvnJv6HYhLTTrye9r7kdJeU_JnYuBo0vN2R2bpWJDd7lxIzLzbV_6kQNJO7Jxkn-udymPjeMH27UTRGU8ugikbU2cwXPIp8nUIx6HdWKZzZua8VQNn-Zl8BTEd1uHKoqlj0A5zaIkSx4NUpznKZjcCGNXgAULL2cRSOFLWUwTpMSzDX_-DZbXT04dkhyFzWD1YoHMjJtumLWADfAfH9wn7U1PiNiW07V7kj_QlB88UJn-mwuKpjOEVkW25K-vc4sMa0DpjrmmhTXMSgA7x46cIzQTt9pNkruBb7D_EB-DCBSaCInnwSWJDjUbsHxYyDiiF6d0xcqXccCIv0GyR93DmQnb0fPnTUY5Rs2p0vvPvdEgwBJSnUNoVZnY1b9fqLGdgkwP8aMFpcoRKOfTfs_bd_3BzUT1Ft5PPyGzw2y6L_tUOj3lRMhqTQ31ithY2iaBetnrBZh4vQY81Vc7HDUDHFM0qhviejTWw73TDYDJMZoYNoSV6_sfaJ-4FqgmQ8-T4i-FhDuqKcslPODRrc2MxWG5y4E5sqQ5VMWuWdrMD63kxTYpneyRvzn-oFkfaNUwSCco981evA8azYtdLxdhXYceuFxFaAVsRliq7hhreuHyRjGCh2sXrlOle4IPP_y0>`_

Il flusso ad alto livello inizia con l'Utente che desidera ottenere un PID e avvia la propria Istanza del Wallet (Passo 0). Di seguito la descrizione dei passaggi rappresentati nell'immagine precedente:

    1. **Individuazione e Trust del PID Provider**: l'Istanza del Wallet individua il PID Provider fidato utilizzando il Catalogo degli Attestati Elettronici e i Servizi di Federazione, stabilendo la trust verso il PID Provider secondo il Trust Model e ottenendo i suoi Metadata, che indicano i formati del PID, gli algoritmi supportati e qualsiasi altro parametro necessario per esigenze di interoperabilità.
    2. **Richiesta del PID**: utilizzando l'Authorization Code Flow definito in [`OpenID4VCI`_], l'Istanza del Wallet richiede il PID al PID Provider.
    3. **Individuazione e Trust del Fornitore di Wallet**: il PID Provider verifica l'autenticità e la validità dell'Istanza del Wallet, stabilendo la trust verso il Fornitore di Wallet e ottenendo i Metadata del Wallet con i parametri necessari per le esigenze di interoperabilità, secondo il Trust Model.
    4. **Autenticazione dell'Utente**: il PID Provider autentica l'Utente con CieID Livello di Garanzia Alto (L3), agendo come un Identity and Access Management Proxy verso il sistema nazionale di eID.
    5. **Recupero dei dati PID dal Registro Pubblico Nazionale**: il PID Provider ottiene i dati PID richiesti dal Registro Pubblico Nazionale (ANPR), che agisce come Fonte Autentica.
    6. **Emissione del PID**: il PID Provider rilascia un PID vincolato al materiale crittografico posseduto dall'Istanza del Wallet richiedente.


Flusso ad Alto Livello per (Q)EAA
----------------------------------

La :numref:`fig_High-Level-Flow-ITWallet-QEAA-Issuance` mostra un'architettura generale ed evidenzia le principali operazioni coinvolte nell'emissione di un (Q)EAA, seguendo le ipotesi elencate di seguito:

  - l'Utente ha un PID valido memorizzato nella propria Istanza del Wallet;
  - il (Q)EAA richiede un profilo di implementazione ad alta sicurezza.

.. _fig_High-Level-Flow-ITWallet-QEAA-Issuance:
.. plantuml:: plantuml/eaa-issuance-high-level-flow.puml
    :width: 99%
    :alt: La figura illustra l'architettura generale e il flusso di alto livello per l'emissione di (Q)EAA.
    :caption: `Emissione di (Q)EAA - Architettura generale e flusso di alto livello. <https://www.plantuml.com/plantuml/svg/ZLHXR-964FtkNx6r8XMaH2INt4cj23eEd1vIL2WuZKuwoHgy4xF2xFfsnoHkrV_UMTmSX7DI8oJZcRVllNqxoqT7OAdSvC5FIgTvAL7qHrUzqLKoCfl2QDGq28BFat6KBE9e7atZBxEeqmrkXr-cTt5o6zt4oNpos-UOQu5RArs0XOt8bKQg2XJ6qieSDBIHwB0G5-Vd1rKBUkshxov_2OAVnHWVUBrOpEQJE5eSEAEo06alUwdPR8mUD7GUZAOpU4HdDdZslfUY9VMWKY1iWPP0i0JN1fgRTDq2LZgqherFaxM1CTiMRGlW6gkMxbh0b4nIiB854f_I5UWC4yYfJTxercIA5iX7o7FyNygUqeuKbQJyS0H3AUUOnv1rGd2LJiDJSKBuH2EJ6tjzCfpFf_V9pVJtE1bDRwTpxlgnFUo-Q2oeol5w36w5yfRVErqU-HbQPtJ79tagmZj-XFoytzaL4xO3EaMnChdaJZVuVgawZ-f7d5ywdOol_XnDH4_iViryBJmzSOLLXDTX7GGpVJAbbc2hpZS4c5cpLN9deVD7DneEHLtnckBlGF1dhxnDlJHhx6lkGFb8yB_3PyMNBBPW7CTRAPs96LYgzarFqUZUZpap_RFF8OcUg0EEOSEILbnGgLYOqjPX72r_lfzXzuY0W84tAD62FtknGBjLAJe1MegnoXH1BaOMfHU0t8aHSCLavNFaPpVHM5ZCb2DR7QdwgywA0M-sFcS-kh3lr5_uwyM7GJ_ryoAOUz1V3ixxlUMWtzlL-Eb1Ww_w7ZIn5r6VJNWQCfrdOoA2Lxak6hcEpfTtvrApHLjzrNwpiIqTlL3Ofg_RVTSeCSTl9JfoB7PacBdUSdpPI5SFUODZyQFXv8u7wws0hnebliyE4B9jVX7-AXxIUklWNkLztyWxNH8exLY0oAfboUmrvoVr78SjkE2_9mIPkwx_QVPnlRMN3usQ4-TAFCh-8sfPRl9_0G00>`_

Analogamente al flusso ad alto livello del PID, il diagramma sopra illustra un flusso ad alto livello per (Q)EAA che inizia dall'Utente che desidera ottenere un (Q)EAA (passo 0). Di seguito la descrizione delle operazioni più rilevanti coinvolte nell'emissione del (Q)EAA:

    1. **Individuazione e Trust del (Q)EAA Provider**: l'Istanza del Wallet ottiene l'elenco dei (Q)EAA Provider fidati utilizzando il Catalogo degli Attestati Elettronici e le API di Federazione (ad esempio, utilizzando l'endpoint Subordinate Listing del Trust Anchor e dei suoi Intermediari), quindi ispeziona i Metadata alla ricerca della disponibilità di Attestati Elettronici di ciascun (Q)EAA Provider.
    2. **Richiesta del (Q)EAA**: utilizzando l'Authorization Code Flow, definito in [`OpenID4VCI`_], l'Istanza del Wallet richiede un (Q)EAA al (Q)EAA Provider.
    3. **Individuazione e Trust del Fornitore di Wallet**: il (Q)EAA Provider verifica l'autenticità e la validità dell'Istanza del Wallet. Durante questo passaggio, il (Q)EAA Provider stabilisce la trust con il Fornitore di Wallet e recupera i Metadata del Wallet contenenti i parametri necessari per l'interoperabilità, come definito dal Trust Model.
    4. **Autenticazione dell'Utente**: il (Q)EAA Provider, agendo come App di Verifica, autentica l'Utente verificando la presentazione del PID.
    5. **Ottenimento degli Attributi**: il (Q)EAA Provider recupera gli Attributi dell'Utente dalla relativa Fonte Autentica.
    6. **Emissione del (Q)EAA**: il (Q)EAA Provider rilascia un (Q)EAA vincolato al materiale crittografico posseduto dall'Istanza del Wallet richiedente.
