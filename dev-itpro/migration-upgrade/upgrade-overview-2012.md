---
title: Een upgrade uitvoeren van Dynamics AX 2012 naar Dynamics 365 for Finance and Operations, Enterprise Edition
description: In dit onderwerp wordt het proces beschreven waarmee klanten die momenteel werken met Microsoft Dynamics AX 2012 hun gegevens en code kunnen verplaatsen naar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.
author: tariqbell
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer, IT Pro
ms.reviewer: margoc
ms.search.scope: Operations Platform
ms.search.region: Global
ms.author: tabell
ms.search.validFrom: 2017-06-16
ms.dyn365.ops.version: Platform update 8
ms.translationtype: Human Translation
ms.sourcegitcommit: 6816e3820ab77c71bbf9bde4a068375448331671
ms.openlocfilehash: 13507fcf9c0d626709aeb4e00a8632411204c20f
ms.contentlocale: nl-nl
ms.lasthandoff: 06/15/2017

---

# <a name="upgrade-microsoft-dynamics-ax-2012-to-microsoft-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Een upgrade uitvoeren van Microsoft Dynamics AX 2012 naar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition

[!include[banner](../includes/banner.md)]

In platformupdate 8 biedt Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, een upgrade-pad waarmee klanten die momenteel werken met Microsoft Dynamics AX 2012 hun gegevens en code kunnen overbrengen naar Finance and Operations. Het upgradeproces is gebaseerd op de volgende elementen:

- Hulpprogramma's waarmee u bestaande aangepaste toepassingscode van AX 2012 kunt aanpassen.
- Een gegevensupgradeproces waarmee u de database kunt aanpassen. Zo kunt u ook uw volledige transactiehistorie bijwerken.

## <a name="overview"></a>Overzicht

Het algehele upgradeproces kan worden weergegeven als drie overkoepelende fasen: Analyseren, Uitvoeren en Valideren.

Het volgende diagram toont het volledige upgradeproces en de activiteiten die deel uitmaken van de verschillende fasen. 

![Upgradeproces](./media/upgrade-process.png)

## <a name="analyze"></a>Analyseren

De activiteiten in de fase Analyseren helpen u een schatting te maken van de arbeid die nodig is voor de upgrade. Ze helpen u ook een projectplan voor te bereiden. Deze activiteiten kunt u uitvoeren voordat u Finance and Operations aanschaft. Ze stellen u in staat een weloverwogen aankoopbeslissing te maken, door een gegevenspunt te bieden over de inzet en resources die u nodig zult hebben.

### <a name="sign-up-for-a-public-preview-in-lcs"></a>Aanmelden voor een openbaar voorbeeld in LCS

Als u analyse-activiteiten wilt uitvoeren voordat u Finance and Operations aanschaft, kunt u zich aanmelden voor een openbare preview. In de openbare preview kunt u uw eigen Finance and Operations-omgevingen implementeren. Ook hebt u toegang tot de hulpmiddelen in Microsoft Dynamics Lifecycle Services (LCS), die worden gebruikt voor het evalueren van uw AX 2012-omgeving en uw bestaande aangepaste code.

Als u een bestaand LCS-project voor AX 2012 hebt, moet u zich nog steeds aanmelden voor een aanvullend nieuw project om Finance and Operations te evalueren.

Als u wilt weten hoe u u een openbare preview voor klanten krijgt, gaat u naar https://mbs.microsoft.com/customersource/global/AX/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Als u wilt weten hoe u u een openbare preview voor partners krijgt, gaat u naar https://mbs.microsoft.com/partnersource/global/news-events/news/Microsoft_Dynamics_AX_Public_Preview.

Houd er rekening mee dat deze openbare preview verschilt van een [evaluatieversie voor 30 dagen](https://aka.ms/D365OperationTrials). Evaluatieversies voor dertig dagen bieden een gedistribueerd exemplaar van Finance and Operations, waarmee u de toepassing kunt om leren kennen en evalueren. De analyseactiviteiten vereisen echter de volledige LCS-ervaring en alle hulpprogramma's.

### <a name="select-the-upgrade-methodology"></a>De upgrademethodologie selecteren
Stel in uw nieuwe LCS-project  de methodologie van het project in op **Upgraden van AX 2012 naar Dynamics 365 for Finance and Operations**. Deze methodologie is speciaal aangebracht voor AX 2012-klanten die een upgrade willen uitvoeren. Hierin worden de drie fasen gedetailleerd beschrijven en vindt u koppelingen naar alle ondersteunende documentatie over het proces.

![Upgrade-methodologie(./media/methodology.png)
 
### <a name="run-the-upgrade-analyzer"></a>Het hulpprogramma Upgradeanalyse uitvoeren
Het hulpprogramma Upgradeanalyse wordt uitgevoerd op uw AX 2012-omgeving en wijst taken aan die u moet uitvoeren om uw AX 2012-omgeving voor te bereiden, zodat de upgrade-ervaring soepeler verloopt en minder kost:

- **Gegevensopschoning**: Met dit proces kunt u gegevens vinden die u verwijderen kunt zonder verlies van functionaliteit. Het hulpprogramma wijst verschillende soorten gegevens aan die u verminderen kunt door een opschoonproces uit te voeren. Voor elk type gegevens wordt een uitleg gegeven over de invloed van de opschoning. U beslist vervolgens zelf of u het opschoonproces uitvoert. De kosten van uw Finance and Operations-abonnement zijn deels gebaseerd op de grootte van de database. Als u de grootte reduceert, verlaagt u dat onderdeel van de abonnementskosten en reduceert u ook de tijd die het upgrade go-live-proces vereist. Een kleinere database draagt bij aan een sneller upgrade.
- **SQL-configuratie**: Met dit proces controleert u de SQL-configuratie en krijgt u aanbevelingen voor optimalisatie. Als SQL optimaal functioneert, bespaart dit proces u tijd die nodig is om het upgradeproces go-live-proces uit te voeren.
- **Afgeschafte functies**: In dit proces worden de onderdelen aangewezen die u momenteel gebruikt, maar die niet beschikbaar zijn in Finance and Operations. Zo kunt u met dit proces vroegtijdig mogelijk verschillen in functionaliteit bepalen. U krijgt hierbij ook suggesties voor alternatieven.

Bovendien moet u als onderdeel van deze stap KBXXXXXXX installeren in de AX 2012-omgeving. Deze hotfix bevat een controlelijst die u vóór de upgrade moet doorlopen. In de AX 2012-omgeving kunt u met deze controlelijst gegevens invoeren die nodig zijn voor de upgradeprocedure. In één van de pre-upgrade controlelijsttaken geeft u aanmeldingsgegevens voor Microsoft Azure Active Directory (Azure AD) op voor elke bestaande AX 2012-gebruiker, zodat elke gebruiker kan zich aanmelden bij Finance and Operations.

De uitvoer van deze stap wordt de werkstroom in het upgradeprojectplan voor uw AX 2012-systeembeheerders.

Zie voor meer informatie [Analyse: het hulpprogramma Upgradeanalyse gebruiken om het migratiewerk te plannen](upgrade-analyzer-tool.md).

### <a name="run-the-code-upgrade-estimation-tools"></a>De hulpprogramma's voor code-upgradeschattingen uitvoeren
In deze stap wordt uw code uit AX 2012 geconverteerd naar de nieuwe indeling en wordt feedback gegeven over conflicten die een ontwikkelaar later moet oplossen. Deze stap vormt de basis voor de schatting van de kosten van uw code-upgrade.

Als u wilt deze stap wilt uitvoeren moet u uw code exporteren vanuit AX 2012 als een modelarchiefexport en deze uploaden naar de LCS-hulpprogramma voor code-upgrade. Het hulpprogramma Code-upgrade levert een bijgewerkte versie van uw code en een rapport over de resterende conflicten die moeten worden opgelost. De ontwikkelaar kan vervolgens de bijgewerkte code en het rapport bekijken om te bepalen hoeveel werk nodig is om uw codebasis te upgraden.

De uitvoer van deze stap vertegenwoordigt de werkstroom in het upgradeprojectplan voor uw Microsoft Dynamics AX-ontwikkelaars.

Zie voor meer informatie [Analyse: een schatting maken van het werk op de code te upgraden](analyze-code-upgrade.md).

### <a name="deploy-a-demo-environment"></a>Een demo-omgeving implementeren
Demo-omgevingen zijn standaardomgevingen met voorbeeldgegevens (niet uw eigen gegevens) en standaardcode (geen aanpassingen). Het wordt aangeraden om een demo-omgeving te implementeren, waarin u nieuwe functies kunt beoordelen en om een basis fit/gap-analyse uit te voeren van standaardprocessen die in AX 2012 worden gebruikt, maar die mogelijk zijn gewijzigd in Finance and Operations. U kunt deze demo-omgevingen in Azure implementeren, of ze downloaden als een virtuele machine (VM) die u op uw eigen hardware uitvoert. Als u ze in Azure implementeert, moet u uw Azure-abonnement opgeven, omdat u nog steeds een openbare previewproject gebruikt en nog geen Finance and Operations-abonnement hebt aangeschaft.

De uitvoer van deze stap vertegenwoordigt de werkstroom in het upgradeprojectplan voor uw functionele of zakelijke gebruikers.

Zie voor meer informatie [Analyse: een sandbox-omgeving implementeren](analysis-sandbox.md)

### <a name="create-a-project-plan"></a>Een projectplan maken
Een sjabloon voor een projectplan is beschikbaar in de upgrade-methodologie. In deze stap wordt de uitvoer uit de vorige stappen van de fase Analyseren gebruikt om het projectplan voor het upgradeproject in te vullen. Het projectplan bevat ook alle testgegevens: testen van de gegevensupgrade, cutover-testen, de functionele testdoorloopherhalingen en details van de verschillende resourcetoewijzingen voor deze taken.

In deze fase levert het projectplan een gegevenspunt dat inzicht geeft in de tijd en kosten die een upgrade naar Finance and Operations inhoudt.

## <a name="execute"></a>Uitvoeren
Tijdens de fase Uitvoeren moet u de taken uitvoeren die u tijdens de fase Analyseren hebt gepland. Als u door wilt gaan met de fase Uitvoeren, moet u Finance and Operations aanschaffen en u moet beschikbare resources hebben die aan de upgrade kunnen werken.

### <a name="switch-to-the-lcs-implementation-project"></a>Overschakelen naar het LCS-implementatieproject
Het openbare previewproject dat u voor de fase Analyseren hebt gebruikt, heeft zijn doel gediend. U kunt het nu verwijderen. Voor de resterende stappen hebt u alleen het projectplan nodig dat u hebt gemaakt in de laatste stap van de fase Analyseren.

Wanneer u een abonnement voor Finance and Operations aanschaft, ontvangt u gedetailleerde informatie over hoe u zich moet aanmelden voor het LCS-project. Dit project wordt een implementatieproject genoemd en wordt het nieuwe permanente LCS-project voor uw abonnement, zolang als u dat abonnement aanhoudt. Het verschil tussen dit project en het openbare previewproject, is dat dit project wordt beheerd door Microsoft. Dit project heeft daarom deze kenmerken:

- Alle omgevingen in het project worden gehost in Azure.
- Het Azure-abonnement dat is gekoppeld aan het project, wordt beheerd door Microsoft. Er vindt daarom geen afzonderlijke facturering plaats voor Azure-kosten. Deze kosten worden gedekt door uw Finance and Operations-abonnement.
- De productie-omgeving in het project wordt beheerd door Microsoft. Daarom worden code-implementaties, upgrades en onderhoud van infrastructuur rechtstreeks uitgevoerd door Microsoft, niet door uw personeel. 

### <a name="perform-the-ax-2012-preparation-tasks"></a>De voorbereidende taken voor AX 2012 uitvoeren
Voer de taken die het hulpprogramma Upgrade-analyzer heeft aangegeven en die worden beschreven in het upgradeprojectplan. Uw Microsoft Dynamics AX-systeembeheerder en -databasebeheerder (DBA) moeten deze taken uitvoeren.

[Gegevensupgrade van AX 2012 naar Dynamics 365 for Operations: pre-upgradecontrolelijst in AX 2012](prepare-data-upgrade.md)

### <a name="perform-code-upgrade"></a>De code-upgrade uitvoeren
Voer de taken uit die zijn gepland tijdens de stap voor het schatten van de code-upgrade in de fase Analyseren. Uw ontwikkelaars moeten deze taken uitvoeren.

Vanaf dit punt moeten codewijzigingen in AX 2012 bevroren worden. Alleen in noodgevallen zijn codewijzigingen nog toegestaan in AX 2012. Als een wijziging wordt aangebracht, moet deze handmatig worden overgezet naar de nieuwe codebasis.

### <a name="develop-new-code"></a>Nieuwe code ontwikkelen
Voer de taken uit van de fit/gap-analyse die is uitgevoerd tijdens de stap 'Een demo-omgeving implementeren' van de fase Analyseren. Deze taken zijn waarschijnlijk een combinatie van functionele taken, die de configuratie definiëren, en ontwikkelingstaken, voor aanpassingen die te maken hebben met nieuwe functies die gaan worden gebruikt.

### <a name="data-upgrade-development-environment"></a>Gegevensupgrade (ontwikkelomgeving)
Nadat uw code-upgradetaken zijn uitgevoerd, kunt u uw AX 2012-database voor het eerst upgraden naar Finance and Operations. Deze eerste upgrade wordt uitgevoerd in een ontwikkelomgeving, zodat u gemakkelijker eventuele problemen in deze fase kunt herstellen of er foutopsporing op uitvoeren. In een ontwikkelomgeving kan een probleem onmiddellijk worden opgespoord, code kan worden gecorrigeerd en de upgrade kan binnen enkele minuten opnieuw worden uitgevoerd. Grotere sandbox-omgevingen bieden deze flexibiliteit niet, en op zijn minst zijn enkele uren vereist om problemen te onderzoeken en te herstellen, code bij te werken, de bijgewerkte code te implementeren en de upgrade opnieuw uit te voeren.

De volgende afbeelding licht het proces toe. Maak een back-up van de AX 2012-database, upload deze naar Azure, herstel hem in de Finance and Operations-omgeving en voer de gegevensupgrade uit.

![Gegevensupgrade in een ontwikkelomgeving](./media/data-upgrade-dev.png)
 
Een gegevensupgrade wordt uitgevoerd door middel van een speciaal type implementeerbaar pakket. Hetzelfde mechanisme wordt gebruikt voor het implementeren van nieuwe Finance and Operations-code van de ene omgeving naar een andere.

Het onderliggende framework dat wordt gebruikt voor het converteren van de gegevens in de database tijdens dit proces is grotendeels hetzelfde als het upgradeframework in AX 2012, dat is gebaseerd op de X++-batchtaken die **ReleaseUpdatexxx**-klassen uitvoeren.

Zie voor meer informatie het onderwerp [Gegevensupgrade van AX 2012 naar Dynamics 365 for Operations in een ontwikkelomgeving](data-upgrade-2012.md).

### <a name="data-upgrade-sandbox-environments"></a>Gegevensupgrade (sandboxomgevingen)
Wanneer de gegevensupgrade in een ontwikkelomgeving is uitgevoerd, kunt u hetzelfde proces uitvoeren in een sandbox-omgeving. De sandbox-omgeving is de omgeving waarin zakelijke gebruikers en functionele teamleden bedrijfsprocessen kunnen testen met behulp van de bijgewerkte gegevens en code uit AX 2012.

In de volgende afbeelding ziet u het proces voor het uitvoeren van de gegevensupgrade in een sandbox-omgeving. Het verschil hier is dat het bacpac-hulpprogramma wordt gebruikt in plaats van een traditionele SQL-back-up. Dit hulpprogramma is vereist om te kunnen converteren tussen Microsoft SQL Server en Azure SQL Database. Het is een standaard SQL-hulpprogramma en is niet specifiek bedoeld voor Finace and Operations.

![Gegevensupgrade in sandboxomgeving](./media/data-upgrade-sandbox.png)

Zie voor meer informatie het onderwerp [Gegevensupgrade van AX 2012 naar Dynamics 365 for Operations in een sandbox-omgeving](upgrade-data-sandbox.md).
 
## <a name="validate"></a>Valideren
Wanneer u de fase Valideren bereikt, hebt u beschikbare omgevingen die uw bijgewerkte aangepaste code en de bijgewerkte gegevens bevatten. In deze fase wordt beschreven hoe u de bijgewerkte omgeving valideert en test of deze naar wens functioneert. Hierin worden ook het proces voor het voorbereiden van de go-live beschreven.

### <a name="perform-cutover-testing-and-create-a-cutover-plan"></a>Cutover-testen uitvoeren en een cutover-plan maken
De term _cutover_ wordt hier gebruikt om het definitieve proces aan te duiden waarbij het nieuwe systeem live gaat. Dit proces bestaat uit de taken die plaatsvinden nadat AX 2012 is uitgeschakeld en vóórdat Finance and Operations wordt ingeschakeld. 

Het doel van het testen is om het cutover-proces te oefenen. Op deze manier kunt u garanderen dat voor iedereen die betrokken is bij de werkelijke cutover voor go-live, deze soepel verloopt.

Er zijn twee belangrijke werkstromen:

- **Technische werkstroom**: deze workstream omvat het proces voor uitvoering van de gegevensupgrade. Uw bedrijf legt een limiet op voor de toegestane lengte van de uitvaltijd. Tijdens deze uitvaltijd zijn AX 2012 en Finance and Operations beide niet beschikbaar. De technische werkstroom moet mogelijk de procedure voor gegevensupgrade tunen, zodat u kunt voldoen aan downtime-limiet van het bedrijf. 
- **Functionele werkstroom**: nadat de gegevensupgrade moeten verschillende configuratietaken worden uitgevoerd in de Finance and Operations-omgeving. Al deze taken moeten worden gedocumenteerd en gekwantificeerd en een resource moet worden toegewezen, omdat de functionele werkstroom samen met de technische werkstroom beide binnen de voorgeschreven downtime-limiet moet passen.

Zie voor meer informatie 
- [Valideren: cutover-testen](upgrade-cutover-testing.md)
- [Valideren: app-validatieproces](app-validation-process.md)

### <a name="functional-test-pass"></a>Functionele testdoorloop
Voer een volledig functionele testdoorloop uit van alle bedrijfsprocessen. Deze testdoorloop is een uitgebreide hertest van alle zakelijke processen waarbij Finance and Operations betrokken is. Deze zakelijke processen omvatten zowel oude processen die zijn overgebracht vanuit AX 2012 en nieuwe processen die nieuwe functies inhouden en die voor het eerst in Finance and Operations worden gebruikt. 

Afhankelijk van de kwaliteit van de code zijn voor probleemherstelling en hertesten mogelijk meerdere herhalingen van de functionele testdoorloop vereist. Wanneer een probleem is opgelost moet u alle betrokken processen opnieuw testen, om er zeker van te zijn dat de processen down- of upstream niet door deze wijziging worden beïnvloed.

Zie voor meer informatie [Valideren: functioneel testen](upgrade-functional-validation.md).

### <a name="pre-go-live-checklist"></a>Controlelijst vóór go-live
De controlelijst voor de go-live is een aanbevolen procedure, die kan helpen de kans op fouten tijdens de uiteindelijke cutover voor go-live te verkleinen. Zet één week vóór de go-live alle configuratiewijzigingen in AX 2012 stil (onder \<module\>\Instellingen). Deze beperking op wijzigingen in de configuratie is alleen procedureel. De Microsoft Dynamics AX-systeembeheerders gaan er alleen mee akkoord wijzigingen van dit type op dat punt in niet meer uit te voeren.

Het is raadzaam om ook codewijzigingen in de codebasis van Finance and Operations te bevriezen. Verdere wijzigingen zijn niet toegestaan, tenzij ze zijn geëvalueerd en het is aangetoond dat ze de go-live niet in de weg staan.  

Nadat de configuratie en codewijzigingen zijn geblokkeerd, moet de gegevensupgrade voor de laatste keer worden uitgevoerd voor de cutover. Zo kunt u ervoor zorgen dat alles nog steeds correct werkt. 

Zie voor meer informatie [Valideren: go-live voorbereiden](upgrade-go-live-prep.md).



### <a name="supported-upgrade-paths"></a>Ondersteunde upgradepaden
Vanaf juni 2017 wordt een upgrade naar Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition, versie 0617, ondersteund vanaf Microsoft Dynamics AX 2012 R3. Alle cumulatieve updates (CU's) van AX 2012 R3 worden ondersteund.

Microsoft Dynamics AX 2012 R2 en Microsoft Dynamics AX 2012 RTM worden momenteel niet ondersteund. Ondersteuning wordt later in 2017 toegevoegd.

Alleen een upgrade naar de cloud-versie van Finance and Operations wordt ondersteund. Upgrade naar de on-premises-versie wordt niet ondersteund. Ondersteuning voor de upgrade naar de on-premises-versie later in 2017 toegevoegd.

