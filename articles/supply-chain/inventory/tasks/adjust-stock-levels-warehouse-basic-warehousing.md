---
title: Voorraadniveaus in het magazijn aanpassen (basale magazijnen)
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadcorrectiejournaal om voorraadniveaus te corrigeren van producten in het magazijn.
author: MarkusFogelberg
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventJournalLossProfit, InventJournalCreate, InventLocationIdLookup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bba1df70cd23a29ddffad96a4a581154619dc74
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5834140"
---
# <a name="adjust-stock-levels-in-the-warehouse-basic-warehousing"></a>Voorraadniveaus in het magazijn aanpassen (basale magazijnen)

[!include [banner](../../includes/banner.md)]

Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadcorrectiejournaal om voorraadniveaus te corrigeren van producten in het magazijn. U moet een voorraadjournaalnaam hebben ingesteld voor voorraadcorrecties voordat u hiermee start. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.


## <a name="create-an-inventory-adjustment-journal"></a>Een voorraadcorrectiejournaal maken
1. Ga naar Voorraadbeheer > Journaalboekingen > Artikelen > Voorraadcorrectie.
2. Klik op Nieuw.
3. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de naam van het voorraadcorrectiejournaal dat u wilt gebruiken.
    * Enkele andere velden worden ingevuld op basis van de instelling van de naam voor het journaal voor voorraadcorrectie die u selecteert.  
5. Klik op OK.

## <a name="create-journal-lines"></a>Journaalregels maken
1. Klik op Nieuw.
2. Markeer in de lijst het veld met het artikelnummer.
3. Selecteer een artikel in het veld Artikelnummer. Als u het demobedrijf USMF gebruikt, typt u 'D0001'.
4. Klik in het veld Locatie op de vervolgkeuzeknop om de zoekopdracht te openen.
5. Selecteer een locatie in de lijst.
6. Klik in het veld Magazijn op de vervolgkeuzeknop om de zoekopdracht te openen.
7. Selecteer een magazijn in de lijst.
    * Als u een artikel met Locatie als verplichte dimensie hebt geselecteerd, moet u de locatie hier opgeven.  
8. Voer in het veld Hoeveelheid een getal in.
    * Het kostprijsveld geeft de kosten per eenheid voor voorraadontvangsten op. Als de kosten niet voor het artikelnummer zijn opgegeven of als u deze handmatig wilt wijzigen, doet u dat hier.  

## <a name="validate-and-post-the-inventory-adjustment-journal"></a>Het voorraadcorrectiejournaal valideren en boeken
1. Klik op Valideren.
2. Klik op OK.
3. Klik op Boeken.
    * Wanneer u dit soort journaal boekt, wordt een voorraadontvangst of -uitgifte geboekt, worden het niveau en de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.  
4. Klik op OK.
5. Het formulier sluiten.
6. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]