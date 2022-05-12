---
title: Elektronische facturering instellen
description: Dit onderwerp bevat een overzicht van het proces voor het instellen en configureren van Elektronische facturering.
author: dkalyuzh
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkalyuzh
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 42e617e26e7658fae9ee54cb8a4dee45314fddaa
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661687"
---
# <a name="electronic-invoicing-setup"></a>Elektronische facturering instellen

[!include [banner](../includes/banner.md)]

Het onderwerp bevat een overzicht van het proces voor het instellen en configureren van Elektronische facturering. U moet de instellingsstappen voltooien in de volgorde die hier is opgegeven. Als een stap verplicht is, maar u slaat deze over, werkt de functionaliteit niet goed en treden er meerdere fouten op tijdens volgende stappen of wanneer u de functionaliteit gebruikt. 

Voordat u begint, moet u controleren of alle hoofdonderdelen correct zijn ingesteld, of u zich hebt aangemeld voor Regulatory Configuration Service (RCS) en een exemplaar van RCS hebt en dat de invoegvoeging voor elektronische facturering is geïnstalleerd voor uw Microsoft Dynamics 365 Finance- of Dynamics 365 Supply Chain Management-omgeving. Zie [Aanmelden voor Elektronische facturering en installeren](e-invoicing-install-add-in-microservices-lcs.md) voor meer informatie.

Stel vervolgens de Azure-resources in die nodig zijn voor Elektronische facturering. Zie [Azure-resources instellen voor elektronische facturering](e-invoicing-set-up-azure-resources.md) voor meer informatie.

Nadat de hoofdonderdelen zijn geconfigureerd, werkt u samen met RCS om de belangrijkste logische onderdelen van elektronische facturering in te stellen. Definieer eerst het aantal serviceomgevingen dat u wilt onderhouden. Op deze manier definieert u de logische gegevens- en configuratie-partities, zodat u een grens hebt tussen een ontwikkel- of testomgeving en de productieomgevingen. Als u het ontwikkelingsproces flexibel wilt instellen, hebt u mogelijk verschillende afzonderlijke ontwikkel- en testomgevingen nodig. Definieer niet alleen serviceomgevingen, maar stel ook direct vanuit RCS een koppeling naar uw bedrijfstoepassingen, zoals Finance of Supply Chain Management, in om de parameters in te stellen die vereist zijn voor een juiste bewerking met elektronische facturering. Zie [Serviceomgevingen](e-invoicing-service-environments.md) voor meer informatie over omgevingen.

Nadat alles is ingesteld, kunt u uw eigen globalisatiefuncties maken die verschillende scenario's definiëren voor de verwerking van elektronische documenten en het omzetten van gegevens, of voor het importeren van de documenten vanuit de algemene opslagplaats. Zie [Werken met Globalisatiefuncties](e-invoicing-working-globalization-features.md) voor meer informatie over het werken met Globalisatiefuncties.

Als uw scenario's integratie met e-mail of SharePoint vereisen om inkomende elektronische documenten te verwerken, gaat u naar [De verwerking van binnenkomende elektronische documenten](e-invoicing-process-incoming-electronic-documents.md) voor informatie over het instellen en gebruiken van deze kanalen.
