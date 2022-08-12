---
title: Versiegeschiedenis weergeven om pagina's en fragmenten terug te zetten
description: In dit artikel wordt beschreven hoe u de versiegeschiedenis van een pagina of fragment kunt bekijken en kunt terugzetten naar een oudere versie in Microsoft Dynamics 365 Commerce Site Builder.
author: phinneyridge
ms.date: 06/21/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: niholman
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: fa2ecdd9d9bc7e60b279d850573b5caa6df2c659
ms.sourcegitcommit: 9cfccb5c260ce56a3457f9ea12e80f54ea55a3b4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183672"
---
# <a name="view-version-history-to-revert-pages-and-fragments"></a>Versiegeschiedenis weergeven om pagina's en fragmenten terug te zetten

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

In dit artikel wordt beschreven hoe u de versiegeschiedenis van een pagina of fragment kunt bekijken en kunt terugzetten naar een oudere versie in Microsoft Dynamics 365 Commerce Site Builder.

Met Commerce Site Builder kunt u de versiegeschiedenis van een pagina of fragment bekijken en zo nodig terugzetten naar een specifieke eerdere versie van een document. Terwijl een document geopend is, kunt u **Geschiedenis weergeven** selecteren op de opdrachtbalk om het dialoogvenster **Versiegeschiedenis** te openen, waarin op het tabblad **Versie** de geschiedenis van alle versies wordt weergegeven en activiteiten voor de pagina of het fragment worden opgeslagen. U kunt vervolgens een eerdere versie van het document in de lijst selecteren, een voorbeeld bekijken en het terugzetten als de huidige versie. Op het tabblad **Activiteit** van het dialoogvenster wordt de volledige activiteitsgeschiedenis van het document weergegeven, inclusief alle gebeurtenissen voor opslaan, publiceren en publicatie ongedaan maken.

> [!NOTE]
> Er wordt een nieuwe versie van een document gemaakt telkens als een siteauteur wijzigingen aanbrengt en vervolgens **Bewerking voltooid** voor het document selecteert. 

Volg deze stappen om de versiegeschiedenis van een pagina of fragment weer te geven en terug te zetten naar een eerdere versie.

1. Open in Site Builder de pagina of het fragment waarvoor u de versiegeschiedenis wilt bekijken.
1. Selecteer **Geschiedenis weergeven** op de opdrachtbalk.

    ![Knop Geschiedenis weergeven.](./media/version-history-1.png)

1. Selecteer een eerdere versie van het document in het dialoogvenster **Versiegeschiedenis** op het tabblad **Versie**. In het eigenschappenvenster aan de rechterkant ziet u een miniatuurweergave van de geselecteerde versie, en informatie over wie deze heeft gewijzigd en wanneer.

    ![Lijstweergave versiegeschiedenis.](./media/version-history-2.png)

1. Als u een volledig weergegeven voorbeeld van de geselecteerde versie van het document wilt weergeven, selecteert u **Voorbeeld**. Als u het voorbeeld wilt sluiten en wilt terugkeren naar het dialoogvenster **Versiegeschiedenis**, selecteert u **Voorbeeld afsluiten**.
1. Als u een eerdere versie van een document wilt herstellen, selecteert u deze in de lijst op het tabblad **Versie** en selecteert u vervolgens **Herstellen**. Het berichtvak **Versie \<version number\> herstellen** verschijnt en u wordt gevraagd om de actie te bevestigen. 

    ![Knop Herstellen en berichtvak ter bevestiging.](./media/version-history-3.png)

1. Als u wilt doorgaan met de herstelactie, selecteert u **Herstellen**. Site Builder wordt vernieuwd en toont de herstelde versie van de pagina of het fragment.
1. Selecteer **Bewerking voltooien** en vervolgens **Publiceren** om de herstelde versie te publiceren.
