---
title: Problemen met de upgrade en migratie naar geavanceerd magazijnbeheer oplossen
description: In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens upgraden en migreren naar geavanceerd magazijnbeheer.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 953b828667a01157767c3ca79349fe972b0fbe9b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826390"
---
# <a name="troubleshoot-upgrade-and-migration-to-advanced-warehouse-management"></a>Problemen met de upgrade en migratie naar geavanceerd magazijnbeheer oplossen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u veelvoorkomende problemen kunt oplossen die kunnen optreden tijdens upgraden en migreren naar geavanceerd magazijnbeheer.

## <a name="i-receive-the-following-error-message-javasecuritycertcertpathvalidatorexception-trust-anchor-for-certification-path-is-not-found"></a>Het volgende foutbericht wordt weergegeven: "java.security.cert.certPathValidatorException: vertrouwensanker voor certificaatpad is niet gevonden."

### <a name="issue-description"></a>Probleembeschrijving

U ontvangt dit foutbericht in de mobiele app Magazijnbeheer, omdat zelfondertekende certificaten niet worden vertrouwd op Android 8+ in on-premises-omgevingen.

### <a name="issue-resolution"></a>Probleemoplossing

Gebruik een externe (openbare) certificeringsinstantie (CA). Er is een oplossing voor dit probleem beschikbaar in versie 1.9.0.0 van de magazijn-app. Zie [Verbindingsproblemen in de mobiele app Magazijnbeheer oplossen](troubleshoot-warehouse-app-connection.md) voor informatie over dit probleem en hoe u het kunt oplossen.

## <a name="what-is-the-approved-process-for-moving-from-basic-warehousing-to-advanced-warehousing"></a>Wat is het goedgekeurde proces voor het verplaatsen van basaal magazijnbeheer naar geavanceerd magazijnbeheer?

### <a name="issue-description"></a>Probleembeschrijving

U werkt momenteel onder voorraad beheer en gebruikt de basisvoorraadfunctionaliteit en u wilt overstappen op geavanceerd magazijnbeheer om gebruik te kunnen maken van mobiele apparaten, waves en werk. U ondervindt echter problemen wanneer u deze overstap wilt maken. U kunt uw producten bijvoorbeeld niet wijzigen, zodat ze opslagdimensies (site, magazijn en locatie) gebruiken, omdat de producten hiervoor transacties hebben. Daarom moet u weten wat het goedgekeurde proces is voor het verplaatsen van basaal magazijnbeheer naar geavanceerd magazijnbeheer.

### <a name="issue-resolution"></a>Probleemoplossing

Zie voor meer informatie over het proces voor het overstappen van basaal magazijnbeheer naar geavanceerd magazijnbeheer de volgende blogberichten en documentatie:

- [Magazijnbeheerproces inschakelen voor bestaande artikelen en magazijnen.](https://cleverax.wordpress.com/2017/12/06/d365fo-enable-warehouse-management-process-for-existing-items-and-warehouses/)
- [Migratie van Microsoft Dynamics AX WMS naar nieuwe R3-magazijn- en transportfunctionaliteit](https://cloudblogs.microsoft.com/dynamics365/no-audience/2015/08/17/migration-of-microsoft-dynamics-ax-wms-to-new-r3-warehouse-and-transportation-functionality/)
- [Migratie van WMSI/WMS2-artikelen](https://cloudblogs.microsoft.com/dynamics365/no-audience/2018/05/03/wmsiwms2-item-migration/)
- [Upgrade van magazijnbeheer van Microsoft Dynamics AX 2012 naar Supply Chain Management](https://docs.microsoft.com/dynamics365/supply-chain/warehousing/upgrade-migration-warehouse-management-processes)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]