---
title: Talent-omgevingen verwijderen
description: In dit onderwerp wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Dynamics 365 Talent geleid.
author: andreabichsel
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: bbc65a77b7c3df6545dfd7aa2109aba5c4e1b57b
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2773029"
---
# <a name="remove-talent-environments"></a>Talent-omgevingen verwijderen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt u door het proces van het verwijderen van een testdrive- of productieomgeving voor Dynamics 365 Talent geleid.

## <a name="removing-a-test-drive-environment"></a>Een testdrive-omgeving verwijderen

Talent-testdrives zijn zo ingesteld dat ze na 60 dagen verlopen. Eigenaren van testdrive-omgevingen kunnen echter hun evaluatie eerder beëindigen met de volgende stappen. 

1. Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.
2. Selecteer **Omgevingen**.
3. Selecteer de testdrive-omgeving die een naampatroon heeft zoals: TestDrive - alias@domein
4. Selecteer **Verwijderen** en bevestig de beslissing. 

De bestaande testdrive-omgeving wordt verwijderd. Wanneer deze is verwijderd, kunt u zich aanmelden voor een nieuwe testdrive-omgeving. 

## <a name="removing-a-production-environment"></a>Een productieomgeving verwijderen

In dit onderwerp wordt ervan uitgegaan dat u Talent hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). 

Aangezien één Talent-omgeving is opgenomen in één Power Apps-omgeving, zijn twee opties mogelijk. De eerste optie is het verwijderen van de gehele Power Apps-omgeving; bij de tweede optie verwijdert u alleen Talent. De eerste optie is het beste wanneer u een Power Apps-omgeving speciaal voor Talent hebt gemaakt en u net met de implementatie bent begonnen, of wanneer er geen integratie is uitgevoerd. De tweede optie is geschikt wanneer u een Power Apps-omgeving hebt die is voorzien van veel gegevens, die worden gebruikt in Power Apps en Power Automate.

> [!Important]
> Controleer voordat u de Power Apps-omgeving verwijdert, of deze niet wordt gebruikt voor de integratie van gegevens buiten het bereik van Talent. Houd er ook rekening mee dat de standaard Power Apps-omgevingen niet kunnen worden verwijderd. 

De gehele Power Apps-omgeving, inclusief Talent en de bijbehorende apps en stromen, verwijderen:

1. Naar het [Power Apps Beheercentrum](https://admin.businessplatform.microsoft.com/) navigeren.
2. Selecteer **Omgevingen**.
3. Selecteer de omgeving die u wilt verwijderen.
4. Selecteer **Verwijderen** en bevestig de beslissing. 
5. Wacht tot de verwijdering voltooid is.
6. Meld u aan bij [Lifecycle Services](https://lcs.dynamics.com/Logon/Index) (LCS) met het account waarmee u zich hebt geabonneerd op Talent. 
7. Selecteer het Talent-project dat de omgeving bevat. 
8. Selecteer in uw LCS-project de tegel **Beheer Talent-app**. 
9. Selecteer het exemplaar dat u wilt verwijderen. 
10. Selecteer **Exemplaar verwijderen** en bevestig uw keuze.  

Als u een Talent-omgeving wilt verwijderen uit een bestaande Power Apps-omgeving, gaat u als volgt te werk. Contact opnemen met ondersteuning en het Talent DevOps-team is tijdelijk totdat deze functie rechtstreeks in de LCS is ingeschakeld.

1. Neem contact op met ondersteuning om een aanvraag voor verwijderen in te dienen.
2. Het ondersteuningsteam dient een aanvraag voor verwijderen in bij het Talent DevOps-team. 
3. Ga verder nadat u de bevestiging hebt ontvangen dat de omgeving is verwijderd.
4.  Meld u aan bij LCS met het account waarmee u zich hebt geabonneerd op Talent. 
5. Selecteer het Talent-project dat de omgeving bevat. 
6. Selecteer in uw LCS-project de tegel **Beheer Talent-app**. 
7. Selecteer het exemplaar dat u wilt verwijderen. Dit zou gemarkeerd moeten zijn met de implementatiestatus **Mislukt**.
8. Selecteer **Exemplaar verwijderen** en bevestig uw keuze. 

