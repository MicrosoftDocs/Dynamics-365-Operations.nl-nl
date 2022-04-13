---
title: Een exemplaar verwijderen
description: In dit onderwerp wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Dynamics 365 Human Resources geleid.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba5d69ca33ac84743b178ded80b482eee6edab1e
ms.sourcegitcommit: 6f6ec4f4ff595bf81f0b8b83f66442d5456efa87
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/25/2022
ms.locfileid: "8487725"
---
# <a name="remove-an-instance"></a>Een exemplaar verwijderen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources uitgelegd.

## <a name="remove-a-test-drive-environment"></a>Een testdrive-omgeving verwijderen

Human Resources-testdrives zijn zo ingesteld dat ze na 60 dagen verlopen. Eigenaren van testdrive-omgevingen kunnen echter hun evaluatie eerder beëindigen met de volgende stappen. 

1. Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.
2. Selecteer **Omgevingen**.
3. Selecteer de testdrive-omgeving die een naampatroon heeft zoals: TestDrive - alias@domein
4. Selecteer **Verwijderen** en bevestig de beslissing. 

De bestaande testdrive-omgeving wordt verwijderd. Wanneer deze is verwijderd, kunt u zich aanmelden voor een nieuwe testdrive-omgeving. 

## <a name="remove-a-production-environment"></a>Een productieomgeving verwijderen

In dit onderwerp wordt ervan uitgegaan dat u Human Resources hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). 

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

1. Volg de instructies in [De Power Apps-omgeving herstellen](/power-platform/admin/recover-environment).

2. Neem contact op met de ondersteuning om de HRM-omgeving te herstellen. Zie voor meer informatie [Ondersteuning krijgen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Apps-omgevingen worden slechts zeven dagen na verwijdering bewaard. U moet de omgeving binnen zeven dagen herstellen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
