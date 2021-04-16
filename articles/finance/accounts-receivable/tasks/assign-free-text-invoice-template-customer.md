---
title: Een sjabloon voor vrije-tekstfacturen toewijzen aan een klant
description: Deze taak geeft aan hoe u een sjabloon voor een vrije-tekstfactuur kunt toewijzen aan een klant.
author: ShivamPandey-msft
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0219521867d1cfb1fa4edcdf20dd70eea8a3d0e1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819885"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a>Een sjabloon voor vrije-tekstfacturen toewijzen aan een klant

[!include [banner](../../includes/banner.md)]

Deze taak geeft aan hoe u een sjabloon voor een vrije-tekstfactuur kunt toewijzen aan een klant. Deze taak gebruikt het demobedrijf USMF en is bedoeld voor de gebruiker die verantwoordelijk is voor het beheren en verwerken van klantenfacturen.

1. Ga in het **navigatiedeelvenster** naar **Modules > Klanten > Klanten > Alle klanten.**
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in het **actievenster** op **Factuur**.
4. Klik op **Terugkerende facturen**. Gebruik deze pagina om sjablonen voor vrije-tekstfacturen toe te wijzen aan klanten en op te geven hoe vaak facturen moeten worden verzonden.  
5. Klik op **Nieuw** om een nieuwe sjabloon toe te wijzen aan de klant.
6. Selecteer in het veld **Sjabloon** de sjabloon voor vrije-tekstfacturen die u wilt toewijzen aan de klant.
7. Zoek en selecteer de gewenste record in de lijst.
8. Klik in de lijst op de koppeling in de geselecteerde rij.
9. Voer in het veld **Begindatum facturering** de datum in waarop de eerste factuur wordt gegenereerd.
10. Voer in de sectie **Einde terugkeerpatroon** een terugkerende einddatum in.  
    * Selecteer een van de volgende: Geen einddatum: er worden voor onbepaalde tijd facturen gegenereerd totdat de sjabloon wordt verwijderd van de klantrekening.
    * Einddatum facturering: selecteer deze optie en voor de laatste datum in waarop de factor kan worden gegenereerd.  
11. Voer in het veld **Maximum cumulatief bedrag** het maximale cumulatieve bedrag in waarna het genereren van facturen wordt gestopt. Het maximale cumulatieve bedrag invoeren dat kan worden gefactureerd op basis van de geselecteerde sjabloon. Als u bijvoorbeeld 1000.00 invoert en maandelijkse facturen genereert voor 100,00, stopt het genereren van facturen na de tiende factuur.  
12. Selecteer in de sectie **Terugkerende facturen genereren door de standaardwaarden te gebruiken uit** de sjabloon voor vrije-tekstfacturen of de klantrekening. Opgeven of de sjabloon voor vrije-tekstfacturen of de klantrekening moet worden gebruikt om de standaardwaarden te bepalen voor taal, boekingsprofiel, btw-groep, btw-groep voor artikelen, lijstcode, land/regio voor levering, valuta, betalingsvoorwaarden, betalingsmethode, betalingsspecificatie, betalingsschema, contantkorting, financiële dimensies en giro-overboekingsstrook bij het maken van facturen.  
13. Selecteer het terugkeerpatroon in het veld **Terugkeerpatroon**.
    + Dagelijks: selecteer deze optie en geef het aantal dagen op in het veld Per. Als u bijvoorbeeld 15 invoert, wordt elke vijftien dagen een factuur gegenereerd voor deze klant.
    + Wekelijks: selecteer deze optie en geef het aantal weken op in het veld Per. Als u bijvoorbeeld 2 invoert, wordt elke twee weken een factuur gegenereerd voor deze klant.
    + Maandelijks: selecteer deze optie en geef het aantal maanden op in het veld Per. Als u bijvoorbeeld 6 invoert, wordt elke zes maanden een factuur gegenereerd voor deze klant.
    + Jaar: selecteer deze optie en geef het aantal jaren op in het veld Per. Als u bijvoorbeeld 2 invoert, wordt elke twee jaar een factuur gegenereerd voor deze klant.  
14. Voer een getal in het veld **Per** in.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]