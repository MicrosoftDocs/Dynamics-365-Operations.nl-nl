---
title: Informatie over ouderdom van klanten instellen en genereren
description: Deze taakbegeleiding helpt u bij de instelling van een ouderdomsperiodedefinitie, ouderdom van klantsaldi te berekenen en saldi weer te geven in de lijst Ouderdomssaldi en de pagina Aanmaningen.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9fd8738cfd3466464c9fec1760e9a369ff3a4a67
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568230"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Informatie over ouderdom van klanten instellen en genereren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taakbegeleiding helpt u bij de instelling van een ouderdomsperiodedefinitie, ouderdom van klantsaldi te berekenen en saldi weer te geven in de lijst Ouderdomssaldi en de pagina Aanmaningen. Bij deze registratie wordt het demobedrijf USMF gebruikt.


## <a name="create-an-aging-period-definition"></a>Een ouderdomsperiodedefinitie maken
1. Ga naar Crediteringen en aanmaningen > Instellingen > Ouderdomsperiodedefinities.
2. Klik op Nieuw.
3. Typ in het veld Ouderdomsperiodedefinitie een waarde.
4. Typ een waarde in het veld Omschrijving.
5. Klik hieronder op Toevoegen om een nieuwe ouderdomsperiode in te voegen.
6. Voer in het veld Periode de omschrijving in om op ouderdomsrapporten weer te geven.
7. Voer een nummer in het veld Eenheid in.
8. Selecteer een optie in het veld Interval.
    * De grootboekperiode stemt de periode af op uw grootboekkalender. Dag, week, maand, kwartaal en jaren definiëren de grootte van het interval op datumtype. Onbeperkt selecteert alle transacties voor of na de vorige periode, afhankelijk van of het de eerste of laatste periode is.  
9. Selecteer een optie in het veld Ouderdomsindicator.
10. Selecteer de periode boven in het raster. Werk de omschrijving bij om de oudste periode in de ouderdomsperiodedefinitie te beschrijven
11. Voer in het veld Periode de nieuwe omschrijving van de ouderdomsperiode in.
12. Sluit de pagina.

## <a name="age-the-balances"></a>Ouderdom saldi berekenen
1. Ga naar Crediteringen en aanmaningen > Periodieke taken > Ouderdom van klantsaldi berekenen.
2. Selecteer in het veld Ouderdomsperiodedefinitie de ouderdomsperiodedefinitie die u hebt gemaakt.
    * U kunt één actieve momentopname voor elke ouderdomsperiodedefinitie hebben.  
    * Alle klanten worden standaard verwerkt. U kunt deze selectie gebruiken om een enkele incassoverzameling klanten te berekenen.  
    * Selecteer de datum van de transactie die u voor de ouderdomsrangschikking wilt gebruiken.  
    * Selecteer een "vanaf" datum voor ouderdomsrangschikking. De standaard is vandaag maar als u dit veld in Geselecteerde datum wijzigt, kunt u de gewenste datum kiezen. Gebruik voor batchverwerking de datum van vandaag.  
3. Vouw het bereik Bedrijf uit. U kunt de bedrijven selecteren die in de momentopname worden opgenomen. Het huidige bedrijf wordt standaard geselecteerd.
4. Klik op OK om de momentopname te verwerken. Het duurt even voor de schuifregelaar verdwijnt. Controleer het berichtencentrum op een bericht.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>De saldi op de lijst Vervallen saldi en op de pagina Aanmaning weergeven
1. Ga naar Crediteringen en aanmaningen > Incasso's > Vervallen saldi.
    * De lijstpagina geeft de saldi voor de klant weer. Het ouderdomspictogram geeft de ouderdomsperiode voor de oudste transactie weer.  
2. Selecteer een klant met een saldo.
3. Vouw het feitenvakgebied Ouderdomsrangschikking uit als u de ouderdomssaldi wilt weergeven.
    * De ouderdomsperiodedefinitie voor het feitenvak is afkomstig van de standaardouderdomsperiodedefinitie die wordt opgegeven in de parameters. U kunt deze wijzigen met het menu Incasso.  

