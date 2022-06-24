---
title: Serviceomgevingen en verbonden toepassingen configureren
description: In dit artikel vindt u informatie over het configureren van serviceomgevingen en gekoppelde toepassingen.
author: dkalyuzh
ms.date: 02/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom:
- "97423"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c1bb3f784148f04c01223ac4e280a18bacfe0e51
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8853217"
---
# <a name="configure-service-environments-and-connected-applications"></a>Serviceomgevingen en verbonden toepassingen configureren

[!include [banner](../includes/banner.md)]

In dit artikel vindt u informatie over het configureren van serviceomgevingen en gekoppelde toepassingen. Er zijn drie stappen voor dit proces. Stap 1 is verplicht en stap 2 en 3 zijn optioneel.

## <a name="step-1-create-a-service-environment"></a>Stap 1: Een serviceomgeving maken

Wanneer u uw serviceomgeving maakt, definieert u de lijst met gebruikers die globalisatiefuncties kunnen implementeren. Voor sommige scenario's definieert u eventueel de lijst met externe toepassingen die met de Elektronische factureringsservice kunnen communiceren. Nummerreeksen instellen als u deze gebruikt in de scenario's.

Zie [Serviceomgevingen](e-invoicing-service-environments.md) om deze stap te voltooien.

## <a name="step-2-add-certificates-and-secrets"></a>Stap 2: Certificaten en geheimen toevoegen

Voeg een verwijzing toe naar de belangrijkste Microsoft Azure Key Vault en geheimen om ze in uw scenario's te gebruiken. Deze stap is verplicht als bij acties in de verwerkingspijplijnen certificaten en geheimen worden gebruikt voor digitale ondertekening of communicatie met externe webservices.

Zie [Klantcertificaten en -geheimen](e-invoicing-customer-certificates-secrets.md) om deze stap te voltooien.

## <a name="step-3-configure-connected-applications"></a>Stap 3: Gekoppelde toepassingen configureren

Als u de communicatie tussen Dynamics 365 Finance of Dynamics 365 Supply Chain Management en Elektronische facturering wilt instellen, moet u Finance of Supply Chain Management configureren om de oproep aan de elektronische factureringsservice samen te stellen en bedrijfsgegevens voor te bereiden in een centrale structuur die kan worden omgezet in de vereiste elektronische indeling. De antwoorden van de service moeten ook correct door de toepassingen worden verwerkt. U kunt deze configuratie rechtstreeks voltooien in uw Finance- of Supply Chain Management-omgeving of u kunt deze voltooien in Regulatory Configuration Service (RCS). Als u de configuratie in RCS voltooit, kunt u deze vervolgens implementeren in uw Finance- of Supply Chain Management-omgeving. In deze stap registreert u de gekoppelde toepassing voor de implementatie van parameters.

Zie [Verbonden toepassingen](e-invoicing-connected-applications.md) om deze stap te voltooien.
