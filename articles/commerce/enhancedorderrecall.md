---
title: Bewerking Order intrekken in POS
description: In dit onderwerp worden de functies uitgelegd die beschikbaar zijn voor de verbeterde pagina´s voor orderintrekking in POS.
author: hhainesms
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: global
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 21e8045d754006345f5ad68e1e67579386c6df4a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010069"
---
# <a name="recall-order-operation-in-pos"></a>Bewerking Order intrekken in POS

[!include [banner](includes/banner.md)]

Met de bewerking voor het **intrekken van orders** in het Commerce Point of Sale (POS) beschikt u over gewijzigde functies om te zoeken en te filteren en over orderspecifieke informatie. Deze functie is beschikbaar in Commerce-versies 10.0.15 en hoger.

Als u deze functie wilt inschakelen, schakelt u de functie **Verbeterde bewerking voor orderintrekking in POS** in de werkruimte **Functiebeheer** in Commerce Headquarters in. Nadat u de functie hebt ingeschakeld, kunt u overwegen om uw [schermindelingen](pos-screen-layouts.md) in POS bij te werken zodat u kunt profiteren van een aantal van de gewijzigde mogelijkheden.

Met de configuratie van de bewerkingsknop **Order intrekken** kunnen organisaties de bewerking implementeren met een vooraf gedefinieerde weergave.

![Configuratie knoppenraster](media/recallorderbuttongrid.png)

De weergaveopties zijn als volgt.
- **Geen**: met deze optie wordt de bewerking zonder specifieke weergave geïmplementeerd. Wanneer gebruikers de bewerking met deze configuratie openen, wordt hen gevraagd orders te zoeken of om een keuze te maken uit een vooraf gedefinieerd orderfilter.
- **Af te handelen orders**: wanneer een gebruiker de bewerking start, wordt automatisch een query uitgevoerd om een lijst met orders te zoeken en weer te geven die door de winkel moeten worden afgehandeld. Deze orders worden geconfigureerd om te worden opgehaald in de winkel of om vanuit de winkel te worden verzonden en de regels van deze orders zijn nog niet verzameld of verpakt.
- **Op te halen orders**: wanneer een gebruiker de bewerking start, wordt automatisch een query uitgevoerd om een lijst met orders te zoeken en weer te geven die zijn geconfigureerd om te worden opgehaald in de huidige winkel van de gebruiker.
- **Te verzenden orders**: wanneer een gebruiker de bewerking start, wordt automatisch een query uitgevoerd om een lijst met orders te zoeken en weer te geven die zijn geconfigureerd voor verzending vanuit de huidige winkel van de gebruiker.

Als de weergave is ingesteld op **Geen** , kan een gebruiker op een van de volgende manieren orders zoeken en ophalen bij het starten van de bewerking **Order intrekken**.
- Streepjescodes van orders scannen. Hiermee wordt gezocht naar overeenkomsten in de velden voor ordernummer, kanaalverwijzing en ontvangst-ID.
- Selecteer **Orders zoeken** of het pictogram **Zoeken en filteren** op de AppBar om het filtermechanisme te gebruiken om orders te vinden die voldoen aan de filtercriteria.
- Maak een keuze uit een vooraf gedefinieerd filter in het vervolgkeuzemenu **Orders weergeven** (af te handelen orders, op te halen orders of te verzenden orders).

![RecallOrderMainMenu](media/recallordermain.png)

Nadat de zoekcriteria zijn toegepast, wordt in de toepassing een lijst met overeenkomende verkooporders weergegeven.

![RecallOrderDetail](media/orderrecalldetail.png)

Een gebruiker kan een order in de lijst selecteren om aanvullende details weer te geven. In het informatievenster aan de rechterkant van het scherm worden specifieke gegevens over de geselecteerde order weergegeven, waaronder orderregeldetails, leveringsdetails en afhandelingsinformatie.

Via de Appbar kan een gebruiker een bewerking selecteren. Afhankelijk van de status van de order kunnen bepaalde bewerkingen niet worden ingeschakeld.

- **Retourneren**: hiermee wordt een retour uitgevoerd voor een of meer facturen die aan de geselecteerde klantorder zijn gerelateerd.

- **Annuleren**: hiermee wordt een volledige annulering van de geselecteerde verkooporder uitgegeven.

- **Afhandelen**: hiermee wordt de gebruiker overgebracht naar de pagina Order afhandelen die vooraf wordt gefilterd voor de geselecteerde order. Alleen orderregels die open zijn voor afhandeling door de winkel van de gebruiker voor de geselecteerde order worden weergegeven.

- **Bewerken**: hiermee kunnen gebruikers wijzigingen aanbrengen in de geselecteerde klantorder.

- **Ophalen**: hiermee wordt de ophaalstroom gestart zodat de gebruiker de producten kan kiezen die moeten worden opgehaald, en wordt de verkooptransactie voor ophalen gemaakt.
