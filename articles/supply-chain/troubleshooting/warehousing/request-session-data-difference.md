---
title: Onverwachte verschillen tussen aanvraag- en sessiegegevens tijdens het testen
description: Er treedt een onverwacht verschil op tussen de aanvraag- en sessiegegevens in de validatieresultaten van de taak van de magazijn-app.
author: mamuszal
ms.date: 03/11/2022
ms.topic: troubleshooting
ms.search.form: WHSValidatorRunInstance_executeRun
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mamuszal
ms.search.validFrom: 2022-03-11
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: da8f0506a76b0d0cc02bfc2e1bff01b4ddccb578
ms.sourcegitcommit: 941119133be1765f653d5d5270dfdf58466e1d07
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/17/2022
ms.locfileid: "8456935"
---
# <a name="unexpected-difference-between-request-and-session-data-during-testing"></a>Onverwachte verschillen tussen aanvraag- en sessiegegevens tijdens het testen

Foutcode: WarehouseMobileDeviceRequestInputValidationError

## <a name="symptoms"></a>Symptomen

Als u het [validatieraamwerk voor de magazijn-apptaak](/dynamics365-release-plan/2019wave2/dynamics365-supply-chain-management/warehouse-app-task-validation-rsat) gebruikt, retourneert de validator het volgende foutbericht:

> Onverwachte verschillen tussen aanvraag- en sessiegegevens. XML-protocol voor mobiele magazijnapparaten geschonden.REQUEST_XML_TAMPERING

## <a name="cause"></a>Oorzaak

De fout treedt op wanneer de uitvoer van de laatste stap die tijdens de testuitvoer is uitgevoerd, niet gelijk is aan de geregistreerde invoer voor de volgende stap. Deze situatie kan zich voordoen omdat de taakvalidator de uitvoer van een vorige stap niet gebruikt als invoer voor een volgende stap. In plaats daarvan wordt geregistreerde XML gebruikt als invoer voor elke stap.

In de meeste gevallen treedt de fout op wanneer u een taak opnieuw uitvoert, maar er voor de test records vereist zijn die zijn gewijzigd of verwijderd tijdens een eerdere run van dezelfde taak.

## <a name="resolution"></a>Oplossing

De test voor het valideren van magazijn-apptaak is geen idempotente bewerking, maar past de onderliggende gegevens aan. Voordat u een taak opnieuw uitvoert, moet u dus mogelijk de relevante gegevens opnieuw instellen.

1. Controleer de XML-uitvoer van de laatste geslaagde teststap om te bepalen waar de testuitvoer is uitgeschakeld.
1. Controleer de test en kijk of alle vereiste verkooporders, transferorders, werkkopteksten en andere records nog aanwezig zijn en de verwachte status hebben.
1. Maak ontbrekende of gewijzigde records opnieuw of bewerk ze. U kunt ook een nieuwe testopzet maken en het ontwerp geldige bestaande records laten gebruiken.
