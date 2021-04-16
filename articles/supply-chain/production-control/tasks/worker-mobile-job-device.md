---
title: Een medewerker configureren met het mobiele taakapparaat
description: In dit onderwerp wordt uitgelegd hoe u de juiste rollen toewijst aan de gebruikersaccount van een medewerker, en de medewerker vervolgens de mogelijk biedt om werkvloerregistraties te doen.
author: ShylaThompson
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysUserManagement, HcmWorker, JmgRegistrationSetupTouch, JmgRegistrationSetupAssignUsers
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3fe4e195763f5329ee7732a2f087094acbad595a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810937"
---
# <a name="configure-a-worker-using-the-mobile-job-device"></a>Een medewerker configureren met het mobiele taakapparaat

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de juiste rollen toewijst aan de gebruikersaccount van een medewerker, en de medewerker vervolgens de mogelijk biedt om werkvloerregistraties te doen.

## <a name="verify-that-a-worker-is-assigned-a-certain-role"></a>Controleren of aan een medewerker een bepaalde rol is toegewezen

Voor dit voorbeeld controleert u of aan gebruiker SHANNON de rol van machineoperator is toegewezen voordat u de medewerkersaccount configureert.

1. Ga naar **Navigatievenster > Modules > Systeembeheer > Gebruikers > Gebruikers**.
2. Zoek naar een gebruiker in het snelfilter. Voer voor dit voorbeeld `shannon` in.
3. Selecteer de koppeling in de kolom **Gebruikers-id** van het gebruikersaccount dat wordt weergegeven.
4. Selecteer in de structuur **Rollen van gebruiker** de optie **Rollen > Machineoperator**.
5. Sluit de pagina's **Gebruikersgegevens** en **Gebruikers** om terug te keren naar de startpagina.

## <a name="configure-worker-account"></a>Medewerkersaccount configureren
1. Ga naar **Navigatievenster > Modules > Human Resources > Medewerkers > Medewerkers**.
2. Zoek naar een gebruiker in het snelfilter. Voer voor dit voorbeeld `shannon` in.
3. Selecteer de koppeling in de kolom **Naam** van het gebruikersaccount dat wordt weergegeven.
4. Selecteer het tabblad **Tijdregistratie**.
5. Selecteer **Activeren op registratieterminals**.
6. Typ of selecteer waarden in de volgende velden:  

    - **Berekeningsgroep**  
    - **Standaardberekeningsgroep**  
    - **Goedkeuringsgroep**  
    - **Standaardprofiel**  
    - **Profielgroep**  

7. Selecteer **OK**.
8. Selecteer **Bewerken** om een badgenummer voor de nieuwe tijdregistratiemedewerker in te voeren. Voer een waarde in het veld **Badge-id** in.
9. Selecteer **Opslaan**.
10. Sluit de pagina's **Medewerkersgegevens** en **Medewerkers**.

## <a name="assign-worker-to-device-group"></a>Medewerker toewijzen aan apparaatgroep
1. Ga naar **Productiebeheer > Instellen > Productie-uitvoering > Taakkaart configureren voor apparaten**.
2. Selecteer **Toevoegen**.
3. Selecteer de gewenste medewerker in de lijst. Voor dit voorbeeld selecteert u **SHANNON**.
4. Selecteer **OK**.
5. Selecteer **Bewerken**.
6. In het veld **Productie-eenheid** kunt u het standaardfilter voor de medewerker instellen. Dit zorgt ervoor dat alleen productietaken voor de geselecteerde productie-eenheid worden weergegeven wanneer de medewerker zich bij het apparaat aanmeldt. Voer de gewenste waarde in.
7. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]