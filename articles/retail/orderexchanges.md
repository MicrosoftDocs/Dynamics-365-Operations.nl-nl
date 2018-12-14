---
title: Een uitwisseling voor een retourorder configureren en verwerken
description: In dit onderwerp wordt uitgelegd hoe een uitwisseling voor een retour configureert in Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 11/12/2018
ms.topic: index-page
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 3331b984693c58c6ee8c49b98ed7d3a8df5b79ff
ms.openlocfilehash: 45b628376a483d3d639e5c018dd93570ed8ce7af
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Een uitwisseling voor een retourorder configureren en verwerken

[!include [banner](includes/banner.md)]

In eerdere versies van Microsoft Dynamics 365 for Retail werden retouren van klantorders verwerkt op basis van het retourorderdocument in Detailhandel Hoofdkantoor. Het retourorderdocument kan echter alleen worden gebruikt om producten te verwerken die worden geretourneerd. De geretourneerde producten worden aangeduid met een negatieve hoeveelheid op de retourorderregels. De verkopen worden weergegeven met een positieve hoeveelheid. Het retourorderdocument ondersteunt echter geen positieve hoeveelheden. Vanwege deze beperking boden eerdere versies van Retail geen ondersteuning voor scenario's waarin productuitwisselingen werden uitgevoerd met behulp van het retourorderdocument.

Er is echter functionaliteit toegevoegd om scenario's met uitwisselingen voor retourorders te ondersteunen. In Retail wordt in plaats van het retourorderdocument nu het verkooporderdocument gebruikt voor de verwerking van deze typen transacties.

## <a name="configure-retail-to-support-exchanges-on-return-orders"></a>Retail configureren om uitwisseling te ondersteunen voor retourorders

Ga als volgt te werk om het systeem zo te configureren dat uitwisseling wordt ondersteund voor retourorders.

1. Ga naar **Detailhandel \> Instelling van hoofdkantoor \> Parameters \> Detailhandelparameters**. Stel op het sneltabblad **Klantorders** de optie **Retourorders verwerken als verkooporders** in op **Ja**.
2. Voer de taak **Algemene configuratie distributieplanning** (**1110**) uit.

## <a name="make-an-exchange"></a>Uitwisselen

Wanneer het systeem is geconfigureerd op de wijze die wordt beschreven in de vorige sectie, selecteert de POS-gebruiker net als in vorige versies van Retail een verkooporder of verkoopfactuur om een retour te verwerken. Wanneer de retourartikelen zijn toegevoegd aan de winkelwagen, kan de gebruiker echter ook nieuwe verkoopregels toevoegen aan de winkelwagen.

Voor deze nieuwe verkoopregels moet de gebruiker alle kenmerken opgeven die vereist zijn om een klantorderregel te verwerken. Deze kenmerken omvatten de leveringsmethode en afhandelingslocatie. Het verschuldigde transactiebedrag is het gecombineerde nettobedrag van de retour- en verkooporderregels. Wanneer voor de transactie wordt betaald, wordt de retourorder geboekt als een verkooporderdocument in Detailhandel Hoofdkantoor en worden de retourregels onmiddellijk gefactureerd.

Om beter inzicht te bieden in de verschillende bedragen voor de winkelwagen, zijn er drie nieuwe velden voor bedragen toegevoegd aan de winkelwagen. U kunt de schermontwerper gebruiken om deze nieuwe velden beschikbaar te maken in de POS-gebruikersinterface.

- **Deposito toegepast**: het depositobedrag dat op een transactie wordt toegepast wanneer de gebruiker een klantorder ophaalt. Als er geen deposito-overschrijving is ingesteld en een deposito van 10 procent is geconfigureerd, is het bedrag in dit veld 90 procent van het totaalbedrag van de klantorder.
- **Uitgevoerd bedrag**: het totale bedrag voor regels waarvoor de leveringsmethode was ingesteld op **Uitgevoerd** toen de klantorder werd gemaakt of bewerkt, of tijdens de uitwisseling van een klantorder. Het bedrag in dit veld is inclusief btw en toeslagen.
- **Geretourneerd bedrag**: het totaalbedrag voor regels met negatieve hoeveelheden tijdens de uitwisseling van een klantorder. Het bedrag in dit veld is inclusief btw en toeslagen.
