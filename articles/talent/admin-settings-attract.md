---
title: Bedrijfsgegevens configureren in Attract
description: In dit onderwerp wordt uitgelegd hoe u bedrijfsgegevens en -branding voor Microsoft Dynamics 365 Talent - Attract configureert.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: db3ec965f3a52810d5f310697b9ed830c3abe681
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460862"
---
# <a name="configure-company-information-in-attract"></a>Bedrijfsgegevens configureren in Attract

[!include [banner](includes/banner.md)]

Het beheercentrum in Microsoft Dynamics 365 Talent: Attract bevat configuratie-instellingen, integratieopties en instellingsopties voor de Attract-toepassing.

## <a name="company-information"></a>Bedrijfsgegevens

Voer een weergavenaam in voor het bedrijf en een bedrijfslogo. De weergavenaam en het logo kunnen vervolgens worden gebruikt in functieplaatsingen en tijdens de onboarding.

## <a name="linkedin-integration"></a>LinkedIn-integratie

Stel integratie met LinkedIn Recruiter System Connect (RSC) in. Nadat u een verbinding met LinkedIn hebt gemaakt met behulp van uw LinkedIn-referenties, kunt u het LinkedIn-profiel, sollicitaties, sollicitatiegesprekfeedback en notities van aanstellende teams van een kandidaat synchroniseren. Een volledige LinkedIn-werverslicentie is vereist. Zie voor meer informatie over LinkedIn Recruiter [Recruiter System Connect (RSC) – veelgestelde vragen](https://www.linkedin.com/help/recruiter/answer/90483).

## <a name="user-permissions"></a>Gebruikersmachtigingen

Rollen aan gebruikers toewijzen in uw organisatie De volgende rollen zijn beschikbaar: **Beheer**, **Werver**, **Aanstellend manager** en **Alleen-lezen**. Zie voor meer informatie over gebruikersmachtigingen [Beveiliging en rollenbeheer in Attract](./security-attract.md).

## <a name="feature-management"></a>Beheer van functies

Wanneer nieuwe functies worden toegevoegd, kunnen deze worden vrijgegeven in een openbare preview. Functies van openbare previews voldoen niet aan alle servicevereisten. Door ze te ontvangen gaat u ermee akkoord uw gegevens te delen met externe systemen. Het kan gebeuren dat uw organisatie niet alle nieuwe functies vereist die worden vrijgegeven. U kunt openbare previewfuncties in- en uitschakelen, afhankelijk van de behoeften van uw organisatie.

## <a name="template-management"></a>Sjabloonbeheer

Een processjabloon bevat alle activiteiten die moeten worden opgenomen als onderdeel van het aanstellingsproces voor een functie. Uw organisatie kan alle teamleden of alleen beheerders toestaan aanstellingsprocessjablonen te maken. Als u teamleden wilt toestaan hun eigen aanstellingsprocessjablonen te maken, schakelt u de sjabloonbeheerfunctionaliteit in. Zie voor meer informatie over processjablonen [Een processjabloon maken in Attract](./process-templates-attract.md).

## <a name="email-template-settings"></a>Instellingen van e-mailsjabloon

Organisaties kunnen e-mailsjablonen voor verschillende scenario's maken. U kunt de koptekstafbeelding selecteren om op te nemen in de e-mailsjablonen. De geselecteerde koptekst wordt vervolgens weergegeven in alle e-mailsjablonen. In de voettekst van de sjabloon kunt u een koppeling toevoegen naar de privacyverklaring van uw organisatie en gebruiksvoorwaarden voor communicatie. Zie [E-mailsjablonen](./email-templates.md) voor meer informatie.

## <a name="offer-process"></a>Aanbiedingsproces

U kunt het goedkeuringsproces voor functieaanbiedingen configureren. U kunt bijvoorbeeld opgeven of een aanbieding moet worden goedgekeurd voordat deze naar een kandidaat wordt verzonden. U kunt ook vereisen dat fiatteurs een opmerking achterlaten met hun beslissing over een aanbieding.

Twee goedkeuringswerkstromen zijn beschikbaar: **Parallel** en **Sequentieel**.

- **Parallel** : goedkeuringen worden op hetzelfde moment naar alle fiatteurs verzonden.
- **Sequentieel** : goedkeuringen worden in een bepaalde volgorde naar de fiatteurs verzonden.

U kunt ook opties configureren die zijn gerelateerd aan de kandidaatervaring. Met één optie kunt u bijvoorbeeld opgeven of kandidaten een aanbieding kunnen afwijzen zonder verdere discussie. Als u de optie **Kandidaten kunnen een aanbieding afwijzen zonder aanvullende discussie** instelt op **Nee**, is de knop **Aanbieding afwijzen** beschikbaar voor kandidaten. Als u deze optie instelt op **Ja**, kunnen kandidaten kunnen het voorstel afwijzen door een reden te selecteren en vervolgens **Aanbieding afwijzen** te selecteren.

U kunt ook een verloopdatum instellen en afdwingen voor aanbiedingen. Als u de optie **Een vervaldatum vereisen voor alle aanbiedingen** instelt op **Ja**, vervallen aanbiedingen na het aantal uren of dagen dat u opgeeft.

Zie voor meer informatie over aanbiedingsbeheer [Aanbiedingsbeheer instellen](./offer-setup.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]