---
title: Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce
description: Dit onderwerp biedt antwoorden op veelgestelde vragen over de evaluatieomgeving van Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e8a3e760353b351d42aff82c0d372d2aca350cd2
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343553"
---
# <a name="dynamics-365-commerce-evaluation-environment-faq"></a>Veelgestelde vragen over evaluatieomgeving voor Dynamics 365 Commerce

[!include [banner](includes/banner.md)]

Dit onderwerp biedt antwoorden op veelgestelde vragen over de evaluatieomgeving van Microsoft Dynamics 365 Commerce.

## <a name="can-we-use-the-commerce-evaluation-environment-as-an-e-commerce-storefront-for-customers-that-currently-implement-retail"></a>Kunnen we de evaluatieomgeving van Commerce gebruiken als e-Commerce-winkel voor klanten die momenteel Retail implementeren?

Nr. De Commerce-evaluatieomgeving is alleen bedoeld voor evaluatie. Neem contact op met Microsoft als u een omgeving nodig hebt voor een klant die Retail implementeert.

## <a name="can-the-commerce-evaluation-environment-be-used-to-provision-the-e-commerce-features-on-top-of-an-existing-applicationenvironment-that-implements-retail"></a>Kan de evaluatieomgeving van Commerce worden gebruikt om de e-Commerce-functies in te richten boven op een bestaande toepassing/omgeving die Retail implementeert?

Nee (meestal). De onderdelen van Commerce-evaluatie zijn alleen beschikbaar voor omgevingen die overeenkomen met de configuraties die zijn opgegeven in de vereisten en inrichtingshandleiding. Bovendien zijn de vereiste basisdemogegevens niet beschikbaar in omgevingen die zijn geïmplementeerd met een oorspronkelijke release die ouder is dan 10.0.8. 

## <a name="what-costs-are-involved-in-deploying-the-commerce-evaluation-environment-on-microsoft-azure-via-microsoft-dynamics-lifecycle-services-lcs"></a>Wat zijn de kosten van het implementeren van de evaluatieomgeving van Commerce op Microsoft Azure via Microsoft Dynamics Lifecycle Services (LCS)?

Een traditionele demo-omgeving voor Dynamics 365 Finance/Dynamics 365 Supply Chain Management/Dynamics 365 Commerce Headquarters (virtuele machine \[VM\]) wordt gehost in uw Azure-abonnement. U kunt de [Azure-prijscalculator](https://azure.microsoft.com/pricing/calculator/) gebruiken om deze kosten te schatten.

Andere onderdelen, zoals Commerce Scale Unit, Commerce Site Builder en uw e-commerce-site zijn beschikbaar als software als een dienst (SaaS) en worden door Microsoft gehost.

## <a name="which-azure-geographies-are-currently-supported-for-the-commerce-evaluation-environment"></a>Welke Azure-regio's worden momenteel ondersteund voor de evaluatieomgeving van Commerce?

De evaluatieomgeving van Commerce kan alleen worden geïmplementeerd in de regio Noord-Amerika.

## <a name="is-there-a-downloadable-virtual-hard-disk-vhd-that-has-the-complete-onebox-virtual-machine-vm-option"></a>Is er een downloadbare virtuele harde schijf (VHD) met de volledige OneBox VM-optie (virtuele machine)?

Dynamics 365 Commerce en Commerce Scale Unit zijn volledig SaaS en moeten in de cloud worden gehost.

## <a name="how-long-can-the-commerce-evaluation-environment-be-used"></a>Hoe lang kan de evaluatieomgeving van Commerce worden gebruikt?

De Commerce-evaluatieomgeving heeft een tijdslimiet van 30 dagen na de datum waarop SaaS-componenten, zoals Commerce Scale Unit, Commerce Site Builder en uw e-commerce-site zijn ingericht.

## <a name="can-i-extend-the-time-limit-for-my-commerce-evaluation-environment"></a>Kan ik de tijdslimiet voor mijn evaluatieomgeving van Commerce verlengen?

Verlenging van de tijds limiet wordt bij uitzondering verleend en wordt per geval beschouwd. Neem contact op met uw Microsoft-partner voor hulp.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van de evaluatieomgeving voor Dynamics 365 Commerce](cpe-overview.md)

[Een evaluatieomgeving voor Dynamics 365 Commerce inrichten](provisioning-guide.md)

[Een Dynamics 365 Commerce-evaluatieomgeving configureren](cpe-post-provisioning.md)

[BOPIS configureren in een Dynamics 365 Commerce-evaluatieomgeving](cpe-bopis.md)

[Optionele functies voor een Dynamics 365 Commerce-evaluatieomgeving configureren](cpe-optional-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
