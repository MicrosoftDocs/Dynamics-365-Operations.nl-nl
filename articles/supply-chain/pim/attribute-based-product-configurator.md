---
title: Op kenmerken gebaseerde verkoopprijzen voor op beperkingen gebaseerde productconfiguratie
description: In dit onderwerp wordt beschreven hoe u verkoopprijsmodellen kunt maken met verkoopprijzen op basis van onderdelen en kenmerken in plaats van op basis van de fysieke stuklijst en de route.
author: sorenva
manager: tfehr
ms.date: 10/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2020-08-17
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: c0f9c1bb94b4dcc3c3c1e7656868ef6e6bd903db
ms.sourcegitcommit: 9ca63cbc6bc6d6baed9d45bce30d0b32e156301c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/12/2020
ms.locfileid: "3988317"
---
# <a name="attribute-based-sales-prices-for-constraint-based-product-configuration"></a>Op kenmerken gebaseerde verkoopprijzen voor op beperkingen gebaseerde productconfiguratie

In dit onderwerp wordt beschreven hoe u verkoopprijsmodellen kunt maken met verkoopprijzen op basis van onderdelen en kenmerken in plaats van op basis van de fysieke stuklijst en de route. U kunt diverse verkoopprijsmodellen maken voor elk productconfiguratiemodel.

## <a name="set-relevant-product-information-management-parameters"></a>Relevante parameters voor productgegevensbeheer instellen

Voordat u begint met het maken van uw prijsmodellen, moet u een standaardvaluta definiëren die wordt gebruikt wanneer u uw verkoopprijsmodellen maakt. U kunt ook aangeven of u een Microsoft Excel-bestand met een prijsspecificatie wilt bijvoegen voor alle order- of offerteregels. Met de prijsspecificatie kunt u details delen met klanten over de manier waarop u tot een bepaalde verkoopprijs voor een geconfigureerd product bent gekomen.

U kunt uw standaardvaluta als volgt instellen:

1. Ga naar **Productgegevensbeheer \> Instellen \> Parameters productgegevensbeheer**.
1. Open het tabblad **Op beperkingen gebaseerde productconfiguratiemodellen**.
1. Open de vervolgkeuzelijst **Standaardvaluta** en selecteer uw valuta.

    ![De standaardvaluta instellen voor op beperkingen gebaseerde productconfiguratie](media/prod-config-currency.png "De standaardvaluta instellen voor op beperkingen gebaseerde productconfiguratie")

1. Als u een Excel-bestand aan een prijsspecificatie voor alle order- of offerteregels wilt koppelen, stelt u in de sectie **Prijsmodel** **Koppelen** in op *Ja*.

## <a name="build-your-sales-price-models"></a><a name="build-price-model"></a>Uw verkoopprijsmodellen maken

U maak een verkoopprijsmodel als volgt:

1. Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.
1. Selecteer het beoogde productconfiguratiemodel.
1. Open in het actievenster het tabblad **Model** en selecteer in de groep **Instellen** **Prijsmodellen**.
1. De pagina **Prijsmodellen** wordt geopend.
1. Selecteer een prijsmodel of voeg een nieuw prijsmodel aan het raster toe.
1. Selecteer **Bewerken** om de bewerkingspagina voor uw geselecteerde model te openen. Dit biedt de volgende functies:
    - In de koptekst van het formulier wordt de standaardvaluta weergegeven en kunt u nieuwe valuta's voor uw prijsinstellingen toevoegen.
    - In het linkerdeelvenster worden alle onderdelen en gebruikersvereisten van het productmodel weergegeven. Elk knooppunt in de productmodelstructuur kan één basisprijsexpressie en een optioneel aantal expressieregels hebben. Een expressieregel bestaat uit een voorwaarde en een expressie en elke expressieregel omvat een productoptie waarmee de prijs van het product kan worden bepaald.
    - Wanneer u uw voorwaarden en expressies opstelt, kunt u dezelfde operators gebruiken als voor berekeningen in een productmodel. De expressie-editor ondersteunt ook zowel voorwaarden als expressies.
1. Selecteer een knooppunt in de linkerkolom en gebruik vervolgens de functies die in de vorige stap worden beschreven om er prijsregels voor in te stellen (zie ook het voorbeeld na deze procedure). Herhaal deze stap desgewenst voor elk knooppunt.

In het volgende voorbeeld wordt een basisprijs weergegeven van een statisch aantal van 899,95 EUR, dat kan worden gewijzigd door een of meer van de volgende vijf expressieregels, afhankelijk van de configuratie die door de klant is geselecteerd:

- Trek voor een witte afwerking 59,95 EUR af.
- Tel 35,95 EUR bij voor hoekbescherming.
- Tel 89,95 EUR bij voor een metalen voorgrill.
- Voor een afwerking met rozenhout telt u 119,95 EUR bij.
- Tel 12,95 EUR bij voor elke eenheid van de luidsprekerhoogte.

![Voorbeeldprijsmodel](media/prod-config-rules-example.png "Voorbeeldprijsmodel")

## <a name="add-support-for-multiple-currencies"></a>Ondersteuning voor meerdere valuta's toevoegen

Wanneer een configureerbaar product wordt verkocht, controleert het systeem of de prijzen expliciet zijn ingesteld in de valuta van de klant. Als dat het geval is, worden de expliciete waarden gebruikt. Zo niet, dan gebruikt het systeem de wisselkoersen die zijn ingesteld voor het verkoopbedrijf om de standaardvalutawaarde om te zetten in de valuta van de klant.

U voegt expliciete prijzen als volgt in een extra valuta toe:

1. Open de bewerkingspagina voor uw prijsmodel, zoals wordt beschreven in [Uw verkoopprijsmodellen maken](#build-price-model).
1. Selecteer de knop **Toevoegen** in de koptekst van het prijsmodel om het dialoogvenster **Valuta's** te openen , waarin de beschikbare valuta's worden weergegeven.
1. Selecteer de valuta die u wilt toevoegen in het vervolgdialoogvenster **Valuta´s** en selecteer vervolgens **OK**.
1. De vervolgkeuzelijst **Huidige valuta** bevat nu de valuta die u zojuist hebt toegevoegd, plus eventuele andere valuta's die mogelijk eerder zijn toegevoegd. Selecteer uw nieuwe valuta en u ziet dat het raster in de sectie **Expressieregels** nu twee expressievelden bevat:
    - **Expressie**: geeft de expressie (of constante waarde) weer waarmee de prijs wordt gezocht met de valuta die momenteel is geselecteerd voor **Huidige valuta**.
    - **Standaardexpressies**: geeft de expressie (of constante waarde) weer waarmee de prijs wordt gezocht met de standaardvaluta die momenteel is geselecteerd voor **Huidige valuta**.

    > [!NOTE]
    > Het veld **Voorwaarde** voor de expressieregels is "eigendom" van de standaardvaluta. Dit betekent dat u de voorwaarde voor andere valuta's niet kunt wijzigen. U kunt ook geen nieuwe expressieregels toevoegen terwijl een andere valuta dan de standaardvaluta is geselecteerd als de **Huidige valuta**.
1. Bewerk indien nodig waarden in de kolom **Expressie** voor de huidige valuta.

In het volgende voorbeeld is _EUR_ de standaardvaluta en is _USD_ toegevoegd als extra valuta.

![Voorbeeld van een model met meerdere valuta's](media/prod-config-rules-currency-example.png "Voorbeeld van een model met meerdere valuta's")

> [!NOTE]
> U kunt geen expressieregels toevoegen die uniek zijn voor een niet-standaardvaluta. Als u expressieregels wilt maken die alleen relevant zijn voor een andere valuta dan de standaardvaluta, stelt u de prijsexpressie voor de standaardvaluta in op nul. Stel vervolgens de toepasselijke expressie in voor de niet-standaardvaluta.

## <a name="test-your-price-model"></a>Uw prijsmodel testen

Om te testen hoe de verkoopprijzen in een configuratiesessie werken, opent u de bewerkingspagina voor uw prijsmodel, zoals wordt beschreven in [Uw verkoopprijsmodellen maken](#build-price-model) en selecteert u vervolgens **Testen** in het actievenster. Het dialoogvenster **Productmodel testen** wordt geopend. In dit venster kunt u het volgende doen:

- Gebruik de configuratie-instellingen die hier worden aangeboden om productopties te selecteren en bekijk vervolgens hoe deze van invloed zijn op de waarde die voor **Prijs en verzenddatum** wordt weergegeven.
- Selecteer **Prijsspecificatie weergeven** om een Excel-document te downloaden waarin alle details worden weergegeven over de manier waarop de prijs is berekend.

![Uw productmodel testen](media/prod-config-test.png "Uw productmodel testen")

De gedownloade spreadsheet bevat zowel de absolute waarde als de bijdrage als een percentage voor elk actief prijselement. Als u de prijsmodeloptie **Koppelen** hebt ingesteld op de pagina **Parameters voor productgegevensbeheer**, wordt dit Excel-blad gekoppeld aan de order- of offerteregel.

![Excel-spreadsheet met prijsspecificatie](media/prod-config-excel-example.png "Excel-spreadsheet met prijsspecificatie")

## <a name="set-up-selection-criteria-for-price-models"></a>Selectiecriteria instellen voor prijsmodellen

Wanneer uw prijsmodellen zijn ingevoerd, moet u ten minste één selectiecriterium instellen om het prijsmodel op te halen wanneer u de offerte of order configureert. U doet dit door een of meer query's in te stellen. In een combinatie met overeenkomende verkoopprijsmodellen bieden de query's grote flexibiliteit bij het instellen van verkoopprijzen voor bepaalde klanten, regio's, perioden en andere criteria.

U stelt als volgt selectiecriteria voor prijsmodellen in:

1. Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.
1. Selecteer het beoogde productconfiguratiemodel.
1. Open in het actievenster het tabblad **Model** en selecteer in de groep **Instellen** **Prijsmodelcriteria**. De pagina **Prijsmodelcriteria** wordt geopend.
1. Als de queryrij die u nodig hebt nog niet bestaat, selecteert u **Nieuw** in het actievenster om een nieuwe rij toe te voegen aan het raster en voert u de volgende instellingen ervoor in:
    - **Naam**: voer een naam voor deze rij in.
    - **Beschrijving**: geef een korte omschrijving van de query en waarvoor deze is bedoeld.
    - **Prijsmodel**: selecteer een [prijsmodel](#build-price-model) (in het huidige configuratiemodel) waarop de query van toepassing is wanneer deze wordt geactiveerd.
    - **Ordertype**: selecteer het type order waarop de query van toepassing is.
    - **Geldig vanaf**: geef de eerste dag op waarop de query van toepassing is.
    - **Verloopt op**: geef de laatste datum op waarop de query van toepassing is.

    ![Criteria voor prijsmodel](media/prod-config-price-model-criteria.png "Criteria voor prijsmodel")

1. Selecteer de rij voor de query die u wilt definiëren en selecteer vervolgens **Bewerken** in het **Actievenster**. Het dialoogvenster van de queryontwerper wordt geopend. Deze werkt net als de meeste queryontwerpers in Supply Chain Management. Gebruik deze methode om de voorwaarden te definiëren op basis waarvan het prijsmodel voor de door u geselecteerde rij moet worden toegepast.

1. Herhaal stap 4-5 voor elke query die u nodig hebt.
    > [!TIP]
    > U kunt tijd besparen door een bestaande rij te kopiëren die er al ongeveer hetzelfde uitziet als een nieuwe rij die u moet toevoegen. Selecteer hiervoor een doelrij en selecteer **Dupliceren** in het actievenster.

1. Wanneer u klaar bent met het instellen van uw criteria, rangschikt u deze in de juiste volgorde in de lijst **Prijsmodelcriteria**. Als u de positie van een rij wilt wijzigen, selecteert u de rij en selecteert u vervolgens **Omhoog** of **Omlaag** in het actievenster.

    > [!IMPORTANT]
    > Tijdens de configuratie wordt gezocht vanaf de bovenkant van de lijst en wordt de eerste query gebruikt die overeenkomt met de gegevens op de offerte- of orderregel. Daarom moet u de meest specifieke query's bovenaan plaatsen. Als u een algemene query boven aan de lijst plaatst, is dit de query die wordt gebruikt, zelfs als er mogelijk een query verder omlaag in de lijst beschikbaar is die bestemd is voor de exacte klant of potentiële klant van de configuratie.

## <a name="set-attribute-based-sales-prices-for-the-product-model-version"></a>Op kenmerken gebaseerde verkoopprijzen instellen voor de productmodelversie

De laatste stap bestaat eruit op kenmerken gebaseerde verkoopprijzen voor de productmodelversie op te geven. Hiervoor gaat u als volgt te werk:

1. Ga naar **Productgegevensbeheer \> Producten \> Productconfiguratiemodellen**.
1. Selecteer het beoogde productconfiguratiemodel.
1. Open in het actievenster het tabblad **Model** en selecteer in de groep **Details productmodel** **Versies**.
1. De pagina **Versies** wordt geopend. Controleer of de **Methode voor prijscalculatie** in ingesteld op **Op kenmerken gebaseerd**.
    ![De methode voor prijscalculatie instellen op Op kenmerken gebaseerd](media/prod-config-versions.png "De methode voor prijscalculatie instellen op Op kenmerken gebaseerd")
