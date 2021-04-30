---
title: ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice
description: In dit onderwerp wordt uitgelegd hoe u ER-configuraties kunt downloaden uit de algemene opslagplaats van de configuratieservice.
author: NickSelin
ms.date: 06/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionImport, ERWorkspace, ERSolutionRepositoryTable
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 105843
ms.assetid: dc44dea2-22ce-401e-98b9-d289e0e2825b
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 6f74602cafe3f0848a9e03f17300ca6242fe1545
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893975"
---
# <a name="download-er-configurations-from-the-global-repository-of-configuration-service"></a>ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u [ER-configuraties](general-electronic-reporting.md#Configuration) kunt downloaden uit de algemene opslagplaats van de configuratieservice. Zie [Microsoft Dynamics 365 for Finance and Operations - Regulatory services, configuratieservice](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) voor meer informatie.

## <a name="open-configurations-repository"></a>Opslagplaats met configuraties openen

1. Meld u aan bij de Dynamics 365 Finance-toepassing met een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

2. Ga naar **Organisatiebeheer > Werkruimten > Elektronische rapportage**.
3. Selecteer in de sectie **Configuratieproviders** de tegel **Microsoft**.
3. Klik op de tegel **Microsoft** op **Opslagplaatsen**.

    ![Werkgebied voor elektronische rapportage](./media/er-download-configurations-global-repo-er-workspace.png)

4. Selecteer in het raster op de pagina **Opslagplaatsen van configuraties** pagina de bestaande opslagplaats van het type **Algemeen**. Als deze opslagplaats niet wordt weergegeven in het raster, volgt u deze stappen:

    1. Selecteer **Toevoegen** om een nieuwe opslagplaats toe te voegen.
    2. Selecteer **Algemeen** als type opslagplaats en selecteer vervolgens **Opslagplaats maken**.
    3. Volg de instructies van de autorisatie als hierom wordt gevraagd.
    4. Voer een naam en beschrijving in voor de opslagplaats en selecteer **OK** om de nieuwe opslagplaats te bevestigen.
    5. Selecteer in het raster de nieuwe opslagplaats van het type **Algemeen**.

5. Selecteer **Openen** om de lijst met ER-configuraties voor de geselecteerde opslagplaats weer te geven.

    ![De pagina Opslagplaatsen van configuraties](./media/er-download-configurations-global-repo-repositories-list.png)

## <a name="import-a-single-configuration"></a>Eén configuratie importeren

1. Selecteer op de pagina **Opslagplaatsen van configuraties** in de configuratiestructuur de gewenste ER-configuratie.
2. Selecteer op het sneltabblad **Versies** de vereiste versie van de geselecteerde ER-configuratie.
3. Selecteer **Importeren** om de geselecteerde versie vanuit de algemene opslagplaats te downloaden naar het huidige exemplaar van Finance.

    > [!NOTE]
    > De knop **Importeren** is niet beschikbaar voor ER-configuratieversies die al aanwezig zijn in het huidige Finance-exemplaar.

    ![Configuratie archiefpagina](./media/er-download-configurations-global-repo-repository-content.png)

## <a name="import-filtered-configurations"></a>Gefilterde configuraties importeren

1. Vouw op de pagina **Opslagplaatsen van configuraties** in de configuratiestructuur het sneltabblad **Filter** uit.
2. Voeg in raster **Labels** de benodigde labels toe.
3. Selecteer de betreffende land-/regiocodes in het veld **Toepasbaarheid land/regio** en selecteer vervolgens **Filter toepassen**.

    > [!NOTE]
    > Op het sneltabblad **Configuraties** worden alle configuraties weergegeven die voldoen aan de opgegeven selectievoorwaarden.

4. Selecteer op het sneltabblad **Configuraties** de optie **Importeren** om de gefilterde configuraties uit de algemene opslagplaats naar het huidige exemplaar te downloaden.
5. Selecteer op het sneltabblad **Configuraties** de optie **Filter opnieuw instellen** om de opgegeven selectievoorwaarden op te schonen.

    ![Configuratie archiefpagina](./media/er-download-configurations-global-repo-filtered-configurations.png)

> [!NOTE]
> Afhankelijk van de ER-instellingen worden configuraties gevalideerd nadat ze zijn geïmporteerd. U krijgt mogelijk meldingen over inconsistentieproblemen die worden vastgesteld. U moet de problemen oplossen voordat u de geïmporteerde configuratieversie kunt gebruiken. Zie voor meer informatie de lijst met gerelateerde bronnen voor dit onderwerp.

> [!NOTE]
> ER-configuraties worden geconfigureerd als afhankelijk van andere configuraties. In combinatie met een geselecteerde configuratie kunnen andere configuraties dus automatisch worden geïmporteerd. Zie [De afhankelijkheid van ER-configuraties voor andere onderdelen definiëren](tasks/er-define-dependency-er-configurations-from-other-components-july-2017.md) voor meer informatie over configuratieafhankelijkheden.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]