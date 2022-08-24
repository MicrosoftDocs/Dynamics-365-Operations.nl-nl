---
title: Een configuratie vanuit Lifecycle Services importeren
description: In dit artikel wordt beschreven hoe u een nieuwe versie van een ER-configuratie (Electronic Reporting) importeert vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: kfend
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
ms.openlocfilehash: 92c5d010430b38cb6c11a87283a2f7d4c29484f8
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290359"
---
# <a name="import-a-configuration-from-lifecycle-services"></a>Een configuratie vanuit Lifecycle Services importeren

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een [configuratie voor elektronische rapportage (ER)](../general-electronic-reporting.md#Configuration) vanuit de [activabibliotheek op projectniveau](../../lifecycle-services/asset-library.md) kan importeren in Microsoft Dynamics Lifecycle Services (LCS).

> [!IMPORTANT]
> Het gebruik van LCS als opslagplaats voor ER-configuraties wordt [afgeschaft](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release). Zie [Afschaffing Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) Storage](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md) voor meer informatie.

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

    U hebt de eerste versie van een voorbeeldgegevensmodelconfiguratie gemaakt en gepubliceerd naar LCS tijdens de procedure in [Een configuratie in Lifecycle Services uploaden](er-upload-configuration-into-lifecycle-services.md). In deze procedure verwijdert u deze versie van de ER-configuratie. Vervolgens importeert u die versie uit LCS verderop in dit artikel.

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


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
