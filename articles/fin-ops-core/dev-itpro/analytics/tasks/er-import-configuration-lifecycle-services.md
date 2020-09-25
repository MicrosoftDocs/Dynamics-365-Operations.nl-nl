---
title: Een configuratie vanuit Lifecycle Services importeren
description: In dit onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een configuratie voor elektronische rapportage (ER) kan importeren vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59dbbf820f7a3de1e5fb31f781943320b8b1a60a
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810638"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Een configuratie vanuit Lifecycle Services importeren

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een [configuratie voor elektronische rapportage (ER)](../general-electronic-reporting.md#Configuration) vanuit de [activabibliotheek op projectniveau](../../lifecycle-services/asset-library.md) kan importeren in Microsoft Dynamics Lifecycle Services (LCS).

In dit voorbeeld selecteert u de gewenste versie van de ER-configuratie en importeert u deze voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld. Als u deze stappen wilt uitvoeren, moet u eerst de stappen in [Een configuratie in Lifecycle Services uploaden](er-upload-configuration-into-lifecycle-services.md) voltooien. Ook is toegang tot LCS vereist.

1. Meld u aan bij de toepassing met een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Systeembeheerder

2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer **Configuraties**.

<a name="accessconditions"></a>
> [!NOTE]
> Zorg ervoor dat de huidige Dynamics 365 Finance-gebruiker lid is van het LCS-project dat de activabibliotheek bevat waartoe de gebruiker [toegang](../../lifecycle-services/asset-library.md#asset-library-support) wil hebben voor het importeren van ER-configuraties.
>
> U hebt geen toegang tot een LCS-project vanuit een ER-opslagplaats voor een ander domein dan het domein dat in Finance wordt gebruikt. Als u het probeert, wordt een lege lijst met LCS-projecten weergegeven en kunt u geen ER-configuraties importeren uit de activabibliotheek op projectniveau in LCS. Als u activabibliotheken op projectniveau wilt openen vanuit een ER-opslagplaats die wordt gebruikt voor het importeren van ER-configuraties, meldt u zich aan bij Finance met de referenties van een gebruiker die hoort bij de tenant (domein) waarvoor het huidige Finance-exemplaar is ingericht.

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a>Een gedeelde versie van een gegevensmodelconfiguratie verwijderen

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Voorbeeldmodelconfiguratie**.

    U hebt de eerste versie van een voorbeeldgegevensmodelconfiguratie gemaakt en gepubliceerd naar LCS tijdens de procedure in [Een configuratie in Lifecycle Services uploaden](er-upload-configuration-into-lifecycle-services.md). In deze procedure verwijdert u deze versie van de ER-configuratie. Vervolgens importeert u die versie uit LCS verderop in dit onderwerp.

2. Zoek en selecteer de gewenste record in de lijst.

    Selecteer voor dit voorbeeld de versie van de configuratie die de status **Gedeeld** heeft. Deze status geeft aan dat de configuratie is gepubliceerd naar LCS.

3. Selecteer **Status wijzigen**.
4. Selecteer **Beëindigen**.

    Door de status van de geselecteerde versie van **Gedeeld** in **Beëindigd** te wijzigen, maakt u de versie beschikbaar voor verwijdering.

5. Selecteer **OK**.
6. Zoek en selecteer de gewenste record in de lijst.

    Selecteer voor dit voorbeeld de versie van de configuratie die de status **Beëindigd** heeft.

7. Selecteer **Verwijderen**.
8. Selecteer **Ja**.

    De enige conceptversie 2 van de geselecteerde gegevensmodelconfiguratie is nu beschikbaar.

9. Sluit de pagina.

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a>Een gedeelde versie van een gegevensmodelconfiguratie importeren vanuit LCS

1. Ga naar **Organisatiebeheer \> Werkgebieden \> Elektronische rapportage**.

2. Selecteer in de sectie **Configuratieproviders** de tegel **Litware, Inc.**

3. Klik op de tegel **Litware, Inc.** op **Opslagplaatsen**.

    U kunt nu de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc. openen.

4. Selecteer **Openen**.

    Selecteer voor dit voorbeeld de opslaglocatierecord **LCS** en open deze. U moet [toegang](#accessconditions) hebben tot het LCS-project en de activabibliotheek die wordt geopend door de geselecteerde ER-opslagplaats.

5. Markeer in de lijst de geselecteerde rij.

    Selecteer de eerste versie van **Voorbeeldmodelconfiguratie** in de lijst met versies.

6. Selecteer **Importeren**.
7. Selecteer **Ja** om de import van de geselecteerde versie van LCS te bevestigen.

    Een informatief bericht bevestigt dat de geselecteerde versie is geïmporteerd.

8. Sluit de pagina.
9. Sluit de pagina.
10. Selecteer **Configuraties**.
11. Selecteer **Voorbeeldmodelconfiguratie** in de structuur.
12. Zoek en selecteer de gewenste record in de lijst.

    Selecteer voor dit voorbeeld de versie van de configuratie die de status **Gedeeld** heeft.

    De gedeelde versie 1 van de geselecteerde gegevensmodelconfiguratie is nu ook beschikbaar.
