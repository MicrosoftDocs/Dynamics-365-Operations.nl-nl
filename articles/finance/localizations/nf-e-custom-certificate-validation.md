---
title: Validatie van aangepast certificaat NF-e
description: Dit onderwerp bevat informatie over het inschakelen en gebruiken van het aangepaste certificaat NF-e.
author: gionoder
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 26ffed1f49d9087ca767aab1b8cac41b099f73cb
ms.sourcegitcommit: 3c88c4adafb78b807842b0b41c69b19cf2b7aa23
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/09/2020
ms.locfileid: "3973087"
---
# <a name="nf-e-custom-certificate-validation"></a>Validatie van aangepast certificaat NF-e

[!include [banner](../includes/banner.md)]

Wanneer u de functie voor verificatie van aangepaste certificaat NF-e inschakelt, kan met aangepaste validatie een verbinding met de webservices tot stand worden gebracht. Deze verbinding is vereist voor het verzenden van NF-e en het ontvangen van autorisatie van SEFAZ.

De eigenschap **Doel van serververificatie** van certificaat V5 wordt uitgegeven door de Braziliaanse basiscertificeringsinstantie. Deze eigenschap is standaard uitgeschakeld en moet handmatig worden ingeschakeld. In sommige gevallen kan de automatische certificaatupdate deze eigenschap uitschakelen. In dat geval wordt de TLS-verbinding beïnvloed en wordt deze niet meer vertrouwd. Ook de mogelijkheid om NF-e te verlenen aan productieomgevingen voor de staten Minas Gerais (MG) en Paraná (PR) wordt beïnvloed.

Met deze update is een alternatieve oplossing voor certificaatvalidatie mogelijk, wat inhoudt dat beveiligde communicatie tot stand kan worden gebracht.


