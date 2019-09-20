---
title: Wat is nieuw of gewijzigd in Dynamics 365 for Talent (6 mei 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 05/06/2019
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
ms.search.validFrom: 2019-05-06
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c541bac532e878c8493a60d95c05c9104d4b96e1
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741539"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-may-6-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 for Talent (6 mei 2019)

[!include [banner](includes/banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

### <a name="select-optional-documents-upon-offer-creation"></a>Optionele documenten selecteren bij het maken van aanbiedingen

Wanneer u een sjabloon voor een aanbiedingspakket selecteert, wordt u nu in Attract gevraagd om de toepasselijke, optionele documenten uit die pakketsjabloon te selecteren. U kunt andere optionele documenten toevoegen tijdens het voorbereiden van de aanbieding.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2282. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="platform-update-26"></a>Platformupdate 26

Zie voor aanvullende details over platformupdate 26 [Voorbeeldfuncties in Dynamics 365 for Finance and Operations platformupdate 26 (april 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-26). 

### <a name="common-data-service-entity-support-for-custom-fields"></a>Ondersteuning van Common Data Service-entiteiten voor aangepaste velden

In de release van deze week ondersteunen de volgende entiteiten nu aangepaste velden: Berekeningsfrequentie vergoeding, Berekeningstarief vergoeding, Vergoedingstype, Werkkalender, Werkkalender feestdag, Betalingscyclus en Identificatietypen werknemer.

### <a name="leave-mass-enrollment-changing-the-tier-basis-to-seniority-date-doesnt-refresh-the-initial-accrual-rate-318526"></a>Als bij massa-inschrijving de laagbasis wordt gewijzigd in "Anciënniteitsdatum datum", wordt het initiële toerekeningstarief niet vernieuwd (318526)

Wanneer u werknemers massaal inschrijft en de laagbasis wijzigt, komt het initiële toerekeningstarief nu overeen met de geselecteerde laagbasis.

### <a name="workflow-showing-duplicate-place-holders-313636"></a>Werkstroom bevat dubbele tijdelijke aanduidingen (313636)

Wijzigingen in deze release maken een einde aan duplicering van tijdelijke aanduidingen bij het verzenden van werkstroommeldingen.

### <a name="dimension-fields-arent-updated-when-using-open-in-excel-176261"></a>Dimensievelden worden niet bijgewerkt bij gebruik van "Openen in Excel" (176261)

Met deze versie kunt u nu de financiële dimensie bijwerken via **Openen in Excel** vanaf de pagina **Werknemer**. 

### <a name="worker-address-created-in-common-data-service-isnt-synced-to-talent-317555"></a>Het adres van een werknemer dat is gemaakt in Common Data Service wordt niet gesynchroniseerd met Talent (317555)

Bij deze wijziging worden adressen die in Common Data Service zijn gemaakt, bijgewerkt in Talent Core HR.


## <a name="in-preview"></a>Preview

### <a name="new-page-to-validate-position-hierarchy-data"></a>Nieuwe pagina voor validatie van positiehiërarchiegegevens

Human Resources (HR) en beheerders kunnen nu de managementhiërarchie valideren voor kringverwijzingen die per ongeluk zijn geïmporteerd. U kunt deze nieuwe pagina openen vanuit **Organisatiebeheer > Koppelingen > Posities > Validatie van positiehiërarchie**.

### <a name="specify-reason-codes-on-leave-types"></a>Redencodes opgeven voor verloftypen

Organisaties hebben mogelijk extra informatie over verlofaanvragen nodig. U kunt nu redencodes voor verloftypen opgeven en toestaan dat werknemers een redencode in hun verlofaanvragen selecteren.

### <a name="require-reason-codes-for-specific-leave-types-on-time-off-requests"></a>Redencodes voor specifieke verloftypen vereisen voor verlofaanvragen

Organisaties vereisen wellicht redencodes voor specifieke verloftypen wanneer werknemers verlofaanvragen indienen. Deze vereiste kan bestaan vanwege bedrijfsbeleid of wettelijke vereisten. U kunt nu opgeven welke verloftypen een redencode vereisen en u kunt vereisen dat werknemers een redencode opgeven voor het verloftype in hun verlofaanvragen.

### <a name="provide-a-leave-and-absence-transaction-list-for-hr"></a>Een lijst met verlof- en afwezigheidstransacties verschaffen voor HR

De mogelijkheid om verlof van werknemers bij te houden en inzicht te krijgen in de berekening van verlof helpt HR niet alleen bij het beantwoorden van werknemersvragen, maar helpt tevens nauwkeurige verloftoekenningen voor werknemers te waarborgen. HR heeft nu een nieuwe weergave om de transacties te bekijken (toekenningen, toerekeningen, correcties en aanvragen) zodat HR-medewerkers de redenen achter saldi kunnen bekijken.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="indicate-instance-type-when-provisioning-talent"></a>Exemplaartype aangeven bij het inrichten van Talent

Bij het inrichten van een nieuw exemplaar van Talent kunt u aangeven of het exemplaartype **Productie** of **Sandbox** is, waardoor nieuwe functies vroegtijdig kunnen worden getest. Alle bestaande exemplaren van Talent worden bijgewerkt naar het exemplaartype Productie. Als u wilt dat een van de bestaande exemplaren wordt bijgewerkt naar het exemplaartype Sandbox, neemt u contact op met de ondersteuning om de wijzigingsaanvraag te initiëren.
