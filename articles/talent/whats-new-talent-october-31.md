---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent Core HR (31 oktober 2018)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 10/31/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: d2ad9be740d917a760815718a1473d7bcba97968
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025927"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-core-hr-october-31-2018"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent: Core HR (31 oktober 2018)

[!include [banner](includes/banner.md)]

**Build 8.1.2031**

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Core HR.

## <a name="create-links-from-talent-to-finance"></a>Koppelingen vanuit Talent maken met Finance
Met deze nieuwe navigatiefunctionaliteit kunt u koppelen van Talent naar Finance, waardoor u direct kunt navigeren in Finance-pagina's. Wanneer koppelingen worden geconfigureerd, kunt u de naam en de groep van de koppeling opgeven, waar de koppeling in Talent moet komen, en de doelpagina die moet worden geopend in Finance.

#### <a name="coming-soon"></a>Binnenkort beschikbaar
Veldcontext wordt in de toekomst toegevoegd om directe navigatie mogelijk te maken naar corresponderende records in Finance. U kunt bijvoorbeeld **Koppeling naar veld** gebruiken om de context te leveren om rechtstreeks naar een specifieke werknemer of positie in Finance te navigeren.

### <a name="configure-target-systems"></a>Doelsystemen configureren

In Talent kunnen systeembeheerders koppelingen definiëren die toegankelijk zullen zijn via het werkgebied Systeembeheer. Deel van de configuratie zijn de Finance-omgevingen waarnaar u wilt navigeren als het ¨doel¨ van de koppeling. U doet dit door het doelsysteem een naam te geven en de URL op te geven van de Finance-omgeving. Hier volgt een voorbeeld van een Finance and Operations-URL die u kunt opgeven: https://devax00124aos.cloud.test.dynamics.com/. Nadat u uw doelsystemen hebt geconfigureerd, kunt u uw koppelingen definiëren.

### <a name="configure-links"></a>Koppelingen configureren

Elke koppeling die wordt gemaakt, heeft de volgende informatie gedefinieerd.

- Koppeling: naam van de koppeling, alleen gebruikt voor identificatie.

- Deze koppeling inschakelen: ingesteld op **Ja** als u de koppeling wilt weergeven voor gebruikers van Talent.

- Weergavenaam - definieer de naam die wordt weergegeven als een koppeling naar Finance. Deze gegevens zijn momenteel niet vertaald.

- Koppelinggedeelte op het formulier: kies op welke pagina u de koppeling wilt weergeven.

- Groep: groepen zijn niet verplicht, maar als u uw koppelingen wilt ordenen met groepen, selecteert u een bestaande groep of maakt u een nieuwe groep met het veld **Groep**.

- Doelsysteem: selecteer het doelsysteem dat is gemaakt met de optie **Doelsysteem configureren**. Dit wordt de Finance-omgeving die wordt gebruikt wanneer met behulp van de koppeling wordt genavigeerd.

- Huidig bedrijf van gebruiker gebruiken - selecteer **Ja** als u de huidige bedrijfscontext van de Gebruiker wilt gebruiken wanneer u navigeert naar Finance. Als **Nee** is geselecteerd, kunt u het bedrijf selecteren dat moet worden gebruikt.

- Doelmenu-item - voer het menu-item vanuit Finance in dat de koppeling moet gebruiken wanneer wordt genavigeerd. Menu-items waarnaar u rechtstreeks kunt navigeren, zijn beschikbaar. Als u het vereiste menu-item zoekt, opent u Finance en opent u de pagina die het doel is van de navigatie. Kopieer het menu-item vanuit de URL. Als u bijvoorbeeld wilt dat de koppeling u brengt naar de werknemerslijst in Finance and Operations, voert u de waarde in die wordt weergegeven na de '&mi' in de URL. https://devax00124aos.cloud.test.dynamics.com/?p=USMF&mi=HcmWorkerListPage_Employees. Het menu-item om te navigeren naar de werknemerslijstpagina in dit voorbeeld is: HcmWorkerListPage_Employees.

- Koppeling naar gegevensbron: selecteer de bron van de gegevens waarnaar de koppeling verwijst. De meest voorkomende bronnen, zoals **Medewerker** en **Positie** zijn beschikbaar.

- Koppeling naar veld - (binnenkort) Deze veldselectie maakt directe navigatie mogelijk vanuit één record in Talent naar één record in Finance.

### <a name="access-to-links"></a>Toegang tot koppelingen

Systeembeheerders zien de nieuw gemaakte koppelingen op de gedefinieerde pagina's, zelfs als de optie **Deze koppeling inschakelen** is ingesteld op **Nee**. Dit kan worden gebruikt voor het testen van koppelingen voordat ze voor andere werknemers beschikbaar zijn. Alle andere rollen zien alleen de geconfigureerde koppelingen nadat de optie **Deze koppeling inschakelen** optie is ingesteld op **Ja**. Werknemers die toegang hebben tot de pagina's waarin de koppelingen voorkomen, hebben toegang tot de koppelingen.

Gebruikers kunnen ook beveiligingsrechten binnen Finance hebben gedefinieerd om toegang te krijgen tot de pagina's in Finance and Operations. Zo niet, dan wordt een beveiligingsdialoogvenster weergegeven wanneer de koppeling wordt gebruikt.


## <a name="other-changesfixes"></a>Andere wijzigingen/oplossingen

### <a name="positions-with-a-future-start-date-cannot-be-assigned-to-a-new-employee"></a>Posities met een toekomstige begindatum kunnen niet worden toegewezen aan een nieuwe werknemer

Er zijn wijzigingen aangebracht om werknemerstoewijzingen voor toekomstige posities mogelijk te maken. Posities met begindatums in de toekomst kunnen worden geselecteerd en de werknemerstoewijzing wordt uitgevoerd bij opslaan of voltooiing van de werkstroom (als de werkstroom is ingeschakeld).

### <a name="new-employee-cannot-be-assigned-existing-position"></a>Aan een nieuwe werknemer kan geen bestaande positie worden toegewezen

Wijzigingen zijn aangebracht, zodat een nieuwe werknemerstoewijzing nu kan worden toegewezen aan bestaande posities.

### <a name="seniority-dateoffice-location-disappears-when-the-employment-start-date-is-in-the-past-and-the-record-is-saved"></a>Anciënniteitsdatum/kantoorlocatie verdwijnt wanneer de begindatum van de aanstelling in het verleden ligt en de record wordt opgeslagen

Wijzigingen zijn aangebracht in het corrigeren van de zichtbaarheid van de **Anciënniteitsdatum** en **Kantoorlocatie** wanneer wijzigingen worden opgeslagen voor werknemers in het verleden.

### <a name="cant-enter-data-for-future-dated-employments-on-the-worker-page"></a>Kan geen gegevens invoeren voor aanstellingen in de toekomst op de medewerkerspagina

Werknemersgegevens voor toekomstige aanstellingen zijn uitgeschakeld op de hoofdmedewerkerspagina. Werknemersgegevens kunnen worden ingevoerd via de **Datumbeheer**-pagina's. Extra wijzigingen worden in toekomstige versies aangebracht om invoeren van aanstellingsgegevens direct tijdens de werkstroom mogelijk te maken.

### <a name="add-validfrom-and-validto-to-hcmpersonalcontactpersonentity"></a>ValidFrom en ValidTo toevoegen aan HcmPersonalContactPersonEntity

De DMF-entiteit (Data Management Framework) HcmPersonalContactPersonEntity is bijgewerkt met "geldig vanaf"- en "geldig tot"-datums om bepaalde vergoedingsintegratiescenario's in te schakelen. 

## <a name="known-issue"></a>Bekend probleem
- **Probleem**: bij het toevoegen van een nieuwe bijlage aan een werknemer zijn de knoppen **Nieuw** en **Bewerken** niet beschikbaar. 
- **Tijdelijke oplossing:** voordat u de bijlagepagina opent, controleert u of de feitenvakken op de pagina **Werknemer** zijn gesloten. Als de feitenvakken worden gesloten wanneer de pagina **Werknemer** wordt geladen, worden de bijlageknoppen ingeschakeld. (Dit probleem wordt opgelost in de volgende platformupdate.)
