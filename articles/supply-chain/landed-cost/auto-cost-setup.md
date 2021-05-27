---
title: Instellingen van automatische kosten
description: In dit onderwerp wordt beschreven hoe u kostenregels in kunt stellen voor verschillende inkomende reisniveaus. Op basis van deze regels worden de kosten berekend en automatisch toegevoegd. Daarom hoeven gebruikers de kosten niet handmatig toe te voegen.
author: sherry-zheng
ms.date: 01/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMCostAutoSetup
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-01-21
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d057522afbf6a6d706c51f7c9e69b656483c7eb1
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021655"
---
# <a name="auto-costs-setup"></a>Instellingen van automatische kosten

[!include [banner](../../includes/banner.md)]

U kunt de pagina **Automatische kosten** gebruiken om kostenregels in te stellen voor verschillende kostengebieden (zoals reizen, verzendingscontainers, folio´s, inkooporders, artikelen of overboekingsorderregels). Op basis van de regels en de velden die gebruikers selecteren wanneer ze records maken voor een van de kostengebieden, berekent het systeem de kosten en voegt het deze automatisch toe. Daarom hoeven gebruikers de kosten niet handmatig toe te voegen.

Als u wilt werken met automatische kosten, gaat u naar **Francoprijzen \> Kosten instellen \> Automatische kosten**. Stel vervolgens uw automatische kostenregels in zoals beschreven in de rest van dit onderwerp.

## <a name="work-with-cost-areas"></a>Werken met kostengebieden

Automatische kosten werken zoals handelsovereenkomsten of automatische diverse toeslagen. Elke automatische kostenrecord behoort tot een specifiek kostenniveau. Gebruik het veld **Kostengebied** in het lijstdeelvenster van de pagina **Automatische kosten** om het kostengebied te selecteren dat u wilt gebruiken. In het lijstvenster worden alleen automatische kosten weergegeven die horen bij het geselecteerde kostengebied. Alle automatische kosten die u maakt, maken deel uit van het geselecteerde kostengebied.

Met kostengebieden kan het systeem kosten verdelen over de inkooporderregels in een kostengebied. Bijvoorbeeld: met de kosten voor één verzendcontainer wordt de waarde verdeeld over alle producten in die container. Als er twee of meer verzendcontainers zijn, kan voor elke container hetzelfde kostentype worden opgegeven. Het containertype kan dus worden gebruikt om de juiste automatische kosten te zoeken.

## <a name="buttons-on-the-action-pane"></a>Knoppen in het actiedeelvenster

De volgende tabel beschrijft de knoppen in het actievenster op de pagina **Automatische kosten**.

| Knop | Beschrijving |
|---|---|
| Bewerken | Bestaande automatische kosten bewerken. |
| Nieuw | Automatische kosten maken. |
| Delete | Automatische kosten verwijderen. |
| Kopiëren uit | Nieuwe automatische kostenrecord maken op basis van een bestaande record. U kunt de nieuwe record vervolgens bewerken. Met deze knop kunt u snel nieuwe automatische kosten maken. |
| Dimensies weergeven | Een dialoogvenster openen waarin u de voorraaddimensies kunt selecteren die worden weergegeven voor de kostentransacties die u bekijkt. Als u selectievakjes uitschakelt, worden er minder voorraaddimensies weergegeven voor de kostentransacties. Er worden daarom minder details weergegeven voor de transactie. Als er een voorraaddimensie voor automatische kosten is opgegeven, worden de automatische kosten alleen toegepast wanneer de opgegeven voorraaddimensie voor het artikel op een reis wordt gebruikt. |

## <a name="settings-on-the-header"></a>Instellingen in de koptekst

De combinatie van instellingen in de koptekstsectie bepaalt wanneer en hoe specifieke automatische kosten aan een reis worden toegevoegd. Automatische kosten worden alleen toegepast op een reis, container of folio als de details van de automatische kosten overeenkomen met de details in de koptekst van dat kostengebied. De som van alle overeenkomende automatische kosten bepaalt de geschatte francoprijzen van een reis. Deze kosten worden verdeeld over alle artikelen voor een vat of reis.

In de volgende tabel worden alle velden beschreven die beschikbaar kunnen zijn in de koptekstsectie. Welke velden beschikbaar zijn, is echter afhankelijk van het kostengebied en de weergavedimensies die momenteel zijn geselecteerd.

| Veld | Beschrijving |
|---|---|
| **Rekeningcode** | <p>Selecteer een van de volgende waarden:</p><ul><li>**Tabel** – De kostenregel is alleen van toepassing op een specifieke leverancier.</li><li>**Groep** – De kostenregel is van toepassing op een specifieke leveranciersgroep. Het systeem zal zoeken naar de [kostentypegroep van de leverancier](costing-parameters-setup.md) die aan de leveranciersrecord is gekoppeld.</li><li>**Alle**: de kostenregel is van toepassing op alle leveranciers. |
| **Verzendbedrijf** | Selecteer de leverancier of leveranciersgroep waarop de kostenregel van toepassing is. Dit veld is alleen beschikbaar als u *Tabel* of *Groep* in het veld **Accountcode** selecteert. |
| **Douane-expediteur** | Selecteer de leverancier of leveranciersgroep waarop de kostenregel van toepassing is. Dit veld is alleen beschikbaar als u *Tabel* of *Groep* in het veld **Accountcode** selecteert. |
| **Artikelcode** | <p>Selecteer een van de volgende waarden:</p><ul><li>**Tabel** – De kostenregel is alleen van toepassing op een specifiek artikel.</li><li>**Groep** – De kostenregel is van toepassing op een specifieke artikelgroep. Het systeem zal zoeken naar de [kostentypegroep van het artikel](costing-parameters-setup.md) die aan de artikelrecord is gekoppeld.</li><li>**Alle**: de kostenregel is van toepassing op alle artikelen.|
| **Artikelrelatie** | Selecteer het artikel of de artikelgroep waarop de kostenregel van toepassing is. Dit veld is alleen beschikbaar als u *Tabel* of *Groep* in het veld **Artikelcode** selecteert. |
| **Leveringsmethode** | Selecteer de leveringsmethode (zoals lucht of zee) die van toepassing is op de kostenregel. |
| **Containertype** | Het type verzendcontainer waarin de goederen worden verzonden Automatische kosten kunnen alleen worden toegepast op een reis als het containertype in de instelling voor automatische kosten overeenkomt met het containertype van de reis. |
| **Van-haven** en **Naar-haven** | De bronhaven ('van') en bestemmingshaven ('naar') van de reis. (Sommige verzendcontainers kunnen verschillende "naar"-havens hebben, omdat de reis mogelijk stopt bij meerdere havens.) Automatische kosten kunnen alleen worden toegepast op een reis als de van- en naar-havens in de instellingen voor automatische kosten overeenkomen met de van- en naar-havens van de reis. |
| **Automatisch kostennummer** | De unieke identificatie van de automatische kostenregel. De waarde van dit veld wordt automatisch gegenereerd op basis van de nummerreeks die is ingesteld op de pagina **Parameters francoprijzen**. |
| **Voorraaddimensies** | Bij sommige kostengebieden kunt u een of meer artikeldimensies opnemen in de koptekst (zoals grootte, kleur, magazijn en batchnummer). Selecteer **Dimensies weergeven** in het actievenster om de dimensies te selecteren die moeten worden opgenomen. |

## <a name="settings-on-the-lines-fasttab"></a>Instellingen op het sneltabblad Regels

Voeg op het sneltabblad **Regels** een rij toe voor elke valuta die kan worden gebruikt wanneer kosten worden toegepast op een inkooporderregel voor een reis. 

Voor artikelen en inkooporders wordt de valuta van elke inkooporderregel vergeleken met de valuta's die zijn opgegeven op het sneltabblad **Regels**. Deze wordt alleen toegepast op de kostenwaarde die is ingesteld voor de overeenkomende regel of het overeenkomende artikel. Als er geen regel is ingesteld voor de valuta van de regel of het artikel, worden de automatische kosten niet toegepast op die regel of dat artikel.

Voor andere typen kostengebieden zijn alle regels op het sneltabblad **Regels** van toepassing op elke reis, verzendingscontainer, folio of overboekingsorderregel die overeenkomt met de waarden die in de koptekst zijn vastgelegd.

In de volgende tabel worden alle velden beschreven die kunnen verschijnen op elke regel. Welke velden beschikbaar zijn, is echter afhankelijk van het kostengebied dat momenteel is geselecteerd.

| Veld | Beschrijving |
|---|---|
| **Valuta** | De valuta selecteren waar de regel betrekking op heeft. Deze valuta is gerelateerd aan de inkooporder. Wanneer het systeem probeert de automatische kosten te vinden die moeten worden toegepast op een reis of reisregels, selecteert het de regel met dezelfde valuta als de inkooporder. Dit veld is alleen beschikbaar als het veld **Kostengebied** is ingesteld op *Inkooporder* of *Artikel*. |
| **Code voor kostentype** | Het kostentype. |
| **Toewijzingsmethode** | <p>De methode die wordt gebruikt om kosten over regels te verdelen. De volgende opties zijn beschikbaar:</p><ul><li><p>**Percentage:** de waarde van het veld **Kostenwaarde** is een percentage dat geldt voor de totale waarde van goederen.</p><p>Als het veld **Kostenwaarde** bijvoorbeeld is ingesteld op *10* en de totale waarde van goederen $800 is, is de kostenwaarde $80 (= $800 × 10 procent).</p></li><li>**Hoeveelheid:** de kosten worden verdeeld aan de hand van de hoeveelheid goederen.</li><li>**Bedrag:** de kosten worden verdeeld aan de hand van de waarde van de goederen.</li><li>**Volume:** de kosten worden verdeeld aan de hand van het volume van de goederen. Het volume wordt opgegeven in de hoofdrecord van het artikel.</li><li>**Gewicht:** de kosten worden verdeeld aan de hand van het gewicht van de goederen. Het gewicht wordt opgegeven in de hoofdrecord van het artikel.</li><li>**Volumetrisch:** de kosten worden verdeeld aan de hand van de volumetrische meting van goederen.</li><li><p>**Meting:** met deze optie kunt u een meting opgeven in de module **Francoprijzen**. Deze wordt vaak gebruikt door organisaties die niet het individuele volume of gewicht van de goederen weten, maar die een nauwkeurigere verdeling vereisen dan met de opties **Bedrag** en **Hoeveelheid** mogelijk is. De expediteur of agent geeft de organisatie het gewicht of de kubieke meting op artikelniveau of inkooporderniveau.</p><p>Bijvoorbeeld: zeevracht is gelijk aan $900. Artikel A heeft een gewicht van 800 kilogram (kg) en een volume van twee kubieke meter (m³). Artikel B heeft een gewicht van 100 kilogram (kg) en een volume van 1 m³. Dit zijn de resultaten wanneer de kosten worden verdeeld op gewicht:</p><ul><li>Artikel A = $800</li><li>Artikel B = $100</li></ul><p>Dit zijn de resultaten wanneer de kosten worden verdeeld op volume:</p><ul><li>Artikel A = $600</li><li>Artikel B = $300</li></ul><p>**Let op:** wanneer het veld **Verdelingsmethode** is ingesteld op *Meting*, gebruikt het systeem de metingen die zijn ingevoerd voor zowel het kostengebied (de verzendcontainer) als de regels. Deze metingen hoeven niet samen het verwachte totaal te zijn. Als u echter wilt dat ze het verwachte totaal opleveren, kunt u een controle uitvoeren door de statistieken te gebruiken om de totale meting te controleren. De instelling van de metingprompt en automatische update van de meting op zending- of containerniveau worden ingesteld in de koptekst van de reis.</p></li></ul> |
| **Begindatum** | Geef de start op van het datumbereik voor kostprijsberekening als er een datumbereik is. Deze datum is de eerste datum waarop de automatische kosten van toepassing zijn. |
| **Einddatum** | Geef het einde op van het datumbereik voor kostprijsberekening als er een datumbereik is. Deze datum is de laatste datum waarop de automatische kosten van toepassing zijn. |
| **Categorie** | <p>Selecteer de methode die wordt gebruikt om kosten te berekenen. De volgende opties zijn beschikbaar:</p><ul><li>**Vast:** de kosten worden verdeeld aan de hand van de verdelingsmethode.</li><li>**Stuks:** kosten worden per stuk toegewezen. Daarom wordt de verdelingsmethode niet gebruikt.</li><li>**Percentage:** er wordt een percentage van de waarde van de goederen toegevoegd. Daarom wordt de verdelingsmethode niet gebruikt.</li><li>**Tarief**: selecteer deze optie als er hoeveelheidsuitsplitsingen zijn. Het veld **Verdelingsmethode** voor de regel moet worden ingesteld op *Meting*.</li><ul> |
| **Uitgesplitst naar hoeveelheid** | <p>Schakel dit selectievakje in om de knop **Hoeveelheidsuitsplitsingen** beschikbaar te maken op het sneltabblad **Regels**. Door hoeveelheidsuitsplitsingen kunnen de kosten worden opgesplitst en kunnen de verschillende kosten verschillen, afhankelijk van de hoeveelheid op de inkooporderregel van de reis. Deze functionaliteit wordt vaak gebruikt wanneer de leveringsmodus lucht is. Het veld **Categorie** voor de regel moet worden ingesteld op *Tarief*.</p><p>De hoeveelheid heeft betrekking op de optie die is geselecteerd in het veld **Verdelingsmethode**. De kostenwaarde is tot de hoeveelheid die is ingevoerd in het veld **Kostenwaarde**.<p>Bijvoorbeeld: hoeveelheden van 45 tot 100 kg produceren een toeslag van $6,00 per meting (zoals kg/m³). Hoeveelheden van meer dan 100 kg produceren een toeslag van $5,50 per meting (zoals kg/m³).</p> |
| **Kostprijs** | Voer de waarde van de kosten in. |
| **Valutacode voor kosten** | Selecteer de valuta van de kosten. |
| **Btw-groep voor artikel** | Selecteer de btw-code voor de kosten. |
| **Minimale kosten** | <p>Dit veld is alleen van toepassing als het selectievakje **Opgesplitst per hoeveelheid** is ingeschakeld. Als de meting deze waarde niet bereikt, wordt de minimumwaarde geselecteerd, ongeacht de kosten die zijn opgegeven op de pagina **Hoeveelheidsuitsplitsingen**.<p>Bijvoorbeeld: hoeveelheden van 0 tot 45 kg produceren een toeslag van $6 per meting (kg/m³). Hoeveelheden van 46 tot 100 kg produceren een toeslag van $5,50 per meting (kg/m³). Als 2 kg wordt verzonden, wordt met de hoeveelheidsuitsplitsing een kostenwaarde van $12 gemaakt. Als het veld **Minimumkosten** echter is ingesteld op *$100*, worden de uiteindelijke kosten $100.</p> |
| **Samenvoegen** | Schakel dit selectievakje in om gebruikers toe te staan deze kosten te verplaatsen van het niveau van de verzendcontainer naar het niveau van de reis. In dat geval kunnen kosten automatisch worden berekend op containerniveau. Deze kunnen echter ook worden gecombineerd en verdeeld over alle artikelen in alle containers op een reis in plaats van alle artikelen in de afzonderlijke containers. |
| **Gekoppeld kostentype** | <p>Koppel de huidige regel aan een andere regel in dezelfde record voor automatische kosten door de waarde **Kostentypecode** op te geven van de regel die u wilt koppelen. Deze functionaliteit is alleen beschikbaar als het veld **Categorie** voor de huidige regel is ingesteld op *Percentage*. Wanneer de huidige regel aan een andere regel is gekoppeld, worden de kosten van de huidige regel gebaseerd op de kosten van de andere regel.</p><p>Vracht is bijvoorbeeld $1.000 en u wilt dat de brandstoftoeslag 10 procent van de vrachtkosten is. In dit geval moet de regel een **Categorie**-waarde *Procent*, een **Kostenwaarde** van *10%* en een waarde **Gekoppeld kostentype** met de instelling *Vracht* hebben.</p> |
| **Waardecorrectie** en **Correctiebedrag** | <p>Met deze velden kunt u de waarde en het bedrag voor verschillende percentagewaarden aanpassen. Deze zijn alleen beschikbaar als het veld **Kostengebied** is ingesteld op *Artikel*.</p><p>Voor verschillende onderdelen van een artikel kan verschillende kostprijsberekening worden ingesteld. Eén onderdeel van een artikel kan een ander kostenpercentage hebben dan de andere onderdelen van dat artikel. Deze benadering is soms vereist om een bepaald deel van de goederen met verschillende tarieven te waarderen.</p><p>Een heffing voor een horloge wordt bijvoorbeeld met twee tarieven berekend: een onderdeel van het horloge heeft een heffing van 10 procent en een tweede onderdeel heeft een tarief van 2 procent. In dit geval wordt de kostprijsberekening tussen de twee onderdelen opgesplitst.</p><p>De kosten worden berekend voor het artikel, maar de kostenwaarde wordt gecorrigeerd met de waarde van de onderdelen die de verschillende kostencategorie hebben. De kosten van de overige onderdelen kunnen vervolgens worden berekend met behulp van het bedrag dat bij de vorige berekening is gecorrigeerd.</p><p>Onderdeel A van het horloge heeft bijvoorbeeld een kostprijs van $9,50 en een heffing van 10 procent en onderdeel B heeft een kostprijs van $0,50 en een heffing van 2 procent. Daarom is het totaal $10,00. Het eerste item is voor de regel van 10 procent. De volgende waarden worden gebruikt:</p><ul><li>**Categorie:** *Percentage*</li><li>**Kostenwaarde:** *10*</li><li>**Gecorrigeerde waarde:** *Corrigeren met*</li><li>**Gecorrigeerde waarde:** *-0,50*</li></ul><p>Met deze instelling wordt opgegeven dat de kosten van het artikel ($ 10) moeten worden verminderd met $0,50 (de prijs van onderdeel B) voordat een heffing van 10 procent wordt berekend. Daarom wordt 10 procent toegepast op $9,50.</p><p>Het tweede item is voor de regel van 2 procent (de $0,50 waarmee de vorige invoer is gecorrigeerd). De volgende waarden worden gebruikt:</p><ul><li>**Categorie:** *Percentage*</li><li>**Kostenwaarde:** *2*</li><li>**Gecorrigeerde waarde:** *Gebruik*</li><li>**Correctie:** *0,50*</li></ul><p>Met deze instelling wordt de resterende heffing berekend die moet worden betaald voor onderdeel B.</p> |
