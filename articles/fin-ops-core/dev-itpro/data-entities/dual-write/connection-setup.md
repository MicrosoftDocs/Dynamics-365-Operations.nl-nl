---
title: Richtlijnen voor het instellen van twee keer wegschrijven
description: In dit artikel worden de scenario's beschreven die worden ondersteund voor instellingen voor twee keer wegschrijven.
author: RamaKrishnamoorthy
ms.date: 06/28/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: b27cabf495448fcd82edd374bb59e6e5a664c7e9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289739"
---
# <a name="guidance-for-dual-write-setup"></a>Richtlijnen voor het instellen van twee keer wegschrijven

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]



U kunt een verbinding voor twee keer wegschrijven instellen tussen een omgeving voor financiën en bedrijfsactiviteiten en een Dataverse-omgeving.

+ Een **omgeving voor financiën en bedrijfsactiviteiten** levert het onderliggende platform voor **apps voor financiën en bedrijfsactiviteiten** (bijvoorbeeld Microsoft Dynamics 365 Finance, Dynamics 365 Supply Chain Management, Dynamics 365 Commerce en Dynamics 365 Human Resources).
+ Een **Dataverse-omgeving** biedt het onderliggende platform voor **Customer Engagement-apps** (Dynamics 365 Sales, Dynamics 365 Customer Service, Dynamics 365 column Service, Dynamics 365 Marketing en Dynamics 365 Project Service Automation).


> [!IMPORTANT]
> De module Human resources in Dynamics 365 Finance ondersteunt verbindingen voor twee keer wegschrijven, maar de Dynamics 365 Human Resources-app ondersteunt dat niet.

Het installatiemechanisme varieert afhankelijk van uw abonnement en de omgeving:

+ Voor nieuwe app-instanties voor financiën en bedrijfsactiviteiten begint het instellen van een verbinding voor twee keer wegschrijven met Microsoft Dynamics Lifecycle Services (LCS). Als u een licentie hebt voor Microsoft Power Platform, krijgt u een nieuwe Dataverse-omgeving als uw tenant er geen heeft.
+ Voor bestaande app-instanties voor financiën en bedrijfsactiviteiten begint het instellen van een verbinding voor twee keer wegschrijven met de omgeving voor financiën en bedrijfsactiviteiten.

Voordat u twee keer wegschrijven voor een entiteit start, kunt u een initiële synchronisatie uitvoeren om bestaande gegevens aan beide zijden van apps voor financiën en bedrijfsactiviteiten en Customer Engagement-apps te verwerken. U kunt de initiële synchronisatie overslaan als u geen gegevens tussen de twee omgevingen hoeft te synchroniseren.

Met een initiële synchronisatie kunt u bestaande gegevens in twee richtingen van de ene naar de andere app kopiëren. Er zijn verschillende instellingsscenario's afhankelijk van de omgevingen die u al hebt en het type gegevens dat deze omgevingen bevatten.

De volgende scenario's met instellingen worden ondersteund:

+ [Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten en een nieuwe instantie van de Customer Engagement-app](#new-new)
+ [Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten en een bestaande instantie van de Customer Engagement-app](#new-existing)
+ [Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten en een nieuwe instantie van de Customer Engagement-app](#new-data-new)
+ [Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten en een bestaande instantie van de Customer Engagement-app](#new-data-existing)
+ [Een bestaande app-instantie voor financiën en bedrijfsactiviteiten en een nieuwe instantie van de Customer Engagement-app](#existing-new)
+ [Een bestaande app-instantie voor financiën en bedrijfsactiviteiten en een bestaande instantie van de Customer Engagement-app](#existing-existing)

## <a name="a-new-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="new-new"></a>Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten en een nieuwe instantie van de Customer Engagement-app

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuwe app-instantie voor financiën en bedrijfsactiviteiten zonder gegevens en een nieuwe instantie van een Customer Engagement-app, voert u de stappen uit in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md). Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:

- Er wordt een nieuwe, lege omgeving voor financiën en bedrijfsactiviteiten ingericht.
- Er wordt een nieuw, leeg exemplaar van een Customer Engagement-app ingericht, waarbij de CRM Prime-oplossing wordt geïnstalleerd.
- Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.
- Tabeltoewijzingen worden ingeschakeld voor live migratie.

Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.

## <a name="a-new-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="new-existing"></a>Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten en een bestaande instantie van de Customer Engagement-app

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuwe app-instantie voor financiën en bedrijfsactiviteiten zonder gegevens en een bestaande instantie van een Customer Engagement-app, voert u de stappen uit in [Instellingen voor twee keer wegschrijven in Lifecycle Services](lcs-setup.md). Wanneer de configuratie van de verbinding is voltooid, worden automatisch de volgende acties uitgevoerd:

- Er wordt een nieuwe, lege omgeving voor financiën en bedrijfsactiviteiten ingericht.
- Er wordt een verbinding voor twee keer wegschrijven tot stand gebracht met DAT-bedrijfsgegevens.
- Tabeltoewijzingen worden ingeschakeld voor live migratie.

Beide omgevingen zijn vervolgens gereed voor synchronisatie met live gegevens.

Voer de volgende stappen uit om de bestaande Dataverse-gegevens te synchroniseren met de app voor financiën en bedrijfsactiviteiten.

1. Maak een nieuw bedrijf in de app voor financiën en bedrijfsactiviteiten.
2. Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.
3. [Laad](bootstrap-company-data.md) de Dataverse-gegevens automatisch met de ISO-bedrijfscode (International Organization for Standardization) van drie letters.
4. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) verderop in dit artikel voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-a-new-customer-engagement-app-instance"></a><a id="new-data-new"></a>Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten met gegevens en een nieuwe instantie van de Customer Engagement-app

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuwe app-instantie voor financiën en bedrijfsactiviteiten met gegevens en een nieuwe instantie van een Customer Engagement-app, voert u de stappen uit in de sectie [Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten en een nieuwe instantie van de Customer Engagement-app](#new-new) eerder in dit artikel. Wanneer de verbinding is voltooid en u de gegevens wilt synchroniseren met de Customer Engagement-app, voert u de volgende stappen uit.

1. Open de app voor financiën en bedrijfsactiviteiten via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.
2. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="a-new-finance-and-operations-app-instance-that-has-data-and-an-existing-customer-engagement-app-instance"></a><a id="new-data-existing"></a>Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten met gegevens en een bestaande instantie van de Customer Engagement-app

Als u een verbinding voor twee keer wegschrijven wilt instellen tussen een nieuwe app-instantie voor financiën en bedrijfsactiviteiten met gegevens en een bestaande instantie van een Customer Engagement-app, voert u de stappen uit in de sectie [Een nieuwe app-instantie voor financiën en bedrijfsactiviteiten en een bestaande instantie van de Customer Engagement-app](#new-existing) eerder in dit artikel. Wanneer de verbinding is voltooid en u de gegevens wilt synchroniseren met de Customer Engagement-app, voert u de volgende stappen uit.

1. Open de app voor financiën en bedrijfsactiviteiten via de LCS-pagina, meld u aan en ga naar **Gegevensbeheer \> Twee keer wegschrijven**.
2. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Voer de volgende stappen uit om de bestaande Dataverse-gegevens te synchroniseren met de app voor financiën en bedrijfsactiviteiten.

1. Maak een nieuw bedrijf in de app voor financiën en bedrijfsactiviteiten.
2. Voeg het bedrijf toe aan de instellingen van de verbinding voor twee keer wegschrijven.
3. [Laad](bootstrap-company-data.md) de Dataverse-gegevens automatisch met de ISO-bedrijfscode van drie letters.
4. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="an-existing-finance-and-operations-app-instance-and-a-new-customer-engagement-app-instance"></a><a id="existing-new"></a>Een bestaande app-instantie voor financiën en bedrijfsactiviteiten en een nieuwe instantie van de Customer Engagement-app

Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaande app-instantie voor financiën en bedrijfsactiviteiten en een nieuwe instantie van een Customer Engagement-app in de omgeving voor financiën en bedrijfsactiviteiten.

1. [De verbinding instellen via de app voor financiën en bedrijfsactiviteiten](enable-dual-write.md).
2. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="an-existing-finance-and-operations-app-instance-and-an-existing-customer-engagement-app-instance"></a><a id="existing-existing"></a>Een bestaande app-instantie voor financiën en bedrijfsactiviteiten en een bestaande instantie van de Customer Engagement-app

Het instellen van een verbinding voor twee keer wegschrijven tussen een bestaande app-instantie voor financiën en bedrijfsactiviteiten en een bestaande instantie van een Customer Engagement-app in de omgeving voor financiële en bedrijfsactiviteiten.

1. [De verbinding instellen via de app voor financiën en bedrijfsactiviteiten](enable-dual-write.md).
2. Als u de bestaande Dataverse-gegevens wilt synchroniseren met de app voor financiën en bedrijfsactiviteiten, [laadt](bootstrap-company-data.md) u de Dataverse-gegevens automatisch met de ISO-bedrijfscode van drie letters.
3. Voer de functie **Initiële synchronisatie** uit voor de tabellen waarvoor u gegevens wilt synchroniseren.

Zie de sectie [Voorbeeld](#example) voor koppelingen naar een voorbeeld en een alternatieve aanpak.

## <a name="example"></a>Voorbeeld

Zie voor een voorbeeld [De tabeltoewijzing Klanten V3—contactpersonen inschakelen](enable-entity-map.md#enable-table-map)

Zie [Overwegingen voor initiële synchronisatie](initial-sync-guidance.md) voor een alternatieve aanpak die is gebaseerd op gegevensvolumes in elke entiteit waarvoor een initiële synchronisatie moet worden uitgevoerd.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
