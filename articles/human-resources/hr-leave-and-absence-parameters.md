---
title: Parameters voor verlof en verzuim configureren
description: In dit onderwerp wordt beschreven hoe u human resources-parameters voor verlof en verzuim definieert in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 79052c550783dee1ba4091ad10bde4d79d7b905e
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8690689"
---
# <a name="configure-leave-and-absence-parameters"></a>Parameters voor verlof en verzuim configureren

>[!Important]
>De functionaliteit die in dit onderwerp wordt vermeld, is momenteel beschikbaar voor klanten van de zelfstandige versie van Dynamics 365 Human Resources. Sommige of alle functionaliteit is beschikbaar als onderdeel van een toekomstige versie van de Finance-infrastructuur na versie 10.0.26 van Finance.


[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Voordat u verlof- en verzuimplannen instelt in Dynamics 365 Human Resources, kunt u het best de instellingen controleren voor alle verwante **Human resources-parameters**, waaronder:

- Nummerreeks voor verlofaanvragen
- FMLA-instellingen (Family and Medical Leave Act)
- Selfservice-instellingen voor werknemers voor verlof- en verzuimaanvragen
- Verlof- en verzuimparameters

## <a name="view-and-change-human-resources-parameters"></a>Human resources-parameters weergeven en wijzigen

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Instellen** de optie **Human resources-parameters**.

3. Controleer op het tabblad **Nummerreeksen** de optie **Nummerreekscode** voor **Verlofaanvraag-id** en wijzig deze indien nodig. Deze instelling bepaalt de volgorde waarin id's voor verlofaanvragen automatisch worden toegewezen.

4. Controleer op het tabblad **FMLA** de FMLA instellingen en wijzig deze indien nodig.

5. Geef op het tabblad **Selfservice werknemer** aan of managers verlof- en verzuimaanvragen kunnen invoeren namens hun werknemers.

7. Selecteer **Opslaan**.

>[!IMPORTANT]
>Het bekijken van verlof en afwezigheid binnen bedrijven wordt momenteel in een voorbeeld weergegeven. U moet de optie in uw **Sandbox**-omgeving inschakelen om de optie voor verlof en verzuim weer te geven. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van previewfuncties.

## <a name="view-and-change-human-resources-shared-parameters"></a>Gedeelde Human Resources-parameters weergeven en wijzigen

1. Op de **Personeelsbeheer** selecteert u het tabblad **Koppelingen**.

2. Selecteer onder **Instellen** de optie **Gedeelde Human Resources-parameters**.

3. Selecteer op het tabblad **Geavanceerde toegang** de optie **Ja** bij **Verlofweergave voor het hele bedrijf inschakelen**.

4. Selecteer **Opslaan**.

## <a name="view-and-change-leave-and-absence-parameters"></a>Parameters voor verlof en verzuim weergeven en aanpassen

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Instellingen** de optie **Parameters voor verlof en verzuim**.

3. Stel op het tabblad **Algemeen** de volgende parameters in:
 
    - Stel **Eenheid voor verlof en verzuim** in op uren of dagen. Bij dagen kunt u de optie **Definitie halve dag inschakelen** om werknemers in staat te stellen om de eerste of de tweede helft van de dag te kiezen in hun verlofaanvraag. 

    - Selecteer **Ingangsdatum servicemaanden** om in te stellen wanneer de toerekeningspercentages van kracht worden voor verlofplannen met servicemaanden.

    - Selecteer **Saldoberekening** om saldi weer te geven vanaf vandaag of vanaf de toerekeningsperiode. Als u vandaag **Saldo vanaf vandaag** selecteert, wordt in het saldo het totaal van alle transitorische posten, correcties en aanvragen vanaf vandaag weergegeven. Als u **Saldo vanaf toerekeningsperiode** selecteert, wordt in het saldo het totaal van alle transitorische posten, correcties en aanvragen weergegeven vanaf de toerekeningsperiode die is gedefinieerd door de frequentie in het verlofplan. 

    - Stel de **Begintijd** in voor de batchtaak voor het **transporteren van vervaldatums**.  
    
    - Selecteer **Ja** om **Werknemers toestaan om verlof te kopen** en **Werknemers toestaan om verlof te verkopen**. Als u **Ja** selecteert voor deze opties, kunt u een inkoop- en verkoopbeleid maken en werknemers in staat stellen om aanvragen voor het kopen en verkopen van verlof in te dienen.

## <a name="configure-calendar-parameters"></a>Kalenderparameters configureren

1. Selecteer op de pagina **Verlof en verzuim** het tabblad **Koppelingen**.

2. Selecteer onder **Instellingen** de optie **Parameters voor verlof en verzuim**.

3. Wijzig op het tabblad **Kalender** de kalenderinstellingen indien nodig.

4. Selecteer **Opslaan**.

## <a name="see-also"></a>Zie ook

- [Overzicht van verlof en verzuim](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
