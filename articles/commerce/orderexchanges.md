---
title: Een uitwisseling voor een retourorder configureren en verwerken
description: In dit artikel wordt uitgelegd hoe u een uitwisseling voor een retour configureert in Dynamics 365 Commerce.
author: josaw1
ms.date: 07/28/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: f33c674e4110b4e45ac58e499a65da2509b00046
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845787"
---
# <a name="configure-and-process-an-exchange-on-a-return-order"></a>Een uitwisseling voor een retourorder configureren en verwerken

[!include [banner](includes/banner.md)]

In eerdere versies van Dynamics 365 Commerce werden retouren van klantorders verwerkt op basis van het retourorderdocument in Headquarters. Het retourorderdocument kan echter alleen worden gebruikt om producten te verwerken die worden geretourneerd. De geretourneerde producten worden aangeduid met een negatieve hoeveelheid op de retourorderregels. De verkopen worden weergegeven met een positieve hoeveelheid. Het retourorderdocument ondersteunt echter geen positieve hoeveelheden. Vanwege deze beperking boden eerdere versies van de app geen ondersteuning voor scenario's waarin productuitwisselingen werden uitgevoerd met behulp van het retourorderdocument.

Er is echter functionaliteit toegevoegd om scenario's met uitwisselingen voor retourorders te ondersteunen. In Commerce wordt in plaats van het retourorderdocument nu het verkooporderdocument gebruikt voor de verwerking van deze typen transacties.

## <a name="configure-commerce-to-support-exchanges-on-return-orders"></a>Commerce configureren om uitwisseling te ondersteunen voor retourorders

> [!NOTE]
> In versie 10.0.20 en hoger van Commerce is een nieuwe functie beschikbaar met de naam Uniforme retourverwerkingservaring in POS. Als u deze functie inschakelt, zijn de onderstaande installatiestappen niet vereist. **Retouren verwerken als verkooporders** wordt een permanent geconfigureerde instelling en u kunt dit niet wijzigen.

Volg deze stappen om het systeem te configureren voor het ondersteunen van uitwisselingen op retourorders, als u de functie **Uniforme retourverwerkingservaring in POS** niet hebt ingeschakeld.

1. Ga naar **Retail en Commerce \> Instelling van hoofdkantoor \> Parameters \> Commerce-parameters**. Stel op het sneltabblad **Klantorders** de optie **Retourorders verwerken als verkooporders** in op **Ja**.
2. Voer de taak **Algemene configuratie distributieplanning** (**1110**) uit.

## <a name="make-an-exchange"></a>Uitwisselen

Wanneer het systeem is geconfigureerd op de wijze die wordt beschreven in de vorige sectie, selecteert de POS-gebruiker net als in vorige versies van de app een verkooporder of verkoopfactuur om een retour te verwerken. Wanneer de retourartikelen zijn toegevoegd aan de winkelwagen, kan de gebruiker echter ook nieuwe verkoopregels toevoegen aan de winkelwagen.

Voor deze nieuwe verkoopregels moet de gebruiker alle kenmerken opgeven die vereist zijn om een klantorderregel te verwerken. Deze kenmerken omvatten de leveringsmethode en afhandelingslocatie. Het verschuldigde transactiebedrag is het gecombineerde nettobedrag van de retour- en verkooporderregels. Wanneer voor de transactie wordt betaald, wordt de retourorder geboekt als een verkooporderdocument in Headquarters en worden de retourregels onmiddellijk gefactureerd.

Om beter inzicht te bieden in de verschillende bedragen voor de winkelwagen, zijn er drie nieuwe velden voor bedragen toegevoegd aan de winkelwagen. U kunt de schermontwerper gebruiken om deze nieuwe velden beschikbaar te maken in de POS-gebruikersinterface.

- **Deposito toegepast**: het depositobedrag dat op een transactie wordt toegepast wanneer de gebruiker een klantorder ophaalt. Als er geen deposito-overschrijving is ingesteld en een deposito van 10 procent is geconfigureerd, is het bedrag in dit veld 90 procent van het totaalbedrag van de klantorder.
- **Uitgevoerd bedrag**: het totale bedrag voor regels waarvoor de leveringsmethode was ingesteld op **Uitgevoerd** toen de klantorder werd gemaakt of bewerkt, of tijdens de uitwisseling van een klantorder. Het bedrag in dit veld is inclusief btw en toeslagen.
- **Geretourneerd bedrag**: het totaalbedrag voor regels met negatieve hoeveelheden tijdens de uitwisseling van een klantorder. Het bedrag in dit veld is inclusief btw en toeslagen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
