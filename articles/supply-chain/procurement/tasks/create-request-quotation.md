--- 
title: Een offerteaanvraag maken
description: Deze procedure laat u zien hoe u een offerteaanvraag maakt.
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: df6d8620316cf0dcde457b06235d9e041a51e100
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---
# <a name="create-a-request-for-quotation"></a>Een offerteaanvraag maken

[!include[task guide banner](../../includes/task-guide-banner.md)]

Deze procedure laat u zien hoe u een offerteaanvraag maakt. Dit wordt gewoonlijk gedaan door een inkoper. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens. U moet de verzoektypen hebben ingesteld voordat u begint. Zodra u deze taak hebt voltooid en een offerteaanvraag hebt gemaakt en verzonden, kunt u de antwoorden per leverancier invoeren, deze vergelijken en het contract toekennen.


## <a name="prepare-a-new-rfq"></a>Een nieuwe offerteaanvraag voorbereiden
1. Ga naar Inkoop en sourcing > Offerteaanvragen > Alle offerteaanvragen.
2. Klik op Nieuw.
    * De volgende inkooptypen zijn beschikbaar: Inkooporder (dit is de standaard): een document dat het aanbod om producten te kopen of de acceptatie van een aanbod om producten te verkopen tegen een betaling bevestigt. Opdracht tot inkoop: dit type wordt automatisch geselecteerd als u een offerteaanvraag rechtstreeks vanuit een opdracht tot inkoop maakt. Als u deze optie handmatig selecteert, verschijnt er een foutmelding. Inkoopovereenkomst: een overeenkomst voor de aanschaf van een bepaalde hoeveelheid of waarde van een product in een bepaalde periode. Als u deze optie selecteert, moet u het datumbereik selecteren dat van toepassing is op de inkoopovereenkomst.  
3. Typ een waarde in het veld Documenttitel.
4. Typ of selecteer een waarde in het veld Verzoektype.
    * Als een beoordelingsmethode aan het verzoektype is gekoppeld, wordt dit de standaardbeoordelingsmethode voor de offerteaanvraag die u maakt. Het is mogelijk om de beoordelingsmethode later te wijzigen.  
    * Typ een datum in het veld Leveringsdatum.  
    * Selecteer de datum waarop u de artikelen wilt ontvangen.  
    * Voer in het veld Vervaldatum en -tijd een datum en tijd in.  
    * Geef de datum en tijd op wanneer leveranciers de offerteaanvraag moeten beantwoorden.  
5. Typ of selecteer een waarde in het veld Magazijn.
    * Het afleveradres wordt standaard ingesteld op het magazijnadres.  
6. Klik op OK.

## <a name="add-lines"></a>Regels toevoegen
    * Nadat u de basisgegevens over uw offerteaanvraag hebt opgegeven, geeft u de goederen of services op waarop u wilt dat leveranciers bieden. Artikel is het standaardregeltype.   
1. Typ of selecteer een waarde in het veld Artikelnummer.
    * Als u USMF gebruikt, kunt u T0020 selecteren.  
2. Voer in het veld Hoeveelheid een getal in.
3. Klik op Regel toevoegen.
4. Selecteer 'Categorie' in het veld Regeltype.
    * U kunt het categorieregeltype gebruiken om offerteaanvragen voor niet-voorraadgoederen of -services te maken. U moet vervolgens het type goederen of services van een hiërarchie van aanschaffingscategorieën selecteren.  
5. Typ of selecteer een waarde in het veld Aanschaffingscategorie.
6. Typ een waarde in het veld Productnaam.
7. Voer in het veld Hoeveelheid een getal in.
8. Typ of selecteer een waarde in het veld Eenheid.

## <a name="add-vendors"></a>Leveranciers toevoegen
1. Klik op Koptekst om van de weergave Regels over te schakelen naar de weergave Koptekst. 
2. Vouw de sectie Leverancier uit.
3. Klik op Leveranciers automatisch toevoegen.
    * U kunt leveranciers automatisch aan de offerteaanvraag toevoegen op basis van de aanschaffingscategorie van de gevraagde artikelen. Als er geen leveranciers zijn goedgekeurd voor de categorieën die zijn opgenomen in de regels, kunt u leveranciers handmatig toevoegen.  
4. Klik op Toevoegen.
5. Typ of selecteer een waarde in het veld Leveranciersrekening.
6. Klik op Toevoegen.
7. Typ of selecteer een waarde in het veld Leveranciersrekening.
    * Zodra u een leverancier hebt geselecteerd, is de status gemaakt. Dat wil zeggen dat de leveranciersgegevens in de RFQ zijn opgeslagen, maar dat u de RFQ niet naar de leverancier hebt gezonden. U kunt een leverancier aan een RFQ toevoegen, ongeacht de status van de leverancier.  

## <a name="send-the-rfq-to-vendors"></a>Offerteaanvraag verzenden naar leveranciers
1. Klik op Verzenden.
    * Controleer op de pagina Offerteaanvraag verzenden of de leveranciers in de lijst de leveranciers zijn die de offerteaanvraag moeten ontvangen.  
2. Klik op Afdrukken.
    * In dit dialoogvenster kunt u de offerteaanvraag afdrukken. Als u ervoor kiest een antwoordblad af te drukken, wordt de inhoud hiervan gedefinieerd in Parameters voor inkoop en sourcing. Om te bepalen hoe u antwoordbladen afdrukt, klikt u op Geavanceerde afdrukopties zodra u het dialoogvenster Afdrukken hebt geopend. Er wordt voor elke leverancier een offerteaanvraag afgedrukt met de regels die de status Gemaakt of Verzonden hebben. Geannuleerde regels en regels met geregistreerde antwoorden worden niet afgedrukt.   
3. Klik op Annuleren.
4. Klik op OK.
5. Sluit de pagina.
6. Sluit de pagina.

## <a name="view-the-rfq-journal"></a>Het offerteaanvraagjournaal weergeven
1. Ga naar Inkoop en sourcing > Offerteaanvragen > Opvolging op offerteaanvragen > Offerteaanvraagjournalen.
2. Klik op Voorbeeld/afdrukken.
3. Klik op Oorspronkelijk voorbeeld.
4. Sluit de pagina.
5. Sluit de pagina.


