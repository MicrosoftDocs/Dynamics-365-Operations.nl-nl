---
title: Bewerken van persoonlijke gegevens beperken
description: Voorkomen dat werknemers contactgegevens bewerken in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EssWorkspace
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-03-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c82114f6600345ee5e2eb9c1c0629ae6c8f0b9a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877680"
---
# <a name="restrict-editing-of-personal-information"></a>Bewerken van persoonlijke gegevens beperken


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [applies to](../includes/applies-to-hr.md)]
[!include [preview feature](./includes/preview-feature.md)]

In dit artikel wordt beschreven hoe u voorkomt dat werknemers contactgegevens bewerken in Dynamics 365 Human Resources. U wilt mogelijk voorkomen dat werknemers bepaalde contactgegevens bewerken, zoals de locatie van hun bedrijf of e-mailadres.

> [!NOTE]
> Als u deze functie wilt gebruiken, moet u eerst **(Preview) Voorkomen dat werknemers adres- en contactgegevens toevoegen of bewerken voor bepaalde doeleinden** in Functiebeheer. Meer informatie over het inschakelen van de previewfuncties vindt u in [Functies beheren](hr-admin-manage-features.md).<br><br>![Voorbeeldfunctie inschakelen.](./media/hr-employee-self-service-restrict-enable.png)

## <a name="choose-the-information-an-employee-can-add-or-edit"></a>De informatie kiezen die een werknemer kan toevoegen of bewerken

1. Selecteer **Personeelsbeheer** in Human Resources, en vervolgens **Koppelingen** en **Parameters Human Resources**.

   ![Ga naar Human Resources-parameters.](./media/hr-employee-self-service-human-resources-parameters.png)

2. Selecteer op de pagina **Parameters voor Human Resources** het tabblad **Selfservice werknemers**.

   ![Selecteer Werknemerselfservice.](./media/hr-employee-self-service-tab.png)

3. Schakel op het tabblad **Selfservice voor werknemers** alle informatie in de sectie **Adres- en contactgegevens** uit die u niet door werknemers wilt laten toevoegen of bewerken. In dit voorbeeld hebben we de **zakelijke** contactgegevens uitgeschakeld.

   ![Bewerken van zakelijke contactgegevens beperken.](./media/hr-employee-self-service-restrict-business.png)

4. Selecteer **Opslaan**.

   ![Wijzigingen opslaan.](./media/hr-employee-self-service-restrict-save.png)

## <a name="employee-experience"></a>Werknemerservaring

Wanneer u hebt ingesteld dat werknemers beperkt contactgegevens kunnen toevoegen of bewerken, kunnen ze de informatie wel bekijken, maar ze kunnen deze niet wijzigen.

Hoewel werknemers in dit voorbeeld geen **Zakelijke** contactgegevens mogen bewerken, kunnen ze de informatie nog wel zien in de **Selfservice werknemers**:

![Zakelijke contactgegevens weergeven.](./media/hr-employee-self-service-restrict-view.png)

Wanneer ze de zakelijke contactgegevens selecteren, wordt het deelvenster **Adres bewerken** echter weergegeven als alleen-lezen en kunnen ze de velden niet wijzigen.

![Zakelijke contactgegevens worden weergegeven als alleen-lezen.](./media/hr-employee-self-service-restrict-read-only.png)

En als zijn **Toevoegen** selecteren om een nieuw adres toe te voegen, kunnen zij in het vervolgkeuzevak **Doel** de optie **Zakelijk** niet selecteren.

![Werknemer kan geen zakelijk toevoegen.](./media/hr-employee-self-service-restrict-add.png)

Werknemers krijgen dezelfde ervaring wanneer ze **Contactgegevens** selecteren op de pagina **Persoonlijke informatie** en een nieuw adres toevoegen. In het vervolgkeuzevak **Doel** worden alleen de typen gegevens weergegeven die ze kunnen toevoegen. 

![Werknemer kan Zakelijk niet selecteren in de vervolgkeuzelijst Doel.](./media/hr-employee-self-service-restrict-purpose.png)

**Contactgegevens** toont nu **Doel** in het raster.

![Doel wordt weergegeven in raster Contactgegevens.](./media/hr-employee-self-service-restrict-purpose-grid.png)

## <a name="see-also"></a>Zie ook

[Overzicht van Selfservice werknemer en Selfservice manager](hr-employee-manager-self-service-overview.md)<br>
[Human Resources-parameters configureren](hr-setup-parameters.md)<br>
[Persoonlijke gegevens bewerken](hr-employee-manager-self-service-edit-personal-information.md)
