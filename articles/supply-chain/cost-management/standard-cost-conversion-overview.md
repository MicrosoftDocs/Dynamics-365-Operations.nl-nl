---
title: Standaardkostprijsconversie - Overzicht
description: Dit artikel geeft een procesoverzicht om u te helpen bij het instellen en uitvoeren van een standaardkostprijsconversie. De genoemde stappen zijn bedoeld om te worden voltooid nadat u de vereisten voor een standaardkostprijsconversie hebt voltooid.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 78212
ms.assetid: d601d9d5-1de3-4868-aff4-534dca01d624
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 236743277a95b8a1170ca05f93106575ea1cc8e4
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187597"
---
# <a name="standard-cost-conversion-overview"></a>Standaardkostprijsconversie - Overzicht

[!include [banner](../includes/banner.md)]

Dit artikel geeft een procesoverzicht om u te helpen bij het instellen en uitvoeren van een standaardkostprijsconversie. De genoemde stappen zijn bedoeld om te worden voltooid nadat u de vereisten voor een standaardkostprijsconversie hebt voltooid. 

Gebruik de pagina **Standaardkostprijsconversies** om het voorraadmodel voor een batch geselecteerde artikelen te veranderen van een werkelijke kostprijsberekening in een standaardkostprijsberekening. Voor het conversieproces moet u eerst een verplichte voorraadafsluiting uitvoeren, dan verschillende stappen uitvoeren gedurende een overgangsperiode (die wordt gedefinieerd door een begindatum voor de overgang en een geplande conversiedatum) en vervolgens de conversie en een bijbehorende voorraadafsluiting uitvoeren.

-   Voorraadafsluiting voorafgaande aan de overgangsperiode: de voorraadafsluiting is een verplichte stap, omdat hiermee de openstaande transacties van een artikel worden vereffend met de oude waarderingsmethode. Tijdens de overgangsperiode kunt u geantedateerde transacties, zoals facturen, invoeren en boeken, zodat u de vorige periode kunt afsluiten. De datum van de voorraadafsluiting moet één dag vóór de begindatum van de overgangsperiode vallen om ervoor te zorgen dat er een duidelijke scheiding ontstaat tussen de oude en de nieuwe voorraadwaarderingsmethode.
-   Conversiestappen tijdens de overgangsperiode: gebruik de pagina **Standaardkostprijsconversies** om een conversierecord te maken die ook een door de gebruiker gedefinieerde ID voor een nieuwe kostprijsberekeningsversie bevat. U brengt in kaart welke artikelen moeten worden geconverteerd en u voert vervolgens de onverwerkte standaardkosten in de nieuwe kostprijsberekeningsversie in. U controleert de geselecteerde artikelen en u gaat na of er sprake is van problemen die de conversie zouden kunnen belemmeren, daarna lost u de gevonden problemen op en voert u opnieuw een controle uit. Nadat de artikelen zijn gecontroleerd en eventuele problemen zijn opgelost, wijzigt u de status van de conversierecord in **Gereed**. Voer de conversie uit op de geplande conversiedatum en voer desgewenst een voorraadafsluiting uit. De voorraadmutaties van een artikel tijdens de overgangsperiode worden geboekt en gewaardeerd op basis van het oude voorraadmodel. Nadat de conversie met succes is uitgevoerd worden de voorraadmutaties vervolgens geherwaardeerd naar de standaardkostprijs.
-   Voorraadafsluiting vóór de conversie: de voorraadafsluiting kan worden uitgevoerd als onderdeel van de conversie op de geplande conversiedatum of als afzonderlijke stap voorafgaande aan de conversie.

Nadat het conversieproces is voltooid, is het voorraadmodel van elk artikel gebaseerd op de standaardkostprijs en is de standaardkostprijs van het artikel ingeschakeld. Volgende voorraadtransacties worden gewaardeerd op basis van de standaardkostprijs van het artikel. Daarnaast worden de fysieke voorraadtransacties van het artikel voor ontvangsten en uitgiften geconverteerd naar de standaardkostprijs op basis van de conversiedatum. De financiële voorhanden voorraad van het artikel wordt ook geconverteerd naar de standaardkostprijs en het waardeverschil wordt geboekt als voorraadherwaardering. Transacties die worden uitgevoerd na de conversie, worden gewaardeerd op basis van de standaardkostprijs van het artikel. U kunt geantedateerde transacties niet invoeren vóór de conversiedatum, omdat een voorraadafsluiting moet worden uitgevoerd één dag voor de conversiedatum. U kunt alleen een conversie uitvoeren als één dag eerder een voorraadafsluiting is uitgevoerd. Deze voorraadafsluiting kan niet worden geannuleerd.

## <a name="1-define-a-standard-cost-conversion-record-and-the-associated-costing-version"></a>1. Definieer een standaardkostprijsconversierecord en de bijbehorende kostprijsberekeningsversie.
Gebruik de pagina **Standaardkostprijsconversies** om een conversierecord te maken. U kunt alleen een nieuwe conversierecord maken als de bestaande conversierecords zijn voltooid. De duur van de geplande overgangsperiode wordt gedefinieerd door de begindatum van de overgang en de geplande conversiedatum. De geplande overgangsperiode hoeft bijvoorbeeld maar één dag te duren. Een geplande overgangsperiode helpt ervoor te zorgen dat het conversieproces voldoende tijd heeft om alle stappen te voltooien. De voorraadafsluiting moet één dag vóór de begindatum van de overgang worden uitgevoerd, zodat vereffeningen zijn voltooid voordat het conversieproces wordt gestart. Om ervoor te zorgen dat de begindatum van de overgang en de datum van de voorraadafsluiting goed op elkaar afgestemd zijn, kunt u ofwel de begindatum van de overgang wijzigen in één dag na een bestaande voorraadafsluiting of een voorraadafsluiting uitvoeren. Wanneer u een conversierecord invoert, voert u ook een door de gebruiker gedefinieerde ID in voor een nieuwe kostprijsberekeningsversie die de standaardkostprijzen van de geconverteerde artikelen bevat. Als u de conversierecord opslaat, wordt de kostprijsberekeningsversie automatisch gemaakt.

## <a name="2-review-and-change-the-new-costing-version-for-the-conversion-record"></a>2. De nieuwe kostprijsberekeningsversie voor de conversierecord controleren en wijzigen
De nieuwe kostprijsberekeningsversie is gekoppeld aan de conversierecord, zoals wordt aangegeven met het kostprijsberekeningstype **Conversie**. De specifieke kostprijsberekeningsversie is vergelijkbaar met een kostprijsberekeningsversie voor standaardkostprijzen en bevat de artikelkostprijsrecords voor artikelen die zijn gekoppeld aan de conversierecord. De specifieke kostprijsberekeningsversie voor een conversierecord heeft de volgende instellingen, die u zou moeten controleren en bewerken op de diverse tabbladen, indien nodig:

-   **Kostprijsberekeningstype:** Dit veld moet worden ingesteld op **Standaardkosten**.
-   **Versie** Met de ID wordt de informatie weergegeven die is ingevoerd in de conversierecord voor de kostprijsberekeningsversie-ID.
-   **Naam:** de naam is standaard leeg. U kunt desgewenst een naam invoeren.
-   **Blokkeren:** Dit veld moet worden ingesteld op **Nee**. U kunt kostenrecords invoeren in de kostprijsberekeningsversie totdat u de status van de conversierecord wijzigt in **Gereed**. De status **Gereed** betekent dat de geselecteerde artikelen zijn gecontroleerd, en dat wijzigingen in kostenrecords niet zijn toegestaan.
-   **Activering van blokkering:** Dit veld moet worden ingesteld op **Ja**. U kunt een kostprijsrecord in behandeling niet handmatig activeren in de specifieke kostprijsberekeningsversie. De activering vindt plaats wanneer u de conversie uitvoert.
-   **Begindatum:** de begindatum geeft de geplande conversiedatum aan die is ingevoerd in de conversierecord.
-   **Site:** Laat dit veld leeg zodat kostenrecords voor alle sites kunnen worden ingevoerd.
-   **Veldgroep Prijstype toestaan:** Stel dit veld in op **Ja**, zodat alleen kostprijsrecords kunnen worden ingevoerd.
-   **Terugvalprincipe:** Dit veld is ingesteld op **Geen**. Stel het terugvalprincipe in op **Actief** als u kostprijsinformatie nodig hebt die is geactiveerd in andere kostprijsberekeningsversies. De kostprijsinformatie over bijvoorbeeld onderdelen, kostencategorieën en indirecte kosten is mogelijk nodig om de kostprijs van gefabriceerde artikelen te berekenen.
-   **Terugvalversie van kostprijsberekening:** Laat dit veld leeg.

Artikelkostprijsgegevens in de specifieke kostprijsberekeningsversie kunnen alleen worden beheerd op de pagina **Standaardkostprijsconversies**. U kunt de pagina **Instellingen kostprijsberekeningsversie** of de pagina **Onderhoud kostprijsberekeningsversie** niet gebruiken om tijdens de conversie kosten voor de kostprijsberekeningsversie te berekenen. U kunt deze pagina's wel gebruiken om de specifieke kostprijsberekeningsversie te beheren wanneer u de conversie hebt uitgevoerd.

## <a name="3-identify-the-items-to-convert-to-standard-cost"></a>3. De artikelen aangeven die moeten worden geconverteerd naar standaardkostprijzen
Gebruik de pagina **Standaardkostprijsconversies** om de afzonderlijke artikelen aan te geven die naar standaardkosten moeten worden geconverteerd. U kunt meerdere artikelen toevoegen via de pagina **Artikelen aan standaardkostprijsconversie toevoegen**. Over het algemeen moet u alle gefabriceerde artikelen opnemen in één conversierecord, zodat de kosten juist worden berekend.

## <a name="4-enter-or-calculate-the-pending-standard-cost-for-each-item-that-is-being-converted"></a>4. De standaardkostprijs in behandeling invoeren of berekenen voor elk artikel dat wordt geconverteerd
Geef in de pagina **Artikelprijs** de standaardkosten in behandeling op in de specifieke kostprijsberekeningsversie voor ingekochte artikelen en transferartikelen. Kostprijsrecords zijn specifiek voor de locatie en u moet de kostprijs in behandeling van een artikel voor elke locatie invoeren. Via de pagina **Artikelprijs** kunt u de standaarden in behandeling voor gefabriceerde artikelen berekenen. U moet de kosten in behandeling voor een gefabriceerd artikel berekenen voor elke productielocatie, tenzij de locatie een transferlocatie is. In dit geval moeten de kosten in behandeling handmatig worden ingevoerd. Sommige artikelen hebben mogelijk productdimensies voor kleur, grootte of configuratie. Op de pagina **Standaardkostprijsconversies** laat het selectievakje **Kostprijs per variant gebruiken** de standaardkosten voor elke combinatie van productdimensies zien. Als dit selectievakje is uitgeschakeld, hoeft u alleen de kostprijs in behandeling voor het artikel in te voeren.

## <a name="5-check-and-resolve-any-issues-for-the-items-that-are-being-converted"></a>5. De artikelen die worden geconverteerd op fouten controleren en de fouten corrigeren
Gebruik het rapport **Controles van standaardkostprijsconversies** om problemen voor de artikelen die worden geconverteerd te identificeren. Als een artikel geen fouten bevat, wordt de status in de conversierecord gewijzigd in **Gecontroleerd**. Als een artikel fouten bevat, moet u deze corrigeren en het rapport opnieuw uitvoeren totdat de status wordt gewijzigd in **Gecontroleerd**. Als u de fouten voor een artikel niet tijdig kunt oplossen, kunt u het artikel desgewenst uit de conversierecord verwijderen en het artikel later converteren.

## <a name="6-change-the-status-of-the-conversion-record-to-ready"></a>6. Wijzig de status van de conversierecord in Gereed.
Als u de status van de conversierecord wijzigt in **Gereed**, wordt een laatste controle uitgevoerd voordat een standaardkostprijsconversie wordt uitgevoerd. De status wordt alleen gewijzigd in **Gereed** als aan de volgende voorwaarden is voldaan:

-   Elk artikel in de conversierecord heeft de status **Gecontroleerd**.
-   De voorraadafsluiting moet één dag eerder zijn uitgevoerd dan de begindatum van de overgang. Om ervoor te zorgen dat de begindatum van de overgang en de datum van de voorraadafsluiting goed op elkaar afgestemd zijn, kunt u ofwel de begindatum van de overgang wijzigen in één dag na een bestaande voorraadafsluiting of een voorraadafsluiting uitvoeren.

## <a name="7-back-up-the-database-before-conversion"></a>7. Een back-up maken vóór conversie
Met de back-up kunt u de database terugzetten als er fouten zijn opgetreden tijdens de conversie.

## <a name="8-perform-the-conversion-when-the-conversion-record-has-a-ready-status"></a>8. Voer de conversie uit als de conversierecord de status Gereed heeft.
Voor de conversie moet u een voorraadafsluiting uitvoeren op een datum die één dag vóór de geplande conversiedatum valt. Met deze stap zorgt u ervoor dat er geen achterstallige transacties kunnen worden ingevoerd tijdens de overgangsperiode. Als u nog geen voorraadafsluiting hebt uitgevoerd, wordt u gevraagd of u dat wilt doen als onderdeel van de conversie. Het conversieproces behandelt één artikel tegelijk. Het start met de laagste artikelen in een productstructuur, op basis van de artikelcode op laag niveau. Wanneer een artikel met succes is geconverteerd, wordt de status in de conversierecord gewijzigd in **Geconverteerd**. Als de conversie wordt onderbroken, is de status van de artikelen die nog niet zijn geconverteerd nog steeds **Gecontroleerd**. Wanneer de conversie is voltooid, heeft dit de volgende consequenties:

-   De status van de conversierecord wordt gewijzigd van **Gereed** in **Voltooid** en de status van elk geselecteerd artikel wordt gewijzigd van **Gecontroleerd** in **Geconverteerd**.
-   De artikelmodelgroep voor geconverteerde artikelen wordt gewijzigd, zodat hiermee een nieuwe groep met een standaardkostprijsvoorraadmodel wordt aangegeven.
-   De standaardkostprijs voor de geconverteerde artikelen is ingeschakeld in de specifieke kostprijsberekeningsversie.
-   Het kostprijsberekeningstype van de kostprijsberekeningsversie wordt gewijzigd van **Conversie** in **Standaardkostprijs** en de kostprijsberekeningsversie werkt nu net als andere kostprijsberekeningsversies voor standaardkostprijzen.

## <a name="9-validate-and-reconcile-the-inventory-values-for-the-converted-items"></a>9. De voorraadwaarden voor de geconverteerde artikelen valideren en afstemmen
Met het rapport **Afschrift van variantieanalyse** kunt u herwaarderingsafwijking analyseren en het rapport **Voorraadwaarde** laat u de voorraadwaarde op een specifieke datum zien.

-   Analyseer de herwaarderingsafwijkingen. Met het rapport **Afschrift van variantieanalyse** kunt u afwijkingen in de voorraadherwaardering weergeven voor de geconverteerde artikelen. Met de pagina **Standaardkostentransacties** kunt u ook de voorraadherwaarderingstransacties weergeven voor de geconverteerde artikelen met voorraad.
-   Analyseer de voorraadwaarde vóór de begindatum van de overgang. Met het rapport **Voorraadwaarde** kunt u voorraadwaarden weergeven voor de geconverteerde artikelen. Gebruik voor de einddatum voor het rapport de datum die één dag voor de begindatum van de overgang ligt.
-   Analyseer de voorraadwaarde vóór de conversiedatum. Met het rapport **Voorraadwaarde** kunt u voorraadwaarden weergeven voor de geconverteerde artikelen. Gebruik voor de einddatum voor het rapport de datum die één dag voor de conversiedatum ligt.
-   Analyseer de voorraadwaarde op de conversiedatum. Met het rapport **Voorraadwaarde** kunt u de voorraadwaarden weergeven vanaf de conversiedatum. De begin- en einddatums voor het rapport moeten beide overeenkomen met de conversiedatum. De selectiecriteria voor het rapport moeten zijn ingesteld op de geconverteerde artikelen.
-   Analyseer achterstallige voorraadmutaties. Met het rapport **Voorraadwaarde** kunt u achterstallige voorraadmutaties weergeven die na de conversie zijn ingevoerd. De begin- en einddatums voor het rapport moeten overeenkomen met de begindatum van de overgang en de conversiedatum, minus één dag. De selectiecriteria voor het rapport moeten zijn ingesteld op de geconverteerde artikelen. In het rapport worden de voorraadmutaties weergegeven die zijn ingevoerd met de standaardkostprijs tijdens de overgangsperiode.


## <a name="additional-resources"></a>Aanvullende resources

[Vereisten voor een standaardkostprijsconversie](prerequisites-standard-cost-conversion.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]