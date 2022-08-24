---
title: Aanmelden voor Elektronische facturering en de service installeren
description: Dit artikel bevat informatie over het aanmelden voor en het installeren van de service voor elektronische facturering.
author: gionoder
ms.date: 02/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: 99f484e5ab8821c78fde776a9d3195dade2a09d5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283952"
---
# <a name="sign-up-for-and-install-the-electronic-invoicing-service"></a>Aanmelden voor Elektronische facturering en de service installeren

[!include [banner](../includes/banner.md)]

Dit artikel bevat informatie over het aanmelden voor en het installeren van de service voor elektronische facturering. Er zijn vier stappen voor dit proces. Stappen 1 tot en met 3 zijn vereist en stap 4 is optioneel.

### <a name="step-1-sign-up-for-regulatory-configuration-service"></a>Stap 1: Meld u aan bij Regulatory Configuration Service.

Regulatory Configuration Services (RCS) bevat de configuratie en het ontwerp waarmee Elektronische facturering wordt geconfigureerd. Resources, zoals omgevingen en functies voor elektronische facturering, worden gemaakt, beheerd en beheer in RCS. Wanneer de resources gereed zijn, worden ze gepubliceerd in de service voor Elektronische facturering.

Zie [Regulatory Configuration Services (RCS) - Globalisatiefuncties](rcs-globalization-feature.md) voor meer informatie over RCS.

U kunt zich registreren voor RCS via de pagina [Regulatory Configuration Service](https://marketing.configure.global.dynamics.com/).

### <a name="step-2-install-the-add-in-for-microservices-in-microsoft-dynamics-lifecycle-services"></a>Stap 2: De invoegtoepassing voor microservices in Microsoft Dynamics Lifecycle Services installeren

De elektronische factureringsservice is een set microservices die wordt gehost in Microsoft-datacenters. Standaard hebben klanten van Dynamics 365 Finance en Dynamics 365 Supply Chain Management geen toegang tot de elektronische factureringsservice. U moet deze installeren als een invoegtoepassing in Microsoft Dynamics Lifecycle Services (LCS). Wanneer u de invoegtoepassing installeert, wordt uw Finance- of Supply Chain Management-omgeving geregistreerd in het register met toepassingen die verbinding mogen maken met de Elektronische factureringsservice.

Voor het voltooien van deze stap gaat u naar [De invoegtoepassing voor microservices in Lifecycle Services installeren](e-invoicing-install-add-in-microservices-lcs.md).

### <a name="step-3-set-up-rcs"></a>Stap 3: RCS instellen

U moet de integratie tussen RCS en de Elektronische factureringsservice instellen. U moet ook de hoofdonderdelen instellen.

Zie [Regulatory Configuration Service (RCS) instellen](e-invoicing-set-up-rcs.md) om deze stap te voltooien.

### <a name="step-4-microsoft-power-platform-plug-in-admin-reference"></a>Stap 4: Beheerdersreferentie voor Microsoft Power Platform-invoegtoepassing

Voor sommige scenario's is integratie met Dataverse voor Microsoft Power Platform vereist.

Deze instelling is momenteel verplicht als u Elektronische factureringsoplossingen gebruikt voor elektronische factureringsscenario's voor Indonesië. Het is echter optioneel voor elektronische factureringsscenario's voor Saudi-Arabië. Zie [Beschikbaarheid van functies voor Elektronische facturering per land or regio](e-invoicing-country-specific-availability.md) voor meer informatie.

Als u deze stap wilt voltooien, gaat u naar [Beheerdersreferentie voor Microsoft Power Platform-invoegtoepassing](e-invoicing-power-platform-plug-in.md).
