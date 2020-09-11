---
title: Ondersteunde scenario's met instellingen voor twee keer wegschrijven
description: In dit onderwerp worden de scenario's beschreven die worden ondersteund voor instellingen voor twee keer wegschrijven.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 08/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 275d24d8f32fd1d2d15356d14c5c6591e8503c65
ms.sourcegitcommit: ec4df354602c20f48f8581bfe5be0c04c66d2927
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/19/2020
ms.locfileid: "3706247"
---
# <a name="supported-scenarios-for-dual-write-setup"></a>Ondersteunde scenario's met instellingen voor twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

U kunt een verbinding voor twee keer wegschrijven instellen tussen een Finance and Operations-omgeving en een Common Data Service-omgeving.

+ Een **Finance and Operations-omgeving** levert het onderliggende platform voor **Finance and Operations-apps** (bijvoorbeeld Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management en Dynamics 365 Retail).
+ Een **Common Data Service-omgeving** biedt het onderliggende platform voor **modelgestuurde apps in Dynamics 365** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 Field Service, Dynamics 365 Marketing en Dynamics 365 Project Service Automation).

>[!IMPORTANT]
>Human resources in Finance and Operations ondersteunt dual-write-verbindingen, maar de Dynamics 365 Human Resources-app ondersteunt dat niet.

Het installatiemechanisme varieert afhankelijk van uw abonnement en de omgeving.

+ Voor nieuwe exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven met Microsoft Dynamics Lifecycle Services (LCS). Als u een licentie hebt voor Microsoft Power Platform, krijgt u een nieuwe Common Data Service-omgeving als uw tenant er geen heeft.
+ Voor bestaande exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven in de Finance and Operations-omgeving.

De volgende scenario's met instellingen worden ondersteund:

+ [Een nieuw Finance and Operations-app-exemplaar en een nieuw, model gestuurd app-exemplaar](#new-new)
+ [Een nieuw Finance and Operations-app-exemplaar en een bestaand, model gestuurd app-exemplaar](#new-existing)
+ [Een nieuw Finance and Operations-app-exemplaar met demogegevens en een nieuw, model gestuurd app-exemplaar](#new-demo-new)
+ [Een nieuw Finance and Operations-app-exemplaar met demogegevens en een bestaand, model gestuurd app-exemplaar](#new-demo-existing)
+ [Een bestaand Finance and Operations-app-exemplaar en een nieuw of bestaand, model gestuurd app-exemplaar](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-model-driven-app-instance"></a><a id="new-new"></a>Een nieuw Finance and Operations-app-exemplaar en een nieuw, model gestuurd app-exemplaar

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een nieuw exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md). Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:

- Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.
- Er wordt een nieuw, leeg exemplaar van een modelgestuurde app ingericht, waarbij de CRM Prime-oplossing wordt geïnstalleerd.
- Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.
- Entiteitstoewijzingen worden ingeschakeld voor live migratie.

Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-model-driven-app-instance"></a><a id="new-existing"></a>Een nieuw Finance and Operations-app-exemplaar en een bestaand, model gestuurd app-exemplaar

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een bestaand exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md). Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:

- Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.
- Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.
- Entiteitstoewijzingen worden ingeschakeld voor live migratie.

Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.

Voer de volgende stappen uit om de bestaande Common Data Service-gegevens te synchroniseren met de Finance and Operations-app.

1. Maak een nieuw bedrijf maken in de Finance and Operations-app.
2. Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.
3. [Laad](bootstrap-company-data.md) de Common Data Service-gegevens automatisch met de ISO-bedrijfscode (International Organization for Standardization) van drie letters.

Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-a-new-model-driven-app-instance"></a><a id="new-demo-new"></a>Een nieuw Finance and Operations-app-exemplaar met demogegevens en een nieuw, model gestuurd app-exemplaar

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met demogegevens en een nieuw exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in de sectie [Een nieuw Finance and Operations-app-exemplaar en een nieuw modelgestuurd app-exemplaar](#new-new) dat eerder in dit onderwerp is beschreven. Wanneer de verbinding is voltooid en u de demogegevens wilt synchroniseren met de modelgestuurde app, voert u de volgende stappen uit.

1. Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.
2. Voer de functie **Initiële synchronisatie** uit voor de entiteiten waarvoor u gegevens wilt synchroniseren.

## <a name="a-new-finance-and-operations-app-instance-that-has-demo-data-and-an-existing-model-driven-app-instance"></a><a id="new-demo-existing"></a>Een nieuw Finance and Operations-app-exemplaar met demogegevens en een bestaand, model gestuurd app-exemplaar

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met demogegevens en een bestaand exemplaar van een modelgestuurde app in Dynamics 365, volgt u de stappen in de sectie [Een nieuw Finance and Operations-app-exemplaar en een bestaand modelgestuurd app-exemplaar](#new-existing) dat eerder in dit onderwerp is beschreven. Wanneer de verbinding is voltooid en u de demogegevens wilt synchroniseren met de modelgestuurde app, voert u de volgende stappen uit.

1. Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.
2. Voer de functie **Initiële synchronisatie** uit voor de entiteiten waarvoor u gegevens wilt synchroniseren.

Voer de volgende stappen uit om de bestaande Common Data Service-gegevens te synchroniseren met de Finance and Operations-app.

1. Maak een nieuw bedrijf maken in de Finance and Operations-app.
2. Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.
3. [Laad](bootstrap-company-data.md) de Common Data Service-gegevens automatisch met de ISO-bedrijfscode van drie letters.

Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-or-existing-model-driven-app-instance"></a><a id="existing-existing"></a>Een bestaand Finance and Operations-app-exemplaar en een nieuw of bestaand, model gestuurd app-exemplaar

Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaand exemplaar van een Finance and Operations-app en een nieuw of bestaand exemplaar van een modelgestuurde app in Dynamics 365 vindt plaats in de Finance and Operations-omgeving.

1. Stel de verbinding in vanuit de Finance and Operations-app.
2. Als u de bestaande Common Data Service-gegevens wilt synchroniseren met de Finance and Operations-app, [laadt](bootstrap-company-data.md) u de Common Data Service-gegevens automatisch met de ISO-bedrijfscode van drie letters.

Omdat voor twee keer wegschrijven wordt uitgevoerd in de modus voor live synchronisatie, beginnen de Common Data Service-gegevens automatisch te stromen naar de Finance and Operations-app.
