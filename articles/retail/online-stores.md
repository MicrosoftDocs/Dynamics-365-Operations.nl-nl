---
title: Online winkeloverzicht
description: Dit artikel bevat informatie over onlinewinkels en hoe ze in Microsoft Dynamics 365 for Retail worden ingesteld.
author: kfend
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 16161
ms.assetid: 646d560c-f856-4701-b4ca-44e357ef09b8
ms.search.region: Global
ms.search.industry: Retail
ms.author: meeram
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 13d7f99766dabf35b80e7100a3017308033e3da6
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="online-store-overview"></a>Online winkeloverzicht

[!include[banner](includes/banner.md)]


Dit artikel bevat informatie over onlinewinkels en hoe ze in Microsoft Dynamics 365 for Retail worden ingesteld.

Dynamics 365 for Retail ondersteunt meerdere detailhandelskanalen. Deze detailhandelskanalen zijn o.a. online winkels, call centers en winkels (ook fysieke winkels genoemd). Een online winkel zorgt ervoor dat een detailhandelaar online is zodat hun klanten producten zowel in hun online winkel als in de fysieke winkel kunnen kopen. Als klanten producten in de online winkel kopen, kunnen deze producten bij hen worden bezorgd of kunnen zij ze ophalen bij een plaatselijke detailhandelwinkel. U maakt een online winkel in de Dynamics 365 for Retail-client. Deze online winkel wordt vervolgens gepubliceerd naar een online winkel van een derde partij die met Dynamics 365 for Retail is geïntegreerd. De online winkel van de derde partij is de UI voor de online winkel en biedt diverse klantbeheersysteem (CMS)- en UI-mogelijkheden. Verschillende integraties van dit type zijn beschikbaar voor Dynamics 365 for Retail. De eigenschappen die u definieert voor de online winkel bepalen de werking van de online winkel. U kunt bijvoorbeeld de navigatiecategoriehiërarchie bepalen in Dynamics 365 for Retail en deze toewijzen aan de online winkel. Bij het publiceren van de online winkel naar de online winkel van de derde partij, wordt de navigatiecategoriehiërarchie weergegeven in de online versie van de winkel. Kopers gebruiken vervolgens de navigatiecategoriehiërarchie om in de online winkel naar producten te zoeken. Om een online winkel te maken, moet u de onderdelen instellen waarmee transacties voor de winkel worden verwerkt. Bijvoorbeeld: u moet assortimenten toevoegen, kenmerken toepassen en verzendwijzen en betalingsmethoden instellen. U kunt ook prijzen, promoties, kortingen, handelsovereenkomsten en verzendvoorwaarden bepalen die specifiek zijn voor de online winkel. Nadat de online winkel is gepubliceerd naar de online winkel van de derde partij, kunt u de productcatalogi maken voor de online winkel. De producten in de catalogus worden productaanbiedingen in de online winkel. Wanneer een klant producten uit de online winkel koopt, wordt de beschikbare voorraad bijgewerkt en gesynchroniseerd in de client. Ook worden verkooporders gegenereerd voor de aankopen en verzonden naar de client voor verwerking en afhandeling van de orders.

## <a name="set-up-an-online-store"></a>Een online winkel instellen
Voor het instellen van een online winkel moet u de volgende taken voltooien.

1.  Maak de online winkel.
2.  Voeg de online winkel toe aan de juiste organisatiehiërarchieën.
3.  Voeg productassortimenten toe met de producten die beschikbaar zijn in de online winkel.
4.  Maak prijsgroepen of wijs deze toe voor de online winkel.
5.  Stel de leveringsmethoden in die beschikbaar zijn voor de online winkel.
6.  Wijs de betalingsmethoden toe die worden aanvaard door de online winkel.
7.  Als kopers producten online mogen bestellen en deze vervolgens ophalen in een lokale winkel, kunt u winkellocatorgroepen toewijzen aan de online winkel.
8.  Kenmerken voor kanalen, producten en verkooporders toewijzen aan de online winkel. Kanaalkenmerken gelden voor de hele online winkel, productkenmerken gelden voor de producten die worden aangeboden in de online winkel en verkooporderkenmerken gelden voor de verkooporders die zijn gegenereerd uit de online winkel.
9.  Wijs kenmerken toe om de eigenschappen in te stellen die bepalen hoe die kenmerken in de online winkel werken. U kunt bijvoorbeeld bepalen dat kenmerken vereist zijn of dat er op kenmerken kan worden gezocht.
10. Publiceer de online winkel om de winkelstructuur op uw keuze van online winkel van een derde partij te genereren. **Belangrijk:** Voordat u de online winkel kunt publiceren, moet u een distributielocatie voor de online winkel instellen.

## <a name="retail-channel-navigation-hierarchies"></a>Hiërarchieën voor detailhandelafzetkanaalnavigatie
Voordat u een online winkel maakt, moet u de detailhandelskanaalnavigatiehiërarchie bepalen die u wilt gebruiken voor de online winkel. De detailhandel navigatiehiërarchie vertegenwoordigt de categoriehiërarchie die in de online winkel wordt weergegeven nadat de winkel is gepubliceerd. Wanneer u detailhandelsproductcatalogi in de online winkel publiceert, worden de producten in de catalogus gekoppeld aan de categorieën in de detailhandelskanaalnavigatiehiërarchie. Kopers gebruiken de hiërarchie om te navigeren in de online winkel.

## <a name="organization-hierarchies"></a>Organisatiehiërarchieën
Organisatiehiërarchieën worden gebruikt om detailhandelskanalen structuur te geven. Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat. Bij het instellen van online winkels, kunt u ze toevoegen aan een organisatiehiërarchie. De winkels delen vervolgens de gegevens die worden gebruikt voor assortimenten, aanvulling en rapportering. Wanneer u een organisatiehiërarchie maakt, kent u er een doelstelling aan toe. Het doel geeft aan hoe de hiërarchie in de bedrijfsstructuur wordt gebruikt. U kunt een organisatiehiërarchie maken voor uw winkels en die hiërarchie gebruiken voor assortimenten, aanvulling en rapportering. U kunt ook een afzonderlijke organisatiehiërarchie maken voor elk doel. U kunt ook meerdere hiërarchieën maken met hetzelfde doel en een apart kanaal toewijzen aan elk van deze. Als u detailhandelsproductcatalogi wilt publiceren naar de online winkel, moet u de online winkel ten minste toevoegen aan een organisatiehiërarchie voor assortimenten. De producten in een catalogus zijn geselecteerd uit de assortimenten die zijn toegewezen aan de online winkel. Wanneer de catalogus wordt gepubliceerd, vergelijkt het publicatieproces de ingangsdatums voor het assortiment dat is toegewezen aan de online winkel met producten die zijn opgenomen in de catalogus om te bepalen welke producten in de online winkel beschikbaar moeten zijn.




