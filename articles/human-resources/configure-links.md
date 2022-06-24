---
title: Koppelingen vanuit Human Resources naar een andere omgeving maken
description: In dit artikel wordt uitgelegd hoe u een koppeling van Microsoft Dynamics 365 Human Resources naar een andere Dynamics 365-omgeving maakt.
author: twheeloc
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-29-11
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0c9efae1061e96c0c42d5ca6a100bb36889ce56b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859661"
---
# <a name="create-links-from-human-resources-to-another-finance-environment"></a>Koppelingen maken van Human Resources naar een andere Finance-omgeving

Een klant kan in twee Dynamics 365-omgevingen werken. De klant kan bijvoorbeeld een Dynamics 365 Human Resources-omgeving hebben op de Finance-infrastructuur en moet verbinding maken met een andere Dynamics 365 Finance-omgeving. 

Met deze functie kunt u koppelingen vanuit een Human Resources-pagina naar een specifieke pagina in een andere Finance-omgeving maken. Wanneer de koppelingen zijn geconfigureerd, kunt u opgeven waar de koppeling beschikbaar is in Human Resources en welke doelpagina wordt geopend in de andere omgeving.

> [!Note] 
> U moet **Verbeteringen in de Human Resources-gebruikerservaring** in **Functiebeheer** inschakelen om deze functie te krijgen.

## <a name="configure-target-systems"></a>Doelsystemen configureren

In Human Resources kunnen systeembeheerders koppelingen definiëren die worden weergegeven op pagina's in **Human Resources**. Delen van de configuratie zijn Finance-omgevingen waarnaar u wilt navigeren als het doel van de koppeling. 

Het doelsysteem configureren:
1. Selecteer op de pagina **Koppelingen configureren** de optie **Doelsysteem configureren**.  
2. Voer de naam van het doelsysteem in en geef de URL van de Finance-omgeving op. Nadat u uw doelsystemen hebt geconfigureerd, kunt u uw koppelingen definiëren.

## <a name="configure-links"></a>Koppelingen configureren

Elke koppeling die u maakt, heeft de volgende informatie gedefinieerd:
 - **Koppeling**: naam van de koppeling. Wordt alleen gebruikt ter identificatie.
 - **Deze koppeling inschakelen**: stel dit in op **Ja** als u de koppeling wilt weergeven voor gebruikers van Human Resources.
 - **Weergavenaam**: voer de naam in die wordt weergegeven als een koppeling naar de secundaire omgeving. 
 - **Koppelinggedeelte op het formulier**: kies op welke pagina u de koppeling wilt weergeven. Koppelingen kunnen alleen worden weergegeven in de werkruimte **Werknemerselfservice** en de pagina's **Taak**, **Positie**, **Werknemer** en **Gestroomlijnde werknemer**.
 - **Groep**: u kunt uw koppelingen met behulp van groepen organiseren. Selecteer een bestaande groep of maak een nieuwe in de kolom **Groep**.
 - **Doelsysteem**: selecteer het doelsysteem dat is gemaakt met de optie **Doelsysteem configureren**. Dit wordt de secundaire omgeving die wordt gebruikt wanneer met behulp van de koppeling wordt genavigeerd.
 - **Huidig bedrijf van gebruiker gebruiken**: selecteer **Ja** als u het huidige bedrijf van de gebruiker wilt gebruiken wanneer u navigeert naar Finance. Selecteer **Nee** om het bedrijf te selecteren dat moet worden gebruikt.
 - **Doelmenu-item**: voer het menu-item vanuit de Finance-omgeving in dat de koppeling moet gebruiken wanneer wordt genavigeerd. Menu-items waarnaar u rechtstreeks kunt navigeren, zijn beschikbaar. 

   U vindt het vereiste menu-item als volgt:
   1. Ga naar de Finance-omgeving en open u de pagina die het doel is van de navigatie. 
   2. Kopieer het menu-item vanuit de URL. Als u bijvoorbeeld wilt dat de koppeling u brengt naar de werknemerslijst in Finance and Operations, voert u de waarde in die wordt weergegeven na de '&mi' in de URL. 
   3. Het menu-item om te navigeren naar de werknemerslijstpagina in dit voorbeeld is: HcmWorkerListPage_Employees.

 - **Koppeling naar gegevensbron**: selecteer de bron van de gegevens waarnaar de koppeling verwijst. De meest voorkomende bronnen, zoals **Medewerker** en **Positie** zijn beschikbaar.

### <a name="access-to-links"></a>Toegang tot koppelingen

Systeembeheerders zien de nieuw gemaakte koppelingen op de gedefinieerde pagina's, zelfs als de optie **Deze koppeling inschakelen** is ingesteld op **Nee**. Dit kan worden gebruikt voor het testen van koppelingen voordat ze voor andere werknemers beschikbaar zijn. Alle andere rollen zien alleen de geconfigureerde koppelingen nadat de optie **Deze koppeling inschakelen** is ingesteld op **Ja**. Werknemers die toegang hebben tot de pagina's waarin de koppelingen voorkomen, hebben toegang tot de koppelingen.

Gebruikers moeten ook beveiligingsrechten hebben in de gedefinieerde secundaire omgeving om de pagina's in die omgeving te kunnen openen. Zo niet, dan wordt een beveiligingsdialoogvenster weergegeven wanneer de koppeling wordt gebruikt.

