---
title: Overzicht van geavanceerde bankafstemming
description: Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en automatisch afstemmen op banktransacties in Microsoft Dynamics 365 voor bewerkingen.  In dit artikel worden de instellingsregels voor afstemming uitgelegd.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Overzicht van geavanceerde bankafstemming

Geavanceerde bankafstemming kunt u elektronische bankafschriften importeren en automatisch afstemmen op banktransacties in Microsoft Dynamics 365 voor bewerkingen.  In dit artikel worden de instellingsregels voor afstemming uitgelegd.  

Er zijn een aantal onderdelen die moeten worden ingesteld voordat u de functie voor geavanceerde bankafstemming. Zie voor meer informatie over het instellen van het importeren van bankafschriften [het importproces bank overzicht instellen](set-up-advanced-bank-reconciliation-import-process.md).  Vereisten voor het instellen van het afstemmingsproces worden hieronder beschreven.

## <a name="transaction-codes"></a>Transactiecodes
Transactiecodes kunnen worden gebruikt als onderdeel van de bankafstemming toewijzingsregels.  Transactiecodes helpt bij de dezelfde typen transacties tussen Dynamics 365 for Operations en uw bankafschrift.  Om dit type aanpassing doet, moet u eerst transactietypes die worden gebruikt voor banktransacties van Dynamics 365 voor bewerkingen definiëren en deze documenttypen toewijzen aan transactiecodes van bankafschriften die door uw bank gebruikt.  Transactietypen voor Dynamics 365 voor banktransacties bewerkingen zijn gedefinieerd op de **banktransactietype** pagina.  Dit is ook waar u de hoofdrekening moet worden gebruikt voor boekingen die zijn gekoppeld aan deze transactietype definiëren. 

Als uw Dynamics 365 voor bewerkingen bank transactiecodes zijn gedefinieerd, vervolgens wijst u deze aan de transactiecodes gebruikt in uw elektronische bankafschriften.  Dit toewijzingsproces wordt uitgevoerd met behulp van de **toewijzing van transactiecode** pagina.  Toewijzing van transactiecode krijgt afzonderlijk voor elke bankrekening.

## <a name="matching-rules-and-matching-rule-sets"></a>Afstemmingsegels en sets met afstemmingsregels
Overeenkomende regels kunnen u criteria definiëren voor automatische afstemming tussen Dynamics 365 voor bewerkingen banktransacties en bankafschrifttransacties.  Instellen van de overeenkomende regels wordt uitgevoerd op **afstemmingsregels** pagina.  Zie voor meer informatie [toewijzingsregels bankafstemming instellen](set-up-bank-reconciliation-matching-rules.md). 

Sets met regels worden gebruikt om een groep van de overeenkomende regels die in volgorde worden uitgevoerd tijdens het afstemmingsproces bank te definiëren.  Sets met regels zijn geconfigureerd op de **afstemming afstemmingsregel** pagina.

## <a name="cash-and-bank-management-parameters"></a>Parameters voor Contanten en bankbeheer
Er gelden een aantal parameters voor het afstemmingsproces geavanceerde bank op de **parameters voor Cash- en bankbeheer** pagina.  De **weergeven overzicht regelbedrag in debet/credit** wijzigt u de weergave van bedragen op de **bankafschrift** pagina.  Als deze optie is ingeschakeld, wordt de transactiebedragen voor bank-instructie weergegeven in afzonderlijke debet en credit-kolommen.  Als niet is ingeschakeld, wordt de transactiebedragen voor bank-instructie weergegeven in een enkel bedragkolom met het juiste teken. 

De Validatieopties instellen op de pagina parameters overschrijven de selecties die zijn ingesteld op de toewijzingsregels.  Zo kan niet handmatig of automatisch overeenkomen met documenten die verdergaan dan het datumverschil is ingesteld op de pagina parameters.  Ook als de optie voor **valideren toewijzing transactietype** is ingeschakeld, moeten de transactietypen worden toegewezen tussen de Dynamics 365 voor bewerkingen banktransactie en bankafschrifttransactie om de transacties handmatig of automatisch worden vergeleken. 

Ook moet u de benodigde nummerreeksen op de **parameters voor Cash- en bankbeheer** pagina.  Op de **nummerreeksen** nummerreekscodes instellen voor het downloaden van het tabblad **-ID, het overzichts-ID, afstemmen-ID en Bank-Afstemming** verwijzingen.

## <a name="bank-account-reconciliation-options"></a>Afstemmingsopties voor bankrekeningen
Geavanceerde bankafstemming voor de bankrekening, moet u eerst inschakelen.  Een aantal extra opties beschikbaar zijn op de **bankrekening** pagina als de functie voor geavanceerde bankafstemming is ingeschakeld. 

**Bankafschriften gebruiken als bevestiging van elektronische betaling** functionaliteit is geïntegreerd in de functie voor bankafstemming elektronische betaling statussen.  Wanneer deze optie is ingeschakeld, bankdocument automatisch worden gemaakt voor de elektronische betaling-status is ingesteld op **verzonden**.  Bovendien wordt de status van een elektronische betaling worden bijgewerkt vanuit **verzonden** naar **ontvangen** nadat de betaling wordt vereffend, afgestemd en worden geboekt. 

De **de naam van de bankrekening in overzichten** veld is de naam die wordt gebruikt voor de bankrekening op uw elektronische bankafschriften.  Deze naam wordt gebruikt wanneer wordt bepaald welke transacties importeren voor een bankrekening met een overzicht met informatie voor meerdere bankrekeningen. 

De optie voor **afstemmen na importeren** wordt automatisch het bankafschrift valideren, een nieuwe bankafstemming en een werkblad maken en de standaard set met afstemmingsregels uitvoeren.  Deze functie automatiseert het proces tot het punt van de transacties die handmatig moet worden afgestemd.  De instelling op de bankrekening wordt standaard bij het importeren.


