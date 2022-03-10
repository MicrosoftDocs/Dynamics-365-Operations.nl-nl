---
title: Een bestelaanvraag voor verbruik maken
description: In dit onderwerp wordt het proces van het maken van een bestelaanvraag beschreven.
author: Henrikan
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f7ca6e843688e0415f7ef31ed7cd40a77eccdeb
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/29/2021
ms.locfileid: "7579443"
---
# <a name="create-a-requisition-for-consumption"></a>Een bestelaanvraag voor verbruik maken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt het proces van het maken van een bestelaanvraag beschreven. Het toont u verschillende manieren om producten in uw aanschaffingscatalogus te zoeken en hoe u een product toevoegt dat niet in uw catalogus staat. Voordat u deze procedure start, moet u een inkoopbeleid instellen met Verbruik als standaardtype bestelaanvraag. U kunt deze procedure met het demobedrijf USMF uitvoeren of uw eigen gegevens gebruiken. De procedure kan alleen via een gebruikersprofiel worden uitgevoerd dat is ingesteld als werknemer. Deze taak moet doorgaans worden uitgevoerd door een werknemer. De werknemersrol **Werknemer** staat toe dat u de taken uitvoert. Als u USMF gebruikt, kunt u zich ook aanmelden als **Alicia**.


## <a name="create-a-new-requisition"></a>Een nieuwe bestelaanvraag maken
1. Ga naar **Navigatievenster > Modules > Inkoopbeheer > Opdrachten tot inkoop > Door mij voorbereide inkoopbestelopdrachten**.
2. Selecteer **Nieuw**.
3. Geef in het veld **Naam** een naam op voor de bestelaanvraag.
4. Voer in het veld **Gevraagde datum** een datum in. De aangevraagde datum en boekhoudingsdatums worden standaard gekopieerd naar de regels van de opdracht tot inkoop. Ze kunnen worden gewijzigd op regelniveau. De gevraagde datum is de gevraagde leveringsdatum.  
5. Voer in het veld **Boekhoudingsdatum** een datum in. De boekhoudingsdatum wordt gebruikt om de boeking in het grootboek te registeren en om te valideren dat de budgetfondsen beschikbaar zijn.  
6. Selecteer **OK**.
7. Selecteer in het veld **Reden** een optie in het vervolgkeuzemenu. De zakelijke reden die u selecteert, verschijnt standaard voor de regels van de opdracht tot inkoop, maar u kunt deze op regelniveau wijzigen.  
8. Selecteer de reden.
9. Voer in het veld **Details** een meer beschrijvende reden voor de bestelaanvraag in.

## <a name="add-a-line-to-the-requisition"></a>Een regel toevoegen aan de bestelaanvraag
1. Selecteer **Regel toevoegen**. Er zijn twee manieren om regels aan de opdracht tot inkoop toe te voegen. Als u al het productnummer kent of al weet dat u een product aanvraagt dat niet in de productcatalogus staat, kunt u de regel direct toevoegen met **Regel toevoegen**. De andere manier is **Producten toevoegen** gebruiken, waarbij u kunt zoeken en filteren om artikelen in de productcatalogus te vinden.    
2. Selecteer de rij die u zojuist hebt gemaakt.
    - De aanvrager is de werknemer die de bestelaanvraag heeft gedaan.   
    - Standaard is de persoon die de bestelaanvraag voorbereidt de werknemer die deze heeft aangevraagd. U moet gemachtigd worden om een bestelaanvraagregel voor te bereiden namens een andere werknemer. Als u dergelijke machtigingen hebt, worden de andere werknemers in deze zoekopdracht weergegeven.  
3. Typ een waarde in het veld **Artikelnummer**. De artikelen die u kunt kiezen, worden beperkt door het categorietoegangsbeleid en de aanschaffingscatalogus voor de kopende rechtspersoon.   
4. Voer een getal in het veld **Hoeveelheid** in.

## <a name="add-more-products-to-the-requisition"></a>Meer producten toevoegen aan de bestelaanvraag
1. Selecteer **Producten toevoegen**. Dit is de optie waar u producten kunt zoeken in de productcatalogus.    
2. Typ in het veld **Aanschaffingscategorieknooppunt** zoeken het eerste gedeelte van de naam van de categorie die u zoekt, en selecteer vervolgens **Enter**. Voer bijvoorbeeld `comput` in.  
3. Gebruik de snelkoppeling **InvokeDefaultButton**.
4. Gebruik **Filter** om de lijst met producten in de geselecteerde categorie te filteren.
5. Selecteer de productkaart die u aan de bestelaanvraag wilt toevoegen.
6. Selecteer **Toevoegen aan regels**.
7. Voer een getal in het veld **Hoeveelheid** in.
8. Typ in het veld **Aanschaffingscategorieknooppunt** zoeken het eerste gedeelte van de naam van de categorie die u zoekt, en selecteer vervolgens **Enter**. Voer bijvoorbeeld `High` (markeerstiften) in.  
9. Gebruik de snelkoppeling **InvokeDefaultButton**.
10. Selecteer **Niet-vermeld product toevoegen aan regels** om een product toe te voegen dat niet in de aanschaffingscatalogus staat.
11. Typ een waarde in het veld **Productnaam**.
12. Typ een waarde in het veld **Eenheid**.
13. Selecteer **OK**.
14. Voer in het veld **Artikelomschrijving** een beschrijving van het product in.
15. Voer een getal in het veld **Hoeveelheid** in.
16. Voer een nummer in het veld **Eenheidsprijs** in. Als u de prijs weet voor een bepaalde leverancier (die u selecteert in het veld van de leveranciersrekening), kan die prijs worden ingevoerd.   
17. Open in het veld **Leverancierrekening** de vervolgkeuzelijst om een optie te selecteren. Welke leveranciers in dit veld beschikbaar zijn, is afhankelijk van het inkoopbeleid en de status afdrukken die de leverancier heeft voor de huidige aanschaffingscategorie. Als alternatief voor het hier selecteren van een leverancier kunt u **Leveranciers voorstellen** selecteren.    
18. Selecteer in de lijst de leverancier die u wilt gebruiken.
19. Typ een waarde in het veld **Extern-artikelnummer**. Dit is een verwijzingsnummer voor het product dat bekend is bij de leverancier. Het kan bijvoorbeeld het artikelnummer van het product in de eigen catalogus van de leverancier zijn.  
20. Selecteer **OK**.

## <a name="distribute-amounts"></a>Bedragen verdelen
1. Selecteer **Financiële items**.
2. Selecteer **Bedragen verdelen**. Dit proces toont hoe de kosten voor de eerste regel tussen 2 rekeningen moeten worden gedistribueerd. Dit kan ook later worden gedaan wanneer de bestelaanvraag wordt gecontroleerd.  
3. Selecteer **Splitsen** om een nieuwe distributieregel te maken.
4. Selecteer in het veld **Grootboekrekening** de eerste kostenplaats die een deel van de kosten moet betalen.
5. Selecteer de andere distributieregel.
6. Geef in het veld Grootboekrekening de andere kostenplaats op.
7. Selecteer **Evenredig verdelen**.
8. Sluit de pagina.

## <a name="view-line-details"></a>Regeldetails weergeven
1. Schakel de uitbreiding van de sectie **Regeldetails** om.

## <a name="submit-the-requisition"></a>De bestelaanvraag indienen
1. Selecteer **Werkstroom** om het dialoogvenster voor beëindiging te openen.
2. Selecteer **Indienen**.
3. Sluit de pagina.
4. Typ in het veld **Opmerking** een opmerking voor de fiatteur van de bestelaanvraag.
5. Selecteer **Indienen**.
6. Sluit de pagina.
7. Vernieuw de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]