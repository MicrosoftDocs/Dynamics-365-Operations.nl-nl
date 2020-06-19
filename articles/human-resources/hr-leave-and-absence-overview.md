---
title: Overzicht
description: In Dynamics 365 Human Resources biedt het werkgebied Verlof en verzuim een flexibel raamwerk voor het maken van nieuwe verlofplannen, workflows voor het beheren van aanvragen en een intuïtieve selfservicepagina voor werknemers om verlof aan te vragen.
author: andreabichsel
manager: AnnBe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ec72d2d741f7f8428a7daa97bb982e9fc00b8c3f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428962"
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

- **Verlofopbouw per bedrijf of plan**: u kunt het toerekeningsproces uitvoeren voor alle bedrijven of voor één bedrijf. U kunt het toerekeningsproces ook uitvoeren voor een specifiek verlofplan voor een specifiek bedrijf. 

- **Verlof kopen**: u kunt beleid voor het kopen van verlof inschakelen en maken, zodat werknemers koopaanvragen kunnen indienen. Werknemers kunnen koopaanvragen indienen en saldi automatisch laten bijwerken asis van de aanvraag.  

- **Bijlagen toevoegen aan goedgekeurde verlofaanvragen**: u kunt een bijlage toevoegen aan een verlofaanvraag die al is goedgekeurd. 

