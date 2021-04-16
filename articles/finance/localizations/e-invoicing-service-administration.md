---
title: Beheeronderdelen voor elektronische facturering
description: Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de functie voor elektronische facturering.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840023"
---
# <a name="electronic-invoicing-administration-components"></a>Beheeronderdelen voor elektronische facturering

[!include [banner](../includes/banner.md)]


Dit onderwerp biedt informatie over de onderdelen die zijn gerelateerd aan het beheer van de functie voor elektronische facturering. Daarnaast vindt u hier informatie over het configureren van de service voor elektronische facturering.

## <a name="azure"></a>Azure

Gebruik Microsoft Azure om de geheimen voor het Key Vault- en opslagaccount te maken. Gebruik de geheimen vervolgens in de configuratie van Elektronische facturering.

## <a name="lifecycle-services"></a>Lifecycle Services

Gebruik Microsoft Dynamics Lifecycle Services (LCS) om de microservices voor het LCS-implementatieproject in te schakelen.

> [!NOTE]
> Voor de installatie van de microservice in LCS is ten minste een Tier 2 virtuele machine vereist. Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie over omgevingsplanning.
 

## <a name="regulatory-configuration-services"></a>Regulatory Configuration Services

Dynamics 365 Regulatory Configuration Services (RCS) is de interface waarmee u Elektronische facturering configureert. Resources, zoals omgevingen en functies voor elektronische facturering, worden gemaakt, beheerd en gehost in RCS. Wanneer de resources gereed zijn, worden ze gepubliceerd in de service voor elektronische facturering.

Zie [Wettelijke services](https://marketing.configure.global.dynamics.com/) voor registratie bij RCS.

Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie over RCS

### <a name="integration-with-electronic-invoicing"></a>Integratie met Elektronische facturering 

Voordat u RCS kunt gebruiken voor het configureren van elektronische facturen, moet u RCS zo configureren dat communicatie met Elektronische facturering is toegestaan. U voltooit deze configuratie op het tabblad **Elektronische facturering** van de pagina **Parameters voor elektronische rapportage**.

#### <a name="service-endpoint"></a>Service-eindpunt

Elektronische facturering is beschikbaar in verschillende Azure-datacentergeografieën. In de volgende tabel wordt de beschikbaarheid per regio vermeld.

| Geografie Azure-datacenter |
|----------------------------|
| VS - oost                    |
| VS - west                    |
| Noordelijke EU                   |
| Westelijke EU                    |

### <a name="service-environments"></a>Serviceomgevingen

Serviceomgevingen zijn logische partities die worden gemaakt om de uitvoering van de elektronische factureringsfuncties in Elektronische facturering te ondersteunen. De beveiligingsrechten en digitale certificaten en de governance (toegangsmachtigingen) moeten worden geconfigureerd op het niveau van de serviceomgeving.

Klanten kunnen net zo veel serviceomgevingen maken als zij willen. Alle serviceomgevingen die door een klant worden gemaakt, zijn onafhankelijk van elkaar.

Serviceomgevingen moeten worden gemaakt en onderhouden in RCS. Wanneer de serviceomgevingen gereed zijn, moeten ze worden gepubliceerd in Elektronische facturering.

#### <a name="service-environment-status"></a>Status van de serviceomgeving

Serviceomgevingen kunnen worden beheerd via de status. De mogelijke opties zijn:

- **Niet gepubliceerd**: de omgeving is gemaakt, maar nog niet gepubliceerd.
- **Gepubliceerd**: de omgeving is gepubliceerd in Elektronische facturering.
- **Gewijzigd**: de kenmerken van een gepubliceerde omgeving zijn gewijzigd, maar de wijzigingen zijn nog niet gepubliceerd.

#### <a name="customer-secrets"></a>Klantgeheimen

De service voor elektronische facturering is verantwoordelijk voor het opslaan van al uw bedrijfsgegevens in de Azure-resources die uw bedrijf bezit. Om er zeker van te zijn dat de service correct werkt en dat alle bedrijfsgegevens die nodig zijn voor en die worden gegenereerd door Elektronische facturering correct worden gebruikt, moet u twee hoofd Azure-resources maken:

- Een Azure-opslagaccount (Blob-opslag) waarin elektronische facturen worden opgeslagen
- Een Azure Key Vault voor de opslag van certificaten en de URI (Uniform Resource Identifier) van het opslagaccount

> [!NOTE]
> Een speciale Key Vault en een opslagaccount van de klant moeten specifiek worden toegewezen voor gebruik met Elektronische facturering.

Zie [Een Azure-opslagaccount en Key Vault maken](e-invoicing-create-azure-storage-account-key-vault.md) voor meer informatie.

#### <a name="users"></a>Gebruikers

Elke serviceomgeving moet een lijst maken met de gebruikers die verbinding kunnen maken vanuit Dynamics 365 Finance en Dynamics 365 Supply Chain Management in Elektronische facturering.

#### <a name="publication"></a>Publicatie

Serviceomgevingen moeten worden gepubliceerd in Elektronische facturering voordat ze kunnen worden gebruikt. Alleen gepubliceerde omgevingen kunnen worden gebruikt door Finance en Supply Chain Management. Daarnaast moet een serviceomgeving worden gepubliceerd voordat updates van de kenmerken van kracht worden op de elektronische factureringsservice.

### <a name="connected-applications"></a>Verbonden toepassingen

Verbonden toepassingen zijn de exemplaren van Finance en Supply Chain Management die u mogelijk wilt bereiken via RCS. Naast de URL van de toepassing en de tenant ervan, bevat een verbonden toepassing de referenties waarmee RCS verbinding kan maken met de omgeving.

Via de verbonden toepassingen kunt u een gedeelte van de elektronische factureringsfunctie in Finance en Supply Chain Management configureren om de gehele elektronische factureringsfunctie te laten werken.

## <a name="finance-and-supply-chain-management"></a>Finance en Supply Chain Management

### <a name="integration-with-electronic-invoicing"></a>Integratie met Elektronische facturering

Voordat u Finance en Supply Chain Management kunt gebruiken om elektronische facturen uit te geven via Elektronische facturering, moet Elektronische facturering worden geconfigureerd zodat kan worden gecommuniceerd met de service.

#### <a name="electronic-invoicing-integration-feature"></a>Integratiefunctie van Elektronische facturering

Als u de communicatie tussen Finance en Supply Chain Management en Elektronische facturering wilt inschakelen, moet u de functie **Integratie van Elektronische facturering** in de werkruimte **Functiebeheer** inschakelen.

#### <a name="service-endpoint"></a>Service-eindpunt

Het service-eindpunt is de URL waar Elektronische facturering zich bevindt. Voordat elektronische facturen kunnen worden uitgegeven, moet het service-eindpunt worden geconfigureerd in Finance en Supply Chain Management om communicatie met de service mogelijk te maken.

Om het service-eindpunt te configureren, gaat u naar **Organisatiebeheer \> Instellen \> Parameter voor elektronisch document** en daarna voert u op het tabblad **Indieningsservices** in het veld **URL van Elektronische facturering** de URL in, zoals wordt beschreven in de tabel uit de sectie **Service-eindpunt**.

#### <a name="environments"></a>Omgevingen

De omgevingsnaam die wordt ingevoerd in Finance en Supply Chain Management, verwijst naar de naam van de omgeving die in RCS wordt gemaakt en gepubliceerd naar Elektronische facturering.

De omgeving moet worden geconfigureerd op het tabblad **Indieningsservices** van de pagina **Parameter voor elektronisch document**, zodat elk verzoek om elektronische facturen uit te geven de omgeving bevat waarin Elektronische facturering kan bepalen welke functie voor elektronische facturering het verzoek moet verwerken.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Elektronische facturen configureren in RCS](e-invoicing-configuration-rcs.md)
- [Elektronische facturen uitgeven in Finance en Supply Chain Management](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
