---
title: Een afzetkanaalnavigatiehiërarchie maken
description: In dit onderwerp wordt beschreven hoe u een kanaalnavigatiehiërarchie maakt in Microsoft Dynamics 365 Commerce.
author: samjarawan
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: d522838bdddf6cda6d7e451b27183f733e3de53df865d49cdadf846cf99cc953
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6749950"
---
# <a name="create-a-channel-navigation-hierarchy"></a>Een afzetkanaalnavigatiehiërarchie maken


[!include [banner](includes/banner.md)]

In dit onderwerp wordt beschreven hoe u een kanaalnavigatiehiërarchie maakt in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Met een kanaalnavigatiehiërarchie kunt u producten groeperen en indelen in categorieën, zodat de producten online of op verkooppunten (POS) kunnen worden bezocht.

## <a name="create-a-channel-navigation-hierarchy"></a>Een afzetkanaalnavigatiehiërarchie maken

Voer de volgende stappen uit om een navigatiehiërarchie voor een kanaal te maken.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Producten en categorieën \> Kanaalnavigatiecategorieën**.
1. Selecteer **Nieuw** in het actievenster.
1. Voer in het vak **Naam** een naam in.
1. Voer in het vak **Omschrijving** een beschrijving in.
1. Selecteer **Maken**.
1. Selecteer in het actievenster **Nieuw categorieknooppunt** om een hoofdknooppunt te maken.
1. Voer in het vak **Naam** een naam in.
1. Voer in het vak **Omschrijving** een beschrijving in.
1. Voer in het vak **Beschrijvende naam** een beschrijvende naam in.
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van een hoofdknooppunt.

![Voorbeeld hoofdknooppunt.](media/create-channel-hierarchy-1.png)

## <a name="create-navigation-category-nodes"></a>Navigatiecategorieknooppunten maken

Voer de volgende stappen uit om extra navigatiecategorieknooppunten te maken die de productcategorieën in het kanaal vertegenwoordigen.

1. Selecteer in het navigatievenster het bovenliggende knooppunt waaraan u een categorie wilt toevoegen.
1. Klik in het actievenster op **Nieuw categorieknooppunt**.
1. Voer in het vak **Naam** een naam in.
1. Voer in het vak **Omschrijving** een beschrijving in.
1. Voer in het vak **Beschrijvende naam** een beschrijvende naam in.
1. Voer in het vak **Weergavevolgorde** een weergavevolgorde in (optioneel).
1. Selecteer **Opslaan** in het actievenster.

In de volgende afbeelding ziet u een voorbeeld van een voltooide kanaalnavigatiehiërarchie.

![Voorbeeld kanaalhiërarchie.](media/create-channel-hierarchy-2.png)

## <a name="add-products-to-category-nodes"></a>Producten aan categorieknooppunten toevoegen

Voer de volgende stappen uit om producten toe te voegen aan categorieknooppunten.

1. Selecteer een categorieknooppunt.
1. Selecteer **Toevoegen** onder **Producten**.
1. Zoek de nieuwe producten die u wilt toevoegen aan de hand van het productnummer of de productnaam en selecteer **OK**.
1. Selecteer **Opslaan** in het actievenster.

> [!NOTE]
> Producten toevoegen aan een knooppunt in de kanaalnavigatiehiërarchie is niet genoeg om de producten te laten weergeven in een geselecteerd kanaal. De producten moeten ook aan een afzetkanaal worden geassorteerd. Meer informatie over assortimenten vindt u in [Assortimentsbeheer](assortments.md).

De volgende afbeelding toont een voorbeeldknooppunt met toegevoegde producten.

![Producten toegevoegd aan een categorieknooppunt.](media/create-channel-hierarchy-3.png)

## <a name="add-product-attribute-groups-to-category-nodes"></a>Productkenmerkgroepen toevoegen aan categorieknooppunten

> [!NOTE]
> U moet kenmerkgroepen maken voordat u ze aan een knooppunt in de kanaalnavigatiehiërarchie kunt toevoegen.

Voer deze stappen uit om een productkenmerkgroep aan een categorieknooppunt toe te voegen.

1. Selecteer een categorieknooppunt.
1. Selecteer **Toevoegen** onder **Productkenmerkgroep**.
1. Zoek de kenmerkgroepen die u wilt toevoegen en klik op **OK**.
1. Selecteer **Opslaan** in het actievenster.

De volgende afbeelding toont een voorbeeldknooppunt met toegevoegde productkenmerkgroepen.

![Productkenmerkgroepen op een knooppunt.](media/create-channel-hierarchy-4.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Assortimenten instellen](set-up-assortments.md)

[Kenmerken en kenmerkgroepen beheren](attribute-attributegroups-lifecycle.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
