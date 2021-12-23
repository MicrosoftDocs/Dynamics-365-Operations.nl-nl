---
title: Cyclustelling
description: In dit artikel wordt beschreven hoe u cyclustelling kunt gebruiken met de met magazijnoplossing die in Magazijnbeheer beschikbaar is. Dit artikel is niet van toepassing op de magazijnoplossing die in Voorraadbeheer beschikbaar is.
author: Mirzaab
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSCycleCountPlan, WHSCycleCountPlanListPage, WHSCycleCountThreshold, WHSWorkTableListPage, SalesShipmentDeviation, WHSRFMenuItemCycleCount, WHSWorkLineCycleCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: 50671
ms.assetid: 49f5c431-b043-4170-aa24-b7d5d1ee063e
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: adaed1d5a4f1ac62df35bcc1497610ce0f44043c
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902216"
---
# <a name="cycle-counting"></a>Cyclustelling

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u cyclustelling kunt gebruiken met de met magazijnoplossing die in Magazijnbeheer beschikbaar is. Dit artikel is niet van toepassing op de magazijnoplossing die in Voorraadbeheer beschikbaar is.

Cyclustelling is een magazijnproces dat u kunt gebruiken om voorhanden voorraadartikelen te controleren. Het cyclustellingsproces kan in drie stappen worden beschreven:

1.  **Cyclustellingwerk maken** - Cyclustellingwerk kan automatisch worden gemaakt op basis van drempelparameters voor artikelen of door een cyclustellingsplan te gebruiken. U kunt ook handmatig cyclustellingswerk maken door de artikel- of magazijnparameters te gebruiken op de pagina **Cyclustellingswerk volgens artikel** of de pagina **Cyclustellingswerk volgens locatie**.
2.  **Cyclustelling verwerken** - Nadat u cyclustellingswerk hebt gemaakt, kunt u het cyclustellingswerk uitvoeren door artikelen in een magazijnlocatie te tellen en het resultaat via een mobiel apparaat in Dynamics 365 Supply Chain Management in te voeren. Als alternatief, kunt u artikelen in een magazijnlocatie tellen zonder het cyclustelling werk te maken. Dit proces wordt *spot cyclustelling* genoemd.
3.  **Verschillen in de getelde waarde oplossen** - Na een cyclustelling hebben artikelen met verschillen in de getelde waarde de werkstatus **In afwachting van controle** hebben op de pagina **Alle werk**. U kunt deze verschillen oplossen op de pagina **Cyclustellingswerk in afwachting van controle**.

De volgende afbeelding licht het cyclustellingsproces toe. ![Processtroom voor cyclustelling.](./media/performcyclecountinginawarehouselocation.jpg)

## <a name="cycle-counting-prerequisites"></a>Vereisten voor cyclustelling
De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u cyclustelling kunt gebruiken.
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Vereiste</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Artikel</td>
<td>Het artikel moet ingeschakeld zijn voor magazijnbeheer processen</td>
</tr>
<tr class="even">
<td>Magazijn</td>
<td>Het magazijn moet ingeschakeld zijn voor magazijnbeheer processen. Om het magazijn in te schakelen voor magazijnbeheerprocessen, selecteert u het magazijn op de pagina <strong>Magazijnen</strong> en selecteert u vervolgens de optie <strong>Magazijnbeheerprocessen gebruiken</strong>. Als u wilt dat werknemers palleten kunnen verplaatsen tijdens een cyclustelling, schakelt u op het sneltabblad <strong>Magazijnbeheer</strong> de optie <strong>Palletverplaatsingen gedurende cyclustelling toestaan</strong> in.</td>
</tr>
<tr class="odd">
<td>Werkgroepen</td>
<td>Optioneel: Maak een werkgroep om het magazijnwerk te onderscheiden op basis van het type werk (in dit geval, cyclustellingswerk).</td>
</tr>
<tr class="even">
<td>Locaties</td>
<td>Cyclustelling voor locaties inschakelen Als u de cyclustelling voor een magazijnlocatie wilt inschakelen, selecteert u op de pagina <strong>Locatieprofielen</strong> de optie <strong>Cyclustelling toestaan</strong>.</td>
</tr>
<tr class="odd">
<td>Parameters voor magazijnbeheer</td>
<td>Parameters instellen voor cyclustelling. Geef op de pagina <strong>Parameters voor magazijnbeheer</strong> de standaardcorrectietypecode, het werkklasse-id en de werkprioriteit voor cyclustelling op.</td>
</tr>
<tr class="even">
<td>Mobiel apparaat</td>
<td><ul>
<li>Maak een menu-item aan voor een van de volgende methoden op de pagina <strong>Menuopties voor mobiel apparaat</strong>:
<ul>
<li>Gebruiker-geleid cyclustelling</li>
<li>Systeem-geleid cyclustelling</li>
<li>Groepering van cyclustelling</li>
<li>Plaatscyclustelling</li>
</ul>
</li>
<li>Een menu instellen voor het mobiel apparaat.</li>
<li>Maak een werkgebruikersaccount aan en wijs een mobiel apparaat menu aan de werkgebruikers-ID toe.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Verwante insteltaken</td>
<td>Een cyclustelling plan voor een magazijnlocatie instellen.</td>
</tr>
</tbody>
</table>

## <a name="automatically-create-cycle-counting-work"></a>Automatisch cyclustellingwerk maken
Er zijn twee manieren om het herhalend maken van cyclustellingswerk in te plannen: cyclustellingsdrempels instellen of cyclustellingsplannen instellen.

-   Een cyclustellingdrempel wijst op de hoeveelheid of percentagelimiet van voorraadartikelen. Cyclustelwerk wordt automatisch gemaakt wanneer de drempellimiet wordt bereikt.
-   Een cyclustellingsplan maakt cyclustelwerk ofwel meteen ofwel periodiek door middel van een batchtaak. Wanneer het cyclustelwerk is gemaakt, bevat de telwerkregel informatie over de locatie waar moet worden geteld. De voorraad die voor handen is en die is gekoppeld aan deze locatie is niet geblokkeerd en is daarom beschikbaar voor reservering en uitgaande verwerking, zelfs als er open tellend werk bestaat.

### <a name="create-cycle-counting-work-based-on-threshold-parameters-for-items"></a>Maak cyclustellingswerk gebaseerd op een drempelparameters voor artikelen

Cyclustellingswerk kan worden aangemaakt als het aantal artikelen in een locatie onder een opgegeven drempelwaarde valt. Er zijn bijvoorbeeld 60 artikelen op een locatie met een cyclustellingdrempel van 40. Tijdens een verkoopordertransactie worden 25 artikelen verzameld vanaf de locatie en op een tijdelijke locatie geplaatst. Omdat de nieuwe artikeltelling minder is dan de drempelhoeveelheid van 35, wordt het cyclustelling werk automatisch aangemaakt voor de locatie.

### <a name="schedule-cycle-counting-work"></a>Cyclustellings werk schema

U kunt een cyclustellingsplan plannen om onmiddellijk of periodiek cyclustelwerk te maken. Wanneer u cyclustellingsplannen instelt, kunt u de werkgroep controleren waarvoor het cyclustellingswerk wordt aangemaakt, het maximumaantal cyclustellingen dat voor artikelen op verschillende locaties wordt gemaakt, en het aantal dagen dat moet verstrijken voordat een magazijnlocatie opnieuw wordt geteld. Een artikel is bijvoorbeeld beschikbaar o drie locaties in het magazijn, en het maximum aantal cyclustellingen is ingesteld op **2**. In dit geval worden bij uitvoering van het cyclustellingsplan twee cyclustellingen gecreëerd voor de twee locaties waar het artikel aanwezig is. In een ander voorbeeld wordt het aantal dagen tussen cyclustellingen ingesteld op **5**. In dit geval wordt het cyclustellingswerk om de vijf dagen gemaakt. Als het cyclustellingswerk echter op dag drie wordt verwerkt, wordt het volgende cyclustellingswerk gecreëerd vijf dagen nadat de laatste cyclustelling werd verwerkt, dus op dag acht.

## <a name="create-cycle-counting-work-manually"></a>Handmatig cyclustelling werk aanmaken
Als u handmatig cyclustellingswerk wilt aanmaken, kunt u de pagina´s **Cyclustellingswerk volgens artikel** of **Cyclustellingswerk volgens locatie** hiervoor gebruiken. U kunt het maximale aantal cyclustellingen opgeven dat tegelijkertijd moet worden gemaakt. Als de magazijnmanager bijvoorbeeld een waarde van **vijf** opgeeft, wordt er cyclustellingswerk aangemaakt voor vijf locaties zelfs als het artikel op 10 locaties aanwezig is. U kunt ook een werkgroep-ID selecteren waaraan u de gemaakte cyclustellingswerk-IDs toewijst. Wanneer een werkgroep-ID wordt verwerkt voor cyclustelling, worden de cyclustellingswerk-ID´s die aan deze werkpool zijn toegewezen verwerkt als een groep.

## <a name="perform-a-cycle-count-by-using-a-mobile-device"></a>Een cyclustelling uitvoeren met een mobiel apparaat
Er zijn verscheidene methoden voor het verwerken van cyclustellingswerk met Supply Chain Management op een mobiel apparaat:

-   **Door gebruiker bestuurd** - De werknemer kan een cyclustellingswerk-ID specificeren die de status **Openstaand** heeft.
-   **Systeem-geleid**: Supply Chain Management wijst een cyclustellingswerk-id toe aan de werknemer.
-   **Groepering van cyclustelling** - De werknemer kan cyclustellingswerk-IDs groeperen die specifiek zijn voor een bepaalde locatie, zone, of een werkpool.
-   **Plaatscyclustelling** - De werknemer kan artikelen in een magazijnlocatie op elk moment tellen, zonder cyclustelling werk te maken. Om plaatscyclustelling op een locatie uit te voeren, voert de werknemer de locatie-ID in.

In de volgende procedure wordt getoond hoe u plaatscyclustelling kunt uitvoeren met een mobiel apparaat. Welke instructies de werknemer op het apparaat ziet, is afhankelijk van de instellingen van het menu-item voor plaatscyclustelling.

1.  Op het mobiele apparaat, selecteer het menu item om spot cyclustelling werk uit te voeren.
2.  Registreer de locatie waar u plaatscyclustelling wilt uitvoeren.
3.  Registreer en bevestig het artikelnummer en de getelde artikelhoeveelheid. **Opmerking:** De status van het cyclustellingswerk wordt bijgewerkt naar **In afwachting van controle** of **Afgesloten** op de pagina **Alle werk**, afhankelijk van de parameters die zijn ingesteld op de pagina **Werknemer**.
4.  Optioneel: Herhaal stap 3 voor de resterende artikelen op de locatie en bevestig dat er geen extra artikelen beschikbaar zijn om te tellen.

## <a name="resolve-cycle-counting-differences"></a>Verschil in cyclustellingen oplossen
Een cyclustellingsverschil treedt op in de volgende scenario´s, als de optie **Is een cyclustellingssupervisor** is ingesteld op **Nee** voor een werkgebruikers-id:

-   De getelde waarde ligt niet binnen de afwijkingslimieten die zijn opgegeven in de velden **Maximale percentagelimiet** of **Maximale hoeveelheidslimiet** op de pagina **Werkgebruikers**. Bijvoorbeeld: de hoeveelheid voorhanden voorraad op een locatie is 50 en de maximale afwijking voor de werkgebruiker is 10. Als de werkgebruiker een waarde invoert die niet tussen 40 en 60 ligt, treedt er een verschil op.
-   De getelde waarde verschilt van de voorhand voorraadhoeveelheid en er zijn geen afwijkingslimieten ingesteld.

U kunt verschillen in de getelde waarde aanpassen en vervolgens de getelde waarde op de pagina **Cyclustellingswerk in afwachting van controle** accepteren. U kun de aangepaste telling van de artikelhoeveelheid verifiëren op de pagina **Voorhanden voorraad per locatie**. De getelde waarde wordt afgewezen als het verschil niet kan worden goedgekeurd.

## <a name="additional-resources"></a>Aanvullende resources
[Mobiele apparaten instellen voor magazijnwerk](configure-mobile-devices-warehouse.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]