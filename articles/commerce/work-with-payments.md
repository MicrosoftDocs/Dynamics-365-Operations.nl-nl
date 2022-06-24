---
title: Betalingsmethoden in callcenters
description: In dit artikel komen de verschillende betalingsmethoden aan bod die u in een callcenter in Dynamics 365 Commerce kunt gebruiken.
author: josaw1
ms.date: 03/28/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MCRSalesTableOrderHistory, MCRCCAuthManagement
audience: Application User
ms.reviewer: josaw
ms.custom: 92163
ms.assetid: 8e738907-870b-466c-ab0c-07f4a4aa47f3
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 7f47b6865f408a1dc833dcf15fc254ef8b802bcc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902706"
---
# <a name="payment-methods-in-call-centers"></a>Betalingsmethoden in callcenters

[!include [banner](includes/banner.md)]

In Dynamics 365 Commerce omvat de configuratie van het callcenterkanaal een instelling met de naam **Ordervoltooiing inschakelen**. Deze instelling zorgt ervoor dat alle orders die gebruikers van het kanaal maken, alleen voor orderverwerking worden vrijgegevens als ze hebben vooraf zijn betaald of vooraf zijn geautoriseerd voor betaling binnen de goedgekeurde marges. Als de instelling **Ordervoltooiing inschakelen** is ingeschakeld, kunnen gebruikers van het callcenter betalingen voor de verkooporders van klanten invoeren met behulp van de functies voor betalingsverwerking van het callcenter. Als de instelling is uitgeschakeld, kunnen callcentergebruikers de betalingsverwerkingsfuncties van het callcenter niet gebruiken, maar kunnen ze nog wel vooruitbetalingen voor verkooporders toepassen met behulp van standaardfunctionaliteit van Klanten.

Als onderdeel van de kanaalconfiguratie kan een bedrijf de betalingsmethoden definiëren die zijn toegestaan voor een callcenterkanaal. Het callcenterkanaal gebruikt de dezelfde betalingsmethoden die zijn gedefinieerd voor de kanalen voor de winkel.

Als u de betalingsmethoden voor een callcenterkanaal wilt configureren, gaat u naar **Detailhandel en commerce** \> **Kanalen** \> **Callcenters** \> **Alle callcenters** en selecteert u in het menu **Instellen** de optie **Betalingsmethoden**.

Wanneer u een betalingsmethode maakt, zijn er vijf betalingsmethodefuncties die u kunt toewijzen.

| Functie            | Omschrijving |
|---------------------|-------------|
| Normaal              | Gebruik de functie **Normaal** op uw betalingsmethode bij het definiëren van betalingsmethoden zoals contant of boekstukken. Wanneer deze soorten betalingen worden toegepast op een verkooporder in het callcenter, is de vlag **Vooruitbetalen** standaard ingesteld op **Ja**. Hierdoor wordt onmiddellijk een vooruitbetaling naar de klantrekening geboekt wanneer deze order wordt ingediend. Gebruikers kunnen de vlag **Vooruitbetalen** indien gewenst wijzigen in **Nee**, zodat het betalingsboekstuk pas wordt gemaakt als de factuur wordt geboekt. De vooruitbetaling wordt geboekt in de transactiehistorie van de klant waarin deze systematisch wordt vereffend met de factuur voor de verkooporder. |
| Controle               | Gebruik de functie **Cheque** wanneer u een bankcheque definieert als een vorm van betaling. Wanneer dit type betaling wordt toegepast op een verkooporder, moet de gebruiker het chequenummer van de klant invoeren bij het verwerken van de betalingstoepassing. Chequebetalingen worden altijd behandeld als vooruitbetalingen wanneer deze worden toegepast en betalingsboekstukken worden direct bij orderindiening gemaakt. Deze vooruitbetalingsboekstukken worden systematisch vereffend met de facturen die worden gemaakt voor de order. |
| Kaarten               | Betalingstypen met kaart verwijzen naar alle soorten betaling waarvoor invoer van een kaartnummer is vereist dat is gedefinieerd op de betaalkaart van de klant. Voorbeelden zijn creditcards en geschenkbonnen. Wanneer u deze betalingstypen configureert, gebruikt u het menu **Kaartinstellingen** voor het definiëren van de kaart-id's die zijn gekoppeld aan deze betalingsmethode. Bij het invoeren van orders kunnen gebruikers aangeven of de kaartbetaling vooruit wordt betaald, met behulp van de optie **Vooruitbetalen** die wordt weergegeven op de pagina voor het invoeren van de betaling. Tenzij het bedrijf vooruitbetalingen verplicht stelt, is de normale stroom van een creditcardbetaling een tweeledig proces, waarbij toestemming wordt verkregen op het moment van de orderinvoer en de betaling vervolgens wordt vereffend en verzameld via de klantenkaart op het moment van facturering. Vooruitbetaling wordt aanbevolen voor betalingen met geschenkbonnen, omdat het saldo van de geschenkbon onmiddellijk wordt verminderd zodat de klant dezelfde waarde niet ergens anders gebruiken. |
| Klant            | De functie **Klant** voor een betalingsmethode houdt in dat de betaling wordt toegepast op de kredietlimiet van de klant of 'op de rekening' wordt gezet. In Commerce kan aan een klant een kredietlimiet zijn toegewezen die kan worden gevalideerd op het moment van orderinvoer. Betalingen die zijn gemaakt met behulp van een betalingsmethode die is gekoppeld aan de functie **Klant** creëren een verplichting ten aanzien van de klantrekening. Wanneer de verkooporder wordt gefactureerd, wordt een openstaand saldo weergegeven. In dergelijke situaties sturen klanten meestal een betaling volgens de afgesloten voorwaarden. U kunt ook kan een eerder openstaand creditboekstuk op rekening van de klant toepassen om het verschuldigde saldo te vereffenen. Houd er rekening mee dat zelfs als u deze betalingsmethode definieert, deze niet wordt weergegeven tussen de betalingsopties in de orderinvoer van het callcenter, tenzij de markering **Op rekening toestaan** is ingesteld voor de klantrecord waarmee u werkt. Deze markering bevindt zich op het tabblad **Standaardwaarden betalingen** van het klantrecord. |
| Betalingsmethode verwijderen/wisselgeld | De functie **Betalingsmethode verwijderen/wisselgeld** wordt niet gebruikt door het callcenter. Dit geldt alleen wanneer u de betalingsmethoden definieert die door de verkooppunttoepassing (POS) in een winkelkanaal worden gebruikt. |

Wanneer betalingsmethoden worden gedefinieerd, moeten ze worden gekoppeld aan een grootboekrekening of een bankrekening. Als u deze stap overslaat, ontvangen gebruikers fouten tijdens het opslaan van het betalingstype.

## <a name="refund-payment-methods"></a>Betalingsmethoden voor restitutie

Voor de verwerking van de restitutiescenario's gebruikt het callcenter verder betalingsmethoden die worden gedefinieerd in de module Klanten. Als u deze betalingsmethoden configureert, gaat u naar **Detailhandel en commerce** \> **Kanaalinstelling** \> **Instellingen van callcenter** \> **Restitutiemethoden van callcenter**. U kunt deze configuratie voltooien om cheques voor terugbetalingen aan klanten uit te voeren. Bijvoorbeeld: als een klant oorspronkelijk voor een order heeft betaald met contant geld of een cheque, wil de gebruiker misschien een restitutiecheque verzenden via de module Klanten. In dit geval moeten de kas- en chequebetalingstypen in het callcenter worden toegewezen aan de juiste betalingsmethode in de module Klanten om te zorgen dat de restitutie correct wordt s verwerkt.

Bovendien als een gebruiker een retourorder verwerkt als een callcentergebruiker in Commerce, maar de gebruiker de retour niet kan koppelen aan een oorspronkelijke verkoop, moet de betalingsmethode **Retour** worden gedefinieerd in de callcenterparameters. Ga naar **Detailhandel en commerce** \> **Kanaalinstelling** \> **Instellingen van callcenter** \> **Parameters van callcenter** en zorg dat op het tabblad **Retourorder/Retour** in het veld **Betalingsmethode** een betalingsmethode is gedefinieerd. De betalingsmethode is de betalingsmethode die wordt gebruikt voor terugbetalingen. Deze wordt normaal gesproken gedefinieerd als een chequemethode of een klantbetalingsmethode.


[!INCLUDE[footer-include](../includes/footer-banner.md)]