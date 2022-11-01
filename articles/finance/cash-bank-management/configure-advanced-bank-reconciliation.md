---
title: Instellingsproces van geavanceerde bankafstemming
description: Met Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en deze automatisch afstemmen met banktransacties in Microsoft Dynamics 365 Finance. In dit artikel worden de instellingsregels voor afstemming uitgelegd.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e9a1757f7901a12a5b0fc3de730953c5b79cbefb
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715410"
---
# <a name="advanced-bank-reconciliation-setup-process"></a>Instellingsproces van geavanceerde bankafstemming

[!include [banner](../includes/banner.md)]

Met Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en deze automatisch afstemmen met banktransacties in Microsoft Dynamics 365 Finance. In dit artikel worden de instellingsregels voor afstemming uitgelegd.  

Er moet een aantal onderdelen worden ingesteld voordat u de functie voor geavanceerde bankafstemming kunt gebruiken. Zie [Het importproces voor geavanceerde bankafstemming instellen](set-up-advanced-bank-reconciliation-import-process.md) voor meer informatie over het instellen van de import van bankafschriften.  Vereisten voor het instellen van het afstemmingsproces worden hieronder gedetailleerd beschreven.

## <a name="transaction-codes"></a>Transactiecodes
Transactiecodes kunnen worden gebruikt als onderdeel van de afstemmingsregels voor bankafstemming. Met transactiecodes kunnen alleen dezelfde typen transacties tussen Finance en uw bankafschrift gemakkelijker worden afgestemd. Voor dit type afstemming moet u eerst transactietypen definiëren die worden gebruikt voor banktransacties van Finance en deze typen vervolgens afstemmen met transactiecodes voor afschriften die door uw bank worden gebruikt. Transactietypen voor banktransacties worden gedefinieerd op de pagina **Banktransactietype**. Op deze pagina definieert u ook de hoofdrekening die moet worden gebruikt voor boekingen die zijn gekoppeld aan dit transactietype. 

Zodra uw banktransactiecodes zijn gedefinieerd, wijst u deze vervolgens toe aan de transactiecodes die worden gebruikt in uw elektronische bankafschriften. Dit toewijzingsproces wordt uitgevoerd met behulp van de pagina **Toewijzing van transactiecode**. Toewijzing van transactiecodes wordt afzonderlijk voor elke bankrekening uitgevoerd.

## <a name="matching-rules-and-matching-rule-sets"></a>Afstemmingsegels en sets met afstemmingsregels
Met afstemmingsregels kunt u criteria definiëren voor automatische afstemming tussen Finance-banktransacties en -bankafschrifttransacties. Instellen van afstemmingsregels wordt uitgevoerd op de pagina **Afstemmingsregels**. Zie [Afstemmingsregels voor bankafstemming instellen](set-up-bank-reconciliation-matching-rules.md) voor meer informatie. 

Sets met afstemmingsregels worden gebruikt om een groep afstemmingsregels te definiëren die achtereenvolgens worden uitgevoerd tijdens het bankafstemmingsproces.  Sets met afstemmingsregels worden geconfigureerd op de pagina **Sets met regels voor afstemmingsregel**.

## <a name="cash-and-bank-management-parameters"></a>Parameters voor Contanten en bankbeheer
Er geldt een aantal parameters specifiek voor het geavanceerde afstemmingsproces voor bankafschriften op de pagina **Parameters voor Contanten en bankbeheer**.  Met **Afschriftregelbedrag tonen in debet/credit** wordt de weergave van bedragen gewijzigd op de pagina **Bankafschrift**. Als deze optie is ingeschakeld, worden de transactiebedragen voor bankafschriften weergegeven in afzonderlijke debet- en creditkolommen. Als deze optie niet is ingeschakeld, worden de transactiebedragen voor bankafschriften weergegeven in één bedragkolom met het juiste teken. 

De validatieopties die zijn ingesteld op de pagina met parameters overschrijven de selecties die zijn ingesteld op de afstemmingsregels. U kunt bijvoorbeeld documenten die buiten het op de parameterpagina ingestelde datumverschil vallen, niet handmatig of automatisch afstemmen. Ook als de optie **Toewijzing van transactietype valideren** is ingeschakeld, moeten de transactietypen worden afgestemd tussen de Finance-banktransactie en -bankafschrifttransactie zodat de transacties handmatig of automatisch kunnen worden afgestemd. 

Ook moet u de benodigde nummerreeksen op de pagina **Parameters voor Contanten en bankbeheer** configureren.  Stel op het tabblad **Nummerreeksen** de nummerreekscodes in voor de verwijzingen **Download-ID, Afschrift-ID en Bankafstemming**.

## <a name="bank-account-reconciliation-options"></a>Afstemmingsopties voor bankrekeningen
Eerst moet u Geavanceerde bankafstemming voor de bankrekening inschakelen. Er is een aantal extra opties beschikbaar op de pagina **Bankrekening** zodra de functionaliteit voor geavanceerde bankafstemming is ingeschakeld. 

Met de functionaliteit **Bankafschriften gebruiken als bevestiging van elektronische betaling** wordt de functie voor bankafstemming met elektronische betalingsstatussen geïntegreerd. Wanneer deze optie is ingeschakeld, wordt er automatisch een bankdocument gemaakt voor de elektronische betalingsstatus die is ingesteld op **Verzonden**. Bovendien wordt de status van een elektronische betaling bijgewerkt van **Verzonden** in **Ontvangen** nadat de betaling is toegewezen, afgestemd en geboekt. 

Het veld **Bankrekeningnaam op afschriften** is de naam die wordt gebruikt voor de bankrekening op uw elektronische bankafschriften. Deze naam wordt gebruikt wanneer wordt bepaald welke transacties voor een bankrekening moeten worden geïmporteerd van een overzicht dat informatie kan bevatten voor meerdere bankrekeningen. 

Met de optie **Afstemmen na importeren** wordt automatisch het bankafschrift gevalideerd, worden een nieuwe bankafstemming en werkblad gemaakt en wordt de standaardset met afstemmingsregels uitgevoerd. Met deze functionaliteit wordt het proces geautomatiseerd tot het moment dat de transacties handmatig moeten worden afgestemd. De instelling op de bankrekening wordt standaard overgenomen bij het importeren.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
