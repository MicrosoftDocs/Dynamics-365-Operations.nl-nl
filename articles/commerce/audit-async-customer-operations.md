---
title: Synchronisatie van klantbewerkingen controleren in Headquarters
description: In dit artikel wordt uitgelegd hoe u de synchronisatie van klantbewerkingen in Microsoft Dynamics 365 Commerce Headquarters controleert om problemen met sitegebruikers te verhelpen.
author: gvrmohanreddy
ms.date: 10/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2022-09-28
ms.openlocfilehash: c615b0b436e01a1423b5611a72f0056b5b14f8e8
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9691064"
---
# <a name="audit-synchronization-of-customer-operations-in-headquarters"></a>Synchronisatie van klantbewerkingen controleren in Headquarters

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit artikel wordt uitgelegd hoe u de synchronisatie van klantbewerkingen in Microsoft Dynamics 365 Commerce Headquarters controleert om problemen met sitegebruikers te verhelpen.

Wanneer organisaties de mogelijkheid beginnen te krijgen om klanten asynchroon te maken en te bewerken, hebben sitebeheerders een manier nodig om bewerkingen weer te geven en problemen op te lossen op basis van sitegebruikersaanvragen of procesproblemen. In die scenario's moeten sitebeheerders bewerkingen voor het maken en bewerken van klanten kunnen controleren en eventuele fouten kunnen oplossen met een selfservicemodel.

## <a name="customer-synchronization-status"></a>Synchronisatiestatus van klant

Wanneer u zich aanmeldt voor de asynchrone modus van klantbeheer en de bijbehorende functies, moeten beheerders van Commerce headquarters een terugkerende batchtaak aanmaken en inplannen voor de **P-taak**, de taak **Klanten en zakenpartners synchroniseren vanuit de asynchrone modus** en de taak **1010**, zodat eventuele asynchrone klanten worden geconverteerd naar synchronisatieklanten in Commerce headquarters. Synchronisatie van klantbeheerbewerkingen vindt plaats wanneer deze taken worden uitgevoerd. Zie [Modus voor het maken van asynchrone klanten](async-customer-mode.md) voor meer informatie.

Als bedrijfseigenaar kunt u de volgende bewerkingen uitvoeren:

- Alle (maak)bewerkingen van sitegebruikers weergeven. Details omvatten de status en een tijdstempel.
- Bewerkingen filteren met behulp van de velden en waarden uit de klantentabel om het auditlogboek te beperken.
- Korte omschrijvingen van wijzigingen weergeven met de statusdetails om bewerkingen op een hoog niveau te begrijpen.
- Bij fouten problematische velden bewerken en corrigeren om vervolgens specifieke klantbewerkingen op te slaan en te synchroniseren.

### <a name="elements-on-the-customer-synchronization-status-page"></a>Elementen op de pagina Synchronisatiestatus van klant

Als u een lijst met alle synchronisatiebewerkingen wilt weergeven, gaat u in Commerce headquarters naar **Commerce en Retail \> Klanten \> Synchronisatiestatus van klant**. In de volgende afbeelding ziet u een voorbeeld van de pagina **Synchronisatiestatus van klant**.

![De pagina Synchronisatiestatus van klant in Commerce headquarters.](media/D365-Commerce-Customer-Mgmt-Audi-Async-Operations.png)

Standaard bevat de lijst met klantsynchronisatiebewerkingen aan de linkerkant van de pagina **Synchronisatiestatus van klant** de volgende kolommen:

- Naam van kanaal
- Klantrekening
- Asynchroon klantaccount
- Tijdstempel van bewerkingen
- Synchronisatiestatus van klant

Rechtsboven op de pagina worden klantrekeningdetails weergegeven, zoals de waarden voor **Klantrekening**, **Retail Async-bewerking**, **Synchronisatiestatus van klant** en **Laatste bekende fout**.

De sectie **Beschrijving van de wijziging** bevat een beschrijving van het type klantbeheerbewerking dat is uitgevoerd (bijvoorbeeld het maken van een klant, het bijwerken van een rekening of een synchronisatiefout in details).

De sectie **Klantkenmerken** bevat een raster met alle klantkenmerken met oude en nieuwe waarden. U kunt deze sectie bewerken als u de waarden van uw klantkenmerken wilt wijzigen om fouten te herstellen en vervolgens opnieuw synchroniseren.
