---
title: Configuratie van twee keer wegschrijven in Finance and Operations-apps en Dataverse controleren
description: In dit onderwerp wordt uitgelegd hoe u kunt bepalen of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 505344b42e6aafc2018e8f8d29ddd1acf59107b4e6d92737c53f3de04850ee40
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6736321"
---
# <a name="verify-dual-write-configuration-in-finance-and-operations-apps-and-dataverse"></a>Configuratie van twee keer wegschrijven in Finance and Operations-apps en Dataverse controleren

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Dataverse. In dit onderwerp wordt specifiek uitgelegd hoe u kunt bepalen of Twee keer wegschrijven is geconfigureerd in Finance and Operations-apps en Dataverse.

## <a name="verify-that-dual-write-is-configured-in-a-finance-and-operations-app"></a>Controleren of Twee keer wegschrijven is geconfigureerd in een Finance and Operations-app

Om te bepalen of de fouten die worden weergegeven wanneer u rijen voor de update probeert op te slaan, afkomstig zijn van Twee keer wegschrijven, controleert u eerst of Twee keer wegschrijven is geconfigureerd.

+ Als u beheerdersrechten hebt in de Finance and Operations-app, gaat u naar **Werkruimten \> Gegevensbeheer** en selecteert u de tegel voor **Twee keer wegschrijven**. Als de details van de gekoppelde omgevingen en de lijst met actieve tabeltoewijzingen worden weergegeven, wordt Twee keer wegschrijven geconfigureerd.

    ![De verbinding met de Finance and Operations-app controleren als u beheerdersbevoegdheden hebt.](media/verify_fin_ops_1.png)

+ Als u geen beheerdersbevoegdheden hebt, wordt er een foutbericht weergegeven: *Kan geen gegevens schrijven naar entiteit \<entity name\>*. In het voorbeeld in de volgende afbeelding kunt u geen klantrij in de Finance and Operations-app maken, omdat Twee keer wegschrijven is geconfigureerd, maar de verwijzingsgegevens voor de klantengroep en de betalingsvoorwaarden zijn niet aanwezig in Dataverse.

    ![De verbinding met de Finance and Operations-app controleren als u beheerdersbevoegdheden hebt.](media/verify_fin_ops_2.png)

Voor informatie over het oplossen van problemen wanneer u gegevens maakt in Finance and Operations-apps leest u [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md).

## <a name="verify-that-dual-write-is-configured-in-dataverse"></a>Controleren of Twee keer wegschrijven is geconfigureerd in Dataverse

Wanneer u gegevens maakt en u de kolom **Bedrijf** ziet op pagina's in Dataverse, is Twee keer wegschrijven geconfigureerd.

![De Dataverse-verbinding controleren.](media/verify_cds.png)

Voor informatie over het oplossen van problemen wanneer u gegevens maakt in Dataverse leest u [Problemen met live synchronisatie oplossen](dual-write-troubleshooting-live-sync.md).

Voor informatie over het weergeven van foutdetails als u fouten tegenkomt bij het maken van gegevens in Dataverse, raadpleegt u [Het traceerlogboek voor de invoegtoepassing inschakelen en weergeven in Dataverse om foutdetails weer te geven](dual-write-troubleshooting.md#enable-view-trace).


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]