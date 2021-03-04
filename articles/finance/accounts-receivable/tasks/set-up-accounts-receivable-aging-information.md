---
title: Informatie over ouderdom van klanten instellen en genereren
description: Deze guide helpt u bij de instelling van een ouderdomsperiodedefinitie, ouderdom van klantsaldi te berekenen en saldi weer te geven in de lijst Ouderdomssaldi en de pagina Aanmaningen.
author: mikefalkner
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustVendReportInterval, CustAgingSnapshot, CustCollectionsPoolsListPage, CustCollections
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 439be64a864056cc19fd156f664a4b90601be040
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441982"
---
# <a name="set-up-and-generate-accounts-receivable-aging-information"></a>Informatie over ouderdom van klanten instellen en genereren

[!include [banner](../../includes/banner.md)]

Deze guide helpt u bij de instelling van een ouderdomsperiodedefinitie, ouderdom van klantsaldi te berekenen en saldi weer te geven in de lijst Ouderdomssaldi en de pagina Aanmaningen. Bij deze registratie wordt het demobedrijf USMF gebruikt.


## <a name="create-an-aging-period-definition"></a>Een ouderdomsperiodedefinitie maken
1. Ga naar **Navigatievenster > Modules > Crediteringen en aanmaningen > Instellen Ouderdomsperiodedefinities**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Ouderdomsperiodedefinitie**.
4. Typ een waarde in het veld **Beschrijving**.
5. Klik **Onder toevoegen** om een nieuwe ouderdomsperiode in te voegen.
6. Voer in het veld **Periode** de beschrijving in die u op ouderdomsrapporten wilt weergeven.
7. Voer een numerieke waarde in het veld **Eenheid** in.
8. Selecteer een optie in het veld **Interval**. De grootboekperiode stemt de periode af op uw grootboekkalender. Dag, week, maand, kwartaal en jaren definiëren de grootte van het interval op datumtype. Onbeperkt selecteert alle transacties voor of na de vorige periode, afhankelijk van of het de eerste of laatste periode is.  
9. Selecteer een optie in het veld **Ouderdomsindicator**.
10. Selecteer de periode boven in het raster. Werk de beschrijving bij om de oudste periode in de ouderdomsperiodedefinitie te beschrijven
11. Voer in het veld **Periode** de nieuwe beschrijving van de ouderdomsperiode in.
12. Sluit de pagina.

## <a name="age-the-balances"></a>Ouderdom saldi berekenen
1. Ga naar **Crediteringen en aanmaningen > Periodieke taken > Ouderdom van klantsaldi berekenen**.
2. Selecteer in het veld **Ouderdomsperiodedefinitie** de ouderdomsperiodedefinitie die u hebt gemaakt.
    + U kunt één actieve momentopname voor elke ouderdomsperiodedefinitie hebben.  
    + Alle klanten worden standaard verwerkt. U kunt deze selectie gebruiken om een enkele incassoverzameling klanten te berekenen.  
    + Selecteer de datum van de transactie die u voor de ouderdomsrangschikking wilt gebruiken.  
    + Selecteer een "vanaf" datum voor ouderdomsrangschikking. De standaard is vandaag maar als u dit veld in Geselecteerde datum wijzigt, kunt u de gewenste datum kiezen. Gebruik voor batchverwerking de datum van vandaag.  
3. Vouw het bereik **Bedrijf** uit. U kunt de bedrijven selecteren die in de momentopname worden opgenomen. Het huidige bedrijf wordt standaard geselecteerd.
4. Klik op **OK** om de momentopname te verwerken. Het duurt even voor de schuifregelaar verdwijnt. Controleer het berichtencentrum op een bericht.

## <a name="view-the-balances-on-the-aged-balances-list-and-on-the-collection-page"></a>De saldi op de lijst Vervallen saldi en op de pagina Aanmaning weergeven
1. Ga naar **Crediteringen en aanmaningen > Incasso's > Vervallen saldi**. De lijstpagina geeft de saldi voor de klant weer. Het ouderdomspictogram geeft de ouderdomsperiode voor de oudste transactie weer.  
2. Selecteer een klant met een saldo.
3. Vouw het feitenvakgebied **Naar ouderdom geschikt** uit als u de ouderdomssaldi wilt weergeven. De ouderdomsperiodedefinitie voor het feitenvak is afkomstig van de standaardouderdomsperiodedefinitie die wordt opgegeven in de parameters. U kunt deze wijzigen met het menu Incasso.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]