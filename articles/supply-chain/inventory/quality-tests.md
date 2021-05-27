---
title: Kwaliteitsbeheertests
description: In dit onderwerp wordt beschreven hoe u tests maakt die kunnen worden gebruikt voor kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.
author: rachel-profitt
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTestTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 95f759d051a520b577cb1cf3d595ce64e0dc4668
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021679"
---
# <a name="quality-management-tests"></a>Kwaliteitsbeheertests

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u tests maakt die kunnen worden gebruikt voor kwaliteitsorders in Microsoft Dynamics 365 Supply Chain Management.

U gebruikt de pagina **Tests** om de afzonderlijke tests definiëren en bekijken aan de hand waarvan wordt bepaald of uw producten voldoen aan de kwaliteitsspecificaties. U kunt een of meer afzonderlijke tests toewijzen aan een testgroep. In dit geval geeft u ook testspecifieke informatie op, zoals de aanvaardbare meetwaarden. Meetwaarden worden gebruikt voor kwantitatieve tests. Voor kwalitatieve tests worden testvariabelen gebruikt.

- Voor kwantitatieve tests wordt het veld **Type** ingesteld op *Geheel getal* of *Breuk*. Er is ook een maateenheid opgegeven. Kwaliteitsspecificaties en testresultaten worden uitgedrukt in getallen.
- Voor kwalitatieve tests wordt het veld **Type** ingesteld op *Optie*. Voor kwalitatieve tests is aanvullende informatie nodig over de testvariabele die wordt gemeten en de vaste opties. Kwaliteitsspecificaties en testresultaten worden uitgedrukt in getallen volgens een uitkomst.

U kunt een testinstrument ook toewijzen aan een test. Testinstrumenten zijn echter niet vereist voor het maken en gebruiken van tests met kwaliteitsorders. Zie [Testinstrumenten voor kwaliteitsbeheer](quality-test-instruments.md) voor meer informatie.

U kunt ook een eenheid voor een test opgeven om de maateenheid aan te geven waarin de testresultaten worden vastgelegd. Een test voor temperatuur kan bijvoorbeeld de eenheid voor graden Fahrenheit of Celsius bevatten.

## <a name="example-of-a-test"></a>Voorbeeld van een test

Een productiebedrijf voert twee tests uit op ingekocht materiaal: een kwantitatieve test op de kwaliteit van het materiaal en een kwalitatieve test op beschadigde verpakking. Het bedrijf definieert aanvullende gegevens voor de kwalitatieve test om de testvariabele (bijvoorbeeld beschadigde verpakking) en het bijbehorende resultaat te definiëren. Het bedrijf maakt gebruikt van de pagina **Testgroepen** om de twee tests toe te wijzen aan een testgroep en om specifieke informatie voor de tests op te geven. De testgroep wordt toegewezen aan een kwaliteitsorder, zodat het bedrijf de testresultaten van de twee tests kan rapporteren.

## <a name="create-a-test"></a>Een test maken

Volg deze stappen om een test te maken.

1. Ga naar **Voorraadbeheer \> Instellingen \> Kwaliteitscontrole \> Tests**.
1. Selecteer in het actievenster de optie **Nieuw** om een rij toe te voegen aan het raster. Stel daarna de volgende velden in voor de nieuwe rij:

    - **Test**: voer een unieke id of naam op voor de test in.
    - **Beschrijving**: voer een gedetailleerde beschrijving voor de test in.
    - **Type**: selecteer het type resultaten dat door de test wordt geproduceerd. Selecteer voor kwantitatieve tests *Breuk* of *Geheel getal*. Selecteer voor kwalitatieve tests *Optie*.
    - **Testinstrument**: selecteer een [testinstrument](quality-test-instruments.md) dat moet worden gebruikt voor de test.
    - **Eenheid**: als u *Breuk* of *Geheel getal* hebt geselecteerd in het veld **Type** (dat wil zeggen, als de test een kwantitatieve test is), selecteert u de maateenheid waarin de testresultaten moeten worden vastgelegd.

1. Sluit de pagina.

> [!NOTE]
> Nadat u een test hebt opgeslaan, kunt u het veld **Type** in het raster niet meer bewerken. Als u het type testresultaten moet wijzigen dat wordt vastgelegd voor een test, selecteert u **Type kwaliteitstest wijzigen** in het actievenster. Stel in het dialoogvenster **Type kwaliteitstest wijzigen** het veld **Nieuw type** in op het gewenste type en selecteer **OK** om het dialoogvenster te sluiten.

## <a name="additional-resources"></a>Aanvullende bronnen

- [Testinstrumenten voor kwaliteitsbeheer](quality-test-instruments.md)
- [Testgroepen voor kwaliteitsbeheer](quality-test-groups.md)
- [Testvariabelen voor kwaliteitsbeheer](quality-test-variables.md)
- [Kwaliteitskoppelingen](quality-associations.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
