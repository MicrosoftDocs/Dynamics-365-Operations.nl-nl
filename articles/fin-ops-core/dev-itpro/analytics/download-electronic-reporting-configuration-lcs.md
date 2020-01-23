---
title: Elektronische rapportageconfiguraties downloaden van Lifecycle Services
description: In dit onderwerp wordt uitgelegd hoe u configuraties voor Elektronische rapportage (ER) kunt downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 01/06/2020
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
ms.openlocfilehash: 4cc14860bd969048c4378b40d97a7940a8710e89
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934649"
---
# <a name="download-electronic-reporting-configurations-from-lifecycle-services"></a>Elektronische rapportageconfiguraties downloaden van Lifecycle Services

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u configuraties voor Elektronische rapportage (ER) kunt downloaden vanuit Microsoft Dynamics Lifecycle Services (LCS).

Deze zelfstudie begeleidt u door het proces voor het downloaden van de nieuwste versie van de configuraties voor Elektronische rapportage (ER) uit Microsoft Dynamics Lifecycle Services (LCS).

1. Meld u aan bij de toepassing met een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

2. Ga naar **Organisatiebeheer** &gt; **Werkgebieden** &gt; **Elektronische rapportage**.
3. Selecteer in de sectie **Configuratieproviders** de tegel **Microsoft**.
4. Klik op de **Microsoft**-tegel op **Opslagplaatsen**.

    [![update-er-from-lcs-for-ms-open-ms-repositories-list](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)](./media/update-er-from-lcs-for-ms-open-ms-repositories-list.png)

5. Selecteer in het raster op de pagina **Opslagplaatsen van configuraties** pagina de bestaande opslagplaats van het type **LCS**. Als deze opslagplaats niet wordt weergegeven in het raster, volgt u deze stappen:

    1. Klik op **Toevoegen** en voeg een nieuwe opslagplaats toe.
    2. Selecteer **LCS** als opslagplaatstype.
    3. Klik op **Opslagplaats maken**.
    4. Volg de instructies van de autorisatie als hierom wordt gevraagd.
    5. Voer een naam en een beschrijving in voor de opslagplaats.
    6. Klik op **OK** om de nieuwe opslagplaats te bevestigen.
    7. Selecteer in het raster de nieuwe opslagplaats van het type **LCS**.

6. Klik op **Openen** om de lijst met ER-configuraties voor de geselecteerde opslagplaats weer te geven.

    [![update-er-from-lcs-for-ms-make-lcs-repository](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)](./media/update-er-from-lcs-for-ms-make-lcs-repository.png)

7. Selecteer in de boomstructuur van het linkervenster de gewenste ER-configuratie.
8. Selecteer op het sneltabblad **Versies** de vereiste versie van de geselecteerde ER-configuratie.
9. Klik op **Importeren** om de geselecteerde versie vanuit LCS te downloaden naar het huidige exemplaar.

    > [!NOTE]
    > De knop **Importeren** is niet beschikbaar voor ER-configuratieversies die al aanwezig zijn in het huidige exemplaar.

    [![update-er-from-lcs-for-ms-download-configuration](./media/update-er-from-lcs-for-ms-download-configuration.png)](./media/update-er-from-lcs-for-ms-download-configuration.png)

> [!NOTE]
> Afhankelijk van de ER-instellingen worden configuraties gevalideerd nadat ze zijn geïmporteerd. U krijgt mogelijk meldingen over inconsistentieproblemen die worden vastgesteld. U moet deze problemen oplossen voordat u de geïmporteerde configuratieversie kunt gebruiken. Zie voor meer informatie de lijst van gerelateerde artikelen voor dit onderwerp.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
