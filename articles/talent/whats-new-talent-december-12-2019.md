---
title: Wat is nieuw of gewijzigd in Dynamics 365 Talent (10 december 2019)
description: In dit artikel worden de functies beschreven die nieuw of gewijzigd zijn in Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 12/10/2019
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
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 18f86f5d87b780d5d4ffc83330d389077987dda6
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4528166"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-december-10-2019"></a>Wat is nieuw of gewijzigd in Dynamics 365 Talent (10 december 2019)

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp worden de functies beschreven die nieuw of gewijzigd zijn in Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Wijzigingen in Attract

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Attract.

## <a name="changes-in-onboard"></a>Wijzigingen in Onboard

Deze versie bevat kleine correcties voor Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Wijzigingen in Core HR

Wijzigingen die worden beschreven in deze sectie, gelden voor buildnummer 8.1.2660. De getallen tussen haakjes in sommige koppen verwijzen naar ondersteuningsnummers in Microsoft Dynamics Lifecycle Services (LCS).

### <a name="feature-management-workspace"></a>Werkgebied Functiebeheer

Het werkgebied **Functiebeheer** bevat een lijst met functies die in elke versie worden geleverd. Nieuwe functies zijn standaard uitgeschakeld. U kunt het werkgebied gebruiken om deze in te schakelen en de bijbehorende documenten weer te geven. Zie [Overzicht Functiebeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview)voor meer informatie over Functiebeheer.

Alle nieuwe functies behouden gedurende minimaal 30 dagen en doorgaans 30-60 dagen de previewstatus. De belangrijkste functies zijn over het algemeen beschikbaar in oktober en april van elk jaar na de previewperiode. Zodra u nieuwe functies in het werkgebied **Functiebeheer** ziet, kunt u deze inschakelen. Sommige functies zijn mogelijk standaard ingeschakeld.
 
Soms is een integrale functie standaard ingeschakeld en kan deze niet worden uitgeschakeld (bijvoorbeeld het werkgebied **Functiebeheer**).
 
Als een functie algemeen beschikbaar is, kan deze worden in- of uitgeschakeld in productieomgevingen. Het werkgebied **Functiebeheer** geeft aan wanneer een preview-functie verplicht wordt. Deze datum is gewoonlijk 1 oktober of 1 april, in overeenstemming met de halfjaarlijkse releaseplannen. U kunt verplichte functies niet uitschakelen. Tot de functie verplicht wordt, kunt u deze in alle omgevingen in- of uitschakelen.

### <a name="streamlined-worker-form-has-moved-to-the-feature-management-workspace-390583"></a>Het gestroomlijnd werknemerformulier is verplaatst naar het werkgebied Functiebeheer (390583)

Met deze wijziging kan het gestroomlijnde werknemerformulier nu worden ingeschakeld in het werkgebied **Functiebeheer**. Deze functie is verplaatst van het formulier **Systeemparameters** in **Systeembeheer**.

### <a name="prevent-hcmworkerpayrollinfo-records-from-being-written-without-a-worker-value-394526"></a>Voorkomen dat HcmWorkerPayrollInfo-records worden geschreven zonder de werknemerswaarde (394526)

Met deze release worden **HcmWorkerPayrollInfo**-records niet meer gemaakt zonder verwijzing van de werknemer in dit scenario. 

### <a name="message-log-associated-to-the-action-isnt-populated-when-the-action-fails-to-complete-374007"></a>Berichtlogboek dat is gekoppeld aan de actie wordt niet ingevuld wanneer de actie niet wordt voltooid (374007)

Deze release bevat een wijziging om het logboek voor actieberichten in te vullen wanneer een actie in bepaalde scenario's mislukt. 

### <a name="common-data-service-integration-batch-job-creation-388030"></a>Het maken van batchtaken voor de integratie van Common Data Service (388030)

Met deze wijziging worden batchtaken voor Common Data Service-integratie gemaakt wanneer de service wordt ingeschakeld.

### <a name="additional-pick-list-values-to-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a>Aanvullende orderverzamellijstwaarden in aangepaste velden worden niet weergegeven in Common Data Service nadat u op Toepassen hebt geklikt in het formulier Aangepaste velden (379599)

Met deze wijziging worden nieuwe orderverzamellijstwaarden ingevoerd in Talent nu gesynchroniseerd met Common Data Service wanneer u uw wijzigingen toepast.

### <a name="update-to-common-data-service-for-then-leave-bank-transaction-entity-turns-into-an-insert-on-talent-side-352938"></a>Bijwerken naar Common Data Service voor de transactie-entiteit Bank verlaten wordt een invoeging in Talent (352938)

Deze wijziging corrigeert een probleem waarbij een update voor een transactie Bank verlaten een nieuwe record maakt in Talent.

## <a name="in-preview"></a>Preview

Preview-functies zijn alleen beschikbaar in **Sandbox**-omgevingen.

### <a name="print-performance-reviews"></a>Prestatiebeoordelingen afdrukken

Zie [Beoordelingen van afdrukprestaties](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in het Dynamics 365: releasewave 2-plan van 2019.

