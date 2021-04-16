---
title: Validatie van aangepast certificaat NF-e
description: Dit onderwerp bevat informatie over het inschakelen en gebruiken van het aangepaste certificaat NF-e.
author: gionoder
ms.date: 10/06/2020
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
ms.openlocfilehash: 895513f51798a797ebf59f8a5be4f5cde006726d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813963"
---
# <a name="nf-e-custom-certificate-validation"></a>Validatie van aangepast certificaat NF-e

[!include [banner](../includes/banner.md)]

Wanneer u de functie voor verificatie van aangepaste certificaat NF-e inschakelt, kan met aangepaste validatie een verbinding met de webservices tot stand worden gebracht. Deze verbinding is vereist voor het verzenden van NF-e en het ontvangen van autorisatie van SEFAZ.

De eigenschap **Doel van serververificatie** van certificaat V5 wordt uitgegeven door de Braziliaanse basiscertificeringsinstantie. Deze eigenschap is standaard uitgeschakeld en moet handmatig worden ingeschakeld. In sommige gevallen kan de automatische certificaatupdate deze eigenschap uitschakelen. In dat geval wordt de TLS-verbinding beïnvloed en wordt deze niet meer vertrouwd. Ook de mogelijkheid om NF-e te verlenen aan productieomgevingen voor de staten Minas Gerais (MG) en Paraná (PR) wordt beïnvloed.

Met deze update is een alternatieve oplossing voor certificaatvalidatie mogelijk, wat inhoudt dat beveiligde communicatie tot stand kan worden gebracht.




[!INCLUDE[footer-include](../../includes/footer-banner.md)]