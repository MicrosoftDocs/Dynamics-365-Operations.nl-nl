---
title: Elektronische rapportageconfiguraties downloaden van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u configuraties voor Elektronische rapportage (ER) kunt downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 08/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 8a18427114bddb7c72024a8d96d33f3fbf8dbe17
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810614"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronische rapportageconfiguraties downloaden van Lifecycle Services

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de nieuwste versie van [ER-configuraties](general-electronic-reporting.md#Configuration) kunt downloaden uit de [bibliotheek met gedeelde activa](../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).

1. Meld u aan bij de toepassing met een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

2. Ga naar **Organisatiebeheer** &gt; **Werkgebieden** &gt; **Elektronische rapportage**.
3. Selecteer in de sectie **Configuratieproviders** de tegel **Microsoft**.
4. Klik op de tegel **Microsoft** op **Opslagplaatsen**.

    [![Microsoft-tegel op de pagina Lokalisatieconfiguraties](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Selecteer in het raster op de pagina **Opslagplaatsen van configuraties** pagina de bestaande opslagplaats van het type **LCS**. Als deze opslagplaats niet wordt weergegeven in het raster, volgt u deze stappen:

    1. Selecteer **Toevoegen** om een opslagplaats toe te voegen.
    2. Selecteer **LCS** als opslagplaatstype.
    3. Selecteer **Opslagplaats maken**.
    4. Volg de instructies op het scherm als u wordt gevraagd om autorisatie.
    5. Voer een naam en een beschrijving in voor de opslagplaats.
    6. Selecteer **OK** om de nieuwe opslagplaats te bevestigen.
    7. Selecteer in het raster de nieuwe opslagplaats van het type **LCS**.

6. Selecteer **Openen** om de lijst met ER-configuraties voor de geselecteerde opslagplaats weer te geven.

    [![De pagina Opslagplaatsen van configuraties](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

    > [!TIP]
    > Als u problemen ondervindt bij het openen van de LCS-opslagplaats voor het downloaden van configuraties uit de bibliotheek met gedeelde activa in LCS, kunt u configuraties vanuit de [globale opslagplaats](er-download-configurations-global-repo.md) downloaden.

7. Selecteer in de configuratiestructuur in het linkerdeelvenster de vereiste ER-configuratie.
8. Selecteer op het sneltabblad **Versies** de vereiste versie van de geselecteerde ER-configuratie.
9. Selecteer **Importeren** om de geselecteerde versie vanuit LCS te downloaden naar het huidige exemplaar.

    > [!NOTE]
    > De knop **Importeren** is niet beschikbaar voor ER-configuratieversies die al aanwezig zijn in het huidige exemplaar.

    [![Configuratie archiefpagina](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Afhankelijk van de ER-instellingen worden configuraties gevalideerd nadat ze zijn geïmporteerd. U krijgt mogelijk meldingen over inconsistentieproblemen die worden vastgesteld. U moet deze problemen oplossen voordat u de geïmporteerde configuratieversie kunt gebruiken. Zie voor meer informatie de lijst met gerelateerde onderwerpen voor dit onderwerp.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)

[ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice](er-download-configurations-global-repo.md)
