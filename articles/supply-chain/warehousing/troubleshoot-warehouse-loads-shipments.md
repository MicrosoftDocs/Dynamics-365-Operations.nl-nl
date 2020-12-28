---
title: Problemen met ladingopbouw en zendingen oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met ladingopbouw en zendingen in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645327"
---
# <a name="troubleshoot-load-building-and-shipments"></a>Problemen met ladingopbouw en zendingen oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met ladingopbouw en zendingen in Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a>Het volgende foutbericht wordt weergegeven: "U kunt geen ladingsregel maken voor deze orderregel omdat deze voorraaddimensies bevat die ongeldig zijn...'

### <a name="issue-description"></a>Probleembeschrijving

Het volgende foutbericht wordt weergegeven wanneer u een retourverkooporder probeert vrij te geven aan het magazijn:

> U kunt geen ladingsregel maken voor deze orderregel omdat deze voorraaddimensies bevat die ongeldig zijn. U kunt niet verwijzen naar voorraaddimensies die zich onder de locatiedimensie in de reserveringshiërarchie bevinden. Verwijder de ongeldige dimensies uit de orderregel.

### <a name="issue-resolution"></a>Probleemoplossing

Helaas ondersteunt het product geen ladingsverwerking voor een verkoopretourproces. Daarom kunt u de retourverkooporder niet vrijgeven aan het magazijn.

Op verkoopordertransacties kunt u niet verwijzen naar voorraaddimensies die zich onder de **Locatie**-dimensie in de reserveringshiërarchie bevinden. Verwijder de ongeldige dimensies uit de orderregel om het probleem op te lossen.

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a>Het volgende fout bericht wordt weergegeven: "Een van de regels bevindt zich al in een lading. Vrijgeven aan magazijn is niet mogelijk."

### <a name="issue-description"></a>Probleembeschrijving

Als u handmatig taken maakt of als u het proces zo instelt dat er al ladingen zijn gemaakt voordat de verkooporderregel wordt ingevoerd, is de veronderstelling dat de volgende vrijgave handmatig wordt uitgevoerd en dat de route en beoordeling van de lading wordt gebruikt.

In een ander mogelijk scenario probeert u een automatische vrijgave aan het magazijn uit te voeren, maar tijdens het waveproces kan er geen werk worden gemaakt. Daarom wordt toch een openstaande zending of lading gemaakt. Deze openstaande zending of lading blokkeert vervolgens alle pogingen om de order automatisch vrij te geven, totdat u de openstaande zending of lading verwijdert of de wave handmatig opnieuw verwerkt.

### <a name="issue-resolution"></a>Probleemoplossing

U kunt alleen vrijgeven vanaf de verkooporderpagina of automatische vrijgave uitvoeren vanaf de vrijgaveverkooporderpagina als er geen lading bestaat voorafgaand aan de vrijgave aan het magazijn. De lading wordt automatisch gemaakt nadat de wave is verwerkt.

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a>Het volgende foutbericht wordt weergegeven: "De correctie van het afleveringsbewijs kan niet worden verwerkt. Het afleveringsbewijs bevat alleen artikelen die onder magazijnbeheerprocessen vallen, aangezien deze niet worden ondersteund door afleveringsbewijscorrectie."

### <a name="issue-description"></a>Probleembeschrijving

Nadat u een afleveringsbewijs hebt geboekt, kunt u deze niet meer annuleren, omdat de knop **Annuleren** niet beschikbaar is. U kunt het afleveringsbewijs ook niet corrigeren. Als u dat probeert, wordt dit foutbericht weergegeven.

### <a name="issue-resolution"></a>Probleemoplossing

Als u geboekte pakbonnen wilt corrigeren voor artikelen die zijn ingeschakeld voor geavanceerd magazijnbeheer (WMS), moet u de boeking uitvoeren vanuit de lading, niet rechtstreeks vanuit de order.

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a>Hoe kan ik werk maken vanuit uitgaande ladingen in plaats van waves?

### <a name="issue-description"></a>Probleembeschrijving

Dit is een manier om dit probleem te reproduceren.

1. Maak een uitgaande lading met een verkooporde of een transferorder.
2. Geef de lading vrij naar het magazijn.
3. U ziet dat er nog geen orderverzamelingwerk is gegenereerd.

### <a name="issue-resolution"></a>Probleemoplossing

Als werk onmiddellijk moet worden gegenereerd wanneer de lading wordt vrijgegeven, moet u de wavesjabloon dienovereenkomstig configureren. Stel op de wavesjabloon de volgende opties in op *Ja*:

- Het maken van waves automatiseren
- Wave verwerken bij vrijgave door magazijn
- Vrijgave wave automatiseren

## <a name="i-cant-re-release-a-partially-shipped-load"></a>Ik kan een gedeeltelijk verzonden lading niet opnieuw vrijgeven.

### <a name="issue-description"></a>Probleembeschrijving

U kunt een gedeeltelijk verzonden lading niet vrijgeven aan het magazijn. Wanneer u de vrijgave aan het magazijn uitvoert, wordt er een bericht weergegeven dat de bewerking is voltooid, maar gebeurt er niets en wordt er geen werk gemaakt voor de resterende hoeveelheid. Dit probleem treedt op wanneer u de transportladingsfunctie gebruikt en er een onvolledige reservering is.

### <a name="issue-resolution"></a>Probleemoplossing

[KB-probleem 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Gedeeltelijk verzonden ladingen kunnen opnieuw in een wave worden geplaatst en verwerkt") is in [release 10.0.15 gecorrigeerd](../get-started/whats-new-scm-10-0-15.md).
