---
title: Overzicht van Vergoedingenbeheer
description: Overzicht van de functie Vergoedingenbeheer in Dynamics 365 Human Resources. Bied uw werknemers uitgebreide vergoedingsopties met een gebruiksvriendelijke online ervaring.
author: andreabichsel
manager: tfehr
ms.date: 09/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ba6623102431eb45bf5d0c96b6583615663d1081
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464321"
---
# <a name="benefits-management-overview"></a>Overzicht van Vergoedingenbeheer

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Om concurrerend te blijven, moet u een uitgebreide reeks vergoedingen bieden om goede werknemers aan te trekken en te behouden. Naast standaardvergoedingen, zoals medische en tandheelkundige dekking, kunt u ook uitgebreide services aanbieden, zoals hulp bij adoptie, recreatieprogramma's en kledingtoelagen. De functie Vergoedingenbeheer in Microsoft Dynamics 365 Human Resources biedt u een flexibele oplossing die een breed scala aan vergoedingsopties ondersteunt. Human Resources bevat ook een gebruiksvriendelijke werknemerservaring waarin uw aanbod wordt gepresenteerd.

- De verbeterde functionaliteit voor vergoedingsplannen biedt u de mogelijkheid om unieke vergoedingsplannen te maken en beheren en ondersteunt complexe vergoedingstarieftabellen en geneste niveaus. U kunt eenvoudig vergoedingsprogramma's, bundels en automatische inschrijvingsregels maken voor een gebruiksvriendelijker werknemerservaring.

- Via flex-kredietprogramma's kunt u zorgen voor een evenredige verdeling van kredieten voor ondersteuning bij pensioenering en andere levensgebeurtenissen.

- De uitgebreide regels om te controleren of iemand voor een bepaalde vergoeding in aanmerking komt, zorgen ervoor dat u de juiste vergoedingen voor de juiste werknemers kunt maken.

- U kunt werknemers een gebruiksvriendelijke optie bieden om zich online in te schrijven voor vergoedingen.

- De verwerking van gekwalificeerde levensgebeurtenissen ondersteunt toekomstige levensgebeurtenissen.

Als u toegang wilt tot de demogegevens, moet u de sandbox-omgeving opnieuw implementeren.

## <a name="enable-benefits-management"></a>Vergoedingenbeheer inschakelen

In dit onderwerp wordt beschreven hoe u functies inschakelt in Human Resources. U leest hier ook welke bestaande functies in Human Resources door Vergoedingenbeheer worden vervangen of worden uitgeschakeld wanneer u Vergoedingenbeheer inschakelt.

> [!IMPORTANT]
> Nadat u Vergoedingenbeheer in een **productie** omgeving hebt ingeschakeld, kunt u dit niet meer uitschakelen. U wordt aangeraden Vergoedingenbeheer in een **sandbox**-omgeving in te schakelen en te testen voordat u dit in een **productieomgeving** activeert. Er zijn belangrijke verschillen tussen de verouderde vergoedingsfunctionaliteit en de nieuwe functionaliteit voor Vergoedingenbeheer. Hiervoor zijn aanvullende instellingen nodig die moeten worden getest voordat ze in de productie worden gebracht.

- [Functies beheren](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a>Werknemersgegevens configureren

Voordat u werknemers voor vergoedingen kunt inschrijven, moet u de vereiste informatie opgeven. U moet een werknemer inschrijven voor **Plan met vaste compensatie** op de begindatum en u moet een **Betalingsfrequentie voor vergoedingen** selecteren in **Details dienstverband** op het formulier **Medewerker**.

Als u een werknemer hebt die een aanvullende vergoeding krijgt, zoals provisies, kunt u een **Jaarlijks salarisbedrag voor vergoedingen** uit de werknemerrecord toevoegen. Human Resources gebruikt **het jaarlijkse salarisbedrag voor vergoedingen** om de dekkingsbedragen vast te stellen in plaats van het vaste jaarlijkse compensatiebedrag. Het **Jaarlijks salarisbedrag voor vergoedingen** moet geldig zijn vanaf de begindatum van de werknemer of het begin van de vergoedingsperiode, afhankelijk van het laatste. Als er voor een werknemer zowel een vast compensatiebedrag als een salarisbeloning wordt geregistreerd, wordt het jaarlijkse salaris voor vergoedingen gebruikt bij het bepalen van de bedragen van de dekking.

Wanneer u een vergoedingsplan maakt dat tarieven op basis van geslacht of leeftijd gebruikt, moet u een geboortedatum en geslacht invoeren voor de werknemer om de kosten van de vergoeding te berekenen.

## <a name="configure-benefits-management"></a>Vergoedingenbeheer configureren

Voordat u vergoedingsplannen voor uw werknemers kunt maken, moet u opties voor de plannen configureren.

- [Parameters voor Vergoedingenbeheer instellen](hr-benefits-setup-parameters.md)
- [Geschiktheidsregels en -opties configureren](hr-benefits-setup-eligibility-rules.md)
- [Opties voor geschiktheid van persoonlijke contactpersonen configureren](hr-benefits-setup-contact-eligibility-options.md)
- [Opties voor dekking maken](hr-benefits-setup-coverage-options.md)
- [Betalingsfrequenties instellen](hr-benefits-setup-payment-frequencies.md)
- [Typen levensgebeurtenissen configureren](hr-benefits-setup-life-event-types.md)
- [Plantypen maken](hr-benefits-setup-plan-types.md)
- [Redencodes instellen](hr-benefits-setup-reason-codes.md)
- [Niveaucodes instellen](hr-benefits-setup-tier-codes.md)
- [Tarieven configureren](hr-benefits-setup-rates.md)
- [Inhoudingen configureren](hr-benefits-setup-deductions.md)
- [Wachtdagen configureren](hr-benefits-setup-waiting-days.md)
- [Wachtperioden configureren](hr-benefits-setup-waiting-periods.md)
- [Afrondingsregels instellen](hr-benefits-setup-rounding-rules.md)
- [Dienstverbandcategorieën maken](hr-benefits-setup-employment-categories.md)
- [Dienstverbandtypen instellen](hr-benefits-setup-employment-types.md)
- [Werknemerselfservice configureren](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a>Vergoedingsplannen maken

In de volgende artikelen wordt uitgelegd hoe u vergoedingsplannen, waaronder bundels en flex-kredietprogramma's, kunt maken.

- [Vergoedingsplannen instellen](hr-benefits-plans-setup.md)
- [Programma's voor flexibel krediet instellen](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a>Vergoedingsplannen verwerken

U moet enkele wijzigingen verwerken om deze actief te maken.

- [Geschiktheid voor inschrijving verwerken](hr-benefits-process-enrollment-eligibility.md)
- [Levensgebeurtenissen verwerken](hr-benefits-process-life-events.md)
- [Wijzigingen in levensgebeurtenissen verwerken](hr-benefits-process-life-event-changes.md)
- [Geschiktheid voor levensgebeurtenis verwerken](hr-benefits-process-life-event-eligibility.md)
- [Tariefwijzigingen verwerken](hr-benefits-process-rate-changes.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]