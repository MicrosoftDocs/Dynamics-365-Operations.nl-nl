---
title: Verwerken van binnenkomende elektronische documenten
description: Dit artikel biedt een overzicht van de verwerking voor binnenkomende elektronische documenten.
author: gionoder
ms.date: 02/28/2022
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
ms.openlocfilehash: 554bc8fde3b2135eb878d885541c76ecd6d66493
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277296"
---
# <a name="processing-of-incoming-electronic-documents"></a>Verwerken van binnenkomende elektronische documenten

[!include [banner](../includes/banner.md)]

Inkomende elektronische documenten, zoals elektronische leveranciersfacturen, kunnen op twee manieren worden geïmporteerd en verwerkt:

- Bestanden worden opgehaald uit externe kanalen en rechtstreeks doorgegeven aan de verbonden toepassing. Vervolgens worden ze na een extra transformatie in de database geïmporteerd.
- Bestanden ondergaan de voorverwerking in de Elektronische factureringsservice en worden vervolgens doorgegeven aan de verbonden toepassing.

Elektronische facturering ondersteunt twee kanalen voor binnenkomende documenten: e-mail en Microsoft SharePoint-mappen.

Er zijn diverse instellingstypen voor de verbinding om op te geven of documenten moeten worden voorverwerkt of rechtstreeks aan de verbonden toepassing moeten worden doorgegeven:

- **Gegevenskanaal**: het document wordt rechtstreeks door het systeem aan de verbonden toepassing doorgegeven.
- **Gegevenskanaal met verwerkingspijplijn**: u kunt extra acties instellen die worden uitgevoerd voordat het document wordt doorgegeven aan de verbonden toepassing.

Zie [Een e-mailkanaal configureren](e-invoicing-configure-email.md) en [Een SharePoint-kanaal configureren](e-invoicing-configure-sharepoint-channel.md) voor informatie over het instellen van de scenario's voor de verwerking van inkomende elektronische documenten voor de verschillende kanalen.
