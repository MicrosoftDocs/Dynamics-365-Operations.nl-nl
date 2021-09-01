---
title: Instellen van parameters voor francoprijzen
description: In dit onderwerp wordt beschreven hoe u algemene gegevens en configuratie-instellingen kunt instellen die in de hele module Francoprijzen worden gebruikt voor boekingen, statusupdates, nummerreeksen en gedrag.
author: sherry-zheng
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ITMParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-07
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: 138ef5b3fc210a6a717200d0c41422ea901373c1dfbf1a53cd558603c11277ea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6747980"
---
# <a name="landed-cost-parameters-setup"></a>Instellen van parameters voor francoprijzen

[!include [banner](../../includes/banner.md)]

U gebruikt de pagina **Parameters voor francoprijzen** om algemene gegevens en configuratie-instellingen in te stellen die in de hele module **Francoprijzen** worden gebruikt voor boekingen, statusupdates, nummerreeksen en gedrag. Het instellen van parameters wordt door rechtspersonen gedeeld en kan door een beheerder worden gewijzigd.

## <a name="open-the-landed-cost-parameters-page"></a>De pagina Parameters voor francoprijzen openen

Als u met de parameters wilt werken, gaat u naar **Francoprijzen \> Instellen \> Parameters voor francoprijzen** en stelt u de velden in zoals wordt beschreven in de volgende subsecties.

![Pagina Parameters voor francoprijzen.](media/landed-cost-parameters.png "Pagina Parameters voor francoprijzen")

## <a name="general-tab"></a>Tabblad Algemeen

### <a name="general-fasttab"></a>Het sneltabblad Algemeen

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Algemeen** van het tabblad **Algemeen** van de pagina **Parameters voor francoprijzen**.

| Instelling | Beschrijving |
|---|---|
| Verzendtarief gebruiken | Er wordt een verzendtarief ingesteld voor de gedefinieerde periode en wordt gebruikt om de kosten te schatten van goederen waarvoor meerdere valuta's worden gebruikt. Stel deze optie in op *Ja* om een verzendtarief te gebruiken. |
| Wisselkoerstype | De standaardverzameling van wisselkoersen die wordt gebruikt voor berekeningen in meerdere valuta's voor een reis en reiskosten. |
| Hoeveelheid van inkooporder bijwerken | Selecteer wat er gebeurt als een gebruiker de hoeveelheid op een inkooporderregel wijzigt:<ul><li>**Accepteren:**: de reishoeveelheid wordt automatisch aangepast.</li><li>**Waarschuwing**: als de regel aan een reis is gekoppeld, wordt er een waarschuwing weergegeven, maar wordt de reishoeveelheid bijgewerkt.</li><li>**Fout**: als de regel aan een reis is gekoppeld, wordt een foutbericht weergegeven en kan de inkooporder niet worden bijgewerkt. De orderregel moet daarom eerst uit de reis worden verwijderd.</li></ul> |
| Automatisch aantal dozen bijwerken | Als deze optie is ingesteld op *Ja*, worden alle kartonnen dozen bij elkaar opgeteld en weergegeven op het niveau van de reis en de container. Als de optie is ingesteld op *Nee*, wordt het aantal kartonnen dozen in eerste instantie ingesteld op 0 (nul). Deze waarde kan indien nodig handmatig worden bewerkt. |

### <a name="costing-fasttab"></a>Sneltabblad Kostprijsberekening

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Kostprijsberekening** van het tabblad **Algemeen** van de pagina **Parameters voor francoprijzen**.

| Instelling | Beschrijving |
|---|---|
| Boekingsspecificatie | De waardecorrectie in het grootboek selecteren:<ul><li>**Totaal**: er wordt een totaalbedrag geboekt naar het grootboek.</li><li>**Artikelgroep**: de correctie wordt per artikelgroep gespecificeerd.</li><li>**Artikelnummer**: De correctie wordt per artikel gespecificeerd. Deze waarde biedt de meeste details.</li></ul> |
| Nul kosten toestaan | Stel deze optie in op *Nee* om een fout weer te geven als een gebruiker een kostenraming probeert te boeken voor een reisfactuur of inkooporder die geen waarde bevat voor de verwachte reiskosten. In het foutbericht wordt vermeld dat kosten van 0 (nul) niet kunnen worden toegewezen en dat de factuurboeking mislukt. In dit geval kan de gebruiker de raming handmatig bijwerken (of de automatische kosten opnieuw configureren) en vervolgens de bijgewerkte waarde ophalen of de kosten verwijderen als deze niet van toepassing zijn.<p>Stel deze optie in *Ja* om toe te staan dat de reiskosten leeg mogen zijn. In dit geval wordt een prijs van 0 (nul) toegewezen op basis van het kostengebied. Er kan vervolgens een factuur met leverancierskosten worden verwerkt met de kostprijs nul wanneer de reis is ontvangen.</p><p>We raden u aan de raming voor de automatische kostprijsrecord te configureren om te voorkomen dat er kostprijs van nul wordt weergegeven. Hoewel deze raming niet volledig nauwkeurig is, is deze toch nauwkeuriger dan een veronderstelde kostprijs van nul.</p> |
| Boekingsdatum correctie | Wanneer u een reiskostenfactuur voor leveranciers maakt, wordt de vereffeningstabel (voorraadcorrecties) ook bijgewerkt. De datum selecteren die standaard is ingesteld op de pagina **Reiskosten selecteren** als u in het factuurjournaal bent:<ul><li>**Transactiedatum**: gebruik de datum van het journaal (boekingsdatum).</li><li>**Factuurdatum inkooporder**: gebruik de financiële boekingsdatum van de voorraadfactuur (inkooporder).</li><li>**Geselecteerde datum**: De gebruiker kan een boekingsdatum opgeven. Hoewel u geen datum leg kunt laten, ontvangt de gebruiker een fout als de datum nog steeds leeg is wanneer de kostenfactuur wordt geboekt.</li></ul> |
| Boekstuk voor inkoopfactuur gebruiken | Als deze optie is ingesteld op *Ja*, wordt voor transacties voor kostentoerekening hetzelfde boekstuknummer gebruikt dat voor de inkoopfactuur wordt gebruikt. Wanneer de optie wordt ingesteld op *Nee* gebruikt het systeem het volgende beschikbare nummer voor de nummerreeks van **Toerekeningskosten boekstuk** die is ingesteld op het tabblad **Nummerreeks** van de pagina **Parameters francoprijzen**.<p>Deze optie is alleen van invloed als de optie **Boeken op toeslagrekening in grootboek** is ingesteld *Ja* op het tabblad **Factuur** van de pagina **Parameters van leveranciers**.</p> |
| Handmatig boeken naar vereffeningsrekening blokkeren | Stel deze optie in op *Ja* om te voorkomen dat er wordt geboekt naar vereffeningsrekeningen waarbij de transactie niet aan een reis is gekoppeld door **Functies \> Reiskosten** te selecteren in het actievenster van het leveranciersfactuurjournaal. We raden u aan om deze optie in te stellen op *Ja*, zodat de reis- en vereffeningsrekening correct kan worden vereffend. |
| Toenamerekening voor toeslagen van kostentype gebruiken | Als deze optie is ingesteld op *Ja*, wordt de toenamerekening voor toeslagen gebruikt die is geconfigureerd voor de relevante kostentypecode op de pagina **Kostentypecodes** om kosten toe te rekenen als onkosten.<p>Deze optie is alleen van invloed als de optie **Boeken op toeslagrekening in grootboek** is ingesteld *Ja* op het tabblad **Factuur** van de pagina **Parameters van leveranciers**. |
| Correcties boeken als afwijking | Als deze optie is ingesteld op *Ja*, wordt de standaardfunctionaliteit genegeerd en worden de voorraadcorrectietransacties die betrekking hebben op afwijkingen tussen de geschatte kosten en de werkelijke kosten, naar een verschillenrekening geboekt.<p>Wanneer deze optie is ingesteld op *Nee*, worden de voorraadcorrectietransacties die betrekking hebben op afwijkingen, verwerkt op basis van de configuratie van de methode voor de kostprijsberekening en de kostentypecode. Voor standaardkosten worden afwijkingen nog steeds naar de verschillenrekening geboekt. Voor het verplaatsen van gewogen gemiddelde (WMA) worden afwijkingen geboekt naar de verschillenrekening of naar de voorraad.</p><p>Deze optie is alleen van invloed als de optie **Boeken op toeslagrekening in grootboek** is ingesteld *Ja* op het tabblad **Factuur** van de pagina **Parameters van leveranciers**.</p> |

### <a name="validation-fasttab"></a>Sneltabblad Validatie

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Validatie** van het tabblad **Algemeen** van de pagina **Parameters voor francoprijzen**.

| Instelling | Beschrijving |
|---|---|
| Meerdere kostenfacturen | Selecteer wat er gebeurt als er meer dan één factuur wordt verwerkt voor een reis, folio of container voor dezelfde diverse toeslagen.<ul><li>**Accepteren**: het systeem moet meerdere kostenfacturen toestaan.</li><li>**Waarschuwing**: er wordt een waarschuwing weergegeven.</li><li>**Fout**: er wordt een foutbericht weergegeven.</li></ul> |
| Meerdere leveranciers per folio | Selecteer wat er gebeurt als er meer dan een inkooporders van een leverancier aan een folio worden toegevoegd.<ul><li>**Accepteren**: het systeem moet de actie toestaan.</li><li>**Waarschuwing**: er wordt een waarschuwing weergegeven, maar de actie kan nog wel worden uitgevoerd.</li><li>**Fout**: er wordt een foutbericht weergegeven en de actie wordt niet uitgevoerd.</li></ul><p>Uw douanemakelaar of lokale wetten kunnen een specifieke waarde voor dit veld verplicht stellen.</p> |
| Tolerantie voor meerdere leveringsmethoden | Selecteer wat er gebeurt als goederen van een inkooporder waarvoor een andere leveringsmodus wordt gebruikt, aan die reis worden toegevoegd.<ul><li>**Accepteren**: het systeem moet de actie toestaan.</li><li>**Waarschuwing**: er wordt een waarschuwing weergegeven, maar de actie kan nog wel worden uitgevoerd.</li><li>**Fout**: er wordt een foutbericht weergegeven en de actie wordt niet uitgevoerd.</li></ul> |
| Tolerantie voor meerdere magazijnen | Selecteer wat er gebeurt als een reis meerdere orderregels bevat die naar verschillende magazijnen moeten worden geleverd. Deze orderregels kunnen over een of meer inkooporders worden verdeeld.<ul><li>**Accepteren**: het systeem moet de actie toestaan.</li><li>**Waarschuwing**: er wordt een waarschuwing weergegeven.</li><li>**Fout**: er wordt een foutbericht weergegeven.</li></ul> |
| Ontbrekend volume | Selecteer wat er gebeurt als een gebruiker een artikel zonder een hoeveelheid aan een reis toevoegt.<ul><li>**Accepteren**: het systeem moet het artikel accepteren.</li><li>**Waarschuwing**: er wordt een waarschuwing weergegeven.</li><li>**Fout**: er wordt een foutbericht weergegeven.</li></ul><p>Als er hoeveelheden worden gebruikt om kosten te berekenen en te verdelen, raden we u aan *Waarschuwing* of *Fout* te selecteren.</p> |
| Serviceprovider zonder reiskosten | Selecteer wat er gebeurt als een gebruiker een factuur voor een serviceprovider probeert te verwerken die niet aan een reis is gekoppeld. <ul><li>**Accepteren**: het systeem moet de actie toestaan.</li><li>**Waarschuwing**: er wordt een waarschuwing weergegeven.</li><li>**Fout**: er wordt een foutbericht weergegeven.</li></ul><p>U wordt aangeraden *Waarschuwing* te selecteren.</p> |

### <a name="defaults-fasttab"></a>Sneltabblad Standaardwaarden

In de volgende tabel worden de velden beschreven die beschikbaar zijn op het sneltabblad **Standaardwaarden** van het tabblad **Algemeen** van de pagina **Parameters voor francoprijzen**.

| Instelling | Beschrijving |
|---|---|
| Journaalnaam | Selecteer het standaardjournaal dat door de functie *Ontvangstjournaal maken* moet worden gebruikt. |
| Reisstatus | Selecteer de status die een reis moet hebben voordat gebruikers een huurcontainer voor verzenden in het systeem kunnen instellen. Deze actie vindt meestal plaats wanneer de goederen in transit of in het dock zijn. |
| Trajectsjabloon | Selecteer de standaardtrajectsjabloon die u voor nieuwe huurcontainers voor verzending wilt gebruiken. Over het algemeen zult u een trajectsjabloon met de huurkosten selecteren. |
| Mutatie | Als de hoeveelheid voor een levering binnen de gedefinieerde tolerantie voor meer of minder valt, wordt er automatisch een mutatiejournaal verwerkt. Selecteer het standaardmutatiejournaal dat u wilt gebruiken. Het veld **Tegenrekening** voor de geselecteerde naam van het mutatiejournaal moet een waarde hebben. |
| Overboeking | Wanneer een minderlevering wordt verwerkt, wordt de hoeveelheid voor een korte ontvangst overgeboekt naar een magazijn voor minderleveringen. Selecteer het standaardoverboekingsjournaal dat u wilt gebruiken. |
| Inkooporders voor niet-reizen uitschakelen | Schakel de functionaliteit voor Francoprijzen voor meer-/minderleveringen uit voor inkooporders die niet aan een reis zijn gekoppeld. |
| Inkooporders voor niet-goederen in transit uitschakelen | Schakel de functionaliteit voor Francoprijzen voor meer-/minderleveringen uit voor inkooporders waarvoor de functionaliteit goederen in transit niet wordt gebruikt. |
| Goederen in transit buiten respijtperiode voor ontvangst | Geef het aantal dagen na de eerste ontvangst van een container op dat extra meerontvangstbonnen nog kunnen worden voltooid voor die container. |

## <a name="status-updates-tab"></a>Tabblad Statusupdates

Het systeem gebruikt statuswaarden om de status van elke reis aan te geven. Waarden van reisstatussen kunnen automatisch worden toegepast op reizen via reistracering of periodieke batchtaken. U kunt deze waarden ook handmatig toepassen door de reis te openen en vervolgens een status te selecteren in de groep **Reis bijwerken** op het tabblad **Beheren** van het actievenster. 

U kunt zoveel waarden voor de reisstatus maken als u wilt. Vier van deze waarden moeten echter worden gedefinieerd als gebruikt voor een speciaal doel op het tabblad **Statusupdates** van de pagina **Parameters voor francoprijzen**. In de volgende tabel worden de velden beschreven die daar beschikbaar zijn.

| Instelling | Beschrijving |
|---|---|
| Kostprijs berekend | Selecteer de reisstatus die aangeeft dat een reis is afgerond. |
| In transit | Selecteer de reisstatus die aangeeft dat een reis in transit is. |
| Gereed voor kostprijsberekening | Selecteer de reisstatus die aangeeft dat een reis gereed is voor kostprijsberekening. Deze status wordt gebruikt wanneer alle voorraadinkoopfacturen en reiskostenfacturen waarbij het veld **Krediet op de reiskosten** is ingesteld op *Leverancier*, voor de reis zijn verwerkt. Reizen waarvan de kostprijs niet kan worden berekend, hebben de status *Gereed voor kostprijsberekening*.|
| Kosten vooraf berekend | Selecteer de reisstatus die aangeeft dat voor een reis de kostprijs vooraf wordt berekend. Deze status wordt gebruikt wanneer een nieuwe kostentransactie aan een reis wordt toegevoegd nadat de kostprijs voor deze reis al is berekend. Er kunnen nieuwe kostentransacties worden toegevoegd aan een eerdere reis waarvoor de kostprijs is berekend wanneer er een tweede vrachtfactuur of onverwachte overligkosten wordt ontvangen. Deze status wordt automatisch toegepast wanneer er nieuwe reiskosten worden toegevoegd aan een reis waarvoor kosten zijn berekend. |

## <a name="voyage-creator-tab"></a>Tabblad Reisontwerper

In de volgende tabel worden de secties beschreven op het tabblad **Reisontwerper** van de pagina **Parameters voor francoprijzen**.

| Sectie | Beschrijving |
|---|---|
| Toleranties | De velden **Buiten volumetolerantie** en **Buiten gewichtstolerantie** geven drempels aan waarboven goederen worden beschouwd als een te grote hoeveelheid goederen en te veel gewicht. Wanneer een gebruiker goederen toevoegt op de pagina **Reisbewerker**, maar de hoeveelheid of het gewicht van de goederen overschrijdt de waarde die u hier hebt ingesteld, wordt er een waarschuwing weergegeven. De waarde van elk veld wordt uitgedrukt als een percentage van het maximumvolume of -gewicht dat is ingesteld voor het relevante type container. U wordt aangeraden een waarde tussen 5 en 10 procent van het maximumvolume of -gewicht te gebruiken. |
| Instellingen voor maken van folio | Het systeem kan meerdere folio's maken terwijl de reis wordt gemaakt. Gebruik deze sectie om te definiëren wanneer er een nieuw folio moet worden gemaakt. Voor elke rij in deze sectie, controleert het systeem de opgegeven tabel en het opgegeven veld en maakt het een folio voor elke unieke veldwaarde. |

## <a name="cost-estimates-tab"></a>Tabblad Geraamde kosten

Het tabblad **Geraamde kosten** van de pagina **Parameters voor francoprijzen** heeft maar één veld: **Standaardversie kostprijsberekening**. Dit veld is alleen van toepassing als de methode voor het berekenen van de kostprijs *Standaardkostprijsberekening* is. Selecteer de standaardversie voor de kostprijsberekening die moet worden gebruikt voor de periodieke taak *Artikelkostprijs bijwerken*. U moet deze instelling mogelijk telkens wijzigen wanneer er een nieuw financieel jaar begint.

## <a name="inventory-dimensions-tab"></a>Tabblad Voorraaddimensies

U gebruikt het tabblad **Voorraaddimensies** van de pagina **Parameters voor francoprijzen** om te bepalen welke beschikbare voorraaddimensies standaard moeten worden weergegeven op elke pagina met francoprijzen waarop dimensies worden gebruikt.

Selecteer een dimensie en stel vervolgens de optie **Reisregels**, **Goederen in transit** en/of **Geraamde kosten** in op *Ja* voor elke pagina waarop die dimensie standaard moet worden weergegeven. Herhaal deze stap zo nodig voor andere dimensies.

De instellingen op dit tabblad bepalen de standaarddimensies voor elke aangewezen pagina voor alle rechtspersonen. Gebruikers die echter op een van de aangewezen pagina's werken, kunnen de standaarddimensies negeren door **Voorraad \> Weergavedimensies** in het actievenster te selecteren.

## <a name="number-sequences-tab"></a>Tabblad Nummerreeksen

Op het tabblad **Nummerreeksen** van de pagina **Parameters voor francoprijzen wordt elk type referentienummerreeks weergegeven dat Francoprijzen** is vereist, maar die worden niet door rechtspersonen gedeeld. Selecteer een nummerreekscode voor elke referentie in de lijst.

> [!NOTE]
> In een configuratie voor meerdere bedrijven moeten voor elk bedrijf (rechtspersoon) verschillende nummerreeksen worden gemaakt.

## <a name="shared-number-sequences-tab"></a>Tabblad Gedeelde nummerreeksen

Op het tabblad **Gedeelde nummerreeksen** van de pagina **Parameters voor francoprijzen wordt elk type referentienummerreeks weergegeven dat door rechtspersonen voor Francoprijzen** wordt gedeeld. Momenteel bevat de lijst slechts één nummerreeks. Deze nummerreeks wordt gebruikt voor de reis-is.

Op de pagina **Alle reizen** kunnen gebruikers alle reizen voor alle rechtspersonen bekijken. Voor het bewerken en verwerken van een reis moeten gebruikers zich echter in de rechtspersoon van de geselecteerde record bevinden.

## <a name="feature-visibility-tab"></a>Tabblad Functiezichtbaarheid

Met Francoprijzen worden functies (velden en functies) aan meerdere gebruikte pagina's in Microsoft Dynamics 365 Supply Chain Management toegevoegd. Deze pagina's omvatten pagina's die betrekking hebben op hoofdgegevens van leveranciers, vrijgegeven producten, inkooporders, overboekingsorders en magazijninstellingen. Als u Francoprijzen gebruikt, moet u deze functies overal zichtbaar maken voordat u hiervan kunt profiteren. Als u Francoprijzen niet gebruikt, kunt u de functies verbergen.

Stel op het tabblad **Functiezichtbaarheid** van de pagina **Parameters voor francoprijzen** de optie **Activeren** in op *Ja* om de functies voor Francoprijzen zichtbaar te maken op locaties waar deze beschikbaar zijn. Stel de optie in op *Nee* om de functies op gemeenschappelijke pagina's buiten Francoprijzen te verbergen. Zelfs wanneer de optie is ingesteld op *Nee*, blijft de module zelf, inclusief de pagina **Parameters voor francoprijzen**, beschikbaar voor gebruikers die over de juiste toegangsmachtigingen beschikken.
