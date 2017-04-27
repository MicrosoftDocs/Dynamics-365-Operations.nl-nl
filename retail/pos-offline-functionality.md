---
title: Offline POS-functionaliteit
description: Dit artikel biedt informatie over de offlinemodus voor Retail Modern POS, waarin POS-apparaten automatisch van de kanaaldatabase naar de offlinedatabase schakelen als de detailhandelserver niet beschikbaar is. Daarnaast bevat dit artikel algemene configuratiegegevens voor de offlinemodus en wordt de gegevenssynchronisatie uitgelegd die plaatsvindt tussen de offlinedatabase en de kanaaldatabase.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 27041
ms.assetid: 20b51874-8912-40cf-9296-864df707315a
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: ef4d20b3302e4a420c7013b77a57ebdfa99fe6a3
ms.lasthandoff: 03/31/2017


---

# <a name="pos-offline-functionality"></a>Offline POS-functionaliteit

[!include[banner](includes/banner.md)]


Dit artikel biedt informatie over de offlinemodus voor Retail Modern POS, waarin POS-apparaten automatisch van de kanaaldatabase naar de offlinedatabase schakelen als de detailhandelserver niet beschikbaar is. Daarnaast bevat dit artikel algemene configuratiegegevens voor de offlinemodus en wordt de gegevenssynchronisatie uitgelegd die plaatsvindt tussen de offlinedatabase en de kanaaldatabase.

<a name="overview"></a>Overzicht
--------

In Retail Modern POS gaat een POS-apparaat in offlinemodus wanneer de detailhandelsserver niet beschikbaar is. Dit betekent dat als de verbinding met de detailhandelsserver verbroken wordt, Retail Modern POS automatisch overschakelt naar de offlinedatabase. Als een gegevensaanvraag tijdens een verkooptransactie niet binnen de time-outinterval, die in het offline profiel is geconfigureerd, slaagt, wordt Retail Modern POS automatisch geschakeld naar de offlinedatabase en zet de verkooptransactie voort. Terwijl het POS-apparaat in offlinemodus is, probeert Retail Modern POS om opnieuw verbinding te maken met de detailhandelsserver na de interval voor opnieuw verbinden die in het offlineprofiel is geconfigureerd. Deze poging om opnieuw te verbinden vindt alleen aan het begin van een transactie plaats.

### <a name="determining-the-connection-mode-of-retail-modern-pos"></a>De verbindingsmodus van Retail Modern POS bepalen

De statuskoptekst in Retail Modern POS geeft de huidige verbindingsstatus aan, en het venster **Verbindingsstatus** toont de status van de laatste poging om met de offlinedatabase te synchroniseren. [![Verbindingsstatus](./media/status.png)](./media/status.png)

### <a name="creating-a-button-to-manually-switch-between-online-and-offline-modes"></a>Een knop maken om handmatig te schakelen tussen en online- en offlinemodus

U kunt een knop toevoegen aan Retail Modern POS om handmatig tussen en online- en offlinemodus te schakelen. Maak een knop voor POS-bewerking **917 – Databaseverbindingstatus**. De naam van deze knop is **Verbinding verbreken** wanneer Retail Modern POS met de detailhandelsserver wordt verbonden en **Verbinden** als de verbinding is verbroken. U kunt deze knop gebruiken om de verbinding te bekijken en om de verbinding met de detailhandelsserver te verbinding of er verbinding mee te maken. [![Knop Verbinding verbreken in Retail Modern POS](./media/details-1024x537.png)](./media/details.png)

## <a name="setup"></a>Instellingen
Om offline ondersteuning voor een POS-apparaat (register) te activeren, stelt u de optie **Offlineondersteuning** in op **Ja** op de pagina **Register**. Een nieuwe kanaaldatabase-entiteit wordt gemaakt en aan de kanaalgegevensgroep van de winkel toegevoegd. Voer vervolgens alle vereiste distributieplanningen uit om de gegevenspakketten voor de offlinedatabase te genereren. Installeer vervolgens de offline versie van Retail Modern POS. Het installatieproces maakt de offlinedatabase. Installeer ook Microsoft SQL Server 2014 Express indien nodig. Offlinegegevenssynchronisatie start na de eerste aanmelding bij Retail Modern POS.

## <a name="data-synchronization"></a>Gegevenssynchronisatie
De Detailhandelsplanner wordt gebruikt om hoofdgegevens naar de offlinedatabase te verzenden. Standaard, wanneer een distributieplanning wordt uitgevoerd, worden de gegevenswijzigingen verzonden naar zowel de kanaaldatabase als de offlinedatabase. Retail Modern POS bevat de async sync-bibliotheek die alle beschikbare gegevenspakketten downloadt en invoegt in de offlinedatabase. Als transacties offline zijn gemaakt, uploadt Retail Modern POS ze naar de detailhandelsserver, zodat ze in de kanaaldatabase kunnen worden ingevoegd. De offline gegevenssynchronisatie kan alleen plaatsvinden als Retail Modern POS wordt uitgevoerd. [![Offline synchronisatie](./media/offline-sync-1024x521.png)](./media/offline-sync.png)




