---
title: Mobiele toepassing voor projecturenstaten
description: Dit onderwerp bevat informatie over de mobiele toepassing Microsoft Dynamics 365 Project Timesheet. Met de mobiele app voor projecturenstaten kunnen gebruikers urenstaten indienen en goedkeuren voor projecten op hun mobiele apparaat.
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: a475085001b8fa10814c864ef35129eb6ebfdfef
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1529874"
---
# <a name="microsoft-dynamics-365-project-timesheet-mobile-application"></a>Mobiele toepassing Microsoft Dynamics 365 Project Timesheet

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>Overzicht

Met de mobiele app Microsoft Dynamics 365 Project Timesheet kunnen gebruikers urenstaten indienen en goedkeuren voor projecten op hun mobiele apparaat (iPhone or Android). Deze mobiele app bevat de urenstaatfunctionaliteit die zich in het gebied Projectbeheer en boekhouding van Microsoft Dynamics 365 for Finance and Operations bevindt, waarmee gebruikersproductiviteit en efficiëntie wordt verbeterd, alsmede de tijdige invoer en goedkeuring van projecturenstaten worden mogelijk gemaakt.

## <a name="download-and-install-the-mobile-app"></a>De mobiele app downloaden en installeren

Download en installeer de mobiele app Microsoft Dynamics 365 Project Timesheet voor Android of iPhone van de mobiele winkel voor uw apparaat.

## <a name="enable-the-app"></a>De app inschakelen 

In Dynamics 365 for Finance and Operations moet de mobiele app voor projecturenstaten worden ingeschakeld. Als u de functionaliteit wilt inschakelen, gaat u naar **Parameters voor Projectbeheer en boekhouding \> Urenstaat** en selecteert u de parameter **Microsoft Dynamics 365 Project Timesheet inschakelen**.

## <a name="sign-in-to-the-app"></a>Aanmelden bij de app

1.  Start de app op uw mobiele apparaat.

2.  Voer uw URL voor Microsoft Dynamics 365 for Finance and Operations in.

3.  De eerste keer dat u zich aanmeldt, wordt u gevraagd uw gebruikersnaam en wachtwoord in te voeren. Voer uw referenties in.

4.  U wordt aangemeld bij uw standaardbedrijf.

## <a name="submit-a-project-timesheet"></a>Een projecturenstaat indienen

U kunt een projecturenstaat in de app maken en indienen. U kunt een nieuwe urenstaat baseren op gegevens uit een vorige urenstaat, opgeslagen regels of projecttoewijzingen. Als u als gemachtigde bent aangewezen, kunt u ook een urenstaat voor een andere werknemer invoeren. Als u een urenstaat wilt maken als gemachtigde, selecteert u de knop **Menu** en selecteert u een resourcenaam.

Met de urenstaatpagina maakt u een nieuwe urenstaat voor de urenstaatperiode op basis van de huidige datum. De werkweek wordt weergegeven. Als de urenstaatperiode meerdere weken bevat, kunt u een andere werkweek in de werkweektabbladen selecteren.
Als een urenstaat voor de huidige datum bestaat, wordt deze weergegeven. Als u een nieuwe urenstaat moet maken in een andere urenstaatperiode, selecteert u de knop **Menu** en selecteert u vervolgens **Nieuwe urenstaat**.

U kunt projectgegevens invoeren door te klikken op de actie **Tijd toevoegen** of de actie **Tijd kopiëren van**. Met de actie **Tijd kopiëren van** worden projectregelgegevens gekopieerd, maar niet de uren. Het menu **Tijd kopiëren van** bevat de volgende opties:

- **Kopiëren uit bestaande urenstaat**: kopieer urenstaatregels uit een bestaande urenstaat.

- **Kopiëren uit favoriet**: maak nieuwe urenstaatregels met behulp van de urenstaatinstellingen die u hebt geselecteerd als favorieten.

- **Kopiëren uit toewijzing**: maak nieuwe urenstaatregels vanuit toegewezen projecten.

De projectgegevens die worden weergegeven, zijn afhankelijk van de mobiele parameters die u hebt gedefinieerd op de pagina **Parameters voor Projectbeheer en boekhouding**.

Selecteer in het veld **Rechtspersoon** de rechtspersoon waarvoor u projectwerk hebt uitgevoerd. Het veld **Rechtspersoon** is alleen beschikbaar als voor uw rechtspersoon ondersteuning voor intercompany-urenstaten is ingeschakeld.

Selecteer de klant die samenhangt met het project voor de urenstaat. Voor de eerste versie op de Android wordt invoer door de klant niet ndersteund omdat u het project eerst moet selecteren. Als u het project eerst hebt geselecteerd, wordt het veld **Klant** automatisch ingevuld.

Selecteer in het veld **Project** het project waarvoor u tijd invoert. Het veld **Klant** wordt automatisch gevuld.

Klant- en zoekopdrachten maken zoeken in zowel klanten als projecten mogelijk.

Selecteer zo nodig gegevens in de velden **Categorie**, **Activiteit**, **Regeleigenschap**, **Btw-groep** en **Btw-groep voor artikel**. Deze velden kunnen worden overschreven.

Het veld **Regeleigenschap** wordt ingesteld op een standaardwaarde op basis van de parameters voor Projectbeheer en boekhouding. Wanneer de parameters voor project/categorie en categorie/resource zijn ingeschakeld, wordt de waarde **Regeleigenschap** ingesteld op de standaardwaarde die u hebt gedefinieerd voor deze validatie. Wanneer de parameters voor project/categorie en categorie/resource niet zijn ingeschakeld, wordt de waarde **Regeleigenschap** als standaard ingesteld volgens het veld **Standaardregeleigenschap inschakelen** op de pagina **Parameters voor Projectbeheer en boekhouding**. De waarde **Regeleigenschap** kan worden overschreven.

Selecteer een dag om tijd toe te voegen. Voer het aantal uren in dat u elke dag werkte.

Klik op **Opmerkingen** als u opmerkingen wilt toevoegen over de uren die u invoert en voer vervolgens opmerkingen in voor een interne doelgroep, klantdoelgroep of beide.
Projectmanagers kunnen interne opmerkingen weergeven. Klantopmerkingen worden in facturen opgenomen.

Als u de regel als een favoriet wilt opslaan, schakelt u het selectievakje in en klikt u vervolgens op **Opslaan als favoriet**.

Financiële dimensies en bijlagen worden niet ondersteund in de mobiele toepassing.

Ga zo nodig verder met het toevoegen van projectregels voor het voltooien van uw urenstaat.

Klik op **Indienen** om de urenstaat te verzenden naar de goedkeuringswerkstroom.

## <a name="review-timesheets"></a>Urenstaten controleren

Er is een lijst met de urenstaten die moeten worden gecontroleerd, beschikbaar in het menu. Deze optie is alleen beschikbaar als u bent aangesteld als een werkstroomfiatteur. Goedkeuring van zowel kopteksten als regels wordt ondersteund. Goedkeuring op regelniveau biedt de mogelijkheid om een of meer regels voor goedkeuring te markeren. Klik na controle van de urenstaatgegevens op **Goedkeuren**, **Machtigen** of **Retourneren** om door te gaan met de werkstroom.
