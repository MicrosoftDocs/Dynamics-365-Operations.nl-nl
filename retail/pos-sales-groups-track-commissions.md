---
title: Provisies volgen in POS door middel van verkoopgroepen
description: 'Het is in de detailhandel gebruikelijk om verkopen bij te houden van de werknemer die met de klant heeft gewerkt: ondersteuning bieden, bij- en meerverkoop en verwerking van de transactie.'
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: f92d81512d84b819d411775d67bfa6934642bcb5
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="track-commissions-in-pos-using-sales-groups"></a>Provisies volgen in POS door middel van verkoopgroepen

[!include[banner](includes/banner.md)]


Het is in de detailhandel gebruikelijk om verkopen bij te houden van de werknemer die met de klant heeft gewerkt: ondersteuning bieden, bij- en meerverkoop en verwerking van de transactie.

Het bijhouden van verkopen per verkoper levert inzicht op in de verkoopvaardigheid van de verkoper. Het bijhouden van verkopen per kassamedewerker geeft inzicht in de snelheid en efficiëntie. Het volgen van verkopen per verkoper wordt ook vaak gebruikt voor het berekenen van provisie of andere beloningen.

## <a name="configuring-a-worker-to-be-a-sales-representative-in-pos"></a>Een medewerker configureren als een verkoper in POS
Wanneer een medewerker wordt toegevoegd aan een verkoopgroep, komt hij of zij in aanmerking voor provisie en kan in het systeem worden geïdentificeerd als een verkoper. Een medewerker die geen lid van een verkoopgroep is, komt niet in aanmerking voor provisie en wordt niet genoemd als een verkoper in de POS-toepassing. In POS wordt de lijst met verkopers afgeleid van alle verkoopgroepen met tenminste één medewerker die is toegewezen aan de winkel. De lijst wordt weergegeven in POS als een combinatie van de verkoopgroep-id en naam (id : naam). Een standaardverkoopgroep kan worden toegewezen aan medewerkers voor scenario's waarin de detailhandelaar ervoor kiest om automatisch de verkoper op POS-regels in te stellen. Gebruikers kunnen kiezen uit alle verkoopgroepen waar de medewerker lid van is.

## <a name="functionality-profile-settings"></a>Functionaliteitsprofielen instellen
Er zijn een aantal instellingen voor functionaliteitsprofielen voor een winkel, die de de flow en het proces in POS bepalen waarbij verkopers zijn betrokken.

|                                       |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Profiel**                           | **Beschrijving**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Standaard naar kassier indien beschikbaar** | Als deze optie is ingeschakeld, vult POS automatisch transactieregels met de standaardverkoopgroep van de huidige kassamedewerker. Als voor een kassamedewerker geen standaardgroep is opgegeven, wordt de waarde niet ingesteld. Een gebruiker kan nog steeds de verkoopgroep handmatig instellen door middel van een POS-knop in het knoppenraster.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| **Vragen om verkoopvertegenwoordiger**   | Deze optie heeft drie mogelijke waarden: **Nee **: Als deze optie is geselecteerd, wordt de gebruiker niet gevraagd om een verkoopgroep te selecteren. De waarde kan nog steeds worden ingesteld door de standaardgroep van een kassamedewerker te gebruiken, of handmatig met behulp van een POS-knop in het knoppenraster. **Begin van transactie**: Als deze optie is geselecteerd en de optie **Standaard naar kassier** niet is ingeschakeld of de huidige kassamedewerker geen standaardverkoopgroep heeft, wordt de gebruiker gevraagd om een verkoopgroep te selecteren aan het begin van elke transactie. Als u een verkoopgroep selecteert vanuit deze vraag, worden alle volgende regels standaard toegewezen aan de geselecteerde verkoopgroep. Een gebruiker kan nog steeds de verkoopgroep handmatig instellen door middel van een POS-knop in het knoppenraster. **Voor elke regel**: Als deze optie is geselecteerd en de optie **Standaard naar kassier** niet is ingeschakeld of de huidige kassamedewerker geen standaardverkoopgroep heeft, wordt de gebruiker gevraagd om een verkoopgroep te selecteren telkens nadat een regel is toegevoegd. Een gebruiker kan nog steeds de verkoopgroep handmatig instellen door middel van een POS-knop in het knoppenraster. |
| **Vereist**                           | Deze optie geldt alleen wanneer POS is geconfigureerd om naar de verkoper te vragen. Als deze optie is ingeschakeld, moet de gebruiker een verkoopgroep kiezen voordat hij of zij doorgaat. Anders wordt de gebruiker gevraagd te kiezen, maar kan hij annuleren en doorgaan zonder een groep te selecteren. Nadat de regel is toegevoegd, kan een gebruiker met de juiste machtigingen nog steeds de verkoopgroep verwijderen uit de regel. 'Verkoopvertegenwoordiger vereisen' wordt niet afgedwongen in deze situatie.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## <a name="displaying-the-sales-representative-information-on-the-pos-transactions-screen"></a>Gegevens van de verkoper weergeven op het POS-transactiescherm
De inhoud en indeling van het POS-transactiescherm kunnen worden geconfigureerd met de schermindelingsontwerper en toegewezen aan winkels, kassa's of medewerkers. Het veld **Verkoopvertegenwoordiger** kan worden toegevoegd aan het tabblad Regels in het deelvenster Ontvangstbewijs.  Hier wordt de id van de opgegeven verkoopgroep getoond voor elke regel in het transactiescherm.

## <a name="adding-sales-representative-operations-to-pos-button-grids"></a>Bewerkingen van verkopers toevoegen aan de POS-knoppenrasters
In POS kunnen gebruikers knoppenrasters configureren, die deel uitmaken van schermindelingen en toegang bieden tot POS-bewerkingen. De volgende POS-bewerkingen kunnen worden toegewezen aan de knoppen in knoppenraster, die betrekking hebben op verkopers.

|                                           |                                                                                                                                                                                                                                                                                              |
|-------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Bewerking**                             | **Beschrijving**                                                                                                                                                                                                                                                                              |
| Verkoopvertegenwoordiger instellen op regel          | Met deze POS-bewerking wordt een lijst weergegeven met in aanmerking komende verkoopgroepen (ID : naam) voor de winkel. Als u een verkoopgroep in deze lijst selecteert, wordt de waarde ingesteld op de huidige transactieregel.                                                                                                            |
| Verkoopvertegenwoordiger wissen op regel        | Deze POS-bewerking verwijdert de huidige waarde van de verkoopgroep voor de huidige transactieregel.                                                                                                                                                                                                  |
| Verkoopvertegenwoordiger instellen voor transactie   | Met deze POS-bewerking wordt een lijst weergegeven met in aanmerking komende verkoopgroepen (ID : naam) voor de winkel. Als u een verkoopgroep in deze lijst selecteert, wordt de standaardwaarde ingesteld op de huidige transactieregel. Alle bestaande regels waaraan geen verkoopgroep is toegewezen, worden ingesteld, evenals alle regels die daarna worden toegevoegd. |
| Verkoopvertegenwoordiger wissen voor transactie | Deze POS-bewerking verwijdert de huidige standaardwaarde van de verkoopgroep voor de huidige transactie. Dit heeft geen invloed op andere regels die al voorkomen in de transactie.                                                                                                                             |

## <a name="calculating-commissions"></a>Provisies berekenen
Provisie wordt berekend voor de medewerkers in de opgegeven verkoopgroepen tijdens het boeken van overzichten of van verkooporders. Het provisiebedrag wordt bepaald op basis van het provisieaandeel van medewerker, zoals dat is gedefinieerd in de verkoopgroep en de bijbehorende instellingen voor provisieberekening voor de klant en/of producten in de transactie.




