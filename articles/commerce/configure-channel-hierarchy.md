---
title: Een kanaal voor een kanaalnavigatiehiërarchie configureren
description: In dit artikel wordt beschreven hoe u een kanaal configureert om een kanaalnavigatiehiërarchie in Microsoft Dynamics 365 Commerce te gebruiken.
author: samjarawan
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: samjar
ms.search.validFrom: 2020-01-20
ms.dyn365.ops.version: Release 10.0.8
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: b15e6eee86880f0315f42b34056385f718cc6bf1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280388"
---
# <a name="configure-a-channel-to-use-a-channel-navigation-hierarchy"></a>Een kanaal voor een kanaalnavigatiehiërarchie configureren


[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven hoe u een kanaal configureert om een kanaalnavigatiehiërarchie in Microsoft Dynamics 365 Commerce te gebruiken.

## <a name="overview"></a>Overzicht

Met kanaalnavigatiehiërarchieën kunt u producten indelen in categorieën, zodat de producten kunnen worden bezocht op een e-commerce site of op verkooppunten (POS). Winkel- en online kanalen moeten met kanaalnavigatiehiërarchieën worden geconfigureerd.

## <a name="configure-the-channel"></a>Het kanaal configureren

Voer de volgende stappen uit om een kanaal te configureren voor het gebruik van een kanaalnavigatiehiërarchie.

1. Ga in het navigatievenster naar **Modules \> Retail en Commerce \> Kanaalinstellingen \> Kanaalcategorieën en productkenmerken**.
1. Selecteer het kanaal dat u wilt configureren.
1. Selecteer in het actievenster **Metagegevens van kenmerken instellen**.
1. Selecteer in de vervolgkeuzelijst **Categoriehiërarchie** de juiste kanaalnavigatiehiërarchie.
1. Selecteer **Opslaan** in het actievenster.
1. Voeg onder **Kenmerkgroep** kenmerkgroepen toe die algemene kenmerken voor alle knooppunten moeten worden.

In de volgende afbeelding ziet u hoe u een kanaal configureert voor het gebruik van een kanaalnavigatiehiërarchie.

![Voorbeeld van kanaalconfiguratie.](media/configure-channel-hierarchy-1.png)

## <a name="set-attribute-metadata"></a>Metagegevens van kenmerken instellen

Als u de metagegevens voor het kenmerk instelt, kunt u op elk knooppunt kenmerken configureren.

Volg deze stappen om metagegevens voor kenmerken in te stellen.

1. Selecteer in het actievenster **Metagegevens van kenmerken instellen**.
1. Selecteer **Kanaalproductkenmerken** voor elk knooppunt.
1. Stel **Kenmerk in kanaal weergeven** in op **Ja** en **Kan worden verfijnd** op **Ja** om verfijningen voor dat kanaal in te schakelen.
1. Nadat u elk knooppunt naar wens hebt geconfigureerd, selecteert u in het **actievenster** de knop **Opslaan**.
1. Selecteer de **X** in de rechterbovenhoek om dit scherm af te sluiten en terug te gaan naar de pagina **Kanaalcategorieën en productkenmerken**.

De volgende afbeelding toont een voorbeeld van een set productkenmerken voor kanalen die is geconfigureerd op een knooppunt van een kanaalcategorie.

![Kanaalkenmerken in een kanaalcategorieknooppunt.](media/configure-channel-hierarchy-2.png)

## <a name="publish-changes"></a>Wijzigingen publiceren

U moet de wijzigingen publiceren om de wijzigingen van kracht te laten worden.

Voer deze stappen uit om wijzigingen te publiceren.

1. Selecteer in het actievenster **Kanaalupdates publiceren**.
1. Selecteer **OK** in het deelvenster **Kanaalupdates publiceren**.

De volgende afbeelding laat zien hoe u kanaalupdates kunt publiceren.

![Afzetkanaalupdates publiceren.](media/configure-channel-hierarchy-3.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Een afzetkanaalnavigatiehiërarchie maken](create-channel-hierarchy.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
