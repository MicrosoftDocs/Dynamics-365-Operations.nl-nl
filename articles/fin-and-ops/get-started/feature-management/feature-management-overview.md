---
title: Overzicht van functiebeheer
description: Dit onderwerp bevat een beschrijving van de functie Functiebeheer en de manier waarop u deze kunt gebruiken.
author: mikefalkner
manager: AnnBe
ms.date: 04/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: IT Pro, Application user
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom:
- month/year of release that feature was introduced in
- in format yyyy-mm-dd
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: e75e42926db22d4fccda86c755b12d9d121a9c0e
ms.sourcegitcommit: be447fc81bc874982bc0185fcb4d87d99bd742c5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/08/2019
ms.locfileid: "1538681"
---
# <a name="feature-management-overview"></a>Overzicht van functiebeheer

[!include[banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

Functies worden toegevoegd en bijgewerkt in elke release van Microsoft Dynamics 365 for Finance and Operations. De functie Functiebeheer biedt een werkgebied waarin u een lijst met functies kunt weergeven die in elke release zijn geleverd. Nieuwe functies zijn standaard uitgeschakeld. U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven.

## <a name="the-feature-management-workspace"></a>Het werkgebied Functiebeheer

U kunt het werkgebied **Functiebeheer** openen door de gewenste tegel te selecteren op het dashboard. Er wordt een pagina weergegeven met een lijst met functies voor alle releases die worden ondersteund door de functie Functiebeheer. In de loop van de tijd zal Microsoft de functie Functiebeheer verbeteren zodat deze extra functionaliteit bevat om u te helpen bij het beheren van functies.

De lijst met functies bevat de volgende informatie:

- **Functienaam**: een beschrijving van de functie die is toegevoegd.
- **Inschakelstatus**: een symbool geeft aan of een functie is ingeschakeld (vinkje), niet is ingeschakeld (leeg), staat gepland voor inschakeling (klok) of verplicht is ingeschakeld (slot). De instelling die hier wordt weergegeven, wordt gebruikt voor alle rechtspersonen. Houd er rekening mee dat zelfs wanneer een functie is ingeschakeld, deze nog steeds aan de beveiliging moet voldoen. Daarom is de functie alleen beschikbaar voor gebruikers die toegang hebben tot de functie op basis van hun beveiligingsrol. Deze is ook alleen beschikbaar voor rechtspersonen waartoe de gebruiker toegang heeft.
- **Inschakeldatum**: de datum waarop de functie is ingeschakeld of wordt ingeschakeld als de datum een toekomstige datum is.
- **Toegevoegde functie**: de datum waarop de functie aan uw omgeving is toegevoegd. Deze datum wordt automatisch ingevoerd wanneer u uw omgeving bijwerkt tijdens de maandelijkse releasecycli.
- **Module**: de module waarop de nieuwe functie van invloed is.

Wanneer u een functie selecteert, wordt aanvullende informatie weergegeven in het detailvenster rechts van de lijst met functies. Boven aan het deelvenster ziet u de functienaam, de datum waarop het onderdeel is toegevoegd, de module waarvoor de functie geldt en een koppeling **Meer informatie**. Selecteer deze koppeling om de documentatie voor de functie weer te geven. Als er geen documentatie beschikbaar is, wordt u naar een tijdelijke pagina geleid. Het detailvenster bevat ook een veld **Opmerkingen** waarin u uw eigen opmerkingen over de functie kunt toevoegen.

Het werkgebied **Functiebeheer** bevat tevens diverse tabbladen met een lijst met functies. 
- **Nieuw**: bevat alle functies die zijn toegevoegd sinds de laatste maandelijkse update. Als u maandelijkse updates hebt overgeslagen, bevat deze alle nieuwe functies sinds u de laatste keer hebt bijgewerkt. De nieuwste functies worden boven aan de lijst weergegeven. Het totale aantal nieuwe functies wordt ook weergegeven in een tegel boven aan de pagina.
- **Niet ingeschakeld**: toont alle functies die niet zijn ingeschakeld. De nieuwste functies worden boven aan de lijst weergegeven. Het totale aantal nieuwe functies wordt ook weergegeven in een tegel boven aan de pagina.
- **Gepland**: toont alle functies die zijn gepland voor inschakeling op een toekomstige datum. De functies met de vroegste geplande datum worden boven aan de lijst weergegeven. Het totale aantal nieuwe functies wordt ook weergegeven in een tegel boven aan de pagina.
- **Alle**: toont alle functies. De nieuwste functies worden boven aan de lijst weergegeven.


## <a name="enable-a-feature"></a>Een functie inschakelen

Als een functie niet is ingeschakeld, wordt een knop **Inschakelen** weergegeven in het detailvenster. U kunt deze knop gebruiken om de functie in te schakelen.

1. Selecteer de functie die u wilt inschakelen en selecteer vervolgens **Inschakelen** in het detailvenster.
2. Er wordt een schuifregelaar weergegeven waarmee u de datum kunt opgeven waarop de functie moet worden ingeschakeld. Deze datum is standaard ingesteld op de huidige datum.
3. Selecteer **Inschakelen** om de functie in te schakelen.

Sommige functies kunnen niet worden uitgeschakeld nadat u ze hebt ingeschakeld. Als de functie die u wilt inschakelen niet kan worden uitgeschakeld, wordt een waarschuwing weergegeven. Op dit moment kunt u **Annuleren** selecteren om de bewerking te annuleren en de functie uitgeschakeld te laten. Als u echter de optie **Inschakelen** selecteert en de functie inschakelt, kunt u deze later niet meer uitschakelen.

Nadat de functie is ingeschakeld, wordt een bericht weergegeven onder de koppeling **Meer informatie** in het detailvenster. Dit bericht geeft aan dat de functie is ingeschakeld of geeft aan wanneer de functie in de toekomst wordt ingeschakeld. Als u een toekomstige datum gebruikt, wordt de functie weergegeven in de lijst **Gepland**. Dit bericht wordt weergegeven telkens wanneer u de functie selecteert in de lijst met functies. Functies die in de toekomst worden gepland, worden om middernacht ingeschakeld door een batchproces op basis van de tijdzone die wordt aangegeven door de systeemdatum. 

## <a name="reschedule-a-feature"></a>Een functie opnieuw plannen

Als een functie zal worden ingeschakeld in de toekomst, wordt een knop **Opnieuw plannen** weergegeven in het detailvenster. Met deze knop kunt u de **inschakeldatum** wijzigen in een andere datum.

1. Selecteer een geplande functie die u opnieuw wilt plannen en selecteer vervolgens **Opnieuw plannen** in het detailvenster.
2. Er wordt een schuifregelaar weergegeven waarmee u de datum kunt opgeven waarop de functie moet worden ingeschakeld. 
3. Selecteer **Inschakelen** om de functie opnieuw te plannen of **Uitschakelen** om de planning te annuleren.

## <a name="disable-a-feature"></a>Een functie uitschakelen

Als een functie al is ingeschakeld, wordt een knop **Uitschakelen** weergegeven in het detailvenster. U kunt deze knop gebruiken om de functie uit te schakelen. De knop **Uitschakelen** is niet beschikbaar als de functie niet kan worden uitgeschakeld nadat deze is ingeschakeld.

- Selecteer de functie die u wilt uitschakelen en selecteer vervolgens **Uitschakelen** in het detailvenster.

- De functie is uitgeschakeld en de datum wordt gewist.

Nadat de functie is uitgeschakeld, wordt een bericht weergegeven onder de koppeling **Meer informatie** in het detailvenster. In dit bericht staat dat de functie nog niet is ingeschakeld, en deze wordt weergegeven in de lijst **Niet ingeschakeld**. Het bericht wordt weergegeven telkens wanneer u de functie selecteert in de lijst met functies.

## <a name="features-that-must-be-enabled"></a>Functies die moeten worden ingeschakeld

Mogelijk wordt een kritieke functie geleverd die automatisch moet worden ingeschakeld wanneer u een update uitvoert. Deze wordt automatisch ingeschakeld op de **inschakeldatum**. Er verschijnt een bericht onder de koppeling **Meer informatie** in het detailvenster. Dit bericht geeft aan dat de functie is ingeschakeld of automatisch wordt ingeschakeld op de **inschakeldatum**. Dit wordt weergegeven telkens wanneer u de functie selecteert in de lijst met functies.

## <a name="assigning-roles"></a>Rollen toewijzen

Het werkgebied **Functiebeheer** kan worden geopend door systeembeheerders en door gebruikers die zijn toegewezen aan de rollen Functiebeheer of Functieweergave die zijn gemaakt ter ondersteuning van de functie Functiebeheer. Gebruikers met de rol Functiebeheer kunnen elke functie in- of uitschakelen. Zij kunnen ook de opmerkingensectie voor de functie bijwerken. Gebruikers in de rol Functieweergave kunnen alleen het werkgebied **Functiebeheer** weergeven. Zij kunnen functies niet in- of uitschakelen.

De rol Functiebeheer en de rol Functieweergave hebben geen voorrang boven de bestaande beveiliging die een gebruiker heeft. De rollen bepalen alleen de toegang tot het inschakelen van functies. Zij bieden geen toegang tot de functies zelf.

## <a name="using-feature-management-to-enable-isv-features-or-custom-features"></a>Functiebeheer gebruiken om ISV-functies of aangepaste functies in te schakelen

Het proces Functiebeheer is momenteel niet beschikbaar voor ISV-functies of aangepaste functies. We voegen extra functionaliteit toe om Functiebeheer te verbeteren en als deze verbeteringen zijn voltooid, wordt Functiebeheer opengesteld voor alle functies en worden er specifieke instructies verstrekt voor het bijwerken van uw functie voor gebruik hiervan.

## <a name="feature-management-and-flighting"></a>Functiebeheer en flighting

Met Functiebeheer kunt u functies beheren die in elke release worden meegeleverd. Met flighting kunnen Microsoft-teams functies vrijgeven voor een beperkt aantal klanten, zodat de functies kunnen worden getest en gevalideerd zonder dat dit gevolgen heeft voor alle klanten. Met Functiebeheer wordt niet de flighting van alle functies bestuurd.
