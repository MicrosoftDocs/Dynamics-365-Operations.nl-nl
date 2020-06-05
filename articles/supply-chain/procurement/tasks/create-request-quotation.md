---
title: Een offerteaanvraag maken
description: Deze procedure laat u zien hoe u een offerteaanvraag maakt.
author: mkirknel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchRFQCaseTableListPage, PurchCreateRFQCase, InventLocationIdLookup, PurchRFQCaseTable, InventItemIdLookupSimple, EcoResCategorySingleLookup, UnitOfMeasureLookup, PurchRFQEditLines, PurchRFQEditLinesPrintOptions, VendRFQJournal, SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 68624a0288f9eaaf8f74b361bb308b8ca3c03b29
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383159"
---
# <a name="create-a-request-for-quotation"></a>Een offerteaanvraag maken

[!include [banner](../../includes/banner.md)]

Deze procedure laat u zien hoe u een offerteaanvraag maakt. Dit wordt gewoonlijk gedaan door een inkoper. U kunt deze procedure gebruiken met het demogegevensbedrijf USMF of met uw eigen gegevens. U moet de verzoektypen hebben ingesteld voordat u begint. Zodra u deze taak hebt voltooid en een offerteaanvraag hebt gemaakt en verzonden, kunt u de antwoorden per leverancier invoeren, deze vergelijken en het contract toekennen.


## <a name="prepare-a-new-rfq"></a>Een nieuwe offerteaanvraag voorbereiden
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Offerteaanvragen > Alle offerteaanvragen**.
2. Klik op **Nieuw**.
    De volgende inkooptypen zijn beschikbaar: Inkooporder (dit is de standaard): een document dat het aanbod om producten te kopen of de acceptatie van een aanbod om producten te verkopen tegen een betaling bevestigt. Opdracht tot inkoop: dit type wordt automatisch geselecteerd als u een offerteaanvraag rechtstreeks vanuit een opdracht tot inkoop maakt. Als u deze optie handmatig selecteert, verschijnt er een foutmelding. Inkoopovereenkomst: een overeenkomst voor de aanschaf van een bepaalde hoeveelheid of waarde van een product in een bepaalde periode. Als u deze optie selecteert, moet u het datumbereik selecteren dat van toepassing is op de inkoopovereenkomst.  
3. In het veld **Documenttitel** typt u een veldwaarde.
4. In het veld **Verzoektype** typt of selecteert u een waarde.
    + Als een beoordelingsmethode aan het verzoektype is gekoppeld, wordt dit de standaardbeoordelingsmethode voor de offerteaanvraag die u maakt. Het is mogelijk om de beoordelingsmethode later te wijzigen.  
    + In het veld **Leveringsdatum** voert u een datum in.  
    + Selecteer de datum waarop u de artikelen wilt ontvangen.  
    + In het veld **Vervaldatum en -tijd** voert u een datum en tijd in.  
    + Geef de datum en tijd op wanneer leveranciers de offerteaanvraag moeten beantwoorden.  
5. In het veld **Magazijn** typt of selecteert u een waarde. Het afleveradres wordt standaard ingesteld op het magazijnadres.  
6. Klik op **OK**.

## <a name="add-lines"></a>Regels toevoegen

Nadat u de basisgegevens over uw offerteaanvraag hebt opgegeven, geeft u de goederen of services op waarop u wilt dat leveranciers bieden. Artikel is het standaardregeltype.

1. Typ of selecteer een waarde in het veld **Artikelnummer**. Als u USMF gebruikt, kunt u T0020 selecteren.  
2. Voer een getal in het veld **Hoeveelheid** in.
3. Klik op **Regel toevoegen**.
4. In het veld **Regeltype** selecteert u 'Categorie'. U kunt het categorieregeltype gebruiken om offerteaanvragen voor niet-voorraadgoederen of -services te maken. U moet vervolgens het type goederen of services van een hiërarchie van aanschaffingscategorieën selecteren.  
5. In het veld **Aanschaffingscategorie** typt of selecteert u een waarde.
6. Typ een waarde in het veld **Productnaam**.
7. Voer een getal in het veld **Hoeveelheid** in.
8. In het veld **Eenheid** typt of selecteert u een waarde.

## <a name="add-vendors"></a>Leveranciers toevoegen
1. Klik op **Koptekst** om van de weergave Regels over te schakelen naar de weergave Koptekst. 
2. Vouw de sectie **Leverancier** uit.
3. Klik op **Leveranciers automatisch toevoegen**. U kunt leveranciers automatisch aan de offerteaanvraag toevoegen op basis van de aanschaffingscategorie van de gevraagde artikelen. Als er geen leveranciers zijn goedgekeurd voor de categorieën die zijn opgenomen in de regels, kunt u leveranciers handmatig toevoegen.  
4. Klik op **Toevoegen**.
5. In het veld **Leveranciersrekening** typt of selecteert u een waarde.
6. Klik op **Toevoegen**.
7. In het veld **Leveranciersrekening** typt of selecteert u een waarde. Zodra u een leverancier hebt geselecteerd, is de status gemaakt. Dat wil zeggen dat de leveranciersgegevens in de RFQ zijn opgeslagen, maar dat u de RFQ niet naar de leverancier hebt gezonden. U kunt een leverancier aan een RFQ toevoegen, ongeacht de status van de leverancier.  

## <a name="send-the-rfq-to-vendors"></a>Offerteaanvraag verzenden naar leveranciers
1. In het **actievenster** klikt u op **Verzenden**. Controleer op de pagina Offerteaanvraag verzenden of de leveranciers in de lijst de leveranciers zijn die de offerteaanvraag moeten ontvangen.  
2. Klik op **Afdrukken**. In dit dialoogvenster kunt u de offerteaanvraag afdrukken. Als u ervoor kiest een antwoordblad af te drukken, wordt de inhoud hiervan gedefinieerd in Parameters voor Inkoopbeheer. Om te bepalen hoe u antwoordbladen afdrukt, klikt u op Geavanceerde afdrukopties zodra u het dialoogvenster Afdrukken hebt geopend. Er wordt voor elke leverancier een offerteaanvraag afgedrukt met de regels die de status Gemaakt of Verzonden hebben. Geannuleerde regels en regels met geregistreerde antwoorden worden niet afgedrukt.   
3. Klik op **Annuleren**.
4. Klik op **OK**.
5. Sluit de pagina.
6. Sluit de pagina.

## <a name="view-the-rfq-journal"></a>Het offerteaanvraagjournaal weergeven
1. Ga naar **Inkoopbeheer > Offerteaanvragen > Opvolging op offerteaanvragen > Offerteaanvraagjournalen**.
2. Klik op **Voorbeeld/afdrukken**.
3. Klik op **Oorspronkelijk voorbeeld**.
4. Sluit de pagina.
5. Sluit de pagina.

