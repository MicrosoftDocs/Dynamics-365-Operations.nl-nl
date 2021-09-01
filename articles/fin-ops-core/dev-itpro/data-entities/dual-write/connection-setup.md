---
title: Richtlijnen voor het instellen van twee keer wegschrijven
description: In dit onderwerp worden de scenario's beschreven die worden ondersteund voor instellingen voor twee keer wegschrijven.
author: RamaKrishnamoorthy
ms.date: 10/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: e4072ee29984a99742de8c99be5943fb0f07639bf3c1c969bf43b1ab7076fd5b
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6776626"
---
# <a name="guidance-for-dual-write-setup"></a>Richtlijnen voor het instellen van twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

U kunt een verbinding voor twee keer wegschrijven instellen tussen een Finance and Operations-omgeving en een Dataverse-omgeving.

+ Een **Finance and Operations-omgeving** levert het onderliggende platform voor **Finance and Operations-apps** (bijvoorbeeld Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce en Dynamics 365 Human Resources).
+ Een **Dataverse-omgeving** biedt het onderliggende platform voor **Customer Engagement-apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing en Dynamics 365 Project Service Automation).

> [!IMPORTANT]
> De module Human resources in Dynamics 365 Finance ondersteunt verbindingen voor twee keer wegschrijven, maar de Dynamics 365 Human Resources-app ondersteunt dat niet.

Het installatiemechanisme varieert afhankelijk van uw abonnement en de omgeving:

+ Voor nieuwe exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven met Microsoft Dynamics Lifecycle Services (LCS). Als u een licentie hebt voor Microsoft Power Platform, krijgt u een nieuwe Dataverse-omgeving als uw tenant er geen heeft.
+ Voor bestaande exemplaren van Finance and Operations-apps begint het instellen van een verbinding voor twee keer wegschrijven in de Finance and Operations-omgeving.

Voordat u twee keer wegschrijven voor een entiteit start, kunt u een initiële synchronisatie uitvoeren om bestaande gegevens aan beide zijden van Finance and Operations-apps en Customer Engagement-apps te verwerken. U kunt de initiële synchronisatie overslaan als u geen gegevens tussen de twee omgevingen hoeft te synchroniseren.

Met een initiële synchronisatie kunt u bestaande gegevens in twee richtingen van de ene naar de andere app kopiëren. Er zijn verschillende instellingsscenario's afhankelijk van de omgevingen die u al hebt en het type gegevens dat deze omgevingen bevatten.

De volgende scenario's met instellingen worden ondersteund:

+ [Een nieuw exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app](#new-new)
+ [Een nieuw exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app](#new-existing)
+ [Een nieuw exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app](#new-data-new)
+ [Een nieuw exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app](#new-data-existing)
+ [Een bestaand exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app](#existing-new)
+ [Een bestaand exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Een nieuw exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een nieuw exemplaar van een Customer Engagement-app, voert u de stappen uit in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md). Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:

- Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.
- Er wordt een nieuw, leeg exemplaar van een Customer Engagement-app ingericht, waarbij de CRM Prime-oplossing wordt geïnstalleerd.
- Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.
- Tabeltoewijzingen worden ingeschakeld voor live migratie.

Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Een nieuw exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app zonder gegevens en een bestaand exemplaar van een Customer Engagement-app, voert u de stappen uit in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md). Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:

- Er wordt een nieuwe, lege Finance and Operations-omgeving ingericht.
- Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.
- Tabeltoewijzingen worden ingeschakeld voor live migratie.

Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.

Voer de volgende stappen uit om de bestaande Dataverse-gegevens te synchroniseren met de Finance and Operations-app.

1. Maak een nieuw bedrijf maken in de Finance and Operations-app.
2. Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.
3. [Laad](bootstrap-company-data.md) de Dataverse-gegevens automatisch met de ISO-bedrijfscode (International Organization for Standardization) van drie letters.
4. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) verderop in dit onderwerp voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Een nieuw exemplaar van de Finance and Operations-app met gegevens en een nieuw exemplaar van de Customer Engagement-app

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met gegevens en een nieuw exemplaar van een Customer Engagement-app, voert u de stappen in de sectie [Een nieuw exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app](#new-new) eerder in dit onderwerp. Wanneer de verbinding is voltooid en u de gegevens wilt synchroniseren met de Customer Engagement-app, voert u de volgende stappen uit.

1. Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.
2. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Een nieuw exemplaar van de Finance and Operations-app met gegevens en een bestaand exemplaar van de Customer Engagement-app

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuw exemplaar van een Finance and Operations-app met gegevens en een bestaand exemplaar van een Customer Engagement-app, voert u de stappen in de sectie [Een nieuw exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app](#new-existing) eerder in dit onderwerp. Wanneer de verbinding is voltooid en u de gegevens wilt synchroniseren met de Customer Engagement-app, voert u de volgende stappen uit.

1. Open de Finance and Operations-app via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.
2. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Voer de volgende stappen uit om de bestaande Dataverse-gegevens te synchroniseren met de Finance and Operations-app.

1. Maak een nieuw bedrijf maken in de Finance and Operations-app.
2. Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.
3. [Laad](bootstrap-company-data.md) de Dataverse-gegevens automatisch met de ISO-bedrijfscode van drie letters.
4. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Een bestaand exemplaar van de Finance and Operations-app en een nieuw exemplaar van de Customer Engagement-app

Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaand exemplaar van een Finance and Operations-app en een nieuw exemplaar van een Customer Engagement-app in de Finance and Operations-omgeving.

1. [Stel de verbinding vanuit de Finance and Operations-app](enable-dual-write.md) op.
2. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Een bestaand exemplaar van de Finance and Operations-app en een bestaand exemplaar van de Customer Engagement-app

Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaand exemplaar van een Finance and Operations-app en een bestaand exemplaar van een Customer Engagement-app in de Finance and Operations-omgeving.

1. [Stel de verbinding vanuit de Finance and Operations-app](enable-dual-write.md) op.
2. Als u de bestaande Dataverse-gegevens wilt synchroniseren met de Finance and Operations-app, [laadt](bootstrap-company-data.md) u de Dataverse-gegevens automatisch met de ISO-bedrijfscode van drie letters.
3. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="example"></a>Voorbeeld

Zie voor een voorbeeld [De tabeltoewijzing Klanten V3—contactpersonen inschakelen](enable-entity-map.md#enable-table-map)

Zie [Overwegingen voor initiële synchronisatie](initial-sync-guidance.md) voor een alternatieve aanpak die is gebaseerd op gegevensvolumes in elke entiteit waarvoor een initiële synchronisatie moet worden uitgevoerd.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]