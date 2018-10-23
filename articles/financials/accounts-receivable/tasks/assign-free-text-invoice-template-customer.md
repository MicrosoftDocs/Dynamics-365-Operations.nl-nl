--- 
title: Sjabloon voor vrije-tekstfacturen toewijzen aan een klant
description: Deze taak geeft aan hoe u een sjabloon voor een vrije-tekstfactuur kunt toewijzen aan een klant.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 317b3bd4c1f395987ef3dbbd268c40be5c688320
ms.contentlocale: nl-nl
ms.lasthandoff: 09/14/2018

---
# <a name="assign-free-text-invoice-template-to-a-customer"></a>Sjabloon voor vrije-tekstfacturen toewijzen aan een klant

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze taak geeft aan hoe u een sjabloon voor een vrije-tekstfactuur kunt toewijzen aan een klant. Deze taak gebruikt het demobedrijf USMF en is bedoeld voor de gebruiker die verantwoordelijk is voor het beheren en verwerken van klantenfacturen.

1. Ga naar Klanten > Klanten > Alle klanten.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in het actievenster op Factuur.
4. Klik op Terugkerende-facturen.
    * Gebruik deze pagina om sjablonen voor vrije-tekstfacturen toe te wijzen aan klanten en op te geven hoe vaak facturen moeten worden verzonden.  
5. Klik op Nieuw om een nieuwe sjabloon toe te wijzen aan de klant.
6. Selecteer de sjabloon voor vrije-tekstfacturen die u wilt toewijzen aan de klant.
7. Zoek en selecteer het gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. De datum invoeren waarop de eerste factuur wordt gegenereerd.
    * Voer een terugkerende einddatum in.  
    * Selecteer een van de volgende: Geen einddatum: er worden voor onbepaalde tijd facturen gegenereerd totdat de sjabloon wordt verwijderd van de klantrekening.  Einddatum facturering: selecteer deze optie en voor de laatste datum in waarop de factor kan worden gegenereerd.  
    * Het maximale cumulatieve bedrag waarna het genereren van facturen wordt gestopt.  
    * Het maximale cumulatieve bedrag invoeren dat kan worden gefactureerd op basis van de geselecteerde sjabloon. Als u bijvoorbeeld 1000.00 invoert en maandelijkse facturen genereert voor 100,00, stopt het genereren van facturen na de tiende factuur.  
    * Genereer terugkerende facturen door de standaardwaarden te gebruiken van sjabloon voor vrije-tekstfacturen of de klantrekening.  
    * Opgeven of de sjabloon voor vrije-tekstfacturen of de klantrekening moet worden gebruikt om de standaardwaarden te bepalen voor taal, boekingsprofiel, btw-groep, btw-groep voor artikelen, lijstcode, land/regio voor levering, valuta, betalingsvoorwaarden, betalingsmethode, betalingsspecificatie, betalingsschema, contantkorting, financiële dimensies en giro-overboekingsstrook bij het maken van facturen.  
10. Selecteer het terugkeerpatroon.
    * Dagelijks: selecteer deze optie en geef het aantal dagen op in het veld Per. Als u bijvoorbeeld 15 invoert, wordt elke vijftien dagen een factuur gegenereerd voor deze klant.  Wekelijks: selecteer deze optie en geef het aantal weken op in het veld Per. Als u bijvoorbeeld 2 invoert, wordt elke twee weken een factuur gegenereerd voor deze klant.  Maandelijks: selecteer deze optie en geef het aantal maanden op in het veld Per. Als u bijvoorbeeld 6 invoert, wordt elke zes maanden een factuur gegenereerd voor deze klant.  Jaar: selecteer deze optie en geef het aantal jaren op in het veld Per. Als u bijvoorbeeld 2 invoert, wordt elke twee jaar een factuur gegenereerd voor deze klant.  
11. Voer een getal in het veld Per in.


