---
title: Kredietblokkeringen voor verkooporders
description: In dit onderwerp wordt beschreven hoe u regels instelt om een kredietblokkering voor een verkooporder op te geven.
author: mikefalkner
manager: AnnBe
ms.date: 01/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 102ea4285407a4f4985cc8dd46ebc1ad21fc6f67
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2020
ms.locfileid: "3977906"
---
# <a name="credit-holds-for-sales-orders"></a>Kredietblokkeringen voor verkooporders
[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u regels instelt om een kredietblokkering voor een verkooporder op te geven. De blokkeringsregels voor kredietbeheer kunnen van toepassing zijn op een individuele klant of op een groep klanten. Blokkeringsregels definiëren reacties op de volgende omstandigheden:

1. Aantal dagen achterstallig
2. Status van rekening
3. Betalingstermijnen
4. Kredietlimiet verlopen
5. Achterstallig bedrag
6. Verkooporderbedrag
7. Gebruikt gedeelte van beschikbaar krediet

Bovendien zijn er twee parameters waarmee u extra scenario's voor het blokkeren van een verkooporder kunt beheren

1. Wijziging in betalingsvoorwaarden
2. Wijziging in vereffeningskortingen

## <a name="set-up-blocking-rules-and-exclusion-rules"></a>Blokkeringsregels en uitsluitingsregels instellen

Wanneer een klant een verkooptransactie initieert, wordt de informatie op de verkooporder gecontroleerd aan de hand van een set blokkeringsregels waarmee wordt bepaald of krediet aan de klant moet worden verleend en of de verkoop doorgang kan vinden. U kunt ook uitsluitingen definiëren die de blokkeringsregels vervangen en toestaan dat een verkooporder wordt verwerkt. U kunt blokkeringsregels en uitsluitingsregels instellen op de pagina **Kredietbeheer > Instellen > Kredietbeheer instellen > Blokkeringsregels**.

### <a name="days-overdue"></a>Dagen achterstallig

Open het tabblad **Dagen achterstallig** als de blokkeringsregel van toepassing is op de klant met een of meer facturen die gedurende een bepaald aantal dagen achterstallig zijn.
1. Selecteer bij **Geldig voor** het bereik klanten voor wie deze regel geldig is.
   - Selecteer **Tabel** als de regel van toepassing is op een specifieke klant.
   - Selecteer **Groep** als de regel wordt toegepast op het niveau van de klantengroep. 
   - Selecteer **Alle** als de regel van toepassing is op alle klanten.
2. Wanneer u het bereik hebt opgegeven, moet u de **Rekening/groep** opgeven die in het bereik moet worden gebruikt.
   - De zoekfunctie geeft voor het bereik **Tabel** een lijst met klanten die u kunt selecteren. 
   - Selecteer een **Groep** als de regel van toepassing is op een klantkredietgroep.
   - Selecteer **Alle** als de regel van toepassing is op alle klanten. 
3. Selecteer **Risicogroep** om criteria te gebruiken voor het toepassen van een kredietbeheerblokkering op klanten die zijn gegroepeerd met een gemeenschappelijke set factoren, zoals hun Dun and Bradstreet-classificatie, het aantal jaren dat ze in bedrijf zijn, hoe lang ze uw klant zijn, enzovoort.  
4. Selecteer het type regel dat u instelt. Met de optie **Blokkering** wordt een regel gemaakt waarmee een order wordt geblokkeerd. Met de optie **Uitsluiting** wordt een regel gemaakt waarmee een andere regel wordt uitgesloten van het blokkeren van een order. 
5. Selecteer een **Waardetype**. De standaardwaarde is een vast aantal dagen. Als u een uitsluiting maakt, kunt u in plaats daarvan een vast aantal dagen of een bedrag opgeven. 
6. Voer het aantal dagen **Achterstallig** in dat wordt toegestaan voor de geselecteerde blokkeringsregel voordat een order een kredietbeheerblokkering krijgt ter beoordeling. Het aantal dagen achterstallig staat voor een extra aantal respijtdagen dat wordt opgeteld bij het aantal dagen na de vervaldatum die op een factuur kan staan voordat deze als achterstallig wordt beschouwd. Als u het **Waardetype** als een bedrag voor een uitsluiting hebt opgegeven, voert u een bedrag en een valuta voor dat bedrag in.

### <a name="accounts-status"></a>Status van rekening

Open het tabblad **Rekeningstatus** als de blokkeringsregel van toepassing is op een klant met de geselecteerde rekeningstatus.
1. Selecteer het type regel dat u instelt.  Met **Blokkering** maakt u een regel waarmee een order wordt geblokkeerd. Met **Uitsluiting** maakt u een regel waarmee een regel wordt uitgesloten van het blokkeren van een order. 
2. Selecteer de **Rekeningstatus** die ervoor zorgt dat de regel een verkooporder blokkeert of uitsluit.

### <a name="terms-of-payment"></a>Betalingstermijnen

Selecteer **Betalingsvoorwaarden** als de blokkeringsregel van toepassing is op de geselecteerde betalingsvoorwaarde.
1. Selecteer het type regel dat u instelt.  Met **Blokkering** maakt u een regel waarmee een order wordt geblokkeerd. Met **Uitsluiting** maakt u een regel waarmee een regel wordt uitgesloten van het blokkeren van een order. 
2. Selecteer de **Betalingsvoorwaarde** die ervoor zorgt dat de regel een verkooporder blokkeert of uitsluit.

### <a name="credit-limit-expired"></a>Kredietlimiet verlopen

Open het tabblad **Kredietlimiet verlopen** als de blokkeringsregel van toepassing is op klanten met vervallen kredietlimieten.
1. Selecteer bij **Geldig voor** het bereik klanten voor wie deze regel geldig is.
   - Selecteer **Tabel** als de regel van toepassing is op een specifieke klant.
   - Selecteer **Groep** als de regel wordt toegepast op het niveau van de klantgroep. 
   - Selecteer **Alle** als de regel van toepassing is op alle klanten.
2. Wanneer u het bereik hebt opgegeven, moet u de **Rekening/groep** opgeven die in het bereik wordt gebruikt.
   - De zoekfunctie geeft voor het bereik **Tabel** een lijst met klanten waaruit u kunt selecteren. 
   - Selecteer een **Groep** als de regel van toepassing is op een kredietbeheergroep.
   - Selecteer **Alle** als de regel van toepassing is op alle klanten. 
3. Selecteer een **Risicogroep** om de lijst met klanten die een kredietbeheerblokkering krijgen verder te beperken. 
4. Selecteer het type regel dat u instelt. 
   - Selecteer **Blokkering** om een regel te maken waarmee een order wordt geblokkeerd. 
   - Selecteer **Uitsluiting** om een regel te maken waarmee een andere regel wordt uitgesloten van het blokkeren van een order. 
5. Voer de **Dagen dat kredietlimiet verlopen is** voor de geselecteerde blokkeringsregel voordat een order een kredietbeheerblokkering krijgt. Het aantal dagen achterstallig staat voor extra respijtdagen die worden opgeteld bij het aantal dagen dat de kredietlimiet is vervallen.

### <a name="overdue-amount"></a>Achterstallig bedrag

Open het tabblad **Achterstallig bedrag** als de blokkeringsregel van toepassing is op klanten met achterstallige bedragen.
1. Selecteer bij **Geldig voor** het bereik klanten voor wie deze regel geldig is.
   - Selecteer **Tabel** als de regel van toepassing is op een specifieke klant.
   - Selecteer **Groep** als de regel wordt toegepast op het niveau van de klantgroep. 
   - Selecteer **Alle** als de regel van toepassing is op alle klanten.
2. Wanneer u het bereik hebt opgegeven, moet u de **Rekening/groep** opgeven die in het bereik wordt gebruikt.
   - De zoekfunctie geeft voor het bereik **Tabel** een zoekmogelijkheid voor klanten. 
   - Selecteer een **Groep** als de regel van toepassing is op een kredietbeheergroep.
   - Selecteer **Alle** als de regel van toepassing is op alle klanten. 
3. Selecteer een **Risicogroep** als u de lijst met klanten die een kredietbeheerblokkering krijgen verder wilt beperken. 
4. Selecteer het type regel dat u instelt. 
   - Selecteer **Blokkering** om een regel te maken waarmee een order wordt geblokkeerd. 
   - Selecteer **Uitsluiting** om een regel te maken waarmee een andere regel wordt uitgesloten van het blokkeren van een order. 
5. Voer **Achterstallig bedrag** in voor de geselecteerde blokkeringsregel voordat een order een kredietbeheerblokkering krijgt ter beoordeling. 
6. Selecteer het **Waardetype** waarmee wordt bepaald welk type waarde wordt gebruikt om ook te testen hoeveel van de kredietlimiet is gebruikt. Voor blokkeringsregels is een percentage vereist, maar een uitsluiting kan een vast bedrag of een percentage hebben. De drempel heeft betrekking op de kredietlimiet.
7. Voer de waarde voor **Drempel kredietlimiet** voor de geselecteerde regel in voordat voor een klant een kredietblokkering wordt ingesteld. Dit kan een bedrag zijn of een percentage dat is gebaseerd op het waardetype.
8. De regel controleert of het **Achterstallig bedrag** en de **Drempel voor kredietlimiet** zijn overschreden. 

### <a name="sales-order"></a>Verkooporder 

Selecteer **Verkooporder** als de blokkeringsregel van toepassing is op de waarde van de verkooporder.
1. Selecteer bij **Geldig voor** het bereik klanten voor wie deze regel geldig is.
   - Selecteer **Tabel** als de regel van toepassing is op een specifieke klant.
   - Selecteer **Groep** als de regel wordt toegepast op het niveau van de klantgroep. 
   - Selecteer **Alle** als de regel van toepassing is op alle klanten.
2. Wanneer u het bereik hebt opgegeven, moet u de **Rekening/groep** opgeven die in het bereik wordt gebruikt.
   - De zoekfunctie geeft voor het bereik **Tabel** een zoekmogelijkheid voor klanten. 
   - Selecteer een **Groep** als de regel van toepassing is op een kredietbeheergroep.
   - Selecteer **Alle** als de regel van toepassing is op alle klanten. 
3. Selecteer een **Risicogroep** als u de lijst met klanten die een kredietbeheerblokkering krijgen verder wilt beperken. 
4. Selecteer het type regel dat u instelt.  
   - Selecteer **Blokkering** om een regel te maken waarmee een order wordt geblokkeerd. 
   - Selecteer **Uitsluiting** om een regel te maken waarmee een andere regel wordt uitgesloten van het blokkeren van een order. 
5. Voer **Verkooporderbedrag** in voor de geselecteerde blokkeringsregel voordat een order een kredietbeheerblokkering krijgt. 

De verkooporderregel bevat een extra instelling waarmee alle andere regels worden vervangen. Als u een uitsluiting wilt maken waarmee de verkooporder wordt vrijgegeven zonder dat rekening wordt gehouden met andere regels, schakelt u het selectievakje **Verkooporder vrijgeven** op de uitsluitingsregel in.

### <a name="credit-limit-used"></a>Kredietlimiet gebruikt

Selecteer **Gebruikte kredietlimiet** als de blokkeringsregel van toepassing is op het gebruikte bedrag van de kredietlimiet van de klant.
1. Selecteer bij **Geldig voor** het bereik klanten voor wie deze regel geldig is.
   - Selecteer **Tabel** als de regel van toepassing is op een specifieke klant.
   - Selecteer **Groep** als de regel wordt toegepast op het niveau van de klantgroep. 
   - Selecteer **Alle** als de regel van toepassing is op alle klanten.
2. Wanneer u het bereik hebt opgegeven, moet u de **Rekening/groep** opgeven die in het bereik wordt gebruikt.
   - De zoekfunctie geeft voor het bereik **Tabel** een zoekmogelijkheid voor klanten. 
   - Selecteer een **Groep** als de regel van toepassing is op een kredietbeheergroep.
   - Selecteer **Alle** als de regel van toepassing is op alle klanten. 
3. Selecteer een **Risicogroep** als u de lijst met klanten die een kredietbeheerblokkering krijgen verder wilt beperken. 
4. Selecteer het type regel dat u instelt.
   - Selecteer **Blokkering** om een regel te maken waarmee een order wordt geblokkeerd. 
   - Selecteer **Uitsluiting** om een regel te maken waarmee een andere regel wordt uitgesloten van het blokkeren van een order. 
5. Selecteer de **Resterende drempel** die het percentage van de kredietlimiet definieert waarmee de verkooporder wordt geblokkeerd. Als de waarde van een order het bedrag van de gebruikte kredietlimiet tot boven het percentage verhoogt, wordt de order geblokkeerd. 

## <a name="put-a-sales-order-on-hold-based-on-other-criteria"></a>Een verkooporder blokkeren op basis van andere criteria
  
### <a name="rank-payment-terms"></a>Positie van betalingsvoorwaarden  

U kunt forceren dat de regels voor kredietcontrole worden uitgevoerd wanneer betalingsvoorwaarden gewijzigd zijn. U moet de betalingsvoorwaarden rangschikken en er een prioriteitswaarde aan toewijzen. Als u de betalingsvoorwaarden voor de order wijzigt in betalingsvoorwaarden die een hoger niveau hebben dan de oude betalingsvoorwaarden, wordt de order naar kredietbeheer verzonden voor goedkeuring.

U kunt de positie van de betalingsvoorwaarden instellen op de pagina **Kredietbeheer > Instellen > Kredietbeheer instellen > Betalingsvoorwaarden rangschikken**.

1. Selecteer te rangschikken betalingsvoorwaarden in het veld **Betalingsvoorwaarden**. Wanneer u een voorwaarde selecteert, wordt de omschrijving weergegeven in het veld **Beschrijving**.
2. Selecteer de rang van de voorwaarde in het veld **Rangschikken**. De waarden zijn allemaal relatief ten opzichte van elkaar, zodat u 1, 2, 3 of 10, 20, 30 kunt gebruiken. U kunt ook dezelfde waarde gebruiken voor de meeste betalingsvoorwaarden, zodat slechts één of twee betalingsvoorwaarden de kredietcontrole activeren.

### <a name="rank-settlement-discounts"></a>Positie van vereffeningskortingen   

U kunt forceren dat de regels voor kredietcontrole worden uitgevoerd wanneer vereffeningskortingen gewijzigd zijn. U moet de vereffeningskortingen rangschikken en er een prioriteitswaarde aan toewijzen. Als u de vereffeningskortingen voor de order wijzigt in vereffeningskortingen die een hoger niveau hebben dan de oude vereffeningskortingen, wordt de order naar kredietbeheer verzonden voor goedkeuring.

U kunt de positie van de betalingsvoorwaarden instellen op de pagina **Kredietbeheer > Instellen > Kredietbeheer instellen > Vereffeningskortingen rangschikken**.

1. Selecteer de **Contantkorting** die u wilt rangschikken. De **Beschrijving** van de vereffeningskorting wordt weergegeven.
2. Selecteer de waarde voor **Rangschikken**. De waarden zijn allemaal relatief ten opzichte van elkaar, zodat u 1, 2, 3 of 10, 20, 30 kunt gebruiken. U kunt ook dezelfde waarde gebruiken voor de meeste vereffeningskortingen, zodat slechts één of twee vereffeningskortingen de kredietcontrole activeren.

## <a name="sequence-the-application-of-rules"></a>Volgorde van toepassing van de regels

De regels worden in een bepaalde volgorde uitgevoerd. Deze kunt u wijzigen naar de behoeften van uw organisatie. 

- Met één voorbeeld van de uitsluitingsregels voor verkooporders kunt u alle regels vervangen die een verkooporder kunnen blokkeren. Maak een uitsluitingsregel voor een verkooporder en markeer de optie **Verkooporder vrijgeven**. De order wordt niet geblokkeerd als die uitsluitingsregel waar is en er worden geen andere regels gecontroleerd.
- Blokkeringsregels kunnen de order blokkeren.
- Uitsluitingsregels worden na blokkeringsregels uitgevoerd. Uitsluitingsregels hebben alleen invloed op de regel waarop ze zijn gedefinieerd. 
- Blokkerings- en uitsluitingsregels worden uitgevoerd in de volgorde Tabel, Groep en Alle. Vanwege deze bewerkingsvolgorde is het mogelijk op het niveau Alle een blokkeringsregel te hebben die niet wordt uitgevoerd omdat een uitsluitingsregel op het niveau Tabel of Groeps wordt uitgevoerd.
- Uitsluitingen vervangen de blokkeringsregel niet als deze op hetzelfde niveau staan. Een uitsluitingsregel op groepsniveau vervangt bijvoorbeeld de blokkeringsregel op groepsniveau niet. U hoeft geen uitsluitingen in te stellen op het niveau Alle, behalve zoals hierboven wordt beschreven, met het ene voorbeeld van de uitsluitingsregel voor verkooporders. 

Het gedrag van de regel **Gebruikte kredietlimiet** verandert op basis van de instellingen voor de parameter **Kredietlimiet voor verkooporder controleren**, die te vinden is op het parameterformulier Crediteringen en aanmaningen.
- Als de parameter is ingesteld op Nee, wordt de regel Gebruikte kredietlimiet niet uitgevoerd.
- Als de parameter is ingesteld op Ja en **Bericht bij overschrijding van kredietlimiet** is ingesteld op Waarschuwing, krijgt u een waarschuwing wanneer de kredietlimiet wordt overschreden. De regels voor **Gebruikte kredietlimiet** worden uitgevoerd om te zien of er regels zijn die u wilt uitvoeren. Voor dit scenario zou u echter normaal gesproken geen regels toevoegen.
- Als de parameter is ingesteld op Ja en **Bericht wanneer kredietlimiet wordt overschreden** is ingesteld op Fout, wordt de kredietlimiet gecontroleerd en wordt de order geblokkeerd als de kredietlimiet wordt overschreden. Daarnaast worden de regels voor **Gebruikte kredietlimiet** uitgevoerd om te zien of er nog meer regels zijn die moeten worden uitgevoerd. Er wordt geen foutbericht weer gegeven, maar de blokkeringsreden **Kredietlimiet overschreden** wordt weergegeven. 

## <a name="settings-that-will-change-the-way-an-order-is-placed-on-hold"></a>Instellingen die de manier waarop een order wordt geblokkeerd veranderen

Orders kunnen worden uitgesloten van kredietbeheer, zelfs als er regels gelden. 

- Als u de instellingen voor **Klant uitsluiten van kredietbeheer** bij **Alle klanten > Een klant selecteren > Sneltabblad Crediteringen en aanmaningen** wijzigt in **Ja**, worden voor de klant geen orders verwerkt
- Als u de waarde bij **Uitsluiten van kredietbeheer** in de **koptekst van verkooporders** op het **sneltabblad Kredietbeheer** wijzigt in **Ja**, worden de regels voor kredietbeheer niet verwerkt. Deze instelling kan alleen worden uitgevoerd door de kredietmedewerker of de kredietbeheerder.

## <a name="processing-orders-on-hold-using-the-credit-management-hold-list"></a>Geblokkeerde orders verwerken met behulp van de blokkeringslijst van kredietbeheer

Met de blokkeringslijst van kredietbeheer kunnen kredietbeheerders alle verkooporders weergeven die geblokkeerd zijn en kunnen ze de blokkeringen verwijderen wanneer de kredietproblemen zijn verminderd. Op de pagina **Blokkeringslijst kredietbeheer** worden alle verkooporders weergegeven die zijn geblokkeerd. U kunt de blokkeringslijst weergeven op de pagina **Alle kredietblokkeringen** (**Kredietbeheer > Blokkeringslijst kredietbeheer > Alle blokkeringen**).
Verkooporders van alle rechtspersonen worden verzonden naar dezelfde blokkeringslijst van kredietbeheer, zodat alle transacties die aandacht behoeven, in een centraal overzicht worden weergegeven. Gebruikers zien alleen de informatie voor de rechtspersonen die voor hen toegankelijk zijn.

Een verkooporder kan om de volgende redenen in de blokkeringslijst worden geplaatst:
1. De klant heeft een factuur die gedurende een opgegeven aantal dagen achterstallig is. 
2. De order heeft een specifieke rekeningstatus.
3. De order heeft specifieke betalingsvoorwaarden.
4. De klant heeft een verlopen kredietlimiet.
5. De klant heeft een achterstallig bedrag en heeft een opgegeven percentage van de kredietlimiet gebruikt
6. De verkooporder overschrijdt een bepaald bedrag.
7. De klant heeft een bepaald percentage van de kredietlimiet overschreden.
8. De betalingsvoorwaarden verschillen van de standaard betalingsvoorwaarden voor de klant.
9. De vereffeningskortingen verschillen van de standaard vereffeningskorting voor de klant.

De reden van blokkering wordt weergegeven voor elke verkooporder in de blokkeringslijst. Als er meerdere redenen zijn voor de blokkering, wordt de reden weergegeven als **Meerdere**. U kunt het menu **Blokkeringsredenen** in het actievenster gebruiken om alle redenen weer te geven waarom de verkooporder is geblokkeerd. U kunt de **Blokkeringsredenen** ook in een feitenvak weergeven.

### <a name="releasing-orders-from-the-hold-list-for-processing"></a>Orders uit de blokkeringslijst voor verwerking vrijgeven

Wanneer u de redenen voor de blokkering hebt onderzocht en u deze hebt verminderd, kunt u de verkooporders vrijgeven voor verdere verwerking.

1) Selecteer een regel in de blokkeringslijst. U kunt meerdere orders vrijgeven door meer dan één regel te selecteren.
2) Selecteer een **Reden voor vrijgave** voor de order die is geselecteerd voor vrijgave.  
3) Voer de **Controledatum** in voor elke order die is geselecteerd voor vrijgave.  
4) Selecteer het menu **Vrijgeven** in het actievenster om een order vrij te geven. Dit menu is pas beschikbaar nadat transacties zijn geselecteerd. De gebruiker krijgt twee opties:
   - Selecteer **Met boeking** als u de blokkering wilt verwijderen en het document wilt boeken met hetzelfde boekingsproces dat is gebruikt toen het werd geblokkeerd. Als de verkooporderbevestiging bijvoorbeeld is geblokkeerd, wordt de verkooporderbevestiging na vrijgave voltooid. Het formulier voor het boeken van verkooporders wordt weergegeven, zodat de gebruiker de bevestiging kan boeken.
   - Selecteer **Zonder boeking** om de blokkering op te heffen zonder verdere verwerking uit te voeren. De verkooporder kan handmatig worden geboekt.

### <a name="rejecting-orders-in-the-hold-list"></a>Orders in de blokkeringslijst afwijzen
U kunt het menu **Afwijzen** in het actievenster gebruiken om een verkooporder af te wijzen
1. Selecteer een regel in de blokkeringslijst. U kunt meerdere orders vrijgeven door meer dan één regel te selecteren.
2. De order wordt verwijderd uit de blokkeringslijst en de verkooporderkoptekst wordt bijgewerkt om aan te geven dat de order is afgewezen.

### <a name="automatically-releasing-credit-management-holds"></a>Kredietbeheerblokkeringen automatisch vrijgeven
Verkooporders worden in de blokkeringslijst geplaatst op basis van de blokkeringsregels. Sommige redenen voor de blokkeringen kunnen echter in de loop van de tijd veranderen als de verkooporder gedurende een bepaalde tijd in de blokkeringslijst blijft. Een klant kan bijvoorbeeld de factuur betalen, waardoor de kredietlimiet wordt vrijgemaakt. 

Met het menu **Evalueren voor vrijgave** kunt u de verkooporders in de blokkeringslijst bekijken en deze automatisch vrijgeven als de reden voor de blokkering is verminderd.
1.  Selecteer het menu **Evalueren voor vrijgave**
2.  Selecteer **Blokkeringsregels verwerken** om alle verkooporders te controleren. Selecteer **Blokkeringsregels voor geselecteerde regels verwerken** als u alleen de geselecteerde regels wilt controleren.
3. Er wordt een schuifregelaar weergegeven, zodat u één klant kunt selecteren. Laat de vervolgkeuzelijst voor klanten leeg voor alle klanten. 
4. Wanneer u op OK klikt, wordt het proces op de achtergrond uitgevoerd en kunt u verder werken aan andere taken. Als u batchverwerking selecteert voordat u op OK klikt, wordt het proces in batch uitgevoerd wanneer u op OK klikt. Het kan enige tijd duren om de geblokkeerde orders in de lijst te verwerken. Gebruik Vernieuwen om de status van de orders bij te werken. 
5.  Als een reden voor het blokkeren niet meer van toepassing is op een order, wordt de reden van de blokkering beschouwd als niet langer geldig. U ziet dan geen vinkje naast de reden wanneer u de reden van de blokkering bekijkt.
6.  Als alle blokkeringsredenen zijn uitgeschakeld, wordt een nieuwe reden, **Gereed voor vrijgave**, toegevoegd aan de lijst met redenen voor blokkering. De verkooporder kan automatisch worden vrijgegeven.
7.  Als de parameter **Automatisch vrijgeven** op het tabblad **Crediteringen en aanmaningen > Instellen > Parameters voor crediteringen en aanmaningen > Krediet > Automatisch vrijgeven** is ingesteld op **Met boeking**, wordt u gevraagd te boeken met behulp van het boekingsformulier voor het document dat is geblokkeerd.
8.  Als de parameter **Automatisch vrijgeven** op het tabblad **Crediteringen en aanmaningen > Instellen > Parameters voor crediteringen en aanmaningen > Krediet > Automatisch vrijgeven** is ingesteld op **Zonder boeking**, moet u de order handmatig boeken.

### <a name="credit-management-approval-workflow"></a>Workflow voor goedkeuring van kredietbeheer

U kunt ook **Workflows voor kredietbeheer** maken om de vrijgave van kredietblokkeringen te beheren. Wanneer u een workflow hebt ingesteld via de pagina **Kredietbeheer > Instellen > Workflows voor kredietbeheer**, worden de orders die zijn gemarkeerd voor vrijgave of afwijzing, verzonden naar de workflow waar ze eerst moeten worden goedgekeurd voordat ze worden vrijgegeven of afgewezen. 

Als u de taken voor vrijgave met of zonder boeking in de workflow opneemt, wordt de verkooporder ook vrijgegeven. Als er echter een storing optreedt in het vrijgaveproces vanwege ontbrekende instellingsgegevens of andere oorzaken, moet u de verkooporder intrekken uit de workflow, het probleem oplossen dat de fout heeft veroorzaakt en de order vervolgens opnieuw indienen bij de workflow.

Als u de taken voor vrijgave zonder boeking niet in uw workflow opneemt, kunt u de verkooporder eenvoudigweg vrijgeven wanneer de goedkeuring is voltooid.

### <a name="forced-credit-hold"></a>Geforceerde kredietblokkering  
  
Het kan zijn dat verkooporders soms moeten worden geblokkeerd, zelfs als de order niet voldoet aan de criteria van de blokkeringsregels. Een kredietbeheerder kan bijvoorbeeld worden geïnformeerd over een probleem met de klant dat niet over krediet gaat en besluiten orders handmatig te blokkeren totdat het probleem is opgelost. U kunt een verkooporder handmatig geforceerd blokkeren als die situatie zich voordoet.

1. Open de verkooporder die u wilt blokkeren.  
2. Selecteer **Geforceerde kredietblokkering** op het tabblad **Kredietbeheer** in het actievenster **Kredietbeheer**.
3. Selecteer een **Reden voor geforceerde blokkering**.
4. Klik op **OK**. De verkooporder wordt teruggestuurd naar de blokkeringslijst van kredietbeheer.

U kunt ook meerdere orders geforceerd blokkeren via de pagina **Kredietbeheer > Periodieke taken >Geforceerde kredietblokkering**. U kunt bijvoorbeeld alle verkooporders voor een bepaalde klant blokkeren.
1. Selecteer de **Reden voor geforceerde blokkering**. 
2. Klik op **Op te nemen records** om de verkooporders te selecteren die u wilt blokkeren. 
3. Klik op **OK** om de geselecteerde verkooporders te verwerken.

Verkooporders die geforceerd zijn geblokkeerd, kunnen niet met workflow worden verwerkt.

#### <a name="releasing-orders-that-were-added-to-the-credit-management-hold-list-with-a-forced-credit-hold"></a>Orders vrijgeven die aan de blokkeringslijst van kredietbeheer zijn toegevoegd met een geforceerde kredietblokkering
Verkooporders met een geforceerde blokkeringsreden kunnen niet automatisch worden vrijgegeven. Als de verkooporder geforceerd is geblokkeerd en u hebt een proces gebruikt waarmee verkooporders automatisch worden vrijgegeven, wordt de verkooporder weergegeven als **Gereed voor vrijgave** en blijft deze in de blokkeringslijst staan. U moet het menu **Vrijgeven** gebruiken om de order vrij te geven.
 
## <a name="free-text-invoices-orders-and-project-invoice-support-in-credit-management"></a>Ondersteuning voor vrije-tekst facturen, orders en projectfacturen in kredietbeheer 
Kredietbeheer kan momenteel alleen worden gebruikt voor verkooporders. Vrije-tekst facturen, POS-verkooporders en Callcenter-orders gebruiken de tijdelijke kredietlimieten en verzekering/garanties die u toevoegt om de kredietlimiet aan te passen. Ze maken geen gebruik van de blokkeringsregels en ze worden niet in de blokkeringslijst geplaatst als er een probleem is met de kredietlimiet.

Er is geen ondersteuning voor projectfacturen in kredietbeheer.
