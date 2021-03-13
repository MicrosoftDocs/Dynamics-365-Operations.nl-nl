---
title: Een exemplaar verwijderen
description: In dit artikel wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources geleid.
author: andreabichsel
manager: tfehr
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1490bd95c284b58497325e57979e63a8190cb386
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112082"
---
# <a name="remove-an-instance"></a>Een exemplaar verwijderen

In dit artikel wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources geleid.

## <a name="remove-a-test-drive-environment"></a>Een testdrive-omgeving verwijderen

Human Resources-testdrives zijn zo ingesteld dat ze na 60 dagen verlopen. Eigenaren van testdrive-omgevingen kunnen echter hun evaluatie eerder beëindigen met de volgende stappen. 

1. Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.
2. Selecteer **Omgevingen**.
3. Selecteer de testdrive-omgeving die een naampatroon heeft zoals: TestDrive - alias@domein
4. Selecteer **Verwijderen** en bevestig de beslissing. 

De bestaande testdrive-omgeving wordt verwijderd. Wanneer deze is verwijderd, kunt u zich aanmelden voor een nieuwe testdrive-omgeving. 

## <a name="remove-a-production-environment"></a>Een productieomgeving verwijderen

In dit artikel wordt ervan uitgegaan dat u Human Resources hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). 

Aangezien één Human Resources-omgeving is opgenomen in één Power Apps-omgeving, zijn twee opties mogelijk. De eerste optie is het verwijderen van de gehele Power Apps-omgeving; bij de tweede optie verwijdert u alleen Human Resources. De eerste optie is het beste wanneer u een Power Apps-omgeving speciaal voor Human Resources hebt gemaakt en u net met de implementatie bent begonnen, of wanneer er geen integratie is uitgevoerd. De tweede optie is geschikt wanneer u een Power Apps-omgeving hebt die is voorzien van veel gegevens, die worden gebruikt in Power Apps en Power Automate.

> [!Important]
> Controleer voordat u de Power Apps-omgeving verwijdert, of deze niet wordt gebruikt voor de integratie van gegevens buiten het bereik van Human Resources. Houd er ook rekening mee dat de standaard Power Apps-omgevingen niet kunnen worden verwijderd. 

De gehele Power Apps-omgeving, inclusief Human Resources en de bijbehorende apps en stromen, verwijderen:

1. Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.
2. Selecteer **Omgevingen**.
3. Selecteer de omgeving die u wilt verwijderen.
4. Selecteer **Verwijderen** en bevestig de beslissing. 
5. Wacht tot de verwijdering voltooid is.
6. Meld u aan bij [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) met het account waarmee u zich hebt geabonneerd op Human Resources. 
7. Selecteer het Human Resources-project dat de omgeving bevat. 
8. Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**. 
9. Selecteer het exemplaar dat u wilt verwijderen. 
10. Selecteer **Exemplaar verwijderen** en bevestig uw keuze.  

Als u een Human Resources-omgeving wilt verwijderen uit een bestaande Power Apps-omgeving, gaat u als volgt te werk. Contact opnemen met ondersteuning en het Human Resources DevOps-team is tijdelijk totdat deze functie rechtstreeks in de LCS is ingeschakeld.

1. Neem contact op met ondersteuning om een aanvraag voor verwijderen in te dienen.
2. Het ondersteuningsteam dient een aanvraag voor verwijderen in bij het Human Resources DevOps-team. 
3. Ga verder nadat u de bevestiging hebt ontvangen dat de omgeving is verwijderd.
4. Meld u aan bij LCS met de account waarmee u zich hebt geabonneerd op Human Resources. 
5. Selecteer het Human Resources-project dat de omgeving bevat. 
6. Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**. 
7. Selecteer het exemplaar dat u wilt verwijderen. Dit zou gemarkeerd moeten zijn met de implementatiestatus **Verwijderd**.
8. Selecteer **Exemplaar verwijderen** en bevestig uw keuze. 

## <a name="recover-a-soft-deleted-environment"></a>Een zacht verwijderde omgeving herstellen

Als u de Power Apps-omgeving verwijdert waarop uw HRM-omgeving is aangesloten, wordt de status van de human resources-omgeving in Lifecycle Services **zacht verwijderd**. In dit geval kunnen gebruikers geen verbinding maken met human resources.

De omgeving herstellen:

1. Volg de instructies in [De Power Apps-omgeving herstellen](/power-platform/admin/recover-environment.md).

2. Neem contact op met de ondersteuning om de HRM-omgeving te herstellen. Zie voor meer informatie [Ondersteuning krijgen](hr-admin-troubleshooting-support.md).

> [!Warning]
> Power Apps-omgevingen worden slechts zeven dagen na verwijdering bewaard. U moet de omgeving binnen zeven dagen herstellen.
