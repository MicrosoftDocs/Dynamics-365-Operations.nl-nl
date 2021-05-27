---
title: Bewerken van persoonlijke gegevens beperken
description: Voorkomen dat werknemers contactgegevens bewerken in Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c5e3eeb66d4f32b1fea1a43fff9f5b09d87d1f53
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018704"
---
# <a name="restrict-editing-of-personal-information"></a>Bewerken van persoonlijke gegevens beperken

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

In dit onderwerp wordt beschreven hoe u voorkomt dat werknemers contactgegevens bewerken in Dynamics 365 Human Resources. U wilt mogelijk voorkomen dat werknemers bepaalde contactgegevens bewerken, zoals de locatie van hun bedrijf of e-mailadres.

> [!NOTE]
> Als u deze functie wilt gebruiken, moet u eerst **(Preview) Voorkomen dat werknemers adres- en contactgegevens toevoegen of bewerken voor bepaalde doeleinden** in Functiebeheer. Meer informatie over het inschakelen van de previewfuncties vindt u in [Functies beheren](hr-admin-manage-features.md).<br><br>![Voorbeeldfunctie inschakelen](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>De informatie kiezen die een werknemer kan toevoegen of bewerken

1. Selecteer **Personeelsbeheer** in Human Resources, en vervolgens **Koppelingen** en **Parameters Human Resources**.

   ![Ga naar Human Resources-parameters](./media/hr-employee-self-service-human-resources-parameters.png)

2. Selecteer op de pagina **Parameters voor Human Resources** het tabblad **Selfservice werknemers**.

   ![Selfservice voor werknemers selecteren](./media/hr-employee-self-service-tab.png)

3. Schakel op het tabblad **Selfservice voor werknemers** alle informatie in de sectie **Adres- en contactgegevens** uit die u niet door werknemers wilt laten toevoegen of bewerken. In dit voorbeeld hebben we de **zakelijke** contactgegevens uitgeschakeld.

   ![Bewerken van zakelijke contactgegevens beperken](./media/hr-employee-self-service-restrict-business.png)

4. Selecteer **Opslaan**.

   ![Wijzigingen opslaan](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Werknemerservaring

Wanneer u hebt ingesteld dat werknemers beperkt contactgegevens kunnen toevoegen of bewerken, kunnen ze de informatie wel bekijken, maar ze kunnen deze niet wijzigen.

Hoewel werknemers in dit voorbeeld geen **zakelijke** contactgegevens mogen bewerken, kunnen ze de informatie nog wel zien in de Selfservice voor werknemers:

![Zakelijke contactgegevens weergeven](./media/hr-employee-self-service-restrict-view.png)

Wanneer ze de zakelijke contactgegevens selecteren, wordt het deelvenster **Adres bewerken** echter weergegeven als alleen-lezen en kunnen ze de velden niet wijzigen.

![Zakelijke contactgegevens worden weergegeven als alleen-lezen](./media/hr-employee-self-service-restrict-read-only.png)

En als zijn **Toevoegen** selecteren om een nieuw adres toe te voegen, kunnen zij in het vervolgkeuzevak **Doel** de optie **Zakelijk** niet selecteren.

![Werknemer kan geen zakelijk toevoegen](./media/hr-employee-self-service-restrict-add.png)

Werknemers krijgen dezelfde ervaring wanneer ze **Contactgegevens** selecteren op de pagina **Persoonlijke informatie** en een nieuw adres toevoegen. In het vervolgkeuzevak **Doel** worden alleen de typen gegevens weergegeven die ze kunnen toevoegen. 

![Werknemer kan Zakelijk niet selecteren in de vervolgkeuzelijst Doel](./media/hr-employee-self-service-restrict-purpose.png)

**Contactgegevens** toont nu **Doel** in het raster.

![Doel wordt weergegeven in raster Contactgegevens](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Zie ook

[Overzicht van Selfservice werknemer en Selfservice manager](hr-employee-manager-self-service-overview.md)<br>
[Human Resources-parameters configureren](hr-setup-parameters.md)<br>
[Persoonlijke gegevens bewerken](hr-employee-manager-self-service-edit-personal-information.md)