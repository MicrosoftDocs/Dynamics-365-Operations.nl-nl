---
title: Nieuwe of gewijzigde functies in Dynamics 365 for Talent (27 augustus 2019)
description: In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 8/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: andreabichsel
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-08-27
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 1d7e5be0d9ba5e372e57f06fec77326561196626
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/06/2019
ms.locfileid: "2899238"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-august-27-2019"></a>Nieuwe of gewijzigde functies in Dynamics 365 for Talent (27 augustus 2019)

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2447. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="preview-features-are-enabled-only-in-sandbox-instances"></a>Preview-functies zijn alleen ingeschakeld in sandbox-exemplaren

Wanneer u een nieuw exemplaar van Talent inricht, kunt u opgeven of het exemplaartype Productie of Sandbox is. In exemplaren van het type Sandbox kunnen nieuwe functies vroegtijdig worden getest. Alle bestaande exemplaren van Talent worden bijgewerkt naar het exemplaartype Productie. Als u wilt dat een van de bestaande exemplaren wordt bijgewerkt naar het exemplaartype Sandbox, neemt u contact op met de ondersteuning om de wijzigingsaanvraag te initiëren.

Zie [Talent inrichten](./provisioning-talent.md) voor meer informatie over hoe wijzigingen worden gepubliceerd.

### <a name="view-extended-information-for-performance-in-manager-self-service"></a>Uitgebreide informatie over prestaties in de selfservice-functionaliteit voor managers weergeven

Met een nieuwe optie kunnen managers de prestaties van hun directe en indirecte ondergeschikten weergeven. Op dit moment kunnen lijnmanagers prestatiedoelstellingen toewijzen en bijwerken, en nieuwe beoordelingen uitgeven. Bovendien kunnen directe leidinggevenden en hun werknemers prestatiejournalen onderhouden en bijwerken om ervoor te zorgen dat het proces voor prestatiebeoordelingen soepel verloopt. Wanneer deze wijziging is geïmplementeerd, kunnen managers prestatiegerelateerde gegevens weergeven en beheren voor indirecte en directe ondergeschikten.

### <a name="deleting-legal-entities-isnt-allowed-if-employees-exist-within-the-company-339849"></a>Het verwijderen van rechtspersonen is niet toegestaan als er werknemers bestaan in het bedrijf (339849)

Met deze wijziging kunt u bedrijven niet wissen of verwijderen als er werknemers en andere gerelateerde gegevens bestaan voor de rechtspersoon.

### <a name="compensation-management-business-intelligence-analytics-dont-match-on-the-compensation-workspace-322493"></a>De Business Intelligence-analytics voor compensatiebeheer komen niet overeen voor het compensatiewerkgebied (322493)

In deze versie zijn compensatie-analytics aangepast om de aan medewerkers toegewezen plannen nauwkeurig weer te geven.

### <a name="workflow-placeholder-company-displays-dat-when-hiring-employees-through-workflow-343905"></a>In de tijdelijke werkstroomaanduiding %company% wordt DAT weergegeven wanneer medewerkers worden aangenomen via de werkstroom (343905)

In deze versie wordt in de tijdelijke aanduiding voor het bedrijf de rechtspersoon weergegeven die aan het dienstverband van de nieuwe medewerker is gekoppeld.

### <a name="the-cdsjobposition-entity-displays-an-error-when-valid-to-date-is-set-349387"></a>De entiteit CDSJobPosition geeft een fout weer wanneer de einddatum voor geldigheid is ingesteld (349387)

In deze release kunnen de velden **Ingangsdatum** van de gegevensbronnen **Positiedetail** en **Positieduur** voor de entiteit **CDSJobPosition** worden bewerkt vanuit Common Data Service. 

### <a name="for-employee-termination-the-last-day-worked-is-populated-on-assignment-end-date-332496"></a>Voor beëindiging van het dienstverband van een medewerker wordt als laatste dag Einddatum van toewijzing ingevuld (332496).

Deze wijziging wordt in plaats van **Einddatum van toewijzing** nu standaard **Einddatum dienstverband** gebruikt. U kunt deze standaardinstellingen wijzigen tijdens het invoeren van gegevens.

### <a name="legal-entities-arent-limited-with-hire-338871"></a>Voor rechtspersonen bestaan geen aanstellingsbeperkingen (338871)
 
Door deze wijziging wordt het aanstellingsproces beperkt zodat alleen de rechts personen worden weergegeven waartoe de gebruiker toegang heeft.  

## <a name="in-preview"></a>Preview

### <a name="streamlined-employee-entry-and-navigation"></a>Gestroomlijnde invoer en navigatie voor werknemers

Deze functionaliteit is nu beschikbaar in sandbox- en proefomgevingen. Als u deze functie wilt inschakelen, navigeert u naar **Systeembeheer > Koppelingen > Instellingen > Systeemparameters > Voorbeeldfuncties**. Selecteer **Verbeterd medewerkersformulier en navigatie**. Hierdoor worden deze wijzigingen voor alle gebruikers ingeschakeld. U kunt deze optie op elk gewenst moment uitschakelen.

Zie [Gestroomlijnde invoer en navigatie voor werknemers](./streamlined-employee-entry.md) voor meer informatie.

## <a name="coming-soon"></a>Binnenkort beschikbaar

### <a name="platform-update-29"></a>Platformupdate 29

Zie voor meer details over platformupdate 29 [Voorbeeldfuncties in Dynamics 365 for Finance and Operations platformupdate 29 (oktober 2019)](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).
