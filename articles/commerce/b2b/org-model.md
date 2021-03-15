---
title: Hiërarchieën voor organisatiemodellering voor B2B-organisaties maken
description: In dit onderwerp wordt beschreven hoe u hiërarchieën voor organisatiemodellen maakt voor B2B-organisaties (business-to-business).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 450efd595a1cc1b72b2e62afbdd4518bcca59cb0
ms.sourcegitcommit: f9df202aefef761be52c0360b0e22da88773914c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/21/2021
ms.locfileid: "5035890"
---
# <a name="create-org-modeling-hierarchies-for-b2b-organizations"></a>Hiërarchieën voor organisatiemodellering voor B2B-organisaties maken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u in Microsoft Dynamics 365 Commerce hiërarchieën voor organisatiemodellen maakt voor B2B-organisaties (business-to-business).

In Commerce Headquarters worden zakenpartnerorganisaties vertegenwoordigd door klant- en klanthiërarchie-entiteiten. De organisatie van zakenpartners en haar gebruikers worden weergegeven als klanten en klanthiërarchieën worden gebruikt om die klanten aan elkaar te koppelen.

Wanneer een aanvraag van een zakenpartner voor toegang tot een B2B-e-commercesite wordt goedgekeurd, worden de volgende acties uitgevoerd:

- Er worden twee nieuwe klantrecords in het systeem gemaakt: een klantrecord **Organisatietype** voor de organisatie van de zakenpartner en een klantrecord **Type persoon** voor de aanvrager (dat wil zeggen, de zakenpartnergebruiker die de aanvraag heeft ingediend).
- Er wordt een nieuw klanthiërarchierecord gemaakt onder **Klant \> Klanthiërarchie**. Deze record heeft de volgende kopteksteigenschappen:

    - **Klanthiërarchie-id**: een unieke id voor de klanthiërarchie. Deze id gebruikt de nummerreeks die is gedefinieerd in gedeelde parameters voor Commerce in Commerce Headquarters.
    - **Naam**: de naam van de organisatie van de zakenpartner, zoals is opgegeven in de aanvraag voor onboarding.
    - **Doel**: deze eigenschap is ingesteld op de vooraf gedefinieerde waarde **B2B-organisatie**.
    - **Organisatie**: de klant-id van de zakenpartner.

Hieronder vindt u de details van de klanthiërarchierecord:

- De klantrecord van de aanvrager is gekoppeld aan de klanthiërarchie.
- De rol van beheerder is gekoppeld aan de aanvrager.

Wanneer de beheerder meer gebruikers toevoegt aan de organisatie van de zakenpartner op een B2B-site, wordt er een nieuwe klantrecord voor elke gebruiker gemaakt in Commerce Headquarters. Deze klantrecord wordt ook toegevoegd aan de relevante klanthiërarchierecord voor de zakenpartner en heeft de rol van een 'gebruiker'.

> [!NOTE]
> In de meeste gevallen moeten de bijbehorende eigenschapswaarden van alle klantrecords in een hiërarchie overeenkomen. Omdat alle gebruikers van zakenpartners bijvoorbeeld gelijksoortige prijzen voor producten moeten hebben, moeten hun prijsgroep en gekoppelde configuraties overeenkomen. Deze consistentie wordt echter niet door het systeem afgedwongen. De relevante gebruikers van Commerce Headquarters moeten er daarom voor zorgen dat de eigenschapswaarden en configuraties overeenkomen voor alle klanten in een bepaalde hiërarchie.

Gebruikers van Commerce Headquarters kunnen de eigenschapswaarden voor alle klantrecords in de hiërarchie naast elkaar bekijken. Selecteer de relevante eigenschappen van de klantrecords door de tabbladnamen te selecteren in het vervolgkeuzemenu. Gebruikers kunnen de eigenschapswaarden rechtstreeks vanuit deze weergave weergeven en bewerken. Als u ook alle waarden van de beheerderklantrecord wilt toepassen op alle gebruikersklantrecords, selecteert u **Overschrijven** in de klanthiërarchiedetails.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2B-e-commercesite instellen](set-up-b2b-site.md)

[Gebruikers van zakenpartners op B2B-sites voor e-commerce beheren](manage-b2b-users.md)

[De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites](payment-method.md)

[De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites](quantity-limits.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]