---
title: Geavanceerde contracten maken voor facturering op basis van voortgang
description: In dit onderwerp wordt uitgelegd hoe u projectcontracten maakt, zodat u facturen voor klanten kunt genereren op basis van een percentage voltooid werk.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 90cae104d0abad909606ef6a0e0c45ed95e74de2
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282819"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Geavanceerde contracten maken voor facturering op basis van voortgang
[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u projectcontracten maakt, zodat u facturen voor klanten kunt maken op basis van een percentage voltooid werk. Factuurbedragen voor de budgetcategorieën van werkzaamheden die u voor een project instelt, worden automatisch berekend. Wanneer u factureert, wordt ingesteld bij de contractonderhandeling van het project met de klant.

Gebruik de procedures in dit onderwerp voor het instellen van een contract, een gekoppeld project en de factureringsregels voor het berekenen van de factuurbedragen voor de budgetcategorieën van werkzaamheden die u voor het project hebt ingesteld.

Nadat u het contract en het project hebt gemaakt, kunt u de details van het project instellen. U kunt bijvoorbeeld de activiteiten definiëren en werknemers toewijzen aan het project.

## <a name="example"></a>Voorbeeld

Uw organisatie is een bedrijf dat zich bezig houdt met het ontwikkelen van software. U komt met een klant overeen dat u een salarisadministratiepakket zult ontwikkelen voor een totaal tarief van 20.000 Amerikaanse dollar (USD). Uw organisatie stemt in met het factureren van de klant als u de specifieke percentages van de projectwerkzaamheden voltooit. U stelt de volgende projectcategorieën voor het werk in, zodat u ze in het factureringsproces kunt gebruiken:

- Advisering
- Ontwerpen
- Installatie

U stelt ook factureringsregels in die automatisch de factuurbedragen berekenen voor het percentage voltooide projectwerkzaamheden in elke categorie.

De budgetmanager maakt een budget voor de projectcategorieën. De hoeveelheid voltooid werk wordt automatisch berekend als een percentage van de werkelijke hoeveelheid werk vergeleken met de gebudgetteerde bedragen.

## <a name="prerequisites"></a>Vereisten

Voordat u een project maakt waarin factureringsregels worden gebruikt, moet u de nummerreeksen instellen voor factureringsregels en een bijzondere-kostenjournaal dat wordt gebruikt om facturering naar rato van voortgang te boeken.

1. Ga naar **Projectbeheer en boekhouding** \> **Instellingen** \> **Projectbeheer- en boekhoudingsparameters**.
2. Stel op de pagina **Projectbeheer- en boekhoudingsparameters** in het tabblad **Nummerreeksen** de nummerreeks in die u wilt gebruiken wanneer factureringsregels worden gemaakt.
3. Ga naar **Projectbeheer en boekhouding** \> **Journalen** \> **Bijzondere kosten**.
4. Selecteer **Nieuw** op de pagina **Bijzondere-kostenjournaal** en voer de journaalnaam in.

## <a name="create-a-contract-for-progress-billings"></a>Een contract maken voor facturering naar rato van voortgang

Gebruik deze procedure om een projectcontract voor een project met een vaste prijs te maken. U maakt een projectfactuur wanneer de voltooiing van het project een opgegeven percentage bereikt.

1. Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Projectcontracten**.
2. Selecteer **Nieuw** op de pagina **Projectcontracten**.
3. Stel in het dialoogvenster **Nieuw projectcontract** de volgende velden in:

    - **Naam**
    - **Type financiering**
    - **Financieringsbron**
    - **Verkoopvaluta**: deze valuta wordt standaard gebruikt voor klantfacturen die gekoppeld zijn aan het projectcontract. U kunt echter de verkoopvaluta voor een bepaalde klantfactuur wijzigen.

4. Selecteer **OK**. De informatie wordt gekopieerd naar de koptekst van de pagina **Projectcontracten**.
5. Vul op de pagina **Projectcontracten** de rest van de vereiste informatie voor het project in.

## <a name="create-a-project-for-progress-billings"></a>Een project maken voor facturering naar rato van voortgang

Volg deze stappen als u een project en eventuele subprojecten wilt maken die aan een projectcontract zijn gekoppeld.

1. Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Alle projecten**.
2. Selecteer **Nieuw** op de pagina **Alle projecten**.
3. Selecteer in het dialoogvenster **Nieuw project** in het veld **Projecttype** de optie **Tijd en materiaal**.
4. Selecteer een projectgroep. Een projectgroep definieert de boekingsgegevens voor de projecten die zijn toegewezen aan de groep.
5. Selecteer **Project maken**.
6. Stel nadat het project is gemaakt, de projectfase in op **Onderhanden**.

## <a name="create-a-budget-for-a-project"></a>Maak een budget voor een project.

Budgetcategorieën worden gebruikt voor het automatisch berekenen van de factuurbedragen voor het percentage voltooide werkzaamheden voor de afzonderlijke categorieën. Volg deze stappen om budgetcategorieën te maken voor de geraamde kosten.

1. Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Alle projecten**.
2. Selecteer op de pagina **Alle projecten** het gewenste project en open het.
3. Selecteer op de pagina **Projecten** in het actievenster op het tabblad **Plan** in de groep **Budget** de optie **Projectbudget**.
4. Voer op de pagina **Projectbudget** de geschatte kosten in voor de afzonderlijke categorieën in het project.

## <a name="create-billing-rules-for-progress-billings"></a>Factureringsregels maken voor facturering naar rato van voortgang

1. Ga naar **Projectbeheer en boekhouding** \> **Projecten** \> **Projectcontracten**.
2. Selecteer op de pagina **Projectcontracten** een projectcontract en open het.
3. Selecteer **Toevoegen** op de pagina Projectcontract in het sneltabblad **Factureringsregels**.
4. Selecteer op de pagina **Factureringsregel** in het veld **Regeltype** de optie **Voortgang**.
5. Voer in het sneltabblad **Regeldetails factureringsregel** in het veld **Contractwaarde** de totale waarde van het contract in.
6. Selecteer in het veld **Categorie** de categorie waarnaar de transactie moet worden geboekt.
7. Selecteer in het veld **Project** het project waarvoor deze factureringsregel wordt gebruikt.
8. Optioneel: u kunt de factureringsregel aan extra projecten toewijzen. Selecteer op het sneltabblad **Project** in de sectie **Beschikbare projecten** een project en selecteer vervolgens de pijl naar rechts om het project toe te voegen aan de sectie **Geselecteerde projecten**.
9. Optioneel: bereken een percentagebedrag dat de klant inhoudt van betalingen op een factuur. Selecteer op het sneltabblad **Inhoudingsvoorwaarden betalingen** de financieringsbron en vul vervolgens het veld **Inhoudingspercentage** in.
10. Herhaal deze stappen voor het maken van aanvullende factureringsregels voor het contract.
