---
title: Bijgewerkte versies van ER-configuraties importeren
description: In dit onderwerp wordt uitgelegd hoe u ER-configuraties (Electronic Reporting) importeert uit de algemene opslagplaats van de configuratieservice.
author: NickSelin
ms.date: 06/09/2020
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
ms.openlocfilehash: 724048991fc8864ef72a5155af66b9c709f4b875
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893951"
---
# <a name="import-updated-versions-of-er-configurations"></a>Bijgewerkte versies van ER-configuraties importeren

[!include [banner](../includes/banner.md)]

Om [ER-configuraties](general-electronic-reporting.md#Configuration) (Electronic Reporting) te delen, wordt gebruik gemaakt van [ER-opslagplaatsen](general-electronic-reporting.md#Repository). U kunt configuraties vanuit verschillende opslagplaatsen [importeren](download-electronic-reporting-configuration-lcs.md) in uw exemplaar van Microsoft Dynamics 365 Finance. Wanneer u configuraties importeert, kunnen [configuratie providers](general-electronic-reporting.md#Provider) nieuwe [versies](general-electronic-reporting.md#component-versioning) van opslagplaatsen publiceren zodat deze kunnen worden gedeeld.

In dit onderwerp wordt uitgelegd hoe u ER-configuraties importeert uit de algemene opslagplaats van de configuratieservice. Zie [Microsoft Dynamics 365 for Finance and Operations - Regulatory services, configuratieservice](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) voor meer informatie.

## <a name="review-the-available-updated-versions"></a>Controleren welke bijgewerkte versies beschikbaar zijn

1. Meld u aan bij Finance met een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Versie-updates van configuraties importeren**.

    ![Pagina Lokalisatieconfiguraties](./media/er-download-updated-versions-global-repo1.png)

4. Selecteer in het dialoogvenster **Versie-updates van ER-configuraties importeren** in het veld **Uitvoeringsmodus** de optie **Alleen beschikbare updates weergeven**. Selecteer vervolgens **OK**. 

    ![Veld voor uitvoeringsmodus ingesteld op Alleen beschikbare updates weergeven](./media/er-download-updated-versions-global-repo2.png)

5. Controleer de meldingen die u krijgt. Deze meldingen leveren de volgende informatie over de ER-configuraties in het huidige Finance-exemplaar en hoe deze overeenkomen met of afwijken van de inhoud van de algemene opslagplaats:

    - Het totale aantal ER-configuraties
    - ER-configuraties die niet aanwezig zijn in de globale opslagplaats
    - ER-configuraties waarvoor de meest recente versie al beschikbaar is in het huidige Finance-exemplaar (om de volledige lijst met deze ER-configuraties weer te geven, selecteert u de koppeling **Berichtdetails**).

        ![Bericht "De meest recente versies van de volgende configuraties zijn al geïmporteerd" en berichtdetails](./media/er-download-updated-versions-global-repo3.png)

    - ER-configuraties waarvoor de meest recente versie beschikbaar is in de algemene opslagplaats en geïmporteerd kan worden in het huidige Finance-exemplaar (om de volledige lijst met deze ER-configuraties weer te geven, selecteert u de koppeling **Berichtdetails**).

        ![Bericht "Updates beschikbaar" en berichtdetails](./media/er-download-updated-versions-global-repo4.png)

## <a name="import-available-updated-versions"></a>Beschikbare bijgewerkte versies importeren

1. Meld u aan bij Finance met een van de volgende rollen:

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

2. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
3. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Versie-updates van configuraties importeren**.
4. Selecteer in het dialoogvenster **Versie-updates voor ER-configuraties importeren** in het veld **Uitvoeringsmodus** de optie **Meest recente updates importeren** om de meest recente versies van ER-configuraties te importeren vanuit de globale opslagplaats in het huidige Finance-exemplaar.
5. Als u een batchtaak voor de import wilt plannen, stelt u op het sneltabblad **Uitvoeren in de achtergrond** de optie **Batchverwerking** in op **Ja**. Als u de import regelmatig wilt herhalen, configureert u het vereiste herhalingspatroon.

    ![Veld Uitvoeringsmodus ingesteld op Meest recente updates importeren](./media/er-download-updated-versions-global-repo5.png)

6. Selecteer **OK**.
7. Als u wilt weten welke configuratieversies zijn geïmporteerd, voert u een van de volgende stappen uit:

    - Als u de importfunctie interactief uitvoert in plaats van een batchtaak te gebruiken, controleert u de meldingen die u ontvangt.

        ![Meldingen die zijn ontvangen tijdens een interactieve importbewerking](./media/er-download-updated-versions-global-repo6.png)

    - Als u de import uitvoert in de batchmodus, volgt u deze stappen:

        1. Ga naar **Algemeen** \> **Query's** \> **Batchtaken** \> **Mijn batchtaken**.
        2. Zoek en selecteer de taak **Versie-updates van ER-configuraties importeren** en selecteer vervolgens in het actievenster op het tabblad **Batchtaak** de optie **Batchtaakhistorie** om de taakhistorie weer te geven.
        3. Selecteer op de pagina **Batchtaakhistorie** de optie **Logboek**. Selecteer vervolgens in de melding die u ontvangt de koppeling **Berichtdetails** om het taaklogboek weer te geven.

        ![Taaklogboek](./media/er-download-updated-versions-global-repo7.png)

> [!IMPORTANT]
> Het wordt niet aangeraden een terugkerende batch taak te plannen om bijgewerkte versies van de ER-configuraties rechtstreeks vanuit de globale opslagplaats te importeren in een productieomgeving, omdat de geïmporteerde versies meteen beschikbaar zijn voor gebruik. Gebruik in plaats daarvan deze aanpak om versies van ER-configuraties te implementeren in een sandbox-omgeving. Ze kunnen vervolgens worden geëvalueerd in de sandbox-omgeving, voordat u ze naar een productie omgeving distribueert.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage (ER)](general-electronic-reporting.md)
- [ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]