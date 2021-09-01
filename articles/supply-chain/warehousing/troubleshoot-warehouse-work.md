---
title: Problemen met magazijnwerk oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomend magazijnwerk in Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f9dbc1e043de5c8f840b291b652ec522c9f1eb6a622e8dab88ced3fa91570e8e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775454"
---
# <a name="troubleshoot-warehouse-work"></a>Problemen met magazijnwerk oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens werken met inkomend magazijnwerk in Microsoft Dynamics 365 Supply Chain Management.

## <a name="i-cant-move-license-plates-that-have-serial-number-items-when-blank-issue-and-blank-receipt-are-allowed-on-the-tracking-dimension-group"></a>Ik kan geen nummerplaten met serienummerartikelen verplaatsen als een lege uitgifte en een lege ontvangst zijn toegestaan in de traceringsdimensiegroep.

### <a name="issue-description"></a>Probleembeschrijving

U kunt een nummerplaat niet verplaatsen via een menuopdracht **Verplaatsing** als het serienummer instellingen heeft van *Lege uitgifte is toegestaan* en *Lege ontvangst toegestaan* in de traceringsdimensiegroep en als er meerdere nummerplaten op dezelfde locatie zijn, waarvan sommige serienummers hebben en andere niet.

### <a name="issue-resolution"></a>Probleemoplossing

Dit probleem wordt verholpen door wijzigingen die in [KB 4571546](https://fix.lcs.dynamics.com/Issue/Details?kb=4571546&bugId=467880&dbType=3&qc=5b46d7faa9cc326cebfe9854cb30be8ea30b21ef33d3572c325fbb21202de687) zijn geïmplementeerd. Deze wijzigingen maken het veld **Serienummer** optioneel als lege ontvangst en lege uitgifte zijn toegestaan.

## <a name="i-receive-the-following-error-message-in-the-warehouse-management-mobile-app-when-i-process-movements-the-inventory-owner-1-is-not-allowed-in-this-process"></a>Het volgende foutbericht wordt weergegeven in de mobiele app Magazijnbeheer bij het verwerken van verplaatsingen: "De voorraadeigenaar %1 is niet toegestaan in dit proces."

### <a name="issue-description"></a>Probleembeschrijving

De traceringsdimensie **Eigenaar** ontbreekt wanneer de mobiele app Magazijnbeheer wordt gebruikt om verplaatsingen te maken. Een normaal voorraadoverboekingjournaal van de Supply Chain Management-client lijkt te werken zoals bedoeld en kan alleen worden geboekt als de dimensie **Eigenaar** is ingevuld.

### <a name="issue-resolution"></a>Probleemoplossing

Microsoft heeft dit probleem beoordeeld en heeft vastgesteld dat het een functiebeperking is. Momenteel ondersteunt magazijnbeheer alleen voorraad die eigendom is van de rechtspersoon.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]