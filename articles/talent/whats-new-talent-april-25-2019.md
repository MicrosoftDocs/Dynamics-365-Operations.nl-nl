---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (23 april 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 04/23/2019
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
ms.search.validFrom: 2019-04-23
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5ec10820761cb22cbff6229babe8a250848214b7
ms.sourcegitcommit: 15154b0aa86110ce5fad6f63e6763103a676a1d2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/10/2019
ms.locfileid: "1624576"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-april-23-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (23 april 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract
Deze versie bevat kleine correcties voor Dynamics 365 for Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard
Deze versie bevat kleine correcties voor Dynamics 365 for Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR
Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2253. Getallen tussen haakjes verwijzen naar ondersteuningsnummers in Lifecycle Services (LCS).

### <a name="common-data-service-entity-support-for-custom-fields"></a>Ondersteuning van Common Data Service-entiteiten voor aangepaste velden
Bij de release van deze week ondersteunen de volgende entiteiten aangepaste velden: Compensatieniveau, Vergoedingsoptie, Vaardigheidstype en Compensatieregio.

### <a name="additional-odata-entities-302992"></a>Aanvullende OData-entiteiten (302992)
De volgende entiteiten worden nu ondersteund in OData: Beroepservaring van werknemer en Opleiding van werknemer.
   
### <a name="performance-journal-attachments-for-managers-and-employees-308248"></a>Bijlagen voor prestatielogboek voor managers en werknemers (308248)
In deze versie zijn er bijlagen beschikbaar voor zowel managers als werknemers bij het maken en bijwerken van journaalposten voor prestaties.

### <a name="employee-rehire-flag-always-available-310047"></a>Vlag voor het opnieuw aanstellen van werknemers altijd beschikbaar (310047)
De optie voor het opnieuw in dienst nemen van werknemers is nu beschikbaar om te worden bijgewerkt buiten het ontslagproces. 

### <a name="cannot-change-the-name-of-my-payment-method-308815"></a>De naam van **Mijn betalingsmethode** kan niet worden gewijzigd (308815)
Personalisatie is ingeschakeld zodat het label **Mijn betalingsmethode** kan worden gewijzigd in Selfservice werknemer.

### <a name="financial-dimensions-against-a-position-cant-be-deleted-293908"></a>Financiële dimensies voor een positie kunnen niet worden verwijderd (293908)
Financiële dimensies kunnen nu worden verwijderd bij het aanvragen van een wijziging voor een bestaande positie en de financiële dimensies overschrijden bedrijfsgrenzen. 

### <a name="customer-is-unable-to-publish-back-data-into-talent-when-opening-the-data-from-excel-302955"></a>Klant kan geen gegevens naar Talent publiceren bij het openen van de gegevens vanuit Excel (302955)
Deze wijziging corrigeert een publicatieprobleem bij gebruik van gerelateerde tabellen.

## <a name="in-preview"></a>Preview

### <a name="allow-reason-codes-to-be-specified-on-leave-types"></a>Toestaan dat redencodes voor verloftypen worden opgegeven
Organisaties hebben mogelijk extra informatie over verlofaanvragen nodig. U kunt nu redencodes voor verloftypen opgeven en mogelijk maken dat werknemers een redencode in hun verlofaanvragen selecteren.

### <a name="require-reason-codes-for-certain-leave-types-on-time-off-requests"></a>Redencodes voor bepaalde verloftypen vereisen voor verlofaanvragen
Organisaties kunnen redencodes vereisen voor specifieke verloftypen wanneer werknemers verlofaanvragen indienen. Dit kan te maken hebben met bedrijfsbeleid of wettelijke vereisten. U kunt nu opgeven welke verloftypen een redencode vereisen en u kunt vereisen dat werknemers een redencode opgeven voor het verloftype in hun verlofaanvragen.

### <a name="provide-leave-and-absence-transaction-list-for-hr"></a>Lijst met verlof- en afwezigheidstransacties verschaffen voor HRM
Door verlof van werknemers bij te houden en inzicht te krijgen in de berekening van verlof helpt HR niet alleen bij het beantwoorden van werknemersvragen, maar zorgt tevens voor nauwkeurige verloftoekenningen voor werknemers. HR heeft nu een nieuwe weergave om de transacties te bekijken (toekenningen, toerekeningen, correcties en aanvragen) om de redenen te zien achter saldi.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="improvements-to-the-user-interface-for-duplicate-employee-check"></a>Verbeteringen in de gebruikersinterface voor controle op dubbele werknemers
Met deze wijziging worden dubbele records gedetecteerd wanneer u naamvelden invoert en met een status wordt het aantal dubbelen weergegeven. U kunt de opgegeven koppeling selecteren om een nieuwe pagina te openen om te beoordelen of de gedetecteerde overeenkomst moet worden gebruikt. Om te voorkomen dat gegevensinvoer wordt onderbroken, wordt het formulier met dubbele records niet automatisch geopend.
## <a name="known-issues"></a>Bekende problemen

### <a name="email-support-for-alerts"></a>E-ondersteuning voor waarschuwingen
Met platformupdate 26 kunnen gebruikers waarschuwingsregels maken waarmee automatisch e-mailmeldingen worden verzonden naar contactpersonen wanneer deze door een gebeurtenis worden geactiveerd.
