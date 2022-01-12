---
title: Overzicht van waarschuwingen (bevat video)
description: Dit onderwerp biedt algemene informatie over waarschuwingen. U kunt waarschuwingen gebruiken om op de hoogte te blijven over de gebeurtenissen die u wilt bijhouden tijdens de werkdag.
author: RichdiMSFT
ms.date: 09/04/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EventCreateRule
audience: Application user
ms.reviewer: sericks
ms.custom: intro-internal
ms.search.region: Global
ms.author: richdi
ms.search.validFrom: 2018-3-30
ms.dyn365.ops.version: Platform update 15
ms.openlocfilehash: 857a837872abff44c8c7af5e938f7610fa61d94e
ms.sourcegitcommit: ef0dd4245fc499907ffe00e2a32f59a6cd96e45d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/18/2021
ms.locfileid: "7937466"
---
# <a name="alerts-overview"></a>Overzicht van waarschuwingen

[!include [banner](../includes/banner.md)]

## <a name="about-alerts"></a>Informatie over waarschuwingen
Meldingen vormen een waarschuwingssysteem voor kritieke gebeurtenissen in het systeem. U kunt waarschuwingen gebruiken om op de hoogte te blijven over de gebeurtenissen die u wilt bijhouden tijdens de werkdag. U kunt eenvoudig uw eigen set met waarschuwingsregels maken, zodat u wordt gewaarschuwd bij leveringen die te laat zijn, orders die zijn verwijderd, prijzen die veranderen of andere gebeurtenissen waarop u moet reageren.

In Enterprise Resource Planning (ERP) zijn er verschillende typische scenario's waarin de waarschuwingsfunctie kan worden gebruikt. Hieronder vindt u enkele voorbeelden.

### <a name="scenario-1-create-an-alert-rule-for-new-sales-orders"></a>Scenario 1: een waarschuwingsregel maken voor nieuwe verkooporders

1. Open de pagina **Alle verkooporders**.
2. Selecteer in het Actievenster op het tabblad **Opties** in de groep **Delen** de optie **Een aangepaste waarschuwing maken**.
3. Selecteer in het dialoogvenster **Waarschuwingsregel maken** op het sneltabblad **Waarschuw mij wanneer** in het veld **Gebeurtenis** de optie **Record is gemaakt**.

### <a name="scenario-2-create-an-alert-rule-for-postponement-of-a-delivery-date"></a>Scenario 2: een waarschuwingsregel maken voor uitstel van een leveringsdatum

1. Open de pagina **Alle inkooporders**.
2. Selecteer een inkooporder-id voor toegang tot de details van de inkooporder.
3. Vouw het sneltabblad **Inkooporderkoptekst** uit.
4. Selecteer in het Actievenster op het tabblad **Opties** in de groep **Delen** de optie **Een aangepaste waarschuwing maken**.
5. Selecteer in het dialoogvenster **Waarschuwingsregel maken** op het sneltabblad **Waarschuw mij wanneer** in het veld **Veld** de optie **Leverdatum**.
6. Selecteer in het veld **Gebeurtenis** de optie **is uitgesteld**.
    
Na het sluiten van het dialoogvenster **Waarschuwingsregel maken** wordt de regel weergegeven op de pagina **Waarschuwingsregels beheren**. U kunt de pagina **Waarschuwingsregels beheren** gebruiken om uw bestaande waarschuwingsregels bij te werken. Zo kunt u gebeurtenistriggers wijzigen, gebeurtenismeldingen bijwerken en vervaldatums instellen. U opent de pagina **Waarschuwingsregels beheren** met de knop **Waarschuw mij** op het tabblad **Opties** van het Actievenster.

## <a name="what-occurs-when-an-alert-rule-is-created"></a>Wat gebeurt er wanneer er een waarschuwingsregel wordt gemaakt?

Wanneer u waarschuwingsregels maakt, kunt u een vooraf gedefinieerde gebeurtenis koppelen aan een specifiek veld. Bijvoorbeeld, wanneer de in het veld opgegeven datum aanbreekt of wanneer de inhoud van een veld verandert. U kunt ook een gebeurtenis koppelen aan de records op een bepaalde pagina. Wanneer bijvoorbeeld een record wordt gemaakt of verwijderd.

Als de geselecteerde gebeurtenis voor het veld of een record op de pagina plaatsvindt, wordt er een waarschuwing naar u verzonden. U maakt bijvoorbeeld een regel waarin u het veld **Leveringsdatum** op een bepaalde inkooporderregel koppelt aan de gebeurtenis **was zoveel tijd geleden al vervallen**. U stelt de periode in op vijf dagen. In dit geval wordt een waarschuwing verzonden vijf dagen na de leveringsdatum van die inkooporderregel.

U kunt bovendien waarschuwingsregels verfijnen door voorwaarden in te stellen. U kunt bijvoorbeeld worden gewaarschuwd over nieuwe inkooporders die zijn gemaakt voor een specifieke leverancieraccounts.

## <a name="preparing-for-an-alert"></a>Voorbereiden op een waarschuwing

Bepaal voordat u een waarschuwingsregel instelt, wanneer of in welke situaties u waarschuwingen wilt ontvangen. Als u weet over welke gebeurtenis u wilt worden gewaarschuwd, gaat u naar de pagina met de gegevens die de gebeurtenis veroorzaken. De gebeurtenis kan een datum zijn die aanbreekt of een specifieke wijziging die plaatsvindt. Daarom moet u de pagina vinden waar de datum is gespecificeerd of die het veld bevat dat verandert of de nieuwe record. Wanneer u deze informatie hebt, kunt u de waarschuwingsregel maken.

## <a name="components-of-an-alert-rule"></a>Onderdelen van een waarschuwingsregel

Een waarschuwingsregel heeft vijf onderdelen:

- **Gebeurtenis**: de gebeurtenis die een waarschuwingsregel activeert, kan een datum zijn of een bepaalde wijziging die plaatsvindt. U definieert gebeurtenissen op het sneltabblad **E-mailwaarschuwingen voor taakstatuswijzigingen verzenden** van het dialoogvenster **Waarschuwingsregel maken**.
- **Voorwaarde**: selecteer op het sneltabblad **Waarschuw mij voor** van het dialoogvenster **Waarschuwingsregel maken** de reikwijdte van de voorwaarde, om te bepalen wanneer u waarschuwingen over gebeurtenissen ontvangt. U kunt de regel alleen op de huidige record toepassen of op alle zichtbare records op de pagina. Als de regel voor rechtspersonen geldt, kunt u de optie **Organisatiebreed** instellen op **Ja**.
- **Verlopen van regel**: geef op het sneltabblad **Waarschuw mij tot** van het dialoogvenster **Waarschuwingsregel maken** op hoe lang de waarschuwingsregel actief moet zijn.
- **Inhoud**: geef op het sneltabblad **Waarschuw mij met** van het dialoogvenster  **Waarschuwingsregel maken** de onderwerptekst en de berichttekst op die in de waarschuwingsberichten wordt gebruikt.
- **Gebruiker**: geef op het sneltabblad **Waarschuwing voor wie** van het dialoogvenster **Waarschuwingsregel maken** op welke gebruiker de waarschuwingsberichten moet ontvangen. Uw gebruikers-ID is standaard geselecteerd.

    > [!NOTE]
    > Deze optie is beperkt tot beheerders van de organisatie.

## <a name="videos"></a>Video's

### <a name="how-to-use-alerts-to-monitor-filtered-data"></a>Waarschuwingen gebruiken om gefilterde gegevens te controleren

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3DWZ3]

De video [Waarschuwingen gebruiken om gefilterde gegevens te controleren](https://youtu.be/ZYKMcv6kl9s) (zie hierboven) is opgenomen in de speellijst voor [Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.

### <a name="alert-rule-options"></a>Opties voor waarschuwingsregels

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE3E4PV]

De video [Opties voor waarschuwingsregels](https://youtu.be/cpzimwOjicM) (zie hierboven) is opgenomen in de [Finance and Operations-afspeellijst](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]