---
title: Problemen met Store Commerce-extensies oplossen
description: In dit artikel wordt beschreven hoe u extensieproblemen in de Microsoft Dynamics 365 Commerce-app Store Commerce kunt oplossen.
author: josaw1
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 1a2d6a68b7556d8b4d05529efd90f9e66f0c5925
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269776"
---
# <a name="troubleshoot-store-commerce-extension-issues"></a>Problemen met Store Commerce-extensies oplossen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u extensieproblemen in de Microsoft Dynamics 365 Commerce-app Store Commerce kunt oplossen.

## <a name="extensions-packages-arent-loaded"></a>Extensiepakketten worden niet geladen

### <a name="extensions-packages-dont-appear-on-the-pos--settings-page"></a>Extensiepakketten worden niet weergegeven op de pagina POS \> Instellingen

Triggers voor Commerce Runtime (CRT) zijn mogelijk niet bijgewerkt om het extensiepakket op te nemen of zijn niet geïmplementeerd. Zie [Uitbreidbaarheid van en triggers voor Commerce Runtime (CRT)](../dev-itpro/commerce-runtime-extensibility-trigger.md) voor meer informatie.

### <a name="extensions-packages-appear-on-the-pos--settings-page-but-the-manifest-isnt-loaded"></a>Op de pagina POS \> Instellingen worden extensiepakketten weergegeven, maar het manifest wordt niet geladen

Bevestig dat de extensiepakketten bestaan in de map **C:\\Program Files\\Microsoft Dynamics 365\\10.0\\Store Commerce\\Extensions**. Als de pakketten bestaan, moet er een **POS**-map zijn met het manifest.

Als er geen **POS**-map is, bevestigt u dat het Store Commerce-project correct verwijst naar het POS-extensieproject. Controleer het referentiepad van het project en controleer of het bestaat. 

In het volgende voorbeeld is te zien dat er voor het installatieprogrammaproject problemen zijn met het extensieproject waarnaar wordt verwezen.

![Verwijzing naar Store Commerce installatieprogrammaproject is niet geldig.](media/ReferenceNotValid.png)

Als de verwijzing voor het extensieproject correct is toegevoegd, is er geen waarschuwings- of afhankelijkheidsprobleem in het installatieprogrammaproject, zoals de onderstaande voorbeeldafbeelding laat zien.

![Verwijzing naar Store Commerce installatieprogrammaproject is geldig.](media/ReferenceValid.png)
