---
title: Een bestelaanvraag voor verbruik maken
description: Deze procedure begeleidt u door het proces voor het maken van een bestelaanvraag.
author: mkirknel
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e81ca3966cf7dae88468ccf107b52b8c3d7b323d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560638"
---
# <a name="create-a-requisition-for-consumption"></a>Een bestelaanvraag voor verbruik maken

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze procedure begeleidt u door het proces voor het maken van een bestelaanvraag. Het toont u verschillende manieren om producten in uw aanschaffingscatalogus te zoeken en hoe u een product toevoegt dat niet in uw catalogus staat. Voordat u deze procedure start, moet u een inkoopbeleid instellen met Verbruik als standaardtype bestelaanvraag. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. De procedure kan alleen via een gebruikersprofiel worden uitgevoerd dat is ingesteld als werknemer.  Deze taak moet doorgaans worden uitgevoerd door een werknemer. De werknemersrol Werknemer staat toe dat u de taken uitvoert. Als u USMF gebruikt, kunt u zich ook aanmelden als Alicia.


## <a name="create-a-new-requisition"></a>Een nieuwe bestelaanvraag maken
1. Ga naar Inkoop en sourcing > Opdrachten tot inkoop > Door mij voorbereide inkoopbestelopdrachten.
2. Klik op Nieuw.
3. Geef de bestelopdracht een naam in het veld Naam.
4. Voer in het veld Aangevraagd een datum in.
    * De aangevraagde datum en boekhoudingsdatums worden standaard gekopieerd naar de regels van de opdracht tot inkoop. Ze kunnen worden gewijzigd op regelniveau. De gevraagde datum is de gevraagde leveringsdatum.  
5. Voer in het veld Boekingsdatum een datum in.
    * De boekhoudingsdatum wordt gebruikt om de boeking in het grootboek te registeren en om te valideren dat de budgetfondsen beschikbaar zijn.  
6. Klik op OK.
7. Klik in het veld Reden op de vervolgkeuzeknop om de zoekopdracht te openen.
    * De zakelijke reden die u selecteert, verschijnt standaard voor de regels van de opdracht tot inkoop, maar u kunt deze op regelniveau wijzigen.    
8. Zoek en selecteer de gewenste record in de lijst.
9. Selecteer de reden
10. Voer in het detailveld een meer beschrijvende reden voor de bestelaanvraag in

## <a name="add-a-line-to-the-requisition"></a>Een regel toevoegen aan de bestelaanvraag
1. Klik op Regel toevoegen.
    * Er zijn twee manieren om regels aan de opdracht tot inkoop toe te voegen. Als u al het productnummer kent of al weet dat u een product aanvraagt dat niet in de productcatalogus staat, kunt u de regel direct toevoegen met 'Regel toevoegen'. De andere manier is 'Producten toevoegen' gebruiken, waarbij u kunt zoeken en filteren om artikelen in de productcatalogus te vinden.    
2. Klik op de rij die u zojuist hebt gemaakt.
    * De aanvrager is de werknemer die de bestelaanvraag heeft gedaan.   
    * Standaard is de persoon die de bestelaanvraag voorbereidt de werknemer die deze heeft aangevraagd. U moet gemachtigd worden om een bestelaanvraagregel voor te bereiden namens een andere werknemer. Als u dergelijke machtigingen hebt, worden de andere werknemers in deze zoekopdracht weergegeven.  
3. Typ een waarde in het veld Artikelnummer.
    * De artikelen die u kunt kiezen, worden beperkt door het categorietoegangsbeleid en de aanschaffingscatalogus voor de kopende rechtspersoon.   
4. Voer in het veld Hoeveelheid een getal in.

## <a name="add-more-products-to-the-requisition"></a>Meer producten toevoegen aan de bestelaanvraag
1. Klik op Producten toevoegen.
    * Dit is de optie waar u producten kunt zoeken in de productcatalogus.    
2. Typ in het veld Aanschaffingscategorieknooppunt zoeken het eerste gedeelte van de naam van de categorie die u zoekt, en klik vervolgens op Enter.
    * Typ bijvoorbeeld comput.  
3. Gebruik de InvokeDefaultButton-snelkoppeling.
4. Gebruik het filter om de lijst met producten in de geselecteerde categorie te filteren.
5. Selecteer de productkaart die u aan de bestelaanvraag wilt toevoegen.
6. Klik op Regels toevoegen.
7. Voer een getal in het veld Hoeveelheid in.
8. Typ in het veld Aanschaffingscategorieknooppunt zoeken het eerste gedeelte van de naam van de categorie die u zoekt, en klik vervolgens op Enter.
    * Typ bijvoorbeeld Mark (markeerstiften).  
9. Gebruik de InvokeDefaultButton-snelkoppeling.
10. Klik op Niet-vermeld product toevoegen aan regels om een product te voegen dat niet in de aanschaffingscatalogus staat.
11. Typ een waarde in het veld Productnaam.
12. Typ een waarde in het veld Eenheid.
13. Klik op OK.
14. Voer in het veld Artikelomschrijving een beschrijving van het product in.
15. Voer in het veld Hoeveelheid een getal in.
16. Voer in het veld Eenheidsprijs een getal in.
    * Als u de prijs weet voor een bepaalde leverancier (die u selecteert in het veld van de leveranciersrekening), kan die prijs worden ingevoerd   
17. Klik in het veld Leverancierrekening op de vervolgkeuzeknop om de zoekopdracht te openen.
    * Welke leveranciers in dit veld beschikbaar zijn, is afhankelijk van het inkoopbeleid en de status afdrukken die de leverancier heeft voor de huidige aanschaffingscategorie. Als alternatief voor het hier selecteren van een leverancier kunt u klikken op de knop Leveranciers voorstellen.    
18. Selecteer in de lijst de leverancier die u wilt gebruiken.
19. Typ een waarde in het veld Extern-artikelnummer.
    * Dit is een verwijzingsnummer voor het product dat bekend is bij de leverancier. Het kan bijvoorbeeld het artikelnummer van het product in de eigen catalogus van de leverancier zijn.  
20. Klik op OK.

## <a name="distribute-amounts"></a>Bedragen verdelen
1. Klik op Financiële items.
2. Klik op Bedragen verdelen.
    * Dit proces toont hoe de kosten voor de eerste regel tussen 2 rekeningen moeten worden gedistribueerd. Dit kan ook later worden gedaan wanneer de bestelaanvraag wordt gecontroleerd.  
3. Klik op Splitsen om een nieuwe distributieregel te maken.
4. Selecteer in het veld Grootboekrekening de eerste kostenplaats die een deel van de kosten moet betalen.
5. Selecteer de andere distributieregel.
6. Geef in het veld Grootboekrekening de andere kostenplaats op.
7. Klik op Evenredig verdelen.
8. Sluit de pagina.

## <a name="view-line-details"></a>Regeldetails weergeven
1. Schakel de uitbreiding van de sectie Regeldetails om.

## <a name="submit-the-requisition"></a>De bestelaanvraag indienen
1. Klik op Werkstroom om het dialoogvenster voor beëindiging te openen.
2. Klik op Aanbieden.
3. Sluit de pagina.
4. Typ in het veld Opmerking een opmerking voor de fiatteur van de bestelaanvraag.
5. Klik op Aanbieden.
6. Sluit de pagina.
7. Vernieuw de pagina.

