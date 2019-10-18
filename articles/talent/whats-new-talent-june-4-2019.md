---
title: Nieuwe of gewijzigde functies in Dynamics 365 Talent (4 juni 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 06/04/2019
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
ms.search.validFrom: 2019-06-04
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 32b168eca210b1371db129c05f7035237eb35c38
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/23/2019
ms.locfileid: "2008979"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-june-4-2019"></a>Nieuwe of gewijzigde functies in Dynamics 365 Talent (4 juni 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="coming-soon-in-attract"></a>Binnenkort in Attract

### <a name="job-approvals-on-the-home-page"></a>Taakgoedkeuringen op de startpagina

Goedkeuringen worden weergegeven in de sectie **Goedkeuringen** op het dashboard. Fiatteurs kunnen hun goedkeuring beoordelen onder **Toegewezen aan u**. Deze sectie bevat de taak-id, titel, andere fiatteurs en de datum waarop de taak is toegewezen. Gebruikers die een taak ter goedkeuring indienen, kunnen hun taken controleren onder **Aangevraagd door u**. In deze sectie worden de fiatteurs weergegeven die de ingediende taak nog moeten goedkeuren.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

De wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2330.

### <a name="new-page-to-validate-position-hierarchy-data"></a>Nieuwe pagina voor validatie van positiehiërarchiegegevens

HR-medewerkers en beheerders kunnen de managementhiërarchie valideren voor kringverwijzingen die onbedoeld zijn geïmporteerd. U kunt deze nieuwe pagina openen via **Organisatiebeheer \> Koppelingen \> Posities \> Validatie van positiehiërarchie**.

### <a name="specify-reason-codes-on-leave-types"></a>Redencodes opgeven voor verloftypen

Organisaties hebben mogelijk extra informatie over verlofaanvragen nodig. U kunt nu redencodes voor verloftypen opgeven en toestaan dat werknemers een redencode in hun verlofaanvragen selecteren.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Redencodes voor specifieke verloftypen vereisen voor verlofaanvragen

Organisaties vereisen wellicht redencodes voor specifieke verloftypen wanneer werknemers verlofaanvragen indienen. Deze vereiste kan bestaan vanwege bedrijfsbeleid of wettelijke vereisten. U kunt opgeven welke verloftypen een redencode vereisen en u kunt vereisen dat werknemers een redencode opgeven voor het verloftype in hun verlofaanvragen.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Een lijst met verlof- en afwezigheidstransacties verschaffen voor HR

De mogelijkheid om verlof van werknemers bij te houden en inzicht te krijgen in de berekening van verlof helpt HR niet alleen bij het beantwoorden van werknemersvragen, maar helpt ook nauwkeurige verloftoekenningen voor werknemers te waarborgen. HR heeft nu een nieuwe weergave om de transacties te bekijken (toekenningen, toerekeningen, correcties en aanvragen) zodat HR-medewerkers de redenen achter verlofsaldi kunnen bekijken.

### <a name="deleting-a-record-from-talent-doesnt-remove-the-record-from-common-data-service"></a>Wanneer een record uit Talent wordt verwijderd, wordt deze niet verwijderd uit Common Data Service

Records die worden verwijderd uit Talent: Core HR, worden nu ook verwijderd uit Common Data Service.

### <a name="variable-compensation-plan-valid-fromto-dates-arent-being-honored"></a>Geldigheidsdatums van variabelecompensatieplannen worden niet gerespecteerd

In deze versie kunt u werknemer niet inschrijven voor een variabelecompensatieplan als de begindatum vóór de begindatum van het plan valt of als de einddatum na de einddatum van het plan valt. 

### <a name="performance-review-comments-are-removed-when-users-select-cancel"></a>Opmerkingen over prestatiebeoordelingen worden verwijderd wanneer gebruikers Annuleren selecteren

In deze versie is een probleem gecorrigeerd waarbij beoordelingsopmerkingen worden verwijderd als een gebruiker een opmerking begint te wijzigen, maar vervolgens **Annuleren** selecteert. 

## <a name="in-preview"></a>Preview

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Preview-functies zijn alleen ingeschakeld in sandbox-exemplaren

Wanneer u een nieuw exemplaar van Talent inricht, kunt u opgeven of het exemplaartype **Productie** of **Sandbox** is. In exemplaren van het type **Sandbox** kunnen nieuwe functies vroegtijdig worden getest. Alle bestaande exemplaren van Talent worden bijgewerkt naar het exemplaartype **Productie**. Als u wilt dat een van de bestaande exemplaren wordt bijgewerkt naar het exemplaartype **Sandbox**, neemt u contact op met de [ondersteuning](https://docs.microsoft.com/dynamics365/unified-operations/talent/talent-support) om de wijzigingsaanvraag te initiëren.

Zie [Talent inrichten](https://docs.microsoft.com/dynamics365/unified-operations/talent/provisioning-talent) voor meer informatie over hoe wijzigingen worden gepubliceerd.

### <a name="restrict-leave-types-in-time-off-requests"></a>Verloftypen in verlofaanvragen beperken

Organisaties kunnen veel verschillende verloftypen aanbieden aan werknemers. Sommige verloftypen zijn mogelijk niet geschikt voor werknemers . Deze verloftypen kunnen in plaats daarvan door HR worden beheerd. In deze versie kunt u configureren voor welke typen verlof werknemers verlofaanvragen kunnen indienen. 

## <a name="coming-soon-in-core-hr"></a>Binnenkort in Core HR

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Uitgebreide informatie over prestaties in de selfservice-functionaliteit voor managers weergeven

Met een nieuwe optie kunnen managers de prestaties van hun directe en indirecte ondergeschikten weergeven. Op dit moment kunnen lijnmanagers prestatiedoelstellingen toewijzen en bijwerken, en nieuwe beoordelingen uitgeven die mede worden beheerd door hun werknemers. Bovendien kunnen directe leidinggevenden en hun werknemers prestatiejournalen onderhouden en bijwerken om ervoor te zorgen dat het proces voor prestatiebeoordelingen soepel verloopt. Wanneer deze wijziging is geïmplementeerd, kunnen managers prestatiegerelateerde gegevens weergeven en beheren voor indirecte en directe ondergeschikten. 

### <a name="print-performance-reviews"></a>Prestatiebeoordelingen afdrukken

Werknemers, managers en HR kunnen de prestatiebeoordeling van een werknemer afdrukken.
