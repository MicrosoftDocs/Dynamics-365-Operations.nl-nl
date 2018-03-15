---
title: Voortschrijdend prognoserapport voor vaste activa
description: In dit onderwerp wordt uitgelegd hoe u het voortschrijdend prognoserapport voor vaste activa gebruikt.
author: saraschi2
manager: 
ms.date: 01/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 23021
ms.assetid: d7e86f72-95db-4423-9b04-761e9536a959
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-12-20
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 7a81697a8e90fb6b0695a02db0868f5708fdbddf
ms.contentlocale: nl-nl
ms.lasthandoff: 02/07/2018

---
# <a name="fixed-assets-roll-forward-report"></a>Voortschrijdend prognoserapport voor vaste activa

[!include[banner](../includes/banner.md)]

Het rapport **Voortschrijdend prognoserapport voor vaste activa** biedt in een gemakkelijk leesbare Microsoft Excel-indeling de gedetailleerde vaste activa-gegevens die u nodig hebt voor periodeafsluiting, financiële overzichten en btw-aangifte. Het rapport bevat begin- en eindsaldi voor vaste activa, samen met de waarderingsverplaatsingen voor de periode, en eventuele nieuwe activaverwervingen en -afstotingen die zijn opgetreden tijdens de periode. Gegevens worden voor afzonderlijke vaste activa gerapporteerd en waarden worden ook samengevat voor vaste-activagroepen en de rechtspersoon.

Het rapport **Voortschrijdend prognoserapport voor vaste activa** gebruikt het raamwerk voor elektronische aangifte (ER). Voordat u het rapport kunt uitvoeren, moeten de configuraties Vast activa-model en Voortschrijdende prognose voor vaste activa worden geïmporteerd vanuit Microsoft Dynamics Lifecycle Services (LCS). Zie voor instructies het onderwerp [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).

Dit rapport is beschikbaar in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3, of als een hotfix voor Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017). Drie hotfixes moeten worden toegepast op omgevingen met de release van juli 2017:

- **KB 4041754:** ER-configuratie (Elektronische Rapportage) kan niet worden gedownload van LCS, want niet van toepassing voor de huidige toepassingsversie na het toepassen van het platformupdatepakket
- **KB 4056107:** Cumulatieve ER-update (GER) 5
- **KB 4056353:** Rapporten met vaste activa-overzichten en -notities voldoen niet aan de vereisten in GAAP en IFRS

In de volgende tabel worden de velden beschreven die beschikbaar zijn in het rapport.

| Veld                                       | Omschrijving |
|---------------------------------------------|-------------|
| Saldi: opening                           | De vaste activa nettoboekwaarde vanaf de 'vanaf'-datum die is opgegeven in het rapport. |
| Saldi: afsluiting                           | De vaste activa nettoboekwaarde vanaf de 'tot'-datum die is opgegeven in het rapport. |
| Verwervingen: openingswaarde                 | De som van alle transacties van de typen **Verwerving** en **Verwervingscorrectie** tot aan de 'vanaf'-datum die is opgegeven in het rapport. |
| Verwervingen: periodeverwervingen           | De som van alle transacties van de typen **Verwerving** en **Verwervingscorrectie** die zijn geboekt tijdens het datumbereik voor het rapport. |
| Verwervingen: periodeafstotingen              | De som van alle verwervingsomkeringen die zijn geboekt en die een afstotingstransactie hadden tijdens het datumbereik van het rapport. |
| Verwervingen: afsluitingswaarde                 | De som van alle transacties van de typen **Verwerving** en **Verwervingscorrectie** tot aan de 'tot'-datum die is opgegeven in het rapport. |
| Afschrijvingen: openingswaarde                | De som van alle transacties van de typen **Afschrijving**, **Afschrijvingscorrectie**, **Speciale afschrijvingsaftrek** en **Buitengewone afschrijving** tot aan de 'vanaf'-datum die is opgegeven in het rapport. |
| Afschrijvingen: periodeafschrijvingen         | De som van alle transacties van de typen **Afschrijving**, **Afschrijvingscorrectie** en **Buitengewone afschrijving** die zijn geboekt tijdens het datumbereik voor het rapport. |
| Afschrijvingen: speciale periodeafschrijvingen | De som van alle transacties van het type **Speciale afschrijvingsaftrek** die zijn geboekt tijdens het datumbereik voor het rapport. |
| Afschrijvingen: periodeafstotingen             | De som van alle afschrijvingsomkeringen die zijn geboekt en die een afstotingstransacties hadden tijdens het datumbereik van het rapport. |
| Afschrijvingen: afsluitingswaarde                | De som van alle transacties van de typen **Afschrijving**, **Afschrijvingscorrectie**, **Speciale afschrijvingsaftrek** en **Buitengewone afschrijving** tot aan de 'tot'-datum die is opgegeven in het rapport. |
| Opwaarderingen/afwaarderingen: openingswaarde        | De som van alle transacties van de typen **Opwaarderingscorrectie**, **Afschrijvingscorrectie** en **Herwaardering** tot aan de 'vanaf'-datum die is opgegeven in het rapport. |
| Opwaarderingen/afwaarderingen: periodeopwaarderingen     | De som van alle transacties van het type **Opwaarderingscorrectie** die zijn geboekt tijdens het datumbereik voor het rapport. |
| Opwaarderingen/afwaarderingen: periodeafwaarderingen   | De som van alle transacties van het type **Afwaarderingscorrectie** die zijn geboekt tijdens het datumbereik voor het rapport. |
| Opwaarderingen/afwaarderingen: periodeherwaarderingen  | De som van alle transacties van het type **Herwaardering** die zijn geboekt tijdens het datumbereik voor het rapport. |
| Opwaarderingen/afwaarderingen: periodeafstotingen     | De som van alle opwaarderings-, afwaarderings- en herwaarderingsomkeringen die zijn geboekt en die een afstotingstransacties hadden tijdens het datumbereik van het rapport. |
| Opwaarderingen/afwaarderingen: afsluitingswaarde        | De som van alle transacties van de typen **Opwaarderingscorrectie**, **Afschrijvingscorrectie** en **Herwaardering** tot aan de 'tot'-datum die is opgegeven in het rapport. |
| Afstotingen: afstotingsdatum                    | De afstotingsdatum voor het vaste-activaboek. |
| Afstotingen: nettoboekwaarde bij afstoting       | De nettoboekwaarde van het vaste-activaboek op het moment van afstoting. |
| Afstotingen: verkoopwaarde                       | De verkoopwaarde voor het vaste-activaboek met een afstoting – verkooptransactie. |
| Afstotingen: uitvalwaarde                      | De uitvalwaarde voor het vaste-activaboek met een afstoting – uitvaltransactie. |
| Afstotingen: winst/verlies                      | De winst- of verlieswaarde die wordt berekend als onderdeel van de afstotingstransactie voor het vaste-activaboek. |

