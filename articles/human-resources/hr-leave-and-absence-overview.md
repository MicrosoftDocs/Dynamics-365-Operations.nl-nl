---
title: Overzicht
description: In Dynamics 365 Human Resources biedt het werkgebied Verlof en verzuim een flexibel raamwerk voor het maken van nieuwe verlofplannen, workflows voor het beheren van aanvragen en een intuïtieve selfservicepagina voor werknemers om verlof aan te vragen.
author: andreabichsel
manager: AnnBe
ms.date: 04/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2bb123b808615ff7d770c7c6b83338a32d922be3
ms.sourcegitcommit: de217452a85429675994e9cc0e06eb4821cab3e5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/30/2020
ms.locfileid: "3325760"
---
# <a name="overview"></a>Overzicht

Dynamics 365 Human Resources helpt u uitstekende verlofvergoedingen aan uw werknemers te bieden. het werkgebied **Verlof en verzuim** biedt een flexibel raamwerk voor het maken van nieuwe verlofplannen, workflows voor het beheren van aanvragen en een intuïtieve selfservicepagina voor werknemers om verlof aan te vragen. Met Analytics kunt u de saldi en het gebruik van uw verlofplannen in uw organisatie meten en bijhouden.

## <a name="set-up-leave-and-absence"></a>Verlof en verzuim instellen

Voordat u verlofplannen voor uw werknemers maakt, moet u enkele installatiestappen uitvoeren:

- [Parameters voor verlof en verzuim configureren](hr-leave-and-absence-parameters.md)
- [Een werktijdkalender maken](hr-leave-and-absence-working-time-calendar.md)
- [Een werkstroom voor verlofaanvragen maken](hr-leave-and-absence-workflow.md)

## <a name="create-and-manage-leave-plans"></a>Verlofplannen maken en beheren

Voordat u plannen voor uw werknemers maakt, moet u verlof- en verzuimtypen maken. Nadat u een verlofplan hebt gemaakt, kunt u werknemers inschrijven voor het plan. U kunt ook het toerekenproces uitvoeren, waarschuwingen maken en analyses voor uw plannen weergeven.

- [Verlof- en verzuimtypen configureren](hr-leave-and-absence-types.md)
- [Een verlof- en verzuimplan maken](hr-leave-and-absence-plans.md)
- [Medewerkers toewijzen aan een verlofplan](hr-leave-and-absence-enroll.md)
- [Verlof- en verzuimplannen toerekenen](hr-leave-and-absence-accrue.md)
- [Analyses voor verlof en verzuim weergeven](hr-leave-and-absence-analytics.md)

## <a name="request-time-off-and-manage-requests"></a>Verlof aanvragen en aanvragen beheren

Uw werknemers kunnen verlofaanvragen indienen en u kunt deze beheren in het werkgebied **Selfservice werknemer**.

- [Verlof aanvragen](hr-employee-self-service-request-time-off.md)
- [Verlof- en verzuimaanvragen beheren](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-known-issues"></a>Bekende problemen met verlof en verzuim

### <a name="rounding-precision"></a>Afrondingsprecisie

U kunt geen **Afrondingsprecisie** instellen wanneer u het **Afrondingstype** instelt. U kunt alleen een **Afrondingsprecisie** instellen met de entiteit **Verlof- en verzuimtype**. 

1. Selecteer vanuit **Verlof- en verzuimtypen** de optie **Openen in Excel** om de entiteit **Verlof- en verzuimtype** te openen.

2. Nadat het bestand is geopend en ingeschakeld, selecteert u **Ontwerpen**.

3. Selecteer in de tabel **Verlof- en verzuimtype** de potloodoptie om te bewerken.

4. Selecteer **RoundingPrecision** en **RoundingType** en vervolgens **Toevoegen** om deze aan de lijst met velden toe te voegen.

5. Selecteer **Bijwerken** en vervolgens **Gereed**.

6. Voer het **Afrondingstype** in of selecteer het voor elk verloftype als dat nog niet is ingesteld. 

7. Voer de **Afrondingsprecisie** voor de toepasselijke typen in.

8. Selecteer **Publiceren** om de wijzigingen door te voeren in Human Resources.

## <a name="leave-and-absence-preview-features"></a>Preview-functies voor verlof en verzuim

U kunt nieuwe preview-functies voor Verlof en verzuim uitproberen in een **sandbox**-omgeving. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van preview-functies. 

[!include [banner](includes/preview-feature.md)]

De preview-functies omvatten:

- **Verlof opschorten**: u kunt verlof en verzuim in Human Resources opschorten voor een werknemer. Als u het verlof opschort, wordt het toegerekende verlof stopgezet voor de geselecteerde verloftypen. Als het opschorten plaatsvindt nadat een toerekening is verwerkt, wordt door het onderbreken van het verlof een evenredige correctie in het verlof van de werknemer gemaakt. U kunt ook redencodes opnemen bij het onderbreken van het verlof van een werknemer. De gebruikerservaring is bijgewerkt om de schorsing aan te geven. 

- **Regels voor transporteren**: u kunt een verloftype voor transporteren opgeven voor verlofsaldi waarvoor transportcorrecties worden overgeboekt. Als een werknemer bijvoorbeeld 10 dagen transporteert, kunt u voor deze 10 dagen een ander verloftype kiezen. 

- **Redencode en opmerkingen voor correcties opnemen**: u kunt een redencode en een opmerking opnemen wanneer u het eindsaldo van een werknemer wijzigt. 

- **Overgang naar verlof- en verzuimparameters**: u kunt nu alleen verlof- en verzuimparameters gebruiken in plaats van HR-parameters te gebruiken. 
