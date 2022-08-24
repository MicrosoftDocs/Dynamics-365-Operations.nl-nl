---
title: Aangepaste validatie van NF-e-certificaat
description: Dit artikel bevat informatie over het inschakelen en gebruiken van het aangepaste certificaat NF-e.
author: gionoder
ms.date: 07/29/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.custom: 97423
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: f78fdbd133aecaf9dbf8abe0006abd6deb1b1b15
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288539"
---
# <a name="nf-e-custom-certificate-validation"></a>Aangepaste validatie van NF-e-certificaat

[!include [banner](../includes/banner.md)]

De eigenschap **Doel van serververificatie** van de certificaten die zijn uitgegeven door de Braziliaanse basiscertificeringsinstantie is standaard uitgeschakeld en moet handmatig worden ingeschakeld. In sommige gevallen kan de automatische certificaatupdate deze eigenschap uitschakelen. In dat geval heeft dit effect op de TLS-verbinding en wordt deze niet meer vertrouwd. Het heeft effect op de mogelijkheid om het Braziliaanse elektronische belastingdocument model 55 (NF-e) uit te geven in productieomgevingen voor de staten Minas Gerais (MG) en Paraná (PR).

Als u de oplossing wilt activeren voor **Validatie van aangepast certificaat NF-e**, gaat u naar **Functiebeheer**. Deze functie biedt een alternatieve oplossing voor de validatie van V5- en V10-certificaten en maakt een betrouwbare verbinding mogelijk met de webservices die vereist zijn voor de beveiligde overdracht van de NF-e en de ontvangst van de autorisatie van SEFAZ.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
