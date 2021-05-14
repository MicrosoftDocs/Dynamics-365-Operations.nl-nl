---
title: Medewerkers zonder dienstverband
description: Medewerkers zonder toekomstig, actief of historisch dienstverband bij uw organisatie worden weergegeven in het formulier Medewerkers zonder dienstverband.
author: andreabichsel
ms.date: 04/06/2021
ms.topic: ''
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorkerV2, HRMMassHireProject, HRMMassHireLine, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2021-04-06
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e1a137de25924f4c4ec6f6b1fe70f9d21af591c0
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924566"
---
# <a name="workers-without-employment"></a>Medewerkers zonder dienstverband

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Medewerkers zonder toekomstig, actief of historisch dienstverband bij uw organisatie worden weergegeven in het formulier **Medewerkers zonder dienstverband**. Medewerkers met deze status kunnen worden weergegeven wanneer u medewerkers importeert zonder dienstverbandrecord, of wanneer u het dienstverband van een medewerker verwijdert via **Medewerkers > Historie dienstverband**.

Het formulier **Medewerkers zonder dienstverband** is standaard beschikbaar voor de volgende rollen:

- HR-assistent
- HR-manager
- Werver
- Manager Compensatie en vergoedingen
- Salarisadministrateur
- Salarismanager
- Opleidingsmanager

In de lijst **Medewerkers zonder dienstverband** kunt u de vermelde personen verwijderen. Deze bevoegdheid wordt standaard gegeven aan de rol HR-assistent. U kunt deze bevoegdheid aan andere rollen toewijzen met de volgende stappen:

1. Selecteer **Systeembeheer** en selecteer vervolgens **Beveiligingsconfiguratie**.

2. Filter op het tabblad **Bevoegdheden** de lijst **Bevoegdheden** op **Medewerkers onderhouden**.

   [![Lijst met bevoegdheden filteren](./media/hr-personnel-workers-without-employment-filter.png)](./media/hr-personnel-workers-without-employment-filter.png)

3. Selecteer in de kolom **Verwijzingen** de optie **Opdrachten in weergavemenu**.

4. Selecteer onder **Opdrachten in weergavemenu** de optie **HcmWorkersWithoutEmployment**.

   [![Formulier selecteren](./media/hr-personnel-workers-without-employment-select.png)](./media/hr-personnel-workers-without-employment-select.png)

5. Stel de machtiging **Verwijderen** in op **Toewijzen**.

6. Selecteer het tabblad **Niet-gepubliceerde objecten**.

7. Selecteer **Alles publiceren**.

   [![Wijzigingen publiceren](./media/hr-personnel-workers-without-employment-publish.png)](./media/hr-personnel-workers-without-employment-publish.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]