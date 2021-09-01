---
title: Validatie van aangepast certificaat NF-e
description: Dit onderwerp bevat informatie over het inschakelen en gebruiken van het aangepaste certificaat NF-e.
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
ms.openlocfilehash: 8144e16b127bdbe954ef44f52c5ac71689a2036e6085e9a4ccc8bb17f91ae9b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6755586"
---
# <a name="nf-e-custom-certificate-validation"></a>Aangepaste validatie van NF-e-certificaat

[!include [banner](../includes/banner.md)]

De eigenschap **Doel van serververificatie** van de certificaten die zijn uitgegeven door de Braziliaanse basiscertificeringsinstantie is standaard uitgeschakeld en moet handmatig worden ingeschakeld. In sommige gevallen kan de automatische certificaatupdate deze eigenschap uitschakelen. In dat geval heeft dit effect op de TLS-verbinding en wordt deze niet meer vertrouwd. Het heeft effect op de mogelijkheid om het Braziliaanse elektronische belastingdocument model 55 (NF-e) uit te geven in productieomgevingen voor de staten Minas Gerais (MG) en Paraná (PR).

Als u de oplossing wilt activeren voor **Validatie van aangepast certificaat NF-e**, gaat u naar **Functiebeheer**. Deze functie biedt een alternatieve oplossing voor de validatie van V5- en V10-certificaten en maakt een betrouwbare verbinding mogelijk met de webservices die vereist zijn voor de beveiligde overdracht van de NF-e en de ontvangst van de autorisatie van SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
