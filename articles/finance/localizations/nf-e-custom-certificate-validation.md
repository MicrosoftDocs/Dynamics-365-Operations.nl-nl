---
title: Aangepaste validatie van NF-e-certificaat
description: Dit artikel bevat informatie over het inschakelen en gebruiken van het aangepaste certificaat NF-e.
author: gionoder
ms.date: 07/29/2021
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
ms.openlocfilehash: 3d69aa9d6d0ce33fbed9ba1c7a7af441e14d0d07
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8875899"
---
# <a name="nf-e-custom-certificate-validation"></a>Aangepaste validatie van NF-e-certificaat

[!include [banner](../includes/banner.md)]

De eigenschap **Doel van serververificatie** van de certificaten die zijn uitgegeven door de Braziliaanse basiscertificeringsinstantie is standaard uitgeschakeld en moet handmatig worden ingeschakeld. In sommige gevallen kan de automatische certificaatupdate deze eigenschap uitschakelen. In dat geval heeft dit effect op de TLS-verbinding en wordt deze niet meer vertrouwd. Het heeft effect op de mogelijkheid om het Braziliaanse elektronische belastingdocument model 55 (NF-e) uit te geven in productieomgevingen voor de staten Minas Gerais (MG) en Paraná (PR).

Als u de oplossing wilt activeren voor **Validatie van aangepast certificaat NF-e**, gaat u naar **Functiebeheer**. Deze functie biedt een alternatieve oplossing voor de validatie van V5- en V10-certificaten en maakt een betrouwbare verbinding mogelijk met de webservices die vereist zijn voor de beveiligde overdracht van de NF-e en de ontvangst van de autorisatie van SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
