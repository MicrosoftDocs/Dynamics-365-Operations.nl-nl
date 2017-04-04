---
title: Elektronische rapportageconfiguraties downloaden van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe elektronische rapportage (ER) configuraties van Microsoft Dynamics Lifecycle Services (LCS) downloaden.
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: 9dca5dec846670da25926826f59d7bce0fa0dcea
ms.lasthandoff: 03/31/2017


---

# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronische rapportageconfiguraties downloaden van Lifecycle Services

In dit onderwerp wordt uitgelegd hoe elektronische rapportage (ER) configuraties van Microsoft Dynamics Lifecycle Services (LCS) downloaden.

Deze zelfstudie begeleidt u door het proces voor het downloaden van de nieuwste versie van de configuraties voor Elektronische rapportage (ER) uit Microsoft Dynamics Lifecycle Services (LCS).

1.  Meld u aan bij Dynamics 365 for Operations met een van de volgende rollen:
    -   Ontwikkelaar elektronische rapportage
    -   Functioneel consultant elektronische rapportage
    -   Systeembeheerder

2.  Ga naar **Organisatiebeheer**&gt;**elektronische aangifte**.
3.  Selecteer in de sectie **Configuratieproviders** de tegel **Microsoft**.
4.  Klik op de **Microsoft**-tegel op **Opslagplaatsen**. [![update-er-from-LCS-for-MS-Open-MS-repositories-List](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)
5.  Selecteer in het raster op de pagina **Opslagplaatsen van configuraties** pagina de bestaande opslagplaats van het type **LCS**. Als deze opslagplaats niet wordt weergegeven in het raster, volgt u deze stappen:
    1.  Klik op **Toevoegen** en voeg een nieuwe opslagplaats toe.
    2.  Selecteer **LCS** als opslagplaatstype.
    3.  Klik op **Opslagplaats maken**.
    4.  Voer een naam en een beschrijving in voor de opslagplaats.
    5.  Klik op **OK** om de nieuwe opslagplaats te bevestigen.
    6.  Selecteer in het raster de nieuwe opslagplaats van het type **LCS**.

6.  Klik op **Openen** om de lijst met ER-configuraties voor de geselecteerde opslagplaats weer te geven. [![update-er-from-LCS-for-MS-Make-LCS-Repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)
7.  Selecteer in de boomstructuur van het linkervenster de gewenste ER-configuratie.
8.  Selecteer op het sneltabblad **Versies** de vereiste versie van de geselecteerde ER-configuratie.
9.  Klik op **Importeren** om de geselecteerde versie vanuit LCS te downloaden naar het huidige exemplaar van Dynamics 365 for Operations. **Opmerking:** de knop **Importeren** is niet beschikbaar voor ER-configuratieversies die al aanwezig zijn in het huidige Dynamics 365 for Operations-exemplaar. [![update-er-from-LCS-for-MS-Download-Configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

**Opmerking:** Afhankelijk van de ER-instellingen worden configuraties gevalideerd nadat ze zijn geïmporteerd. U krijgt mogelijk meldingen over inconsistentieproblemen die worden vastgesteld. U moet deze problemen oplossen voordat u de geïmporteerde configuratieversie kunt gebruiken. Zie de lijst met verwante artikelen voor dit onderwerp voor meer informatie.

<a name="see-also"></a>Zie ook
--------

[Overzicht van elektronische rapportage](general-electronic-reporting.md)


