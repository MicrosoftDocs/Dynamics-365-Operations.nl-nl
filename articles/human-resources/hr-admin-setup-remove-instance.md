---
title: Een exemplaar verwijderen
description: In dit artikel wordt het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources beschreven.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0ce676c93e133cc04ad9c49417ed2ca0d6791e93
ms.sourcegitcommit: 1401d66b6b64c590ca1f8f339d622e922920cf15
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/20/2022
ms.locfileid: "9178467"
---
# <a name="remove-an-instance"></a>Een exemplaar verwijderen

_**Is van toepassing op:** Human resources in de zelfstandige infrastructuur_ 

> [!NOTE]
> Vanaf juli 2022 kunnen er geen nieuwe Human Resources-omgevingen worden ingericht in de zelfstandige Human Resources-infrastructuur en er kunnen geen nieuwe Microsoft Dynamics LCS-projecten (Lifecycle Services) in worden gemaakt. Klanten kunnen Human Resources-omgevingen implementeren in de infrastructuur voor financiën en bedrijfsactiviteiten. Zie voor meer informatie [Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten inrichten](/hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> De infrastructuur van de app voor financiën en bedrijfsactiviteiten ondersteunt het verwijderen van een omgeving. Zie [Een omgeving verwijderen](../fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure.md#delete-an-environment) voor meer informatie over het verwijderen van een omgeving.

In dit artikel wordt het proces van het verwijderen van een testdrive- of productieomgeving voor Microsoft Dynamics 365 Human Resources uitgelegd.

## <a name="remove-a-test-drive-environment"></a>Een testdrive-omgeving verwijderen

Human Resources-testdrives zijn zo ingesteld dat ze na 60 dagen verlopen. Eigenaren van testdrive-omgevingen kunnen echter hun evaluatie eerder beëindigen met de volgende stappen. 

1. Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.
2. Selecteer **Omgevingen**.
3. Selecteer de testdrive-omgeving die een naampatroon heeft zoals: TestDrive - alias@domein
4. Selecteer **Verwijderen** en bevestig de beslissing. 

De bestaande testdrive-omgeving wordt verwijderd. Wanneer deze is verwijderd, kunt u zich aanmelden voor een nieuwe testdrive-omgeving. 

## <a name="remove-a-production-environment"></a>Een productieomgeving verwijderen

In dit artikel wordt ervan uitgegaan dat u Human Resources hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). 

Aangezien één Human Resources-omgeving is opgenomen in één Power Apps-omgeving, kunnen twee opties worden overwogen bij het verwijderen van een omgeving: 
- **De gehele Power Apps-omgeving verwijderen.** Deze optie heeft de voorkeur wanneer de Power Apps-omgeving speciaal voor de inrichting van Human Resources is gemaakt, de implementatie net is begonnen of wanneer u geen ingestelde integraties hebt.  
- **Alleen Human Resources verwijderen.** Deze optie is geschikt wanneer er een ingestelde Power Apps-omgeving is waarin veel gegevens zijn ingevuld die worden gebruikt in Microsoft Power Apps en Power Automate.


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

Als u de Power Apps-omgeving verwijdert waarmee uw Human Resources-omgeving is verbonden, wordt de status van de Human Resources-omgeving in LCS **Voorlopig verwijderd**. In dit geval kunnen gebruikers geen verbinding maken met human resources.

De omgeving herstellen:

1. Volg de instructies in [De Power Apps-omgeving herstellen](/power-platform/admin/recover-environment).

2. Neem contact op met de ondersteuning om de HRM-omgeving te herstellen. Zie voor meer informatie [Ondersteuning krijgen](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).

> [!Warning]
> Power Apps-omgevingen worden slechts zeven dagen na verwijdering bewaard. U moet de omgeving binnen zeven dagen herstellen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
