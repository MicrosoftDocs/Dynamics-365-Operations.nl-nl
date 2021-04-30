---
title: Handmatig een vraagprognose wijzigen
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
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889019"
---
# <a name="modify-a-demand-forecast-manually"></a>Handmatig een vraagprognose wijzigen

[!include [banner](../../includes/banner.md)]

Deze procedure laat zien hoe u de prognose voor een artikel kunt wijzigen. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF. Deze procedure is bedoeld voor de productieplanner.

## <a name="modify-the-forecast-for-a-selected-item"></a>De prognose voor een geselecteerd artikel wijzigen

De prognose voor een geselecteerd artikel wijzigen:

1. Ga naar **Modules \> Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Zoek en selecteer de gewenste record in de lijst. Selecteer het artikel waarvoor u de prognose wilt wijzigen.
1. Open in het actievenster het tabblad **Plan** en selecteer **Vraagprognose**.
1. Selecteer een rij in de lijst. Als er geen prognoseregels zijn, maakt u een nieuwe regel door **Nieuw** te selecteren in het actievenster.  
1. Voer in het veld **Verkoophoeveelheid** een positief getal in. Dit getal geeft de geraamde hoeveelheid voor het artikel aan. Als u een negatief getal opgeeft, wordt er een fout weergegeven.
1. Vul zo nodig de andere velden in.
1. Selecteer **Opslaan** in het actievenster.

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a>De prognose voor een of meer artikelen wijzigen met Microsoft Excel

De prognose voor een of meer artikelen wijzigen met Microsoft Excel:

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
