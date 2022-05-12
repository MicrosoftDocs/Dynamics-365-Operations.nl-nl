---
title: Instelling van parameterwaarden voor kostprijsberekening
description: Wanneer u de module Francoprijzen instelt, kunt u verschillende sets algemene waarden definiëren die beschikbaar zijn wanneer u specifieke typen parameterwaarden voor kostprijsberekening selecteert in andere delen van de app. In dit onderwerp wordt uitgelegd hoe u deze waardensets instelt.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostTypeTable, ITMCostTypeGroup, ITMCostTransferGroup, ITMCostTemplateTable, ITMVolumetricDivisorTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 335bed49b05bf64547d7ded885f365a30487484f
ms.sourcegitcommit: d715e44b92b84b1703f5915d15d403ccf17c6606
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/27/2022
ms.locfileid: "8644633"
---
# <a name="costing-parameter-values-setup"></a>Instelling van parameterwaarden voor kostprijsberekening

[!include [banner](../../includes/banner.md)]

Wanneer u de module **Francoprijzen** instelt, kunt u verschillende sets algemene waarden en gerelateerde instellingen per waarde definiëren. Deze waarden zijn dan beschikbaar wanneer u specifieke typen parameterwaarden voor kostprijsberekening selecteert in andere delen van de app. In dit onderwerp wordt uitgelegd hoe u deze waardensets instelt.

## <a name="set-up-cost-type-codes"></a>Codes voor kostentypen instellen

Kostentypecodes bepalen welk type kosten wordt gemaakt wanneer de goederen in het magazijn worden aangevoerd, of de francoprijzen van het traject. Hoewel ze meestal de waarde van de goederen verhogen, kunnen ze ook worden gebruikt om bedragen in het grootboek op te bouwen. Grootboekcorrecties worden gebruikt wanneer kosten in de loop van de tijd of tijdens een reeks trajecten worden toegerekend en in één transactie worden verrekend.

> [!NOTE]
> Als de tabel met het kostentype wordt gedeeld tussen rechtspersonen, moet het rekeningschema ook worden gedeeld tussen rechtspersonen. Anders werken de boekingstransacties niet correct.

Als u uw kostentypecodes wilt instellen, gaat u naar **Francoprijzen \> Kostprijsberekening instellen \> Kostentypecodes**. U kunt de knoppen in het actiedeelvenster gebruiken om nieuwe kostentypecodes te maken, bestaande codes te bewerken of een geselecteerd kostentype te verwijderen.

In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke kostentypecode.

| Veld | Beschrijving |
|---|---|
| Code voor kostentype | Voer een naam voor de kostentypecode in. |
| Beschrijving | Voer een omschrijving van de kostentypecode in. |
| Verzendtarief gebruiken | Stel deze optie in op *Ja* als de wisselkoers voor het traject (ook wel een managementkoers genoemd) moet worden gebruikt om de waarde van deze kosten te berekenen. In dit geval wordt het verzendtarief gebruikt in plaats van de standaard- of spotwisselkoers om facturen in vreemde valuta's om te wisselen. |
| Aangiftecategorie | In dit veld wordt een rapportagecategorie voor het kostentype vastgesteld. Rapporten kunnen worden afgedrukt op rapportagecategorieën of op kostentype. |
| Debettype | Selecteer of het kostentype het artikel, de grootboekrekening of de leverancier moet debiteren. |
| Debetboeking | Als het veld **Debettype** is ingesteld op *Grootboekrekening*, selecteert u de omschrijving van de boeking. |
| Debetrekening | Als het veld **Debettype** is ingesteld op *Grootboekrekening*, selecteert u welke grootboekrekening moet worden gebruikt. |
| Credittype | Selecteer of dit kostentype het artikel, de grootboekrekening of de leverancier moet crediteren. |
| Creditboeking | Als het veld **Credittype** is ingesteld op *Grootboekrekening*, selecteert u de omschrijving van de boeking. |
| Creditrekening | Als het veld **Credittype** is ingesteld op *Grootboekrekening*, selecteert u welke grootboekrekening moet worden gebruikt. |
| Vereffeningsrekening | Selecteer de vereffeningsrekening voor het kostentype. Het is raadzaam een afzonderlijke vereffeningsrekening op te geven per kostentype om te helpen bij de afstemming. |
| Boekingstype standaardkosten | Als u standaardkostprijsberekening gebruikt, selecteert u de omschrijving van de boeking. |
| Standaardrekening voor kostenafwijkingen | <p>Als u standaardkostprijsberekening gebruikt, wordt de rekening die hier is opgegeven, gebruikt om eventuele verschillen te boeken. Deze rekening gebruikt de francoprijzenuitsplitsing op de pagina **Artikelprijzen**. Deze uitsplitsing wordt gemaakt door de periodieke routine te gebruiken om prijzen bij te werken.</p><p>De standaardkosten van een artikel zijn bijvoorbeeld $ 15,00, de FOB is $ 13,00 en de vrachtkosten zijn $ 2,00. Wanneer de factuur voor de voorraad wordt ontvangen, wordt het artikel op $ 15,00 ontvangen, maar is er een standaardprijsafwijking van $ 2,00 voor het artikel, omdat de werkelijke FOB $ 13,00 is. Deze afwijking wordt geboekt naar de standaardprijsafwijkingsrekening die is ingesteld in het artikelboekingsprofiel. Aangezien de geschatte vrachtkosten $ 2,00 zijn, is er geen afwijking wanneer de voorraadfactuur wordt geboekt. Wanneer de factuur voor vrachtkosten echter wordt ontvangen, worden de vrachtkosten $ 2,50 per eenheid. Daarom wordt $ 0,50 verschil geboekt naar de opgegeven kosten. |
| Verschillenrekening voor zwevend gemiddelde | <p>Als u kostprijsberekening met zwevend gemiddelde gebruikt, wordt de rekening die hier is opgegeven, gebruikt om eventuele verschillen te boeken.</p><p>De geschatte vrachtkosten zijn $ 2,00. Wanneer de factuur voor vrachtkosten echter wordt ontvangen, worden de vrachtkosten $ 2,50 per eenheid. Daarom moet $ 0,50 afwijking worden geboekt.</p><p>Wanneer de optie **Correcties als afwijking boeken** op *Ja* is ingesteld op de pagina **Parameters francoprijzen**, worden alle afwijkingen tussen de geschatte en werkelijke verzendkosten geboekt naar de rekening voor de gemiddelde afwijking die hier is opgegeven. Wanneer de optie **Correcties als afwijking boeken** wordt ingesteld op *Nee*, wordt de standaardfunctionaliteit gebruikt en wordt de afwijking toegepast op de voorraad of op de rekening voor de gemiddelde afwijking die hier wordt opgegeven, afhankelijk van de aanwezige voorraad.</p> |
| Toenamerekening voor toeslagen | Selecteer de rekening die wordt gebruikt om kostenramingen samen te voegen wanneer de inkoopfactuur wordt geboekt. Dit veld wordt alleen gebruikt als de optie **Toenamerekening voor kostentypetoeslag gebruiken** is ingesteld op *Ja* op het sneltabblad **Kostprijsberekening** op het tabblad **Algemeen** van de pagina **Parameters voor francoprijzen**. |
| Toeslagenrekening | Selecteer de rekening die wordt gebruikt voor het vastleggen van de inkomende transportkosten die door een leverancier zijn gefactureerd. Het bedrag wordt als een debet geboekt. De tegenrekening is de voorraadwijzigingsrekening. Deze boeking wordt alleen gebruikt wanneer de optie **Boeken op toeslagrekening in grootboek** is ingesteld *Ja* op de pagina **Parameters van leveranciers**. |
| Verschillenrekening | De rekening die wordt gebruikt als tegenrekening voor de kosten wanneer de inkoopfactuur wordt geboekt. Dit veld wordt alleen gebruikt als de optie **Toenamerekening voor kostentypetoeslag gebruiken** is ingesteld op *Ja* op het sneltabblad **Kostprijsberekening** op het tabblad **Algemeen** van de pagina **Parameters voor francoprijzen**. |

## <a name="vendor-cost-type-groups"></a>Kostentypegroepen voor leveranciers

Met leverancierskostentypegroepen kunt u bepalen hoe *automatische kosten* worden gevonden en toegepast op een traject. Leveranciers met vergelijkbare importkosten worden gekoppeld. Alle leveranciers van opkomende markten betalen bijvoorbeeld hetzelfde accijnspercentage voor hetzelfde type product dat vanuit een gevestigde markt wordt ingekocht.

U kunt kostentypegroepen voor leveranciers onderhouden door naar **Francoprijzen \> Kostprijsberekening instellen \> Kostentypegroepen voor leveranciers** te gaan. De pagina **Kostentypegroepen voor leveranciers** bevat een raster met alle bestaande kostentypegroepen voor leveranciers. U kunt de knoppen in het actiedeelvenster gebruiken om rijen in het raster toe te voegen, te verwijderen en te bewerken.

In de volgende tabel worden de velden beschreven die op elke rij in het raster beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| Kostentypegroepen voor leveranciers | Voer een unieke naam in voor de kostentypegroep van de leverancier (bijvoorbeeld *Opkomende markten*). |
| Beschrijving | Voer een omschrijving van de kostentypegroep voor leveranciers in. Deze omschrijving kan gedetailleerde informatie geven over het niveau of het type toeslag dat aan de leveranciersgroep is gekoppeld. |

## <a name="item-cost-type-groups"></a>Kostentypegroepen voor artikelen

Met kostentypegroepen voor artikelen kunt u bepalen hoe *automatische kosten* worden gevonden en toegepast op een traject. Vergelijkbare artikelen worden gekoppeld. Alle artikelen met een heffingstarief van 5 procent kunnen bijvoorbeeld tot een specifieke kostentypegroep behoren.

U kunt kostentypegroepen voor artikelen onderhouden door naar **Francoprijzen \> Kostprijsberekening instellen \> Kostentypegroepen voor artikelen** te gaan. De pagina **Kostentypegroepen voor artikelen** bevat een raster met alle bestaande kostentypegroepen voor artikelen. U kunt de knoppen in het actiedeelvenster gebruiken om rijen in het raster toe te voegen, te verwijderen en te bewerken.

In de volgende tabel worden de velden beschreven die op elke rij in het raster beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| Kostentypegroepen voor artikelen | Voer een unieke naam in voor de kostentypegroep van het artikel (bijvoorbeeld *Heffing 5%*). |
| Beschrijving | Voer een omschrijving van de kostentypegroep voor artikelen in. Deze omschrijving kan gedetailleerde informatie geven over het niveau of het type toeslag dat aan de artikelgroep is gekoppeld. |

> [!NOTE]
> Het kostentype van het artikel is aan het artikel gekoppeld via het veld **Kostentypegroep** op het sneltabblad **Inkoop** van de pagina **Vrijgegeven product** van het artikel.

## <a name="transfer-order-cost-type-groups"></a>Kostentypegroepen voor overboekingsorders

Met kostentypegroepen voor overboekingsorders kunt u bepalen hoe *automatische kosten* worden gevonden. Vergelijkbare artikelen worden gekoppeld. Alle artikelen met een heffingstarief van 7 procent kunnen bijvoorbeeld tot een specifieke kostentypegroep behoren.

U kunt kostentypegroepen voor overboekingsorders onderhouden door naar **Francoprijzen \> Kostprijsberekening instellen \> Kostentypegroepen voor overboekingsorders** te gaan. De pagina **Kostentypegroepen voor overboekingsorders** bevat een raster met alle bestaande kostentypegroepen voor overboekingsorders. U kunt de knoppen in het actiedeelvenster gebruiken om rijen in het raster toe te voegen, te verwijderen en te bewerken.

In de volgende tabel worden de instellingen beschreven die op elke rij in het raster beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| Kostentypegroepen voor overboekingsorders | Voer een unieke naam in voor de kostentypegroep van de overboekingsorder (bijvoorbeeld *Heffing 7%*). |
| Beschrijving | Voer een omschrijving van de kostentypegroep voor overboekingsorders in. Deze omschrijving kan gedetailleerde informatie geven over het niveau of het type toeslag dat aan de kostentypegroep voor overboekingsorders is gekoppeld. |

> [!NOTE]
> Het kostentype voor overboekingsorders is aan het artikel gekoppeld via het veld **Kostengroep voor overboekingsorders** op het sneltabblad **Inkoop** van de pagina **Vrijgegeven product** van het artikel.

## <a name="cost-templates"></a>Kostensjablonen

U gebruikt kostensjablonen om standaardwaarden in te stellen voor instellingen die gebruikers die de kostenraming krijgen mogelijk niet weten. Met kostensjablonen kunt u de complexiteit in het ramingsproces verminderen door de selecties die gebruikers moeten maken, te minimaliseren om een juiste raming te krijgen.

Als u wilt werken met kostensjablonen, gaat u naar **Francoprijzen \> Kostprijsberekening instellen \> Kostensjablonen**. Op de pagina **Kostensjablonen** worden in het lijstdeelvenster aan de linkerkant alle huidige kostensjablonen weergegeven. U kunt de knoppen in het actiedeelvenster gebruiken om sjablonen toe te voegen, te verwijderen en te bewerken.

In de volgende tabel worden de instellingen beschreven die beschikbaar zijn voor elke sjabloon.

| Veld | Beschrijving |
|---|---|
| Kostensjabloon | Een unieke naam invoeren voor de kostensjabloon. Met de naam wordt meestal de factor of kostenvermenigvuldiger voor de sjabloon beschreven. |
| Beschrijving | Voer een omschrijving van de kostensjabloon in. |
| Verzendbedrijf | Selecteer de leveranciersrekening van het expeditiebedrijf dat u aan de kostensjabloon wilt koppelen. |
| Leveringsmethode | Selecteer de leveringsmodus die via de kostensjabloon moet worden gebruikt wanneer de geraamde kosten van een artikel worden berekend. Via dit veld kunt u de automatische kosten bepalen die zijn gekoppeld aan de goederen in de kostenraming. |
| Type verzendcontainer | Selecteer het type containertype voor de verzending dat u aan de kostensjabloon wilt koppelen. Via dit veld kunt u de automatische kosten bepalen die zijn gekoppeld aan de goederen in de kostenraming. |
| Douane-expediteur | Selecteer de douane-expediteur (leverancier) die u aan de kostensjabloon wilt koppelen. Via dit veld kunt u de automatische kosten bepalen die zijn gekoppeld aan de kostenraming. |
| Factor | Voer een factor in die moet worden toegepast op de uiteindelijke kostenraming van goederen. Voer bijvoorbeeld *1,10* in om 10 procent op te tellen bij de berekende kostenraming. |

## <a name="volumetric-divisors"></a>Volumetrische delers

Volumedelers worden gebruikt om het volumegewicht te berekenen. Elk expeditie-/vrachtvervoerbedrijf formuleert zijn eigen volumedeler. Bovendien verschillen de verdelers van een bedrijf meestal, afhankelijk van de leveringsmodus. Lucht en zee hebben bijvoorbeeld heel andere delers. Een bedrijf kan de regels ook ingewikkelder maken, afhankelijk van de plaats vanwaar het verzendt. De volgende formule wordt gebruikt om het volumegewicht te vinden: VolumetricWeight = Volume ÷ VolumetricDivisor.

Een pakket dat per vliegtuig wordt verzonden, heeft bijvoorbeeld een volume van 3 kubieke meter (m³). Het bedrijf berekent de kosten op volumegewicht en past een volumedeler van 6 toe. Deze deler wordt gedeeld door het volume om het volumegewicht te bepalen. Daarom is het volumegewicht voor dit voorbeeld 3 ÷ 6 = 0,5 kilogram (kg).

Als u volumedelers wilt instellen, gaat u naar **Francoprijzen \> Kostprijsberekening instellen \> Volumedelers**. De pagina **Volumedelers** biedt een raster met alle bestaande volumedelers. U kunt de knoppen in het actiedeelvenster gebruiken om rijen in het raster toe te voegen, te verwijderen en te bewerken.

In de volgende tabel worden de velden beschreven die op elke rij in het raster beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| Verzendbedrijf | Selecteer de leveranciersrekening van het expeditiebedrijf dat is gekoppeld aan de volumedelers. |
| Code voor kostentype | Selecteer de kostentypecode die aan de volumedeler is gekoppeld. Gebruik dit veld om kostentypen in rapportage-buckets te zetten. Rapporten kunnen worden afgedrukt op rapportagecategorieën of op kostentype. |
| Vertrekhaven | Selecteer de poort "van" waarop de volumedeler van toepassing is. |
| Volumetrische deler | Voer de waarde van de volumedeler in die op de rij van toepassing is. Het volume van elk pakket wordt gedeeld door de waarde die hier u invoert, om het volumegewicht van het pakket te bepalen. |

> [!NOTE]
> De maximumwaarde tussen het **werkelijke gewicht** en het **volumegewicht** wordt door het systeem gebruikt.
