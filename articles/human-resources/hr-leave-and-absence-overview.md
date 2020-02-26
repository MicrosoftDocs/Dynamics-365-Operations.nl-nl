---
title: Overzicht
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 9a36f6b6ba696fa926ab3d6298568dddfce43a57
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008660"
---
# <a name="overview"></a>Overzicht

Dynamics 365 Human Resources helpt u uitstekende verlofvergoedingen aan uw werknemers te bieden. het werkgebied **Verlof en verzuim** biedt een flexibel raamwerk voor het maken van nieuwe verlofplannen, workflows voor het beheren van aanvragen en een intuïtieve selfservicepagina voor werknemers om verlof aan te vragen. Met Analytics kunt u de saldi en het gebruik van uw verlofplannen in uw organisatie meten en bijhouden.

## <a name="set-up-leave-and-absence"></a>Verlof en verzuim instellen

Voordat u verlofplannen voor uw werknemers kunt maken, moet u enkele installatiestappen uitvoeren:

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

- [Vrije tijd aanvragen](hr-employee-self-service-request-time-off.md)
- [Verlof- en verzuimaanvragen beheren](hr-employee-self-service-manage-requests.md)

## <a name="leave-and-absence-preview-features"></a>Preview-functies voor verlof en verzuim

U kunt nieuwe preview-functies voor Verlof en verzuim uitproberen in een **sandbox**-omgeving. Zie [Functies beheren](hr-admin-manage-features.md) voor meer informatie over het inschakelen van preview-functies. De preview-functies omvatten:

- **Verlof- en verzuimkalender** - verlof- en verzuimparameters zijn verplaatst van **Parameters personeel** naar een nieuw scherm met de naam **Parameters verlof en verzuim**. Het nieuwe scherm bevat een nieuw tabblad **Kalender**. In deze preview wordt alleen een subset van de parameters ingeschakeld. U kunt het nieuwe scherm openen via het tabblad **Koppelingen** van het werkgebied **Verlof en verzuim**. De kalenders omvatten:
  - **Bedrijfskalender**: hierin worden alle verlofaanvragen voor werknemers weergegeven. Personen met de **Human resources**-rol hebben toegang tot deze kalender via het tabblad **Koppelingen** van het werkgebied **Verlof en verzuim**.
  - **Managerteamkalender** - hier worden alle verlofaanvragen van ondergeschikten weergegeven. Managers hebben toegang tot de kalender via het tabblad **Mijn team** in Werknemerselfservice onder **Verlof en verzuim**. 

- **Vakantiekalenders voor verlof en verzuim** - tot de typen verlof behoort de nieuwe optie **Vakantie** die in combinatie met de werktijdkalender wordt gebruikt. Dagen die worden gedefinieerd als feestdagen en sluitingsdagen, worden nu aangemerkt als **Vakantie** wanneer werkdagen worden gegenereerd. Wanneer de opbouw van verlofdagen wordt verwerkt, worden correcties aangebracht in werknemers die aan de kalender zijn toegewezen voor vakantiedagen die op een werkdag vallen.

- **Controle van verlofopbouw** - op een nieuw scherm kunt u controleren wanneer de verlofopbouw is verwerkt en verwijderd, zowel door alle werknemers als door individuele werknemers. U kunt dit nieuwe scherm openen via het tabblad **Koppelingen** van het werkgebied **Verlof en verzuim**.

- **Verwijdering van verlofopbouw** - u kunt nu verlofopbouwrecords voor bepaalde verlofplannen verwijderen. U kunt toegang krijgen tot deze nieuwe optie via het tabblad **Koppelingen** van het werkgebied **Verlof en verzuim**. Voor afzonderlijke werknemers wordt deze optie weergegeven in de groep **Verlof en verzuim** in het werknemersprofiel. 

- **Verlofopbouw afronden** - nieuwe opties voor **Verloftype** bepalen welk type afronding voor verlofopbouw moet worden gebruikt, plus de decimale nauwkeurigheid van de afronding tijdens het verlofopbouwproces. Wanneer de verlofopbouw wordt verwerkt, worden de afronding en de precisie toegepast op de verlofopbouwrecords. 

- **Meerdere verloftypen configureren voor één verlofplan** - met een nieuwe kolom in het verlofopbouwschema kunt u meerdere verloftypen voor een verlof- en verzuimplan met verschillende verlofopbouwschema's definiëren. Het vorige veld **Verloftype** is verwijderd. Bij de inschrijving van de werknemers worden de saldi voor de typen verlof nu weergegeven in een tabel in plaats van boven aan het scherm.

  > [!IMPORTANT]
  > U kunt deze functie niet uitschakelen nadat u deze hebt ingeschakeld.

- **De voltijdsequivalent (FTE) van een werknemer gebruiken voor verlofopbouw** : een nieuwe kolom in het verlofopbouwschema maakt het gebruik van de FTE voor de verlofopbouw mogelijk. Wanneer de verlofopbouw wordt verwerkt, gebruikt de toepassing de primaire positie van de werknemer en de ingestelde FTE om het van de evenredige bedrag van de verlofopbouw te bepalen.

  > [!NOTE]
  > Deze functie is alleen beschikbaar als u **Meerdere verloftypen per verlofplan configureren** inschakelt. 
