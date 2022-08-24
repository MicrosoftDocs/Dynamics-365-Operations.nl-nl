---
title: Configuratie voor twee keer wegschrijven verifiëren in apps voor financiën en bedrijfsactiviteiten en Dataverse
description: In dit artikel wordt uitgelegd hoe u kunt bepalen of Twee keer wegschrijven is geconfigureerd in apps voor financiën en bedrijfsactiviteiten en in Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 4ff7821fce661f174f57fb45667d4ceb3cfcede9
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289385"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Configuratie voor twee keer wegschrijven verifiëren in apps voor financiën en bedrijfsactiviteiten en Dataverse

[!include [banner](../../includes/banner.md)]





Dit artikel bevat informatie voor het oplossen van problemen met de integratie van Twee keer wegschrijven tussen apps voor financiën en bedrijfsactiviteiten en Dataverse. In dit onderwerp wordt specifiek uitgelegd hoe u kunt bepalen of Twee keer wegschrijven is geconfigureerd in apps voor financiën en bedrijfsactiviteiten en in Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Configuratie voor twee keer wegschrijven verifiëren in een app voor financiën en bedrijfsactiviteiten

Om te bepalen of de fouten die worden weergegeven wanneer u rijen voor de update probeert op te slaan, afkomstig zijn van Twee keer wegschrijven, controleert u eerst of Twee keer wegschrijven is geconfigureerd.

+ Als u beheerdersrechten hebt in de app voor financiën en bedrijfsactiviteiten, gaat u naar **Werkgebieden \> Gegevensbeheer** en selecteert u de tegel **Twee keer wegschrijven**. Als de details van de gekoppelde omgevingen en de lijst met actieve tabeltoewijzingen worden weergegeven, wordt Twee keer wegschrijven geconfigureerd.

    ![De verbinding met de app voor financiën en bedrijfsactiviteiten controleren als u beheerdersbevoegdheden hebt.](media/verify_fin_ops_1.png)

+ Als u geen beheerdersbevoegdheden hebt, wordt er een foutbericht weergegeven: *Kan geen gegevens schrijven naar entiteit \<entity name\>*. In het voorbeeld in de volgende afbeelding kunt u geen klantrij in de app voor financiën en bedrijfsactiviteiten maken, omdat Twee keer wegschrijven is geconfigureerd, maar de verwijzingsgegevens voor de klantengroep en de betalingsvoorwaarden zijn niet aanwezig in Dataverse.

    ![De verbinding met de app voor financiën en bedrijfsactiviteiten controleren als u geen beheerdersbevoegdheden hebt.](media/verify_fin_ops_2.png)

Voor informatie over het oplossen van problemen wanneer u gegevens maakt in apps voor financiën en bedrijfsactiviteiten raadpleegt u [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Controleren of Twee keer wegschrijven is geconfigureerd in Dataverse

Wanneer u gegevens maakt en u de kolom **Bedrijf** ziet op pagina's in Dataverse, is Twee keer wegschrijven geconfigureerd.

![De Dataverse-verbinding controleren.](media/verify_cds.png)

Voor informatie over het oplossen van problemen wanneer u gegevens maakt in Dataverse leest u [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md).

Voor informatie over het weergeven van foutdetails als u fouten tegenkomt bij het maken van gegevens in Dataverse, raadpleegt u [Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Dataverse om foutdetails weer te geven](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
