---
title: B2B-zakenpartners beheren met behulp van klanthiërarchieën
description: In dit onderwerp wordt beschreven hoe u klanthiërarchieën kunt gebruiken om zakenpartners voor B2B-e-commercewebsites (business-to-business) met Microsoft Dynamics 365 Commerce te beheren.
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d6e594cbb824a8b823912118e99b819585adc45e
ms.sourcegitcommit: 8bcb9c13eccb14e61c39ca6578d135b64090fad2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2022
ms.locfileid: "8313828"
---
# <a name="manage-b2b-business-partners-using-customer-hierarchies"></a>B2B-zakenpartners beheren met behulp van klanthiërarchieën

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u klanthiërarchieën kunt gebruiken om zakenpartners voor B2B-e-commercewebsites (business-to-business) met Microsoft Dynamics 365 Commerce te beheren.

In Commerce Headquarters wordt een entiteit *klanthiërarchie* gebruikt om de zakenpartnerorganisaties te vertegenwoordigen die uw B2B-e-commercesite gebruiken. Voordat u klanthiërarchieën kunt gebruiken om zakenpartners te beheren, moet u de mogelijkheden voor B2B-e-commerce in Commerce Headquarters inschakelen en vervolgens een nummerreeks definiëren voor de klanthiërarchie.

## <a name="enable-the-b2b-e-commerce-feature-in-commerce-headquarters"></a>De functie voor B2B-e-commerce inschakelen in Commerce Headquarters

Als u gebruik wilt maken van de B2B-e-commercemogelijkheden, moet u eerst de functie **Het gebruik van B2B e-commercemogelijkheden inschakelen** in Commerce Headquarters inschakelen.

1. Ga naar **Werkruimten \> Functiebeheer**.
1. Op het tabblad **Alle** kunt u in het filtervak zoeken naar **Module: Retail en Commerce**.
1. Zoek en selecteer de functie met de naam **Het gebruik van B2B e-commercemogelijkheden inschakelen** en selecteer **Nu inschakelen** in de rechterbenedenhoek.

## <a name="define-a-number-sequence-for-the-customer-hierarchy"></a>Een nummerreeks definiëren voor de klanthiërarchie

Nummerreeksen worden gebruikt om leesbare, unieke id´s te maken voor hoofdgegevensregistraties en transactieregistraties die deze nodig hebben. U moet een nummerreeks definiëren die wordt gebruikt om de id voor de klanthiërarchie te genereren. Zie [Overzicht van nummerreeksen](/dynamics365/fin-ops-core/fin-ops/organization-administration/number-sequence-overview) voor meer informatie over nummerreeksen.

Volg deze stappen om een nummerreeks voor de klanthiërarchie in Commerce Headquarters te definiëren.

1. Ga naar **Retail en commerce \> Instelling van hoofdkantoor \> Nummerreeksen \> Nummerreeksen**.
1. Maak een nieuwe nummerreeks of selecteer een bestaande nummerreeks om deze opnieuw te gebruiken.
1. Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde Commerce-parameters**.
1. Voeg op het tabblad **Nummerreeksen** aan de verwijzing **Klanthiërarchie-id** de nummerreeks toe die u eerder hebt gemaakt of geselecteerd.

![Nummerreeks die is toegevoegd aan de verwijzing Klanthiërarchie-id.](../media/NumberSequenceCustHierarchy.png)

## <a name="how-the-approval-process-works"></a>Hoe het goedkeuringsproces werkt

Wanneer een zakelijke partner verzoekt om deel te nemen aan een B2B-e-commercesite, slaat het systeem de aanvraag op als *prospect*. Een Commerce Headquarters-persona, zoals Bedrijfsbeheerder detailhandel, kan partneraanvragen goedkeuren of afwijzen. Zie [Gebruikers van zakenpartners op B2B-e-commercewebsite beheren](manage-b2b-users.md) voor meer informatie over het beheren van aanvragen van zakelijke partners en goedkeuringen van prospects.

Wanneer een prospect wordt goedgekeurd, maakt het systeem twee nieuwe klantrecords:

- Eén klantrecord van het type **Organisatie** vertegenwoordigt de organisatie die verzoekt om een zakenpartner te worden.
- Eén klantrecord van het type **Persoon** vertegenwoordigt de persoon die de aanvraag heeft ingediend.

Daarnaast wordt een nieuwe klanthiërarchierecord gemaakt in **Retail en Commerce \> Klanten \> Klanthiërarchieën**. Deze klanthiërarchierecord heeft de volgende kopteksteigenschappen:

- **Klanthiërarchie-id**: de unieke id van de klanthiërarchie. Deze id gebruikt de nummerreeks die u hebt gedefinieerd in gedeelde parameters voor Commerce.
- **Naam**: de naam van de organisatie van de zakenpartner, zoals is opgegeven in de aanvraag voor onboarding. Dit veld is bewerkbaar.
- **Doel**: deze eigenschap is ingesteld op de vooraf gedefinieerde waarde **B2B-organisatie**.
- **Organisatie**: de klant-id van de zakenpartnerorganisatie.

De persoon die de onboardingaanvraag heeft ingediend, wordt toegevoegd op het sneltabblad **Hiërarchie** en krijgt de rol **Beheerder**. Wanneer de beheerder meer gebruikers toevoegt aan de organisatie van de zakenpartner op een B2B-site, wordt er een nieuwe klantrecord voor elke gebruiker gemaakt. De klantrecord wordt ook toegevoegd aan de relevante klanthiërarchierecord voor de zakenpartner en krijgt de rol **Gebruiker**.

### <a name="examples"></a>Voorbeelden

Een persoon met de naam Sam J. dient een onboardingaanvraag in namens de Microsoft-organisatie. Nadat de aanvraag is goedgekeurd, worden er twee nieuwe klantaccounts gemaakt: een van het type **Persoon** voor Sam J. en een van het type **Organisatie** voor Microsoft.

Zoals het voorbeeld in de volgende afbeelding laat zien, wordt er ook een nieuwe klanthiërarchierecord gemaakt. Deze record heeft dezelfde naam als de organisatie (**Microsoft**) en de rol **Beheerder** wordt toegewezen aan Sam J. als beheerder voegt Sam J. alle andere Microsoft-gebruikers van de B2B-site aan deze hiërarchie toe en wijst de rol van **Gebruiker** hieraan toe. In dit voorbeeld is Sush R. toegevoegd als gebruiker.

![Voorbeeld van een klanthiërarchierecord.](../media/CustomerHierarchy2.png)

Open de klantrecord om te bepalen of een klant aan een klanthiërarchie is gekoppeld. Zoals het onderstaande voorbeeld laat zien, wordt in het veld **Klanthiërarchie-id** in de sectie **B2B** op het sneltabblad **Retail** aangegeven of de klant deel uitmaakt van een klanthiërarchie. De optie **B2B-beheerder** geeft aan of de klant een beheerder van die hiërarchie is.

![Voorbeeld van de sectie B2B op het sneltabblad Retail van een klantrecord, waarin de klant is gekoppeld aan een hiërarchie en als beheerder is opgegeven.](../media/CustomerHierarchyMapping2.png)

In de meeste gevallen moeten de eigenschapswaarden van alle klantrecords in een hiërarchie overeenkomen. Omdat alle gebruikers van zakenpartners bijvoorbeeld gelijksoortige prijzen voor producten moeten hebben, moeten hun prijsgroep en gekoppelde configuraties overeenkomen. Deze consistentie wordt echter niet door het systeem afgedwongen. De relevante gebruikers van Commerce Headquarters moeten er daarom voor zorgen dat de eigenschapswaarden en configuraties overeenkomen voor alle klanten in een bepaalde hiërarchie.

Gebruikers van Commerce Headquarters kunnen de eigenschapswaarden voor alle klantrecords in een hiërarchie naast elkaar bekijken. Zoals het voorbeeld in de volgende afbeelding laat zien, kunt u de optie **Algemeen** gebruiken in de vervolgkeuzelijst op het sneltabblad **Hiërarchie** en vervolgens een sectie van de klantrecord selecteren om de gerelateerde eigenschappen weer te geven. Gebruikers kunnen de eigenschapswaarden rechtstreeks in deze weergave bewerken. Als u alle waarden van een klantrecord van een beheerder wilt kopiëren naar alle gebruikers, selecteert u **Overschrijven** op het sneltabblad **Hiërarchie**.

![Voorbeeld van een klanthiërarchierecord met de knop Overschrijven en de optie in de vervolgkeuzelijst.](../media/HierarchyDetails2.png)

[!include [footer-include](../../includes/footer-banner.md)]
