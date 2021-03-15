---
title: Beheeronderdelen van de invoegtoepassing voor elektronische facturering
description: Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de invoegtoepassing voor elektronische facturering.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104365"
---
# <a name="electronic-invoicing-add-on-administration-components"></a>Beheeronderdelen van de invoegtoepassing voor elektronische facturering

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de invoegtoepassing voor elektronische facturering. Daarnaast vindt u hier informatie over het configureren van de invoegtoepassingsservice voor elektronische facturering.

## <a name="azure"></a>Azure

Gebruik Microsoft Azure om de geheimen voor het Key Vault- en opslagaccount te maken. Gebruik de geheimen vervolgens in de configuratie van de invoegtoepassing voor elektronische facturering.

## <a name="lifecycle-services"></a>Lifecycle Services

Gebruik Microsoft Dynamics Lifecycle Services (LCS) om de invoegtoepassing voor de microservices voor het LCS-implementatieproject in te schakelen.

Selecteer in LCS de tegel **Beheer van previewfuncties** en schakel de functie **e-Factureringsservice** in.

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) is de interface waarmee u de invoegtoepassing voor elektronische facturering configureert. Resources, zoals omgevingen en functies voor elektronische facturering, worden gemaakt, beheerd en gehost in RCS. Wanneer de resources gereed zijn, worden ze gepubliceerd in de invoegtoepassingsservice voor elektronische facturering.

Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie over RCS

### <a name="integration-with-the-electronic-invoicing-add-on"></a>Integratie met de invoegtoepassing voor elektronische facturering

Voordat u RCS kunt gebruiken voor het configureren van elektronische facturen, moet u RCS zo configureren dat communicatie met de invoegtoepassing voor elektronische facturering is toegestaan. U voltooit deze configuratie op het tabblad **Invoegtoepassing voor elektronische facturering** van de pagina **Parameters voor elektronische rapportage**.

#### <a name="service-endpoint"></a>Service-eindpunt

De URL van de invoegtoepassing voor elektronische facturering kan variëren, afhankelijk van de geografie van het Azure-datacenter. In de volgende tabel wordt de beschikbaarheid per regio vermeld:

| Geografie Azure-datacenter | URL van service-eindpunt                                                       |
|----------------------------|----------------------------------------------------------------------------|
| VS - oost                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| VS - west                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| Noordelijke EU                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| Westelijke EU                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a>Sollicitatie-ID

De toepassings-id is de id van de invoegtoepassing voor elektronische facturering. In dit geval is de waarde vast: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.

#### <a name="lcs-environment-id"></a>LCS-omgevings-id

De LCS-omgevings-id is de id van het LCS-abonnement van uw organisatie.

### <a name="service-environments"></a>Serviceomgevingen

Serviceomgevingen zijn logische partities die worden gemaakt om de uitvoering van de elektronische factureringsfuncties in de invoegtoepassing voor elektronische facturering te ondersteunen. De beveiligingsrechten en digitale certificaten en de governance (toegangsmachtigingen) moeten worden geconfigureerd op het niveau van de serviceomgeving.

Klanten kunnen net zo veel serviceomgevingen maken als zij willen. Alle serviceomgevingen die door een klant worden gemaakt, zijn onafhankelijk van elkaar.

Serviceomgevingen moeten worden gemaakt en onderhouden in RCS. Wanneer de serviceomgevingen gereed zijn, moeten ze worden gepubliceerd in de invoegtoepassing voor elektronische facturering.

#### <a name="service-environment-status"></a>Status van de serviceomgeving

Serviceomgevingen kunnen worden beheerd via de status. De mogelijke opties zijn:

- **Niet gepubliceerd**: de omgeving is gemaakt, maar nog niet gepubliceerd.
- **Gepubliceerd**: de omgeving is gepubliceerd in de invoegtoepassing voor elektronische facturering.
- **Gewijzigd**: de kenmerken van een gepubliceerde omgeving zijn gewijzigd, maar de wijzigingen zijn nog niet gepubliceerd.

#### <a name="customer-secrets"></a>Klantgeheimen

De invoegtoepassing voor elektronische facturering is verantwoordelijk voor het opslaan van al uw bedrijfsgegevens in de Azure-resources die uw bedrijf bezit. Om er zeker van te zijn dat de service correct werkt en dat alle bedrijfsgegevens die vereist zijn voor en die worden gegenereerd door de invoegtoepassing voor elektronische facturering alleen worden gebruikt door de invoegtoepassing, moet u twee Azure-resources maken:

- Een Azure-opslagaccount (Blob-opslag) waarin elektronische facturen worden opgeslagen
- Een Azure Key Vault voor de opslag van certificaten en de URI (Uniform Resource Identifier) van het opslagaccount

> [!NOTE]
> Een speciale Key Vault en een opslagaccount van de klant moeten specifiek worden toegewezen voor gebruik met de invoegtoepassing voor elektronische facturering.

Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.

#### <a name="users"></a>Gebruikers

Elke serviceomgeving moet een lijst maken met de gebruikers die verbinding kunnen maken vanuit Dynamics 365 Finance en Dynamics 365 Supply Chain Management in de invoegtoepassing voor elektronische facturering.

#### <a name="publication"></a>Publicatie

Serviceomgevingen moeten worden gepubliceerd in de invoegtoepassing voor elektronische facturering voordat ze kunnen worden gebruikt. Alleen gepubliceerde omgevingen kunnen worden gebruikt door Finance en Supply Chain Management. Daarnaast moet een serviceomgeving worden gepubliceerd voordat updates van de kenmerken van kracht worden op de elektronische factureringsservice.

### <a name="connected-applications"></a>Verbonden toepassingen

Verbonden toepassingen zijn de exemplaren van Finance en Supply Chain Management die u mogelijk wilt bereiken via RCS. Naast de URL van de toepassing en de tenant ervan, bevat een verbonden toepassing de referenties waarmee RCS verbinding kan maken met de omgeving.

Via de verbonden toepassingen kunt u een gedeelte van de elektronische factureringsfunctie in Finance en Supply Chain Management configureren om de gehele elektronische factureringsfunctie te laten werken.

## <a name="finance-and-supply-chain-management"></a>Finance en Supply Chain Management

### <a name="integration-with-electronic-invoicing-add-on"></a>Integratie met de invoegtoepassing voor elektronische facturering

Voordat u Finance en Supply Chain Management kunt gebruiken om elektronische facturen uit te geven via de invoegtoepassing voor elektronische facturering, moet de invoegtoepassing worden geconfigureerd zodat kan worden gecommuniceerd met de service.

#### <a name="electronic-invoicing-add-on-integration-feature"></a>Integratiefunctie van de invoegtoepassing voor elektronische facturering

Als u de communicatie tussen Finance en Supply Chain Management en de invoegtoepassing voor elektronische facturering wilt inschakelen, moet u de **Integratiefunctie van de invoegtoepassing voor elektronische facturering** in de werkruimte **Functiebeheer** inschakelen.

#### <a name="service-endpoint"></a>Service-eindpunt

Het service-eindpunt is de URL waar de invoegtoepassing voor elektronische facturering zich bevindt. Voordat elektronische facturen kunnen worden uitgegeven, moet het service-eindpunt worden geconfigureerd in Finance en Supply Chain Management om communicatie met de service mogelijk te maken.

Om het service-eindpunt te configureren, gaat u naar **Organisatiebeheer \> Instellen \> Parameter voor elektronisch document** en daarna voert u op het tabblad **Indieningsservices** in het veld **URL van de invoegtoepassing voor elektronische facturering** de URL in, zoals wordt beschreven in de tabel uit de sectie **Service-eindpunt**.

#### <a name="environments"></a>Omgevingen

De omgevingsnaam die wordt ingevoerd in Finance en Supply Chain Management, verwijst naar de naam van de omgeving die in RCS wordt gemaakt en gepubliceerd naar de invoegtoepassing voor elektronische facturering.

De omgeving moet worden geconfigureerd op het tabblad **Indieningsservices** van de pagina **Parameter voor elektronisch document**, zodat elk verzoek om elektronische facturen uit te geven de omgeving bevat waarin de invoegtoepassing voor elektronische facturering kan bepalen welke functie voor elektronische facturering het verzoek moet verwerken.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Elektronische facturen configureren in RCS](e-invoicing-configuration-rcs.md)
- [Elektronische facturen uitgeven in Finance en Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]