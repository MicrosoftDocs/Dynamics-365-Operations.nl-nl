---
title: 'Guide: handmatig een vraagprognose wijzigen'
description: Dit onderwerp laat zien hoe u de prognose voor een artikel kunt wijzigen
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83575da4d382743b45c2de7964a7cbf1cc366989955884100dcb766a67166cf1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6741280"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Guide: handmatig een vraagprognose wijzigen

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u de prognose voor een artikel kunt wijzigen. Deze procedure is bedoeld voor de productieplanner.

## <a name="modify-the-forecast-for-a-selected-item"></a>De prognose voor een geselecteerd artikel wijzigen

De prognose voor een geselecteerd artikel wijzigen:

1. Ga naar **Modules \> Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer de gewenste record in de lijst. Selecteer het artikel waarvoor u de prognose wilt wijzigen.
1. Open in het actievenster het tabblad **Plan** en selecteer **Vraagprognose**.
1. Selecteer een rij in de lijst. Als er geen prognoseregels zijn, maakt u een nieuwe regel door **Nieuw** te selecteren in het actievenster.  
1. Voer in het veld **Verkoophoeveelheid** een positief getal in. Dit getal geeft de geraamde hoeveelheid voor het artikel aan. Als u een negatief getal opgeeft, wordt er een fout weergegeven.
1. Vul zo nodig de andere velden in.
1. Selecteer **Opslaan** in het actievenster.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>De prognose voor een of meer artikelen wijzigen met Microsoft Excel

Ga als volgt te werk om de prognose voor een of meer artikelen te wijzigen met Microsoft Excel:

1. U kunt een van de volgende dingen doen:
    - Open de **pagina Vraagprognose** voor een artikel (het maakt niet uit welke pagina) zoals wordt beschreven in de vorige sectie.
    - Ga naar **Hoofdplanning \> Prognose \> Prognose handmatig invoeren \> Vraagprognoseregels**.
1. Selecteer in het actievenster **Openen in Microsoft Office \> Invoer vraagprognose**.
1. Selecteer een downloadlocatie, sla deze op en open het gedownloade bestand in Excel.
1. Als er een waarschuwing wordt gegeven, kiest u **Bewerken inschakelen**.
1. Meld u in Excel aan bij Supply Chain Management met het Microsoft Dynamics-taakvenster. U moet zich aanmelden via de optie **Aangemeld houden** en u moet de app voor gegevensverbinding vertrouwen.
1. In het Excel-werkblad worden nu alle huidige vraagprognoseregels voor uw bedrijf weergeven.  U kunt naar wens vraagprognoseregels toevoegen, verwijderen en bewerken.
1. Selecteer **Publiceren** in het Microsoft Dynamics-taakvenster om de wijzigingen weer naar Supply Chain Management te uploaden.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
