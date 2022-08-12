---
title: Kwaliteitsbeheer voor magazijnprocessen
description: Dit artikel biedt informatie over de functie Kwaliteitsbeheer voor magazijnprocessen. Met deze functie worden de mogelijkheden van kwaliteitsbeheer uitgebreid en kunnen gebruikers besturingselementen voor artikelbemonstering integreren in het ontvangstproces van het magazijn via magazijnbeheerprocessen (WMS).
author: yufeihuang
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2020-04-02
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: 13c9bf522ededb5896c5f8462bfe123e9a9edb2c
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069237"
---
# <a name="quality-management-for-warehouse-processes"></a>Kwaliteitsbeheer voor magazijnprocessen

[!include [banner](../includes/banner.md)]

Met de functie _Kwaliteitsbeheer voor magazijnprocessen_ kunt u besturingselementen voor artikelbemonstering integreren in het ontvangstproces van het magazijn via magazijnbeheerprocessen (WMS). Magazijnwerk kan automatisch worden gegenereerd om de voorraad naar de kwaliteitscontrolelocatie te verplaatsen op basis van een percentage of een vaste hoeveelheid, of op basis van elke *n* de nummerplaat. Nadat een kwaliteitsorder is voltooid, kunt u automatisch werk genereren om de voorraad naar de volgende locatie in het proces te verplaatsen, afhankelijk van de kwaliteitsresultaten.

De functie _Kwaliteitsbeheer voor magazijnprocessen_ vergroot de mogelijkheden van de basisfunctie voor kwaliteitsbeheer. Het biedt de mogelijkheid om kwaliteitsorders te maken voor de voorraad die wordt verzonden naar de locatie van de kwaliteitscontrole, hoewel kwaliteitsorders niet altijd vereist zijn. Daarom is het mogelijk om een lichtgewicht kwaliteitscontroleproces te gebruiken dat is gebaseerd op magazijnwerkzaamheden.

## <a name="turn-on-the-quality-management-for-warehouse-processes-feature"></a>De functie Kwaliteitsbeheer voor magazijnprocessen inschakelen

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Magazijnbeheer*
- **Functienaam:** *Kwaliteitsbeheer voor magazijnprocessen*

## <a name="key-benefits"></a>Belangrijkste voordelen

De functie _Kwaliteitsbeheer voor magazijnprocessen_ genereert automatisch werkzaamheden als onderdeel van het ontvangstproces, om de voorraadhoeveelheid die is vereist voor kwaliteitscontrole te verplaatsen naar een locatie voor kwaliteitscontrole. Als de ontvangen hoeveelheid hoger is dan de hoeveelheid die is vereist voor kwaliteitscontrole (volgens de instellingen voor artikelbemonstering), wordt de overschothoeveelheid verplaatst naar een inkomende locatie die is gedefinieerd in de instelling van de locatierichtlijn. Nadat de kwaliteitsorder is gevalideerd, wordt automatisch de werktaak gegenereerd om de hoeveelheid voor de kwaliteitsorder te verplaatsen naar een nieuwe binnenkomende of retourlocatie op basis van de validatieresultaten en de instelling van de locatierichtlijn. Het automatisch genereren van werktaken met alleen de hoeveelheid die naar en van de kwaliteitscontrole moet worden verplaatst, zorgt voor een geïntegreerde proceservaring.

> [!NOTE]
> Wanneer de functie _Kwaliteitsbeheer voor magazijnprocessen_ wordt ingeschakeld, kunt u nog steeds gebruikmaken van het handmatige proces. In het handmatige proces gebruikt de magazijnmedewerker voorraadmutatie en verplaatsing met sjabloon om te zorgen dat de magazijntaak wordt gemaakt om voorraad van een kwaliteitscontrolelocatie te verplaatsen naar een nieuwe locatie. U kunt ook nog een richtlijn voor inkomende locaties instellen die voorraad in zijn geheel naar een kwaliteitscontrolelocatie verplaatst, zonder rekening te houden met de instellingen voor artikelbemonstering.

## <a name="quality-management-and-the-quality-management-for-warehouse-processes-feature"></a>Kwaliteitsbeheer en de functie Kwaliteitsbeheer voor magazijnprocessen

Wanneer de functie _Kwaliteitsbeheer voor magazijnprocessen_ wordt ingeschakeld, verandert de instelling van de belangrijke entiteiten voor magazijnbeheer en kwaliteitsbeheer. De volgende afbeelding geeft een overzicht van de entiteiten waarmee kwaliteitsorders voor magazijnprocessen kunnen worden ingeschakeld. Tekst tussen haakjes geeft de voorgestelde acties aan wanneer kwaliteitsbeheer is toegepast voordat de functie _Kwaliteitsbeheer van magazijnprocessen_ werd ingeschakeld.

![Entiteiten voor kwaliteitsbeheer.](media/quality-management-entity-diagram.png "Entiteiten voor kwaliteitsbeheer")

## <a name="enablers-the-quality-item-sampling-and-quality-order-work-order-types"></a>Ingeschakeld door: de werkordertypen Kwaliteit artikelbemonstering en kwaliteitsorder

De functie _Kwaliteitsbeheer voor magazijnprocessen_ introduceert twee werkordertypen waarmee het maken van werk kan worden ingeschakeld:

- **Kwaliteit artikelbemonstering**: dit werkordertype wordt gebruikt om taken te maken waarmee geregistreerde voorraad naar de kwaliteitscontrole wordt verplaatst.
- **Kwaliteitsorder**: dit werkordertype wordt gebruikt om taken te maken waarmee de voorraad wordt verplaatst van kwaliteitscontrole naar een nieuwe locatie op basis van de instelling van de locatierichtlijn.

### <a name="work-classes-location-directives-and-work-templates"></a>Werkklassen, locatierichtlijnen en werksjablonen

De werkordertypen _Kwaliteit artikelbemonstering_ en _Kwaliteitsorder_ worden toegepast door locatierichtlijnen, werkklassen en werksjablonen.

Voordat magazijnwerk automatisch kan worden gegenereerd om de voorraad naar kwaliteitscontrole te verplaatsen, moet u deze stappen uitvoeren om uw systeem in te stellen.

1. Maak afzonderlijke werkklassen voor de werkordertypen _Kwaliteit artikelbemonstering_ en _Kwaliteitsorder_. Op deze manier zorgt u ervoor dat het juiste werk automatisch kan worden gegenereerd op basis van de twee werkordertypen en dat dit werk vervolgens kan worden uitgevoerd met de mobiele app Magazijnbeheer.
1. Stel een werksjabloon op voor elk type werkorder:

    - Stel een werksjabloon in die het werkordertype _Kwaliteit artikelbemonstering_ gebruikt om geregistreerde voorraad automatisch naar een kwaliteitscontrolelocatie te verplaatsen.
    - Stel een werksjabloon in die het werkordertype _Kwaliteitsorder_ gebruikt om voorraad naar een kwaliteitscontrolelocatie te verplaatsen nadat de kwaliteitscontrole is uitgevoerd.

1. Stel voor elk werkordertype locatie-instructies in met de juiste locaties voor kwaliteitscontrole waarnaar de voorraad moet worden verplaatst. Nadat de kwaliteitscontrole is voltooid, zorgt de locatierichtlijn voor het werkordertype _Kwaliteitsorder_ ervoor dat een nieuwe doellocatie wordt geselecteerd, zodat de voorraad kan worden verplaatst uit de locatie van de kwaliteitscontrole.
1. Stel de relevante menuopties voor het mobiele apparaat in voor het ondersteunen van de verplaatsing van de ontvangen voorraad naar de kwaliteitscontrolelocatie en voor de verplaatsing naar een nieuwe locatie van voorraad die voor de kwaliteitscontrole slaagt of niet.

Zie het [voorbeeldscenario](#example-scenario) aan het einde van dit artikel voor een stapsgewijs voorbeeld waarin wordt beschreven hoe u deze instellingen voltooit.

## <a name="enable-a-warehouse-for-quality-management"></a>Een magazijn inschakelen voor kwaliteitsbeheer

Voordat de functie _Kwaliteitsbeheer voor magazijnprocessen_ kan worden toegepast op een bepaald magazijn, moet u deze stappen volgen om de functie beschikbaar te maken voor dat magazijn.

1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Magazijnen**.
1. Selecteer het magazijn om kwaliteitsbeheer in te schakelen.
1. Stel op het sneltabblad **Magazijn** de optie **Kwaliteitsorder inschakelen voor magazijnprocessen** in op _Ja_. (Deze optie kan alleen op _Ja_ worden ingesteld voor magazijnen die gebruikmaken van WMS (magazijnbeheerprocessen).)

Wanneer de optie **Kwaliteitsorder inschakelen voor magazijnprocessen** is ingesteld op _Ja_, wordt in de instelling van de kwaliteitskoppeling bepaald of de functie _Kwaliteitsbeheer voor magazijnprocessen_ werkelijk wordt toegepast op het geselecteerde magazijn. U kunt de instelling van de optie op elk gewenst moment wijzigen in _Nee_. In dat geval is de functie niet meer van toepassing voor het magazijn, ongeacht de instelling van de kwaliteitskoppeling.

## <a name="quality-control"></a>Kwaliteitscontrole

De functie _Kwaliteitsbeheer voor magazijnprocessen_ regelt verschillende belangrijke instellingen voor kwaliteitskoppelingen en artikelbemonstering.

### <a name="quality-associations"></a>Kwaliteitskoppelingen

Elke [kwaliteitskoppelingsrecord](enable-quality-management.md) definieert de set met testen, het aanvaardbare kwaliteitsniveau en het bemonsteringsplan dat van toepassing is op de gegenereerde kwaliteitsorders. Volg deze stappen als u een kwaliteitskoppelingsrecord wilt instellen.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Kwaliteitskoppelingen**.
1. Maak of selecteer de kwaliteitskoppelingsvermelding voor het artikel of de groep waarmee u werkt, of voor alle artikelen.
1. Stel op het sneltabblad **Voorwaarden** het veld **Toepasselijk magazijntype** in op een van de volgende waarden:

    - **Alleen kwaliteitsbeheer voor magazijnprocessen**: schakel de functie _Kwaliteitsbeheer voor magazijnprocessen_ in. U kunt deze waarde alleen selecteren als het verwijzingstype is ingesteld op *Inkoop* of *Productie*.
    - **Alles**: schakel de functie _Kwaliteitsbeheer voor magazijnprocessen_ uit. Selecteer deze waarde voor alle verwijzingstypen behalve *Inkoop* en *Productie*.

> [!NOTE]
> De functie _Kwaliteitsbeheer voor magazijnprocessen_ heeft alleen effect als het artikel op de brondocumentregel gebruikmaakt van magazijnbeheerprocessen (WMS) en als de optie **Kwaliteitsorder inschakelen voor magazijnprocessen** is ingesteld op _Ja_ voor het magazijn op de brondocumentregel.

Wanneer een artikel wordt geregistreerd (of gereedgemeld), bepaalt het systeem welke kwaliteitskoppelingen van toepassing zijn.

Wanneer de functie _Kwaliteitsbeheer voor magazijnprocessen_ is ingeschakeld, wordt het betreffende magazijntype logisch ingevoegd in de vierde zoekgroep van de kwaliteitskoppelingshiërarchie. De volgende tabel bevat een logische weergave van de zoekhiërarchie.

| Zoekgroep | Omschrijving |
|---|---|
| Groep 1 | Controleer voor elke kwaliteitskoppeling de waarden voor **verwijzingstype**, **gebeurtenistype** en **uitvoeringsovereenkomst** voor het artikel. Als de brondocumentregel overeenkomt, gaat u naar groep 2. |
| Groep 2 | Controleer voor elke kwaliteitskoppeling de waarde voor **artikelcode** (_Tabel_, _Groep_ of _Alle_) voor het artikel. _Tabel_ is specifieker dan _Groep_ en _Groep_ is specifieker dan _Alle_. Als er een overeenkomst is voor _Tabel_ (een specifiek artikel), gaat u naar groep 3. Als er geen overeenkomst is voor _Tabel_, zoekt u naar een overeenkomst voor _Groep_. Als er geen overeenkomst is voor _Groep_, is _Alle_ van toepassing. Als er een overeenkomst is, gaat u naar groep 3. |
| Groep 3 | Controleer voor elke kwaliteitskoppeling de **Rekeningcode** en de **Broncode** voor het artikel. De logica die wordt toegepast, lijkt op de logica die wordt toegepast voor de waarde van **Artikelcode**. |
| Groep 4 | Controleer voor elke kwaliteitskoppeling de waarde voor **Toepasselijk magazijntype** (_Alleen kwaliteitsbeheer voor magazijnprocessen_ of _Alle_) voor het artikel. Als de optie **Kwaliteitsorder inschakelen voor magazijnprocessen** is ingesteld op _Ja_ voor het magazijn in het brondocument, en het artikel op de brondocumentregel is ingesteld op _Magazijnbeheerprocessen gebruiken_, zijn koppelingen met een overeenkomst voor _Alleen kwaliteitsbeheer voor magazijnprocessen_ en koppelingen met een overeenkomst voor _Alle_ van toepassing, als beide bestaan. Als de optie **Kwaliteitsorder inschakelen voor magazijnprocessen** is ingesteld op _Nee_ voor het magazijn in het brondocument, en het artikel op de brondocumentregel is ingesteld op _Magazijnbeheerprocessen gebruiken_, is alleen kwaliteitsbeheer van toepassing. |

U hebt bijvoorbeeld een magazijn gedefinieerd waarvoor de optie **Kwaliteitsorder inschakelen voor magazijnprocessen** is ingesteld op _Ja_ en u hebt twee kwaliteitskoppelingen die zijn gedefinieerd voor het verwijzingstype *Inkoop*: één voor alle artikelen en één voor het gebeurtenistype *Registratie*. Het enige verschil tussen de twee kwaliteitskoppelingen is de waarde **Toepasselijk magazijntype**: deze is ingesteld op _Alle_ voor de ene kwaliteitskoppeling en op _Alleen kwaliteitsbeheer voor magazijnprocessen_ voor de andere. In dit geval zijn beide kwaliteitskoppelingen even specifiek en beide zijn van toepassing.

De waarde van het veld **Testgroep** voor de kwaliteitskoppelingen is ook een factor. In dit veld wordt de testprocedure gedefinieerd die moet worden toegepast. Als de waarde voor **Testgroep** hetzelfde is voor beide koppelingen, wordt één kwaliteitsorder gemaakt, voor de kwaliteitskoppeling waarvoor de waarde voor **Toepasselijk magazijntype** is ingesteld op _Alleen kwaliteitsbeheer voor magazijnprocessen_. Als de waarde voor **Testgroep** niet hetzelfde is voor beide koppelingen, worden twee kwaliteitsorders gemaakt. De eerste kwaliteitsorder wordt gemaakt voor de kwaliteitskoppeling waarvoor **Toepasselijk magazijntype** is ingesteld op _Alleen kwaliteitsbeheer voor magazijnprocessen_. De tweede kwaliteitsorder wordt gemaakt voor de kwaliteitskoppeling waarvoor **Toepasselijk magazijntype** is ingesteld op _Alle_.

> [!NOTE]
> De waarde voor _Alleen kwaliteitsbeheer voor magazijnprocessen_ wordt als meer specifiek beschouwd dan _Alle_ wanneer de criteria voor de kwaliteitskoppelingen voor de groepen 1 en 2 gelijk zijn en wanneer de testgroep hetzelfde is. Er worden alleen twee kwaliteitsorders gemaakt wanneer de testgroepen verschillen.

#### <a name="reference-types"></a>Verwijzingstypen

Wanneer de waarde voor **Verwijzingstype** is _Inkoop_ en de waarde voor **Toepasselijk magazijntype** is _Alleen kwaliteitsbeheer voor magazijnprocessen_, moet het veld **Gebeurtenistype** op het sneltabblad **Proces** zijn ingesteld op _Registratie_. _Registratie_ is het enige ondersteunde gebeurtenistype voor het verwijzingstype _Inkoop_ wanneer u de functie _Kwaliteitsbeheer voor magazijnprocessen_ gebruikt.

#### <a name="quality-processing-policy"></a>Beleid voor kwaliteitsverwerking

Met de functie _Kwaliteitsbeheer voor magazijnprocessen_ kunt u werk maken op basis van alleen artikelbemonstering. Dat maakt een licht proces mogelijk. De voorraad waarmee werk wordt gemaakt, is afhankelijk van de artikelbemonstering die aan de kwaliteitskoppeling is gekoppeld. Wanneer het lichtgewicht proces wordt gebruikt, kan de kwaliteitsafdeling nadat een werknemer de hoeveelheid in de kwaliteitscontrolelocatie heeft geplaatst, handmatig een kwaliteitsorder maken als een kwaliteitsorder is vereist.

In **het veld Kwaliteitsverwerkingsbeleid** op het sneltabblad **Kwaliteitsorderproces** wordt bepaald of er een kwaliteitsorder wordt gemaakt wanneer werk wordt gemaakt waarbij een artikel naar de locatie van de kwaliteitscontrole wordt verplaatst. U kunt dit veld instellen op _Kwaliteitsorder maken_ of _Alleen werk maken_. De standaardwaarde is _Kwaliteitsorder maken_.

> [!NOTE]
> Ongeacht of u handmatig kwaliteitsorders maakt, genereert het systeem automatisch werk om artikelen te verplaatsen uit de kwaliteitscontrolelocatie wanneer de kwaliteitsorder is gemarkeerd als gevalideerd.

Het maken van werk voor een kwaliteitsorder is niet gerelateerd aan de instelling van de kwaliteitskoppeling. Als een werksjabloon bestaat met een waarde voor **Werkordertype** van *Kwaliteitsorder*, en als aan de querycriteria wordt voldaan voor die werksjabloon, wordt door de validatie van een kwaliteitsorder het maken van werk voor een kwaliteitsorder geactiveerd.

#### <a name="referenced-item-sampling"></a>Verwijzing naar artikelbemonstering

Elke kwaliteitskoppeling moet naar een artikelbemonstering verwijzen. Een artikelbemonstering geeft de hoeveelheid aan die wordt verzonden voor kwaliteitscontrole. Dit kan zo worden ingesteld dat het alleen van toepassing is op kwaliteitskoppelingen waarvoor **Toepasselijk magazijntype** is ingesteld op _Alleen kwaliteitsbeheer voor magazijnprocessen_. Als de waarde voor **Bemonsteringsbereik** voor een artikelbemonstering is ingesteld op _Laden_ of _Zending_, of als de waarde voor **Hoeveelheidsspecificatie** is _Volledige nummerplaat_, kan naar de artikelbemonstering alleen worden verwezen door kwaliteitskoppelingen waarbij de waarde voor **Toepasselijk magazijntype** is ingesteld op _Alleen kwaliteitsbeheer voor magazijnprocessen_.

Als u een artikelbemonstering definieert die gebruikmaakt van het toepasselijke magazijntype _Alleen kwaliteitsbeheer voor magazijnprocessen_, wordt een foutbericht weergegeven als u ernaar probeert te verwijzen via een kwaliteitskoppeling die de functie _Kwaliteitsbeheer voor magazijnprocessen_ niet gebruikt.

> [!NOTE]
> Artikelbemonstering waarbij volledig blokkeren wordt gebruikt, wordt niet ondersteund voor kwaliteitskoppelingen waarbij het veld **Toepasselijk magazijntype** is ingesteld op _Alleen kwaliteitsbeheer voor magazijnprocessen_.

### <a name="item-sampling"></a>Artikelbemonstering

Artikelbemonstering bepaalt hoe vaak artikelen worden verzonden voor kwaliteitscontrole. De functie _Kwaliteitsbeheer voor magazijnprocessen_ introduceert het begrip _artikelbemonsteringsbereik_. Het systeem gebruikt het artikelbemonsteringsbereik wanneer wordt beoordeeld of en hoe kwaliteitsorders en/of de hoeveelheid werk voor kwaliteitsartikelen moeten worden gemaakt.

Als u artikelbemonstering wilt instellen, gaat u naar **Voorraadbeheer \> Instellen \> Kwaliteitscontrole \> Artikelbemonstering** en stelt u het veld **Bemonsteringsbereik** in op een van de volgende waarden:

- **Order**: de brondocumentregel is de basis voor het beoordelen of en hoe kwaliteitsorders en/of de hoeveelheid werk voor kwaliteitsartikelen worden gemaakt. Deze waarde is de standaardwaarde en wanneer deze is geselecteerd, werkt het systeem op dezelfde manier als wanneer de functie _Kwaliteitsbeheer voor magazijnprocessen_ niet is ingeschakeld.
- **Lading**: ladingen worden gebruikt als basis voor het beoordelen of en hoe een kwaliteitsorder en/of werk worden gemaakt. Deze waarde is alleen beschikbaar wanneer de functie _Kwaliteitsbeheer voor magazijnprocessen_ is ingeschakeld.
- **Zending**: zendingen worden gebruikt als basis voor het beoordelen of en hoe een kwaliteitsorder en/of werk worden gemaakt. Deze waarde is alleen beschikbaar wanneer de functie _Kwaliteitsbeheer voor magazijnprocessen_ is ingeschakeld.

> [!NOTE]
> Wanneer het veld **Bemonsteringsbereik** is ingesteld op *Lading* of *Zending*, worden de entiteiten voor lading en zending gebruikt als deze beschikbaar zijn. Als ze niet beschikbaar zijn, wordt de orderentiteit gebruikt.

De functie _Kwaliteitsbeheer voor magazijnprocessen_ introduceert tevens de waarde voor *Volledige nummerplaat* voor het veld **Hoeveelheidsspecificatie**. Deze waarde ondersteunt het maken van werk voor een kwaliteitsorder en bemonsteringswerk voor kwaliteitsartikelen op basis van de nummerplaat. Wanneer u deze waarde selecteert, worden de volgende wijzigingen aangebracht:

- De optie **Aantal onderbreken per artikel** en het veld **Per nde nummerplaat** op het sneltabblad **Proces** worden beschikbaar.
- Het veld **Waarde** op het sneltabblad **Bemonsteringshoeveelheid** is niet beschikbaar.
- De opties **Per bijgewerkte hoeveelheid**, **Locatie** en **Nummerplaat** zijn allemaal ingesteld op *Ja* en de instellingen kunnen niet worden gewijzigd.

Met de optie **Aantal onderbreken per artikel** wordt bepaald of het aantal van de nummerplaat wordt beoordeeld per artikel of voor alle artikelen in het bemonsteringsbereik. Productvarianten worden als hetzelfde artikel behandeld. Met deze optie bepaalt u ook of het aantal exemplaren van de nummerplaat voor elk artikel opnieuw wordt ingesteld.

De waarde van het veld **Per nde nummerplaat** bepaalt hoe vaak kwaliteitsorders worden gemaakt met betrekking tot het aantal artikelen dat is geregistreerd. Met de waarde *3* wordt elk derde artikel bijvoorbeeld verzonden naar kwaliteitscontrole, beginnend met het eerste item. De waarde moet groter zijn dan 0 (nul).

Terwijl werknemers artikelen ontvangen met de mobiele app Magazijnbeheer, controleert het systeem of er een kwaliteitskoppeling is ingesteld voor elk binnenkomend artikel. Als er een kwaliteitskoppeling is ingesteld, gebruikt het systeem de artikelbemonsterings record die voor die kwaliteitskoppeling is geconfigureerd om te bepalen hoe kwaliteitsorders, bemonsteringswerk voor kwaliteitsartikelen en werk voor inkooporders worden gemaakt.

> [!NOTE]
> Wanneer de ontvangstregistratie wordt uitgevoerd in de webclient (via de kleine registratiepagina of het artikelontvangstjournaal voor inkooporderregels), wordt er geen werk voor bemonstering of inkooporders voor het kwaliteitsartikel gemaakt, ongeacht de instelling. In plaats daarvan wordt voor artikelen die overeenkomen met een kwaliteitskoppeling, de artikelbemonstering waarnaar wordt verwezen, alleen gebruikt om het maken van kwaliteitsorders te controleren.

## <a name="examples-of-automatic-generation-of-quality-orders"></a>Voorbeelden van het automatisch genereren van kwaliteitsorders

De volgende voorbeelden laten zien hoe de instellingen van een kwaliteitskoppeling en de bijbehorende artikelbemonstering van invloed zijn op het genereren van kwaliteitsorders wanneer het veld **Toepasselijk magazijntype** is ingesteld op _Alleen kwaliteitsbeheer voor magazijnprocessen_.

Wanneer **Hoeveelheidsspecificatie** is ingesteld op de waarde _Volledige nummerplaat_, bepaalt het veld **Per nde nummerplaat** voor welke nummerplaten de bemonsteringswerk voor kwaliteitsartikelen wordt gemaakt. De eerste nummerplaat gaat altijd naar kwaliteitscontrole en vervolgens geeft de waarde van dit veld aan dat elke *n* de nummerplaat na die nummerplaat ook moet gaan.

De waarde voor **Verwijzingstype** voor de volgende voorbeelden is _Inkoop_ en de waarde van het **Gebeurtenistype** is *Registratie*.

| Bemonsteringsbereik | Specificatie van hoeveelheid | Per bijgewerkte hoeveelheid | Per opslagdimensie | Aantal onderbrekingen per artikel | Per nde nummerplaat | Resultaat |
|---|---|---|---|---|---|---|
| Order | Volledige nummerplaat | Ja _(vergrendeld/niet bewerkbaar)_ | <p>Locatie: Ja</p><p>Nummerplaat: Ja _(vergrendeld/niet bewerkbaar)_</p> | Nee | 3 | <p>**Hoeveelheid orderregel: 100 EA**</p><ol><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP1<p>Bemonsteringswerk van kwaliteitsartikel voor 20 EA</p><p>Kwaliteitsorder 1 voor 20 EA</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP2<p>Inkooporderwerk voor 20 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP3<p>Inkooporderwerk voor 20 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP4<p>Bemonsteringswerk van kwaliteitsartikel voor 20 EA</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP5<p>Inkooporderwerk voor 20 EA (opslag)</p></li></ol> |
| Order | Vaste hoeveelheid = 1 | Ja | <p>Locatie: Ja</p><p>Nummerplaat: Ja</p> | Nee | Niet van toepassing | <p>**Hoeveelheid orderregel: 100**</p><ol><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP1<p>Bemonsteringswerk van kwaliteitsartikel voor 1 EA</p><p>Kwaliteitsorder 1 voor 1 EA</p><p>Inkooporderwerk voor 19 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP2<p>Bemonsteringswerk van kwaliteitsartikel voor 1 EA</p><p>Kwaliteitsorder 1 voor 1 EA</p><p>Inkooporderwerk voor 19 (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP3<p>Bemonsteringswerk van kwaliteitsartikel voor 1 EA</p><p>Kwaliteitsorder 1 voor 1 EA</p><p>Inkooporderwerk voor 19 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP4<p>Bemonsteringswerk van kwaliteitsartikel voor 1 EA</p><p>Kwaliteitsorder 1 voor 1 EA</p><p>Inkooporderwerk voor 19 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 20 EA, LP5<p>Bemonsteringswerk van kwaliteitsartikel voor 1 EA</p><p>Kwaliteitsorder 1 voor 1 EA</p><p>Inkooporderwerk voor 19 EA (opslag)</p></li></ol> |
| Order | Procent = 10 | Nee | <p>Locatie: Nee</p><p>Nummerplaat: Nee</p> | Nee | Niet van toepassing | <p>**Hoeveelheid orderregel: 100 EA**</p><ol><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 50 EA, LP1<p>Bemonsteringswerk van kwaliteitsartikel voor 10 EA</p><p>Kwaliteitsorder 1 voor 10 EA</p><p>Inkooporderwerk voor 40 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 50 EA, LP2<p>Inkooporderwerk voor 50 EA (opslag)</p></li></ol> |
| Inlezen | Procent = 5 | Ja _(vergrendeld/niet bewerkbaar)_ | <p>Locatie: Nee</p><p>Nummerplaat: Nee</p> | Nee | Niet van toepassing | <p>**Hoeveelheid orderregel: 500 EA**</p><p>**Twee ladingen: eerste lading 200 EA, tweede lading 300 EA**</p><ol><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor de eerste lading voor 100 EA<p>Bemonsteringswerk van kwaliteitsartikel voor 5 EA</p><p>Kwaliteitsorder 1 voor 5 EA</p><p>Inkooporderwerk voor 95 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor de eerste lading voor 100 EA<p>Bemonsteringswerk van kwaliteitsartikel voor 5 EA</p><p>Kwaliteitsorder 1 voor 5 EA</p><p>Inkooporderwerk voor 95 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor de tweede lading voor 300 EA<p>Bemonsteringswerk van kwaliteitsartikel voor 15 EA</p><p>Kwaliteitsorder 1 voor 15 EA</p><p>Inkooporderwerk voor 285 EA (opslag)</p></li></ol> |
| Volgorde | Procent = 10 | Ja | <p>Locatie: Ja</p><p>Nummerplaat: Ja</p> | Nee | Niet van toepassing | <p>**Hoeveelheid orderregel: 100**</p><ol><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 50 EA, LP1<p>Bemonsteringswerk van kwaliteitsartikel voor 5 EA</p><p>Kwaliteitsorder 1 voor 5 EA</p><p>Inkooporderwerk voor 45 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 50 EA, LP2<p>Bemonsteringswerk van kwaliteitsartikel voor 5 EA</p><p>Kwaliteitsorder 1 voor 5 EA</p><p>Inkooporderwerk voor 45 (opslag)</p></li></ol> |
| Inlezen | Volledige nummerplaat | Ja _(vergrendeld/niet bewerkbaar)_ | <p>Locatie: Ja</p><p>Nummerplaat: Ja _(vergrendeld/niet bewerkbaar)_</p> | Nee | 3 | <p>**Twee artikelen:**</p><ul><li>**Hoeveelheid voor orderregel voor artikel A: 120 EA (4 pallets)**</li><li>**Hoeveelheid voor orderregel voor artikel B: 90 EA (3 pallets)**</li></ul><p>**Eén lading, twee ladingsregels met elke orderregel**</p><ol><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP1<p>Bemonsteringswerk van kwaliteitsartikel voor 30 EA</p><p>Kwaliteitsorder 1 voor 30 EA</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP2<p>Inkooporderwerk voor 30 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP3<p>Inkooporderwerk voor 30 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP4<p>Bemonsteringswerk van kwaliteitsartikel voor 30 EA</p><p>Kwaliteitsorder 1 voor 30 EA</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel B, 30 EA, LP5<p>Inkooporderwerk voor 30 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel B, 30 EA, LP6<p>Inkooporderwerk voor 30 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP7<p>Bemonsteringswerk van kwaliteitsartikel voor 30 EA</p><p>Kwaliteitsorder 1 voor 30 EA</p></li></ol> |
| Inlezen | Volledige nummerplaat | Ja _(vergrendeld/niet bewerkbaar)_ | <p>Locatie: Ja</p><p>Nummerplaat: Ja _(vergrendeld/niet bewerkbaar)_</p> | Ja | 3 | <p>**Twee artikelen:**</p><ul><li>**Hoeveelheid voor orderregel voor artikel A: 120 EA (4 pallets)**</li><li>**Hoeveelheid voor orderregel voor artikel B: 90 EA (3 pallets)**</li></ul><p>**Eén lading, twee ladingsregels met elke orderregel**</p><ol><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP1<p>Bemonsteringswerk van kwaliteitsartikel voor 30 EA</p><p>Kwaliteitsorder 1 voor 30 EA</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP2<p>Inkooporderwerk voor 30 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP3<p>Inkooporderwerk voor 30 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP4<p>Bemonsteringswerk van kwaliteitsartikel voor 30 EA</p><p>Kwaliteitsorder 1 voor 30 EA</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel B, 30 EA, LP5<p>Bemonsteringswerk van kwaliteitsartikel voor 30 EA</p><p>Kwaliteitsorder 1 voor 30 EA</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel B, 30 EA, LP6<p>Inkooporderwerk voor 30 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor artikel A, 30 EA, LP7<p>Inkooporderwerk voor 30 EA (opslag)</p></li></ol> |
| Inlezen | Procent = 10 | Ja _(vergrendeld/niet bewerkbaar)_ | <p>Locatie: Nee</p><p>Nummerplaat: Nee</p> | Nee | Niet van toepassing | <p>**Hoeveelheid orderregel: 100 EA**</p><p>**Er worden geen ladingen gemaakt. Orderbereik wordt toegepast.**</p><ol><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 50 EA, LP1<p>Bemonsteringswerk van kwaliteitsartikel voor 5 EA</p><p>Kwaliteitsorder 1 voor 5 EA</p><p>Inkooporderwerk voor 45 EA (opslag)</p></li><li>Registreer de ontvangst in de mobiele app Magazijnbeheer voor 50 EA, LP2<p>Bemonsteringswerk van kwaliteitsartikel voor 5 EA</p><p>Kwaliteitsorder 1 voor 5 EA</p><p>Inkooporderwerk voor 45 EA (opslag)</p></li></ol> |

Wanneer een werknemer een van de kwaliteitsorders valideert die in de vorige tabel worden weergegeven, wordt door het systeem automatisch een kwaliteitsorder gegenereerd om de voorraad van de kwaliteitscontrolelocatie naar de locatie te verplaatsen die is gedefinieerd in de locatierichtlijn voor het werkordertype voor de _Kwaliteitsorder_. U kunt een locatie voor dit doel instellen, zoals een retour- of opslaglocatie, afhankelijk van het testresultaat voor de kwaliteitsorder. Zie het [voorbeeldscenario](#example-scenario) aan het einde van dit artikel voor een voorbeeld van deze instelling.

U kunt een kwaliteitsorder die al is gevalideerd opnieuw openen, mits voor de kwaliteitsorder die is gekoppeld aan het verplaatsen van de voorraad vanuit de locatie van de kwaliteitscontrole, de **Werkstatus** niet de waarde *Gesloten* of *In uitvoering* heeft.

## <a name="process-insights-when-multiple-quality-associations-coexist"></a>Procesinzichten als meerdere kwaliteitskoppelingen bestaan

Er kunnen meerdere kwaliteitskoppelingen worden gedefinieerd voor en toegepast op dezelfde brondocumentregel en het veld **Toepasselijk magazijntype** kan worden ingesteld op _Alleen kwaliteitsbeheer voor magazijnprocessen_ voor sommige kwaliteitskoppelingen en op _Alle_ voor andere.

In het volgende voorbeeld heeft **Verwijzingstype** de waarde _Inkoop_.

1. De eerste kwaliteitskoppeling wordt op de volgende manier ingesteld:

    - **Toepasselijk magazijntype:** *Alleen kwaliteitsbeheer voor magazijnprocessen*
    - **Artikelcode:** *A0001*
    - **Rekeningcode:** *Alle*
    - **Testgroep:** *Monster*
    - **Artikelbemonstering:** *5 stuks*

1. De tweede kwaliteitskoppeling wordt op de volgende manier ingesteld:

    - **Toepasselijk magazijntype:** *Alle*
    - **Artikelcode:** *Alle*
    - **Rekeningcode:** *Alle*
    - **Testgroep:** *behuizing*
    - **Artikelbemonstering:** *1 stuks*

1. De derde kwaliteitskoppeling wordt op de volgende manier ingesteld:

    - **Toepasselijk magazijntype:** *Alleen kwaliteitsbeheer voor magazijnprocessen*
    - **Artikelcode:** *Alle*
    - **Rekeningcode:** *104*
    - **Testgroep:** *impedantie*
    - **Artikelbemonstering:** *elke tweede nummerplaat* (deze instelling betekent dat voor de eerste, derde, vijfde enzovoort ontvangen nummerplaat een kwaliteitsorder wordt gemaakt.)

1. De vierde kwaliteitskoppeling wordt op de volgende manier ingesteld:

    - **Toepasselijk magazijntype:** *Alle*
    - **Artikelcode:** *Alle*
    - **Rekeningcode:** *Alle*
    - **Testgroep:** *impedantie*
    - **Artikelbemonstering:** *5 stuks*

1. De vijfde kwaliteitskoppeling wordt op de volgende manier ingesteld:

    - **Toepasselijk magazijntype:** *Alle*
    - **Artikelcode:** *Alle*
    - **Rekeningcode:** *Alle*
    - **Testgroep:** *kegel*
    - **Artikelbemonstering:** *10%*

Er is nu een inkooporder voor een hoeveelheid van 10 stuks van artikel A0001 gemaakt voor leverancier 104. Vervolgens wordt met behulp van de mobiele app Magazijnbeheer een inkooporderregel met een hoeveelheid van 10 als ontvangen geregistreerd op één nummerplaat. Hier volgt het resultaat:

- Er is één kwaliteitsorder van de eerste kwaliteitskoppeling voor de testgroep met *behuizingen*. De hoeveelheid is 5. Er is geen kwaliteitsorder van de tweede kwaliteitskoppeling, omdat de criteria voor de eerste kwaliteitskoppeling meer specifiek betrekking hebben op de testgroep voor *behuizingen*.
- Er is één kwaliteitsorder van de derde kwaliteitskoppeling voor de testgroep *impedantie*. De hoeveelheid is 10. Er is geen kwaliteitsorder van de vierde kwaliteitskoppeling, omdat de criteria voor de eerste kwaliteitskoppeling meer specifiek betrekking hebben op de testgroep voor *impedantie*.
- Er is één kwaliteitsorder van de vijfde kwaliteitskoppeling voor de testgroep *kegel*. De hoeveelheid is 1.

In samenhang met het maken van één kwaliteitsorder voor elk van de drie kwaliteitskoppelingen worden ook bemonsteringswerkzaamheden voor kwaliteitsartikelen gemaakt. De geregistreerde hoeveelheid is slechts 10. Vanwege de artikelbemonsteringsinstellingen zijn er in totaal 16 kwaliteitsorders die zijn gemaakt voor het toepasselijke magazijntype voor *Alleen kwaliteitsbeheer voor magazijnprocessen*, wat de fysieke geregistreerde hoeveelheid van 10 overschrijdt. Daarom wordt er geen werk gemaakt voor de volledige hoeveelheid van kwaliteitsorders (16), omdat slechts 10 fysiek beschikbaar zijn voor verplaatsing naar de kwaliteitscontrolelocatie. De prioriteit die wordt gebruikt voor het maken van bemonsteringswerk van kwaliteitsartikelen volgt de volgorde van het maken van kwaliteitsorders:

- **Eerste kwaliteitsorder (hoeveelheid = 5):** bemonsteringswerkzaamheden van kwaliteitsartikel worden gemaakt voor 5. Er blijft nu een hoeveelheid van 5 (10 – 5) over om verdere bemonsteringswerkzaamheden te maken voor kwaliteitsartikelen.
- **Tweede kwaliteitsorder (hoeveelheid = 10):** bemonsteringswerkzaamheden van kwaliteitsartikel worden gemaakt voor 5. Er blijft nu een hoeveelheid van 0 over om verdere bemonsteringswerkzaamheden te maken voor kwaliteitsartikelen.
- **Derde kwaliteitsorder (hoeveelheid = 1):** er worden geen bemonsteringswerkzaamheden gemaakt.

Als onderdeel van het proces voor het maken van de kwaliteitsorders wordt een voorraadblokkering van een hoeveelheid van 10 gemaakt. Er wordt naar deze voorraadblokkering verwezen voor elk van de drie kwaliteitsorders. De som van de hoeveelheid kwaliteitsorders is 16.

Wanneer de kwaliteitsorders worden gevalideerd, wordt geprobeerd om werk voor kwaliteitsorders te maken voor elke gevalideerde kwaliteits. Omdat de som van de hoeveelheid kwaliteitsorders hoger is dan de hoeveelheid die daadwerkelijk is geblokkeerd en dus beschikbaar is voor het maken van werk, kan er geen kwaliteitsorder worden gemaakt voor de volledige hoeveelheid kwaliteitsorders, zoals hier wordt weergegeven. (In dit voorbeeld wordt het vorige voorbeeld in dit onderwerp voortgezet.)

1. **Valideer de tweede kwaliteitsorder die wordt gemaakt (hoeveelheid = 10). Het werk voor de kwaliteitsorder wordt gemaakt voor een hoeveelheid van 4.**

    Het maken van werkzaamheden voor kwaliteitsorders wordt geactiveerd door een wijziging in de voorraadblokkeringshoeveelheid. Omdat de som van de kwaliteitsorder is ingesteld op 16, zal de validatie van 10 stuks ertoe leiden dat er 6 kwaliteitsorders overblijven om te worden gevalideerd. De voorraadblokkeringshoeveelheid wordt verlaagd van 10 naar 6. De gereduceerde hoeveelheid van 4 wordt toegewezen voor het maken van werk voor kwaliteitsorders.

2. **Valideer de eerste kwaliteitsorder die wordt gemaakt (hoeveelheid = 5). Het werk voor de kwaliteitsorder wordt gemaakt voor een hoeveelheid van 5.**

    Het maken van werkzaamheden voor kwaliteitsorders wordt geactiveerd door een wijziging in de voorraadblokkeringshoeveelheid. Omdat de som van de kwaliteitsorder is ingesteld op 6, zal de validatie van 5 stuks ertoe leiden dat er 1 kwaliteitsorders overblijven om te worden gevalideerd. De voorraadblokkeringshoeveelheid wordt verlaagd van 6 naar 1. De gereduceerde hoeveelheid van 5 wordt toegewezen voor het maken van werk voor kwaliteitsorders.

3. **Valideer de derde kwaliteitsorder die wordt gemaakt (hoeveelheid = 1). Het werk voor de kwaliteitsorder wordt gemaakt voor een hoeveelheid van 1.**

    Het maken van werkzaamheden voor kwaliteitsorders wordt geactiveerd door een wijziging in de voorraadblokkeringshoeveelheid. Omdat de som van de kwaliteitsorder is ingesteld op 1, zal de validatie van 1 stuks ertoe leiden dat er 0 (nul) kwaliteitsorders overblijven om te worden gevalideerd. De voorraadblokkering wordt verwijderd (dat wil zeggen dat de voorraadblokkeringshoeveelheid wordt verminderd van 1 naar 0). De gereduceerde hoeveelheid van 1 wordt toegewezen voor het maken van werk voor kwaliteitsorders.

> [!NOTE]
> Het maken van werk voor kwaliteitsorders is afhankelijk van de voorraadblokkeringshoeveelheid waarnaar wordt verwezen in één of meer kwaliteitsorders. Als de som van de hoeveelheden van de kwaliteitsorder groter is dan de hoeveelheid van de voorraadblokkering waarnaar wordt verwezen, bepaalt de volgorde waarin de kwaliteitsorders worden gevalideerd, hoe werk voor de kwaliteitsorder wordt gemaakt.

## <a name="canceling-quality-item-sampling-work"></a>Bemonsteringswerk van kwaliteitsartikel annuleren

U kunt het werk annuleren dat wordt gemaakt voor de bemonstering van kwaliteitsartikelen. Voer de volgende stappen uit om te bepalen wat er gebeurt wanneer dit werk wordt geannuleerd.

1. Ga naar **Magazijnbeheer \> Instellingen \> Parameters voor magazijnbeheer**.
1. Stel op het tabblad **Algemeen**, op het sneltabblad **Werk** de optie **Ontvangstbewijs ongedaan maken bij annuleren van werk** in op een van de volgende waarden:

    - **Ja**: wanneer bemonsteringswerk voor het kwaliteitsartikel wordt geannuleerd, wordt de bijbehorende kwaliteitsorder verwijderd en wordt de voorraad niet geregistreerd.
    - **Nee**: wanneer bemonsteringswerk voor het kwaliteitsartikel wordt geannuleerd, wordt de bijbehorende kwaliteitsorder niet verwijderd en blijft de voorraad geregistreerd.

## <a name="cross-docking"></a>Cross-docken

U kunt instellingen voor kwaliteitskoppelingen hebben waarmee werkzaamheden voor artikelbemonstering worden gemaakt. Wanneer er echter sprake is van cross-docken naast een kwaliteitskoppeling waarmee bemonsteringswerk voor kwaliteitsartikelen wordt gemaakt, kunnen de bemonsteringswerkzaamheden alleen worden gemaakt als er voldoende hoeveelheid is voor cross-docken. In gevallen waarbij de optie **Kwaliteitsorder inschakelen voor magazijnprocessen** is ingesteld op _Ja_ voor het ontvangende magazijn en het veld **Toepasselijk magazijntype** is ingesteld op _Alleen kwaliteitsbeheer voor magazijnprocessen_ voor een kwaliteitskoppeling, heeft het maken van bemonsteringswerkzaamheden voor kwaliteitsartikelen voorrang boven werk voor cross-docken. Ook als de hoeveelheid de behoefte voor cross-docken overschrijdt, worden alleen artikelbemonsteringswerkzaamheden gemaakt.

## <a name="destructive-testing"></a>Destructieve testen

U kunt een testgroep definiëren die destructieve tests uitvoert. In het geval van een destructieve test is de veronderstelling dat de hoeveelheid van het geteste artikel wordt vernietigd als onderdeel van de test, ongeacht het testresultaat. De manier waarop de functie _Kwaliteitsbeheer voor magazijnprocessen_ destructieve testen ondersteunt, lijkt op de manier waarop kwaliteitsbeheer deze ondersteunt wanneer de functie niet is ingeschakeld. Voordat de kwaliteitsorder kan worden gevalideerd, moet de kwaliteitscontroleur de orderverzamellocatie opgeven voor de hoeveelheid die is vernietigd. U kunt orderverzamelen registreren op de pagina Kwaliteitsorder door **Voorraadpick \> Orderverzamelen** te selecteren in het actievenster. Nadat de orderverzameling voor de kwaliteitsorder is geregistreerd, kan de validatie worden voltooid.

## <a name="example-scenario"></a>Voorbeeldscenario

### <a name="prepare-the-scenario"></a>Het scenario voorbereiden

Om dit scenario te kunnen gebruiken, moet u het systeem op de volgende manier voorbereiden:

- Controleer of de demogegevens op het systeem zijn geïnstalleerd en selecteer de rechtspersoon **USMF**.
- Schakel de functie _Kwaliteitsbeheer voor magazijnprocessen inschakelen_ in bij [Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).
- Configureer magazijn 51 om de functie _Kwaliteitsbeheer voor magazijnprocessen_ te gebruiken door de volgende stappen uit te voeren:

    1. Ga naar **Magazijnbeheer \> Instellen \> Magazijn \> Magazijnen**.
    1. Selecteer magazijn 51.
    1. Stel op het sneltabblad **Magazijn** de optie **Kwaliteitsorder inschakelen voor magazijnprocessen** in op *Ja*.

### <a name="quality-in-setup--move-to-the-quality-control-location"></a>Instellingen kwaliteit in: verplaatsen naar de locatie van de kwaliteitscontrole

U moet nu een basisinstelling voorbereiden die ervoor zorgt dat uw systeem de functie _Kwaliteitsbeheer voor magazijnprocessen_ ondersteunt voor magazijn 51. (De demogegevens gebruiken een kwaliteitsbeheerlocatie met de naam *QMS*. In dit scenario wordt naar deze locatie meermaals verwezen.) U gaat de volgende elementen voorbereiden, zoals is beschreven in de subsecties van deze sectie:

- Werkklasse
- Werksjabloon
- Locatierichtlijnen
- Artikelbemonstering
- Kwaliteitskoppeling
- Menuopties voor mobiel apparaat

#### <a name="work-class-for-quality-in"></a>Werkklasse voor kwaliteit-in

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.
1. Maak een werkklasse en stel de volgende waarden in:

    - **Werkklasse-id:** _QualityIn_
    - **Omschrijving:** _Bemonstering kwaliteitsartikel_
    - **Werkplaatstype:** _Bemonstering kwaliteitsartikel_

#### <a name="work-template"></a>Werksjabloon

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Stel het veld **Werkordertype** in op _Bemonstering kwaliteitsartikel_.
1. Maak een werksjabloon en stel de volgende waarden in:

    - **Werksjabloon:** _51 kwaliteit_
    - **Omschrijving werksjabloon:** _51 kwaliteit_

1. Voeg een regel toe aan de werksjabloon en stel de volgende waarden in:

    - **Werktype:** _Orderverzamelen_
    - **Werkklasse-id:** _QualityIn_

1. Voeg een tweede regel toe aan de werksjabloon en stel de volgende waarden in:

    - **Werktype:** _Wegzetten_
    - **Werkklasse-id:** _QualityIn_

#### <a name="location-directive"></a>Locatierichtlijnen

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Stel het veld **Werkordertype** in op _Bemonstering kwaliteitsartikel_.
1. Maak een locatierichtlijn en stel de volgende waarden in:

    - **Naam:** _51 naar kwaliteit_
    - **Werktype:** _Wegzetten_
    - **Locatie:** 5
    - **Magazijn:** _51_

1. Voeg een regel toe aan de locatierichtlijn en stel de volgende waarden in:

    - **Vanaf hoeveelheid:** _1_
    - **Tot hoeveelheid:** _1000000_

1. Maak een actie voor de locatierichtlijn en stel de volgende waarde in:

    - **Naam:** _Kwaliteit_

1. Selecteer voor de nieuwe actie van de locatierichtlijn **Query bewerken** en geeft u een record met het volgende **bereik** op:

    - **Tabel:** *Locaties*
    - **Veld:** _Locatieprofiel-id_
    - **Criteria:** *QMS*

1. Selecteer **OK** om de query op te slaan en sla de nieuwe locatierichtlijn op.

Vervolgens moet u de volgorde van de bestaande locatierichtlijnen voor de inkooporder voor magazijn 51 wijzigen. De demogegevens bevatten twee locatierichtlijnen met voor **Werkordertype** de waarde _Inkoop_: de ene heet _51 QMS_ en de tweede _51 PO Direct_. Als u de functie *Kwaliteitsbeheer voor magazijnprocessen* wilt toepassen voor magazijn 51, moet u ervoor zorgen dat de locatierichtlijn _51 QMS_ niet wordt toegepast. In plaats van de locatierichtlijn te verwijderen (omdat u deze echter in de toekomst zou willen gebruiken), hoeft u alleen de volgorde te wijzigen.

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Stel het veld **Werkordertype** in op _Inkooporder_.
1. Selecteer volgnummer 5 in de volgordelijst voor de locatierichtlijn _51 PO Direct_.
1. Verplaats het geselecteerde volgnummer naar boven naar volgnummer 4.
1. Controleer of het volgnummer van de locatierichtlijn _51 QMS_ nu ten minste 5 is.

#### <a name="item-sampling"></a>Artikelbemonstering

Met de functie _Kwaliteitsbeheer voor magazijnprocessen_ worden enkele nieuwe voorzieningen voor artikelbemonstering toegevoegd. De waarde van voor **Bemonsteringsbereik** kan nu _Order_, _Zending_ of _Lading_ zijn en de waarde voor de **Bemonsteringshoeveelheid** kan nu _Volledige nummerplaat_ zijn.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Artikelbemonstering**.
1. Maak een artikelbemonsteringsrecord en stel de volgende waarden in:

    - **Artikelbemonstering:** _3de LP_
    - **Beschrijving:** _Elke derde nummerplaat_
    - **Bemonsteringsbereik:** _Order_

1. Stel op het sneltabblad **Bemonsteringshoeveelheid** het veld **Hoeveelheidsspecificatie** in op _Volledige nummerplaat_.
1. Stel op het sneltabblad **Proces** het veld **Per nde nummerplaat** in op _3_.
1. Schakel in de sectie **Per opslagdimensie** zowel **Magazijn** als **Voorraadstatus** in.

#### <a name="quality-associations"></a>Kwaliteitskoppelingen

Maak een kwaliteitskoppeling voor de nieuwe artikelbemonstering.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitsbeheer \> Kwaliteitskoppelingen**.
1. Maak een record voor de kwaliteitskoppeling en stel de volgende waarden in:

    - **Verwijzingstype:** _Inkoop_
    - **Artikelcode:** _Tabel_
    - **Artikel:** _M9201_
    - **Locatie:** _5_

1. Stel op het sneltabblad **Proces** het veld **Gebeurtenistype** in op *Registratie*.
1. Stel op het sneltabblad **Voorwaarden** het veld **Toepasselijk magazijntype** in op *Alleen kwaliteitsbeheer voor magazijnprocessen*.
1. Stel op het sneltabblad **Kwaliteitsorderproces** het veld **Kwaliteitsverwerkingsbeleid** in op _Kwaliteitsorder maken_.
1. Klik met de rechtermuisknop in het veld **Testgroep** op het sneltabblad **Specificaties** en selecteer vervolgens **Details weergeven** om de pagina **Testgroepen** te openen.
1. Maak op de pagina **Testgroepen** op het tabblad **Overzicht** van het bovenste raster een testgroep en stel de volgende waarden in:

    - **Testgroep:** _QMS_
    - **Omschrijving:** _QMS test_
    - **Aanvaardbare hoeveelheid:** _100_
    - **Artikelbemonstering:** _3de LP_ (selecteren)

1. Voeg op het tabblad **Overzicht** van het onderste raster een record toe voor één test en stel de volgende waarden in:

    - **Reeks:** *1*
    - **Test:** *Behuizing meten*

1. Stel op het tabblad **Testen** van het onderste raster de volgende waarden in:

    - **Testvariabelen:** *Goedgekeurd/Afgekeurd*
    - **Standaardresultaat:** *Goedgekeurd*

1. Sla de nieuwe testgroep op en sluit de pagina **Testgroepen**.
1. Ga terug naar de pagina **Kwaliteitskoppelingen** en selecteer in het veld **Testgroep** **QMS**.
1. Sla de record op.

#### <a name="mobile-device-menu-items-for-quality-in"></a>Menuopdrachten van mobiel apparaat voor kwaliteit-in

Als u de instellingen voor het verplaatsen van goederen naar de kwaliteitscontrolelocatie wilt voltooien, moet u de bemonsteringstaken voor kwaliteitsartikelen beschikbaar maken via een menuopdracht op mobiele apparaten.

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer de menuopdracht **Opslag van inkoop** op het mobiele apparaat.
1. Voeg op het sneltabblad **Werkklassen** de werkklasse-id *QualityIn* toe.

#### <a name="summary-your-setup-to-move-goods-to-quality-control"></a>Samenvatting: de instellingen voor het verplaatsen van goederen naar kwaliteitscontrole

U hebt nu een kwaliteitskoppeling gedefinieerd die de functie *Kwaliteitsbeheer voor magazijnprocessen* gebruikt om het maken van kwaliteitsorders te activeren. U hebt de werk- en locatiegegevens voor magazijn 51 ingesteld om ervoor te zorgen dat specifieke taken worden gemaakt wanneer een inkoopregistratie wordt uitgevoerd voor artikel M9201. Deze instelling zorgt ervoor dat elke derde nummerplaat die wordt geregistreerd, wordt verplaatst naar een kwaliteitslocatie (_QMS_) en dat er een kwaliteitsorder wordt gemaakt voor de hoeveelheid van de nummerplaat. Alle overige artikelen worden verplaatst naar de opslaglocatie in plaats van de kwaliteitscontrolelocatie.

### <a name="process-quality-management-work"></a>Taken voor kwaliteitsbeheer verwerken

1. Ga naar **Inkoop en sourcing \> Inkooporders \> Alle inkooporders**.
1. Maak een inkooporder en stel de volgende waarden in:

    - **Geef een leveranciersrekening op:** *104*
    - **Magazijn:** *51*

1. Voeg een inkooporderregel toe en stel de volgende waarden in:

    - **Artikel:** *M9201*
    - **Hoeveelheid:** *20*
    - **Maateenheid:** *EA*
    - **Magazijn:** *51*

1. Noteer het nummer van de inkooporder, zodat u het later kunt gebruiken.
1. Ga naar een mobiel apparaat of emulator waarin de mobiele app Magazijnbeheer wordt uitgevoerd en meld u aan bij magazijn 51 met *51* als gebruikers-id en *1* als wachtwoord.
1. Ga naar **Inkomend \> Inkoop ontvangen** en voer de volgende waarden in:

    - **Inkoopordernummer:** het nummer van de inkooporder die u zojuist hebt gemaakt
    - **Hoeveelheid:** *5*
    - **Eenheid:** *EA*

1. Totdat de regel volledig is ontvangen, blijft u ontvangen op basis van de regel, met *5 EA* tegelijk. (In totaal worden vier nummerplaten gemaakt.)
1. Meld u af bij de mobiele app Magazijnbeheer.
1. Ga in de webclient naar **Inkoopbeheer \> Inkooporders \> Alle inkooporders**.
1. Zoek uw inkooporder en open deze.
1. Selecteer in de sectie **Inkooporderregels** de regel voor artikelnummer *M9201* en selecteer vervolgens **Inkooporderregels \> Werkgegevens**.
1. De tweede en derde werkkopteksten zijn normale opslagtaken, terwijl de eerste en de vierde werkkopteksten de bemonsteringswerkzaamheden van het kwaliteitsartikel zijn. Dit resultaat is consistent met de instellingen voor artikelbemonstering, die zo zijn geconfigureerd dat ze van elke derde nummerplaat een monster nemen.

#### <a name="move-to-the-quality-control-location"></a>Verplaatsen naar de kwaliteitscontrolelocatie

U gaat de nummerplaten nu naar de aangegeven locaties verplaatsen. De eerste en vierde nummerplaat gaan naar de kwaliteitscontrolelocatie, terwijl de tweede en derde nummerplaten rechtstreeks naar de opslag gaan.

1. Ga naar een mobiel apparaat of emulator waarin de mobiele app Magazijnbeheer wordt uitgevoerd en meld u aan bij magazijn 51 met *51* als gebruikers-id en *1* als wachtwoord.
1. Ga naar **Inkomend \> Opslag van inkoop** en sla elke nummerplaat uit de vorige procedure op totdat u alle werkzaamheden hebt afgesloten.

#### <a name="summary-process-quality-management-work"></a>Samenvatting: Taken voor kwaliteitsbeheer verwerken

U hebt nu de bemonsteringswerkzaamheden voor kwaliteitsartikelen uitgevoerd voor de eerste en vierde nummerplaat door ze naar de kwaliteitscontrolelocatie te verplaatsen. U hebt ook de tweede en derde nummerplaat opgeslagen. De volgende stap is het testen en controleren van de kwaliteitsorder.

### <a name="quality-out-setup-move-from-the-quality-control-location-to-storage-or-return"></a>Instellingen Kwaliteit-uit: van de kwaliteitsbeheerlocatie naar opslag of retourneren

Wanneer werknemers kwaliteitsorderresultaten rapporteren, worden automatisch taken gegenereerd.

U gaat nu door gaan met de vereiste basisinstellingen van de werkklasse, de werksjabloon en de locatierichtlijn om kwaliteitsbeheer in te schakelen voor magazijnprocessen, zodat het vereiste werk kan worden gemaakt om de hoeveelheid van de kwaliteitsorder te verplaatsen van de kwaliteitscontrolelocatie naar een aangewezen magazijnlocatie.

#### <a name="work-class-for-quality-out"></a>Werkklasse voor kwaliteit-uit

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werkklassen**.
1. Maak een werkklasse en stel de volgende waarden in:

    - **Werkklasse-id:** *QualityOut*
    - **Omschrijving:** *Kwaliteit uit*
    - **Werkordertype:** *Kwaliteitsorder*

#### <a name="work-templates"></a>Werksjablonen

1. Ga naar **Magazijnbeheer \> Instellen \> Werk \> Werksjablonen**.
1. Wijzig de waarde **Werkordertype** in *Kwaliteitsorder*.
1. Maak een werksjabloon en stel de volgende waarden in:

    - **Werksjabloon:** *51 kwaliteit-uit*
    - **Omschrijving werksjabloon:** *51 kwaliteit-uit*

1. Voeg een regel toe en stel de volgende waarden in:

    - **Werktype:** *Orderverzamelen*
    - **Werkklasse-id:** **QualityOut**

1. Voeg een tweede regel toe en stel de volgende waarden in:

    - **Werktype:** *Wegzetten*
    - **Werkklasse-id:** *QualityOut*

#### <a name="location-directives"></a>Instructielocatie

1. Ga naar **Magazijnbeheer \> Instellen \> Locatierichtlijnen**.
1. Wijzig de waarde **Werkordertype** in *Kwaliteitsorder*.
1. Maak een locatierichtlijn en stel de volgende waarden in:

    - **Naam:** *51 geslaagd*
    - **Werktype:** *Wegzetten*
    - **Locatie:** *5*
    - **Magazijn:** *51*

1. Selecteer in het actievenster de optie **Query bewerken** het dialoogvenster Query-editor te openen.
1. Stel op het tabblad **Bereik** de volgende waarden in:

    - **Tabel:** *Kwaliteitsorders*
    - **Veld:** *Status*
    - **Criteria:** *Geslaagd*

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Voeg op het sneltabblad **Regel** een regel toe en stel de volgende waarden in:

    - **Vanaf hoeveelheid:** *1*
    - **Tot hoeveelheid:** *1000000*

1. Voeg op het sneltabblad **Acties locatierichtlijn** een rij toe en stel de volgende waarde in:

    - **Naam:** *Geslaagd*

1. Selecteer in het sneltabblad **Acties locatierichtlijn** de optie **Query bewerken** om het dialoogvenster Query-editor te openen.
1. Stel op het tabblad **Bereik** de volgende waarden in:

    - **Tabel:** *Locaties*
    - **Veld:** *Zone-id*
    - **Criteria:** *Bulk*

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Selecteer in het actievenster **Opslaan** om de nieuwe locatierichtlijn op te slaan.
1. Maak een tweede locatierichtlijn en stel de volgende waarden in:

    - **Naam:** *51 mislukt*
    - **Werktype:** *Wegzetten*
    - **Locatie:** *5*
    - **Magazijn:** *51*

1. Selecteer in het actievenster de optie **Query bewerken** het dialoogvenster Query-editor te openen.
1. Stel op het tabblad **Bereik** de volgende waarden in:

    - **Tabel:** *Kwaliteitsorders*
    - **Veld:** *Status*
    - **Criteria:** *Mislukt*

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Voeg op het sneltabblad **Regel** een regel toe en stel de volgende waarden in:

    - **Vanaf hoeveelheid:** *1*
    - **Tot hoeveelheid:** *1000000*

1. Voeg op het sneltabblad **Acties locatierichtlijn** een rij toe en stel de volgende waarde in:

    - **Naam:** *Mislukt*

1. Selecteer in het sneltabblad **Acties locatierichtlijn** de optie **Query bewerken** om het dialoogvenster Query-editor te openen.
1. Stel op het tabblad **Bereik** de volgende waarden in:

    - **Tabel:** *Locaties*
    - **Veld:** *Zone-id*
    - **Criteria:** *Retourneren*

1. Selecteer **OK** om de query op te slaan en het dialoogvenster te sluiten.
1. Selecteer in het actievenster **Opslaan** om de nieuwe locatierichtlijn op te slaan.

#### <a name="mobile-device-menu-items-for-quality-out"></a>Menuopdrachten van mobiel apparaat voor kwaliteit-uit

1. Ga naar **Magazijnbeheer \> Instellen \> Mobiel apparaat \> Menuopties voor mobiel apparaat**.
1. Selecteer de menuopdracht **QMS wegzetten** op het mobiele apparaat.
1. Voeg op het sneltabblad **Werkklassen** de werkklasse-id *QualityPut* toe.

Magazijnmedewerkers kunnen nu een kwaliteitsorder selecteren met de menuopdracht **QMS wegzetten**. Goederen waarvoor de kwaliteitscontrole is mislukt, kunnen op een retourlocatie worden geplaatst en goederen die zijn geslaagd, kunnen op de locatie voor bulk-001 worden geplaatst.

#### <a name="summary-your-setup-to-move-goods-from-quality-control"></a>Samenvatting: de instellingen voor het verplaatsen van goederen uit kwaliteitscontrole

U hebt de werk- en locatiegegevens voor magazijn 51 ingesteld om ervoor te zorgen dat taken automatisch worden gemaakt wanneer kwaliteitsorders zijn uitgevoerd. Deze instelling zorgt ervoor dat elke nummerplaat na kwaliteitscontrole wordt verplaatst naar een bulklocatie of een retourlocatie.

### <a name="process-quality-management-work"></a>Taken voor kwaliteitsbeheer verwerken

1. Ga naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.
1. Selecteer de eerste kwaliteitsorder voor de geregistreerde hoeveelheden.
1. Selecteer **Valideren**. De status van de test wordt bijgewerkt in *Mislukt*.
1. Ga naar **Magazijnbeheer \> Alle werkzaamheden**.
1. Open de taak die u zojuist hebt gemaakt en u ziet dat de waarde van **Werkordertype** nu *Kwaliteitsorder* is. Het werk bevat een regel met de wegzetlocatie *Retour* en de status *Mislukt*. (Als de status van de kwaliteitsorder *Geslaagd* is, zou de wegzetlocatie in plaats daarvan *Bulk* zijn.)
1. Ga terug naar **Voorraadbeheer \> Periodieke taken \> Kwaliteitsbeheer \> Kwaliteitsorders**.
1. Selecteer de tweede kwaliteitsorder voor de geregistreerde artikelen.
1. Selecteer **Resultaten** boven het onderste raster. Werk de waarde van **Resultaathoeveelheid** bij naar *5* en controleer of de waarde voor **Testresultaat** wordt gewijzigd in een vinkje.
1. Selecteer **Valideren** en sluit de pagina.
1. Selecteer op de pagina **Kwaliteitsorders** **Valideren** en voer de validatie uit. De status wordt bijgewerkt naar *Geslaagd*.

    > [!NOTE]
    > De validatiegebeurtenis activeert het maken van kwaliteitsordertaken om de hoeveelheid van de kwaliteitscontrolelocatie naar een nieuwe locatie te verplaatsen.

1. Ga naar **Magazijnbeheer \> Alle werkzaamheden**.
1. Selecteer de taak die net is gemaakt en u zet dat er een tweede kwaliteitsorder is gemaakt, waarbij de opslaglocatie *BULK-001* is.
1. Ga naar een mobiel apparaat of emulator waarin de mobiele app Magazijnbeheer wordt uitgevoerd en meld u aan bij magazijn 51 met *51* als gebruikers-id en *1* als wachtwoord.
1. Ga naar **Kwaliteit \> Opgeslagen uit QMS** en verwerk beide nummerplaten die aan de beide werkzaamheden zijn gekoppeld, zodat ze worden gesloten.

> [!NOTE]
> Mogelijk wilt u de kwaliteit-uit vermelding toevoegen aan een menuopdracht voor het mobiele apparaat met de activiteitscode *Openstaande werklijst weergeven*. Zie de menuopdracht van het mobiele apparaat met de naam **Werklijst** in de demogegevens voor een voorbeeld. Voeg eerst de productklasse *Kwaliteitsorder* toe aan een gebruikersspecifieke menuopdracht, omdat deze werkklasse is vereist voor het weergeven van werk in de werklijst. Voeg vervolgens de werkklasse *Kwaliteitsorder* toe aan de menuopdracht **Werklijst**. Gebruikers die toegang hebben tot de werklijst, kunnen vervolgens het werk dat automatisch wordt gegenereerd door het valideren van de kwaliteitsorder, verzamelen en verwerken.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van het beheer van kwaliteit en niet-conformeringen](quality-management-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]