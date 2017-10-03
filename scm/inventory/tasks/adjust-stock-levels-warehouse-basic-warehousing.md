---
title: Voorraadniveaus in het magazijn aanpassen (basale magazijnen)
description: Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadcorrectiejournaal om voorraadniveaus te corrigeren van producten in het magazijn.
author: MarkusFogelberg
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mafoge
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 9b947a02be981155053e33a4ef20e19bf2a194a5
ms.openlocfilehash: f96db79bcb6ec26daaeb66d29edb18486daafab0
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# Voorraadniveaus in het magazijn aanpassen (basale magazijnen)

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure begeleidt u door het proces voor het maken en boeken van een voorraadcorrectiejournaal om voorraadniveaus te corrigeren van producten in het magazijn. U moet een voorraadjournaalnaam hebben ingesteld voor voorraadcorrecties voordat u hiermee start. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. Deze taken worden normaal gesproken uitgevoerd door een magazijnmedewerker.


## Een voorraadcorrectiejournaal maken
1. Ga naar Voorraadbeheer > Journaalboekingen > Artikelen > Voorraadcorrectie.
2. Klik op Nieuw.
3. Klik in het veld Naam op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Klik in de lijst op de naam van het voorraadcorrectiejournaal dat u wilt gebruiken.
    * Enkele andere velden worden ingevuld op basis van de instelling van de naam voor het journaal voor voorraadcorrectie die u selecteert.  
5. Klik op OK.

## Journaalregels maken
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

## Het voorraadcorrectiejournaal valideren en boeken
1. Klik op Valideren.
2. Klik op OK.
3. Klik op Boeken.
    * Wanneer u dit soort journaal boekt, wordt een voorraadontvangst of -uitgifte geboekt, worden het niveau en de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.  
4. Klik op OK.
5. Het formulier sluiten.
6. Sluit de pagina.

