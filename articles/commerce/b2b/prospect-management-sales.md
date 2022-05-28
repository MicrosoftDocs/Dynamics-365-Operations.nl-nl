---
title: Gebruikers van zakenpartners op B2B-e-commercewebsite beheren met Dynamics 365 Sales
description: In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Sales kunt gebruiken om goedkeuringen van zakenpartners voor B2B-e-commercewebsites (business-to-business) met Dynamics 365 Commerce te beheren.
author: shajain
ms.date: 2/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: shajain
ms.search.validFrom: 2022-01-31
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 540e8f26d7f2a08060a3839f9e4f97bf8ddcafac
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8692558"
---
# <a name="manage-business-partner-users-on-b2b-e-commerce-websites-using-dynamics-365-sales"></a>Gebruikers van zakenpartners op B2B-e-commercewebsite beheren met Dynamics 365 Sales

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u Microsoft Dynamics 365 Sales kunt gebruiken om goedkeuringen van zakenpartners voor B2B-e-commercewebsites (business-to-business) met Dynamics 365 Commerce te beheren. Organisaties die al hebben geïnvesteerd in de Dynamics 365 Sales-oplossing kunnen de concepten voor leads en verkoopkansen gebruiken voor het goedkeuringsproces voor zakenpartners in B2B.

Zie voor achtergrondinformatie over het goedkeuringsproces voor B2B-bedrijfspartners [Zakenpartners op B2B-e-commercewebsites beheren](manage-b2b-users.md).

Potentiële zakenpartners kunnen het onboardingproces voor een B2B-e-commercewebsite starten door een onboardingaanvraag in te dienen via een koppeling op de B2B-website. Nadat de aanvraag is ingediend en de relevante taken (zoals **P-0001** en **Orders en kanaalaanvragen synchroniseren**) worden uitgevoerd in Commerce Headquarters, wordt de onboardingaanvraag opgeslagen op de pagina **Alle prospects** in Commerce Headquarters. Het goedkeuringsproces voor prospects van zakenpartners kan vervolgens worden voltooid in Sales.

Nadat de integratie tussen Sales en Commerce is ingeschakeld, leidt het maken van een prospect van een zakenpartner in Commerce tot een *lead* in Sales.

In de volgende afbeelding ziet u een voorbeeld van een pagina voor het maken van leads voor een prospect van een zakenpartner in Sales.

![Pagina voor het maken van leads in Dynamics 365 Sales.](../media/LeadInSales.png)

In de afbeelding wordt in de sectie **Contactpersoon** de persoon weergegeven die de onboardingaanvraag heeft ingediend. In de sectie **Bedrijf** wordt de organisatie getoond. Een opmerking in het gedeelte **Tijdlijn** geeft aan dat de lead is gegenereerd door de infrastructuur voor twee keer wegschrijven. Omdat deze door de infrastructuur voor twee keer wegschrijven is gemaakt, wordt deze lead niet weergegeven in de vervolgkeuzelijst **Mijn openstaande leads**. In plaats daarvan wordt deze weergegeven onder een nieuwe weergave die **Alle commerciële B2B-leads** heet.

Wanneer een gebruiker de lead kwalificeert, worden op basis van het standaardkwalificatieproces Sales een record *verkoopkans*, een record *contactpersoon* en een record *rekening* gemaakt. De infrastructuur voor twee keer wegschrijven wordt gebruikt om de records contactpersoon en rekening naar Commerce te schrijven. De contactpersoon wordt gemaakt als klant van het type *persoon* en het bedrijf wordt gemaakt als klant van het type *organisatie*. Als een gebruiker **Sluiten als binnengehaald** selecteert voor de verkoopkans, wordt de prospect goedgekeurd in Commerce. Door de goedkeuring van een prospect wordt een klanthiërarchie gemaakt.

Alle resterende bedrijfsprocessen vinden plaats in Commerce. Deze processen omvatten het verzenden van e-mailberichten naar de zakenpartner, het definiëren van kredietlimietbeheer voor de gebruikers en het toevoegen van meer gebruikers aan de B2B-site. Als een gebruiker de lead echter diskwalificeert of de verkoopkans markeert als verloren in plaats van de lead te kwalificeren, wordt de prospect in Commerce als afgewezen gemarkeerd en wordt naar de aanvrager een e-mail voor afwijzing van de onboarding verzonden.

## <a name="enable-integration-between-sales-and-commerce"></a>Integratie tussen Sales en Commerce inschakelen

De integratie tussen Verkoop en Commerce is gebaseerd op de infrastructuur voor twee keer wegschrijven. Daarom moet Twee keer wegschrijven worden ingeschakeld en werken, zodat klanten die in het ene systeem worden gemaakt naar het andere systeem worden geschreven. Zie [Overzicht van Twee keer wegschrijven](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) voor meer informatie over de infrastructuur voor twee keer wegschrijven.

Nadat de instelling van Twee keer wegschrijven is voltooid, kan de implementatiepartner naar [Microsoft AppSource](https://appsource.microsoft.com/) gaan en de oplossing met de naam [Dual-write Commerce solutions](https://partner.microsoft.com/dashboard/commercial-marketplace/offers/7ca1d8c9-dc79-4cb7-a82e-8dc96a25acca/overview) zoeken. Installeer het pakket met behulp van de standaardinstallatiewizard en test het vervolgens door een prospect op een B2B-site te maken. Nadat de prospect is gemaakt, controleert u of de aanvraag wordt weergegeven in **Alle prospects** in Commerce en controleert u of de prospect wordt weergegeven als lead in Sales.

## <a name="additional-resources"></a>Aanvullende bronnen

[Gebruikers van zakenpartners op B2B-e-commercewebsite beheren](manage-b2b-users.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
