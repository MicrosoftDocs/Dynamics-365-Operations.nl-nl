---
title: Human Resources-parameters configureren
description: In dit onderwerp wordt uitgelegd hoe u bedrijfsspecifieke parameters instelt in Dynamics 365 Human Resources.
author: twheeloc
ms.date: 11/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1fc8ba3f69f216d66850485b6ba33cd324a57156
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8689405"
---
# <a name="configure-human-resources-parameters"></a>Human Resources-parameters configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

De instellingen van bepaalde parameters van Human Resources worden in alle bedrijven gedeeld, terwijl de instellingen van andere parameters bedrijfsspecifiek zijn. In dit onderwerp wordt uitgelegd hoe u bedrijfsspecifieke Human Resources-parameters instelt.

Twee pagina's worden gebruikt om de parameters voor Human resources in te stellen. Voor parameters die door bedrijven worden gedeeld, gebruikt u de pagina **Gedeelde Human resources-parameters**. Voor parameters die bedrijfsspecifiek zijn (met andere woorden, de instellingen gelden voor één bedrijf), gebruikt u de pagina **Parameters personeel**.

![Ga naar Human Resources-parameters.](./media/hr-employee-self-service-human-resources-parameters.png)

Op de **Human resources-parameters** pagina, zijn de instellingen verdeeld over zes tabbladen:

- **Algemeen**
- **Werving**: (dit tabblad is niet opgenomen in Dynamics 365 Human Resources)
- **Compensatie**
- **Nummerreeksen**
- **FMLA**
- **Selfservice werknemer**
- **Selfservice manager**
- **Vergoedingenbeheer**
- **Verlof en verzuim**
- **Betalingsmethoden**

Elk tabblad bevat informatie over één bedrijf.

## <a name="general"></a>Algemeen

De instellingen op het tabblad **Algemeen** bepalen het uiterlijk van informatie over verzuim, letsel en ziekte, en nieuwe werknemers. De instellingen op dit tabblad definieert tevens sommige standaardwaarden die worden weergegeven terwijl u werkt. Op dit tabblad kunt u het volgende doen:

- Een kleur selecteren om op openstaande verzuimtransacties toe te passen.
- Het te gebruiken stijlblad voor rapporten opgeven.
- Integratie tussen trainingscursussen en verzuimregistratie inschakelen.
- De verzuimcode selecteren die wordt gebruikt om deze integratie te beheren.
- Aangeven hoe lang een case met letsel- en ziekte-incidenten moet worden bewaard.
- Het standaardidentificatienummer opgeven dat wordt weergegeven wanneer een nieuwe werknemer wordt aangenomen.
- De datum opgeven die wordt gebruikt voor het berekenen van servicejaren. 

![Tabblad Algemeen.](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a>Werving

De instellingen op het tabblad **Werving** definiëren de documenttypen die worden gebruikt voor correspondentie die automatisch naar sollicitanten wordt verzonden. U kunt ook het wervingsproject aangeven dat voor open sollicitaties wordt gebruikt.

De periode die is gedefinieerd als **ouderdomsperiode voor het wervingsproject**, bepaalt welke wervingsprojecten worden opgenomen op de tegel **Verouderende projecten** in het werkgebied **Wervingsbeheer**. De periode die wordt ingesteld voor de sollicitatiedeadlinewaarschuwing wordt gebruikt om wervingsprojecten weer te geven die hun sollicitatiedeadline naderen op de tegel **Einde van sollicitatietermijn nadert** in het werkgebied **Werving**.

Zie [Werving kandidaten voor functie](hr-personnel-recruit.md) voor meer informatie over werving.

## <a name="compensation"></a>Compensatie

In Dynamics 365 Finance definiëren de instellingen op het tabblad **Compensatie** of gebruikers moeten bevestigen dat ze informatie willen opslaan voor een vaste- of variabele-compensatieplan. Als u het selectievakje **Opslaan van validatie activeren** inschakelt, worden gebruikers wanneer zij een compensatie-gerelateerde pagina afsluiten, gevraagd of zij de record willen opslaan. Op sommige pagina's in Compensatiebeheer kunnen gebruikers geen gegevens verwijderen. Door gebruikers te vragen of ze gegevens daadwerkelijk willen opslaan, worden er mogelijk minder gegevens opgeslagen die naderhand niet meer kunnen worden verwijderd. Als u **Opslaan van validatie activeren** uitschakelt, worden records direct opgeslagen, misschien voordat de gebruiker klaar is. Als u Prestatiebeheer gebruikt, kunt u met het tabblad **Compensatie** ook een beoordelingsmodel selecteren om te gebruiken in plaats van het model dat wordt toegewezen aan compensatieplannen wanneer prestaties worden beoordeeld.

In Human Resources kunt u op het tabblad **Compensatie** ervoor kiezen de toegang tot compensatieplannen te beperken en een standaardvaluta in te stellen.

Zie [Overzicht van compensatieplannen](hr-compensation-overview.md) voor meer informatie over compensatieplannen.

![Tabblad Compensatie.](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a>Nummerreeksen

De instellingen op het tabblad **Nummerreeks** bepalen de reeksen die worden gebruikt om automatisch id's toe te wijzen aan items in Human Resources, zoals:

- Aanvragen
- Verzuimregistraties
- Resultaten van compensatieproces
- Casenummers
- Cursussen
- Cursusagenda's

Om nummerreeksverwijzingen en codes te onderhouden, gebruikt u de lijstpagina **Nummerreeksen** (selecteer **Organisatiebeheer > Nummerreeksen > Nummerreeksen**).

Zie [Overzicht van nummerreeksen](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json) voor meer informatie.

> [!NOTE]
> Het aantal uren dat is gewerkt, kan niet groter zijn dan 1250, en de lengte van het dienstverband kan niet langer dan 12 maanden zijn. Deze maximumwaarden zijn in overeenstemming met de federale wetgeving in de verenigde Staten.

![Tabblad Nummerreeksen.](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a>FMLA

Op het tabblad FMLA stelt u geschiktheidsvereisten voor FMLA en uren voor rechten van FMLA in. Zie [Verlof- en verzuimparameters configureren](hr-leave-and-absence-parameters.md) voor meer informatie.

![Tabblad FMLA.](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a>Werknemerselfservice

De instellingen op het tabblad **Selfservice werknemer** beïnvloeden hoe deze **selfservice voor werknemers** wordt weergegeven. Op dit tabblad kunt de volgende taken uitvoeren:

- Een naam invoeren voor het werkgebied **Selfservice werknemer**
- Selecteren welke informatie een manager voor werknemers kan invoeren
- Nuttige koppelingen toevoegen voor werknemers
- Voorkomen dat werknemers zakelijke contactgegevens toevoegen of bewerken. Zie [Persoonlijke gegevens bewerken beperken](hr-employee-self-service-restrict-editing.md) voor meer informatie.

Zie [Overzicht Selfservice voor werknemers en managers](hr-employee-manager-self-service-overview.md) voor meer informatie over het instellen van **Selfservice voor werknemers**.

![Tabblad Selfservice werknemer.](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a>Selfservice manager

De instellingen op het tabblad **Selfservice managers** beïnvloeden wat managers zien in **Selfservice managers**. Op dit tabblad kunt u de volgende opties configureren:

- Het bereik voor verlopende records
- Informatie die managers kunnen zien in verlopende records
- Of managers openstaande functies voor indirecte ondergeschikten kunnen bekijken
- Weergaven van vertrekkende werknemers
- Nuttige koppelingen voor managers

Zie [Overzicht Selfservice voor werknemers en managers](hr-employee-manager-self-service-overview.md) voor meer informatie over het instellen van **Selfservice voor managers**.

![Tabblad Selfservice managers.](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a>Vergoedingenbeheer

Op het tabblad **Vergoedingenbeheer** kunt u e-mailopties voor Vergoedingenbeheer configureren. Zie [Overzicht van Vergoedingenbeheer](hr-benefits-management-overview.md) voor meer informatie over het instellen en het gebruik van Vergoedingenbeheer.

![Tabblad Vergoedingenbeheer.](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a>Verlof en verzuim

Zie [Overzicht van Verlof en verzuim](hr-leave-and-absence-overview.md) voor meer informatie over het instellen en gebruiken van Verlof en verzuim.

## <a name="payment-methods"></a>Betalingsmethoden

Op het tabblad **Betalingswijzen** kunt u de betalingswijzen selecteren die door uw organisatie worden ondersteund. Zie [Overzicht van compensatieplannen](hr-compensation-overview.md) voor meer informatie over de configuratie van compensatieplannen.

![Tabblad Betalingswijzen.](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
