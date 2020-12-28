---
title: Nieuwe of gewijzigde functies in Dynamics 365 Talent (9 juli 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-07-09
ms.dyn365.ops.version: Talent
ms.openlocfilehash: feb39966d98fa7bde9a6bfad26b07fbd224da59b
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528025"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-july-9-2019"></a>Nieuwe of gewijzigde functies in Dynamics 365 Talent (9 juli 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

### <a name="coming-soon-in-attract"></a>Binnenkort in Attract

#### <a name="job-approvals-appear-on-the-home-page"></a>Functiegoedkeuringen worden weergegeven op de startpagina

Goedkeuringen worden weergegeven in de sectie **Goedkeuringen** op het dashboard. Fiatteurs kunnen hun goedkeuringen controleren onder **Aan u toegewezen**, waar de taak-ID, functietitel, andere fiatteurs en de toewijzingsdatum worden weergegeven. Gebruikers die een functie ter goedkeuring indienen, kunnen hun functies controleren onder **Aangevraagd door u**, waar de fiatteurs worden weergegeven die de ingediende functie nog moeten goedkeuren.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2374.

### <a name="platform-update-28-for-finance-and-operations"></a>Platformupdate 28 voor Finance and Operations

Zie voor meer details over platformupdate 28 voor Finance and Operations [Voorbeeldfuncties in Dynamics 365 Finance and Operations platformupdate 28 (juli 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-28).

### <a name="entity-support-for-custom-fields-in-common-data-service"></a>Entiteitsondersteuning voor aangepaste velden in Common Data Service 

De volgende entiteiten ondersteunen aangepaste velden: 

- **Vastecompensatieplan**
- **Instelling van compensatiereferentiepunten**
- **Regel voor instellen van compensatiereferentiepunten**
- **Inkomstencode salaris**
- **Salarisperiode**
- **Gebeurtenis voor vaste compensatie**
- **Compensatieraster**

Alle bijgewerkte entiteiten in Talent weergeven:

1. Selecteer **Systeembeheer**, **Koppelingen** en **Common Data Service-configuratie**.
2. Selecteer het vervolgkeuzemenu **CDS-entiteitsnaam**. Alle vermelde entiteiten hebben betrekking op de meest recente versie. 

###  <a name="full-name-added-to-worker-entity-in-common-data-service"></a>Volledige naam toegevoegd aan entiteit Medewerker in Common Data Service

Het veld **Volledige naam** is toegevoegd aan de entiteit **Medewerker**.

### <a name="full-time-equivalent-higher-than-10"></a>Full-time equivalent groter dan 1,0

Er wordt nu een waarschuwing weergegeven als een waarde hoger dan 1,0 wordt ingevoerd voor een fulltime medewerker op een positie. 

### <a name="a-warning-no-longer-displays-on-the-worker-page-when-there-is-no-future-dated-employment"></a>Er wordt geen waarschuwing meer weergegeven op de medewerkerspagina wanneer er geen toekomstige aanstelling is.

U ontvangt geen bericht meer met de mede deling dat er een toekomstige aanstelling bestaat wanneer u naar de pagina **Medewerker** navigeert vanuit de lijst **Vertrekkende medewerkers** in het werkgebied **Personeelsbeheer**. 

### <a name="unable-to-delete-a-business-process-in-talent"></a>Een bedrijfsproces kan niet worden verwijderd in Talent

U kunt bedrijfsprocessen nu verwijderen in het werkgebied **Bedrijfsproces**.

### <a name="leave-balance-no-longer-displays-zero-for-plans-with-no-accruals-when-using-balance-as-of-accrual-period"></a>Voor verlofsaldo wordt niet meer nul weergegeven voor plannen zonder toerekeningen bij gebruik van Saldo vanaf toerekenperiode

Voor plannen die zijn ingesteld zonder toerekeningen kan nu een saldo worden weergegeven.

## <a name="in-preview"></a>Preview

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Preview-functies zijn alleen ingeschakeld in sandbox-exemplaren

Wanneer u een nieuw exemplaar van Talent inricht, kunt u opgeven of het exemplaartype **Productie** of **Sandbox** is. In exemplaren van het type **Sandbox** kunnen nieuwe functies vroegtijdig worden getest. Alle bestaande exemplaren van Talent worden bijgewerkt naar het exemplaartype **Productie**. Als u wilt dat een van de bestaande exemplaren wordt bijgewerkt naar het exemplaartype **Sandbox**, neemt u contact op met de [ondersteuning](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) om de wijzigingsaanvraag te initiëren.

Zie [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) voor meer informatie over hoe wijzigingen worden gepubliceerd.

### <a name="restrict-leave-types-in-time-off-requests"></a>Verloftypen in verlofaanvragen beperken

Organisaties kunnen veel verschillende verloftypen aanbieden aan werknemers. Sommige verloftypen zijn mogelijk niet geschikt voor werknemers . Deze verloftypen kunnen in plaats daarvan door HR worden beheerd. In deze versie kunt u configureren voor welke typen verlof werknemers verlofaanvragen kunnen indienen. 

## <a name="coming-soon-in-core-hr"></a>Binnenkort in Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Uitgebreide informatie over prestaties in de selfservice-functionaliteit voor managers weergeven

Met een nieuwe optie kunnen managers de prestaties van hun directe en indirecte ondergeschikten weergeven. Op dit moment kunnen lijnmanagers prestatiedoelstellingen toewijzen en bijwerken, en nieuwe beoordelingen uitgeven die mede worden beheerd door hun werknemers. Bovendien kunnen directe leidinggevenden en hun werknemers prestatiejournalen onderhouden en bijwerken om ervoor te zorgen dat het proces voor prestatiebeoordelingen soepel verloopt. Wanneer deze wijziging is geïmplementeerd, kunnen managers prestatiegerelateerde gegevens weergeven en beheren voor indirecte en directe ondergeschikten. 

### <a name="entities-supporting-custom-fields"></a>Entiteiten die aangepaste velden ondersteunen

De volgende entiteiten worden ingeschakeld voor aangepaste velden in Common Data Service: 

- **Verloftype**
- **Bankrekening medewerker**
- **Werkkalender**
