---
title: Werken met vooraf ingestelde indelingen
description: In dit onderwerp wordt beschreven hoe u werkt met vooraf ingestelde indelingen in Microsoft Dynamics 365 Commerce.
author: phinneyridge
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: niholman
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ce54be1032777ffcaac474773cdeeef3b9028110
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793916"
---
# <a name="work-with-preset-layouts"></a>Werken met vooraf ingestelde indelingen

[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u werkt met vooraf ingestelde indelingen in Microsoft Dynamics 365 Commerce.

Lees voordat u de procedures in dit onderwerp uitvoert, eerst [Vooraf ingestelde en aangepaste indelingen](templates-layouts-overview.md#preset-and-custom-layouts). Zie [Overzicht sjablonen en indelingen](templates-layouts-overview.md) voor een algemeen overzicht.

## <a name="create-a-new-preset-layout"></a>Een nieuwe vooraf ingestelde indeling maken

Er zijn twee methoden voor het maken van een vooraf ingestelde indeling. U kunt een bestaande aangepaste indeling opslaan als een nieuwe vooraf ingestelde indeling of u kunt een geheel nieuwe indeling maken.

### <a name="create-a-preset-layout-from-an-existing-custom-layout"></a>Een vooraf ingestelde indeling maken op basis van een bestaande aangepaste indeling

Voer deze stappen uit om een vooraf ingestelde indeling te maken op basis van een bestaande aangepaste indeling.

1. Open een bestaande pagina waarin momenteel geen vooraf ingestelde indeling wordt gebruikt en die een modulestructuur heeft die u opnieuw wilt gebruiken voor andere pagina's op uw site.
1. Selecteer **Bewerken** om de pagina uit te checken.
1. Selecteer **Opslaan als nieuwe indeling**. Het dialoogvenster **Opslaan als nieuwe indeling** wordt geopend.
1. Voer een naam en beschrijving voor de vooraf ingestelde indeling in. De waarden die u invoert, worden weergegeven voor andere ontwerpers wanneer ze nieuwe pagina's maken vanuit uw indeling of overschakelen naar deze pagina. Voer daarom waarden in die nuttig zijn voor pagina-ontwerpers.
1. Selecteer **OK**.

De vooraf ingestelde indeling is nu beschikbaar wanneer u nieuwe pagina's maakt of een andere indeling selecteert voor een pagina in dezelfde sjabloonhiërarchie.

> [!TIP]
> Als u snel wilt zien of een specifieke pagina afhankelijk is van een vooraf ingestelde indeling, selecteert u de pagina in de lijstweergave met pagina's en controleert u de metagegevens voor de indeling in het eigenschappenvenster aan de rechterkant.

### <a name="create-a-new-preset-layout"></a>Een nieuwe vooraf ingestelde indeling maken

Voer deze stappen uit om een nieuwe vooraf ingestelde indeling te maken.

1. Selecteer **Indelingen** in het navigatievenster aan de linkerkant.
1. Selecteer **Nieuwe indeling**. Het dialoogvenster **Nieuwe indeling** wordt geopend.
1. Selecteer de sjabloon die u voor de vooraf ingestelde indeling wilt gebruiken.
1. Voer een naam en beschrijving voor de vooraf ingestelde indeling in. De waarden die u invoert, worden weergegeven voor andere ontwerpers wanneer ze nieuwe pagina's maken vanuit uw indeling of overschakelen naar deze pagina. Voer daarom waarden in die nuttig zijn voor pagina-ontwerpers.
1. Klik op **OK** om de nieuwe vooraf ingestelde indeling te maken en de indelingseditor te openen.
1. Voeg in de indelingseditor modules toe en configureer modules met de overzichtsstructuur aan de linkerkant en het eigenschappenvenster aan de rechterkant. (Het proces lijkt op het proces voor het toevoegen en configureren van modules voor een sjabloon in de sjablooneditor.) De rangschikking van modules en alle vergrendelde standaardinstellingen wordt de gecentraliseerde moduleconfiguratie voor pagina's waarvoor deze vooraf ingestelde indeling wordt gebruikt.

## <a name="modify-a-preset-layout"></a>Een vooraf gedefinieerde indeling wijzigen

Volg deze stappen om een vooraf ingestelde indeling te wijzigen.

1. Selecteer **Indelingen** in het navigatievenster aan de linkerkant.
1. Selecteer in de overzichtsstructuur aan de linkerkant de module die u wilt wijzigen in de indelingseditor. Voer vervolgens een van deze stappen uit:

    - Als u een module omhoog of omlaag binnen het bovenliggende niveau wilt verplaatsen, selecteert u de knop met het weglatings teken (**...**) voor de module en vervolgens **Omhoog** of **Omlaag**.
    - Als u de standaardinstellingen van een module wilt wijzigen, gebruikt u het eigenschappenvenster om standaardwaarden in te voeren en deze desgewenst te vergrendelen voor alle pagina's daaronder.
    - Als u nieuwe modules of fragmenten aan containermodules wilt toevoegen, selecteert u de knop met het weglatingsteken en selecteert u vervolgens **Module toevoegen** of **Fragment toevoegen**.
    - Als u een module uit de indeling wilt verwijderen, selecteert u de knop met het weglatingsteken en selecteert u **Verwijderen**.

## <a name="change-a-preset-layout-theme"></a>Een thema voor een vooraf ingestelde indeling wijzigen

Een normale gewoonte is het instellen van een standaardthema voor alle pagina's met een vooraf ingestelde indeling.

Voer de volgende stappen uit om het thema in te stellen of te wijzigen voor alle onderliggende pagina's met de vooraf ingestelde indeling.

1. Selecteer in de overzichtsstructuur aan de linkerkant de paginacontainermodule in de indelingseditor. (Meestal is deze module het tweede knooppunt met de naam **Standaardpagina**.)
1. Selecteer in het eigenschappenvenster aan de rechterkant een thema in het veld **Thema**.

## <a name="save-check-in-preview-and-publish-a-preset-layout"></a>Een vooraf ingestelde indeling opslaan, inchecken, vooraf bekijken en publiceren

Om een vooraf ingestelde indeling op te slaan en in te checken, volgt u deze stappen.

1. Selecteer de optie **Opslaan** boven aan de indelingseditor. Opgeslagen wijzigingen zijn niet van invloed op vervolgpagina's totdat ze zijn ingecheckt.
1. Selecteer **Bewerken voltooien**. Uw wijzigingen zijn nu detecteerbaar voor vervolgworkflows.

Als u de wijzigingen wilt bekijken, opent u een bestaande pagina die de vooraf ingestelde indeling gebruikt of maakt u een nieuwe pagina op basis van de indeling.

Nadat u een voorbeeld van de wijzigingen in de vooraf ingestelde indeling hebt bekeken, volgt u een van deze stappen om de indeling naar uw live site te publiceren:

* Ga naar **Indelingen**, selecteer de indeling en selecteer **Publiceren.**
* Selecteer de indelingsnaam om de indelingseditor te openen en selecteer vervolgens **Publiceren**.
* Publiceer een pagina die verwijst naar de niet-gepubliceerde indeling. De indeling wordt automatisch gepubliceerd.

> [!WARNING]
> Op meerdere pagina's kan naar een vooraf ingestelde indeling worden verwezen. Wanneer u een vooraf ingestelde indeling publiceert, kan dit van invloed zijn op de indeling van meerdere pagina's.

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht sjablonen en indelingen](templates-layouts-overview.md)

[Werken met sjablonen](work-with-templates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
