---
title: Uitzonderingen voor orderverzameling op verkoop- en transferregels handmatig verwerken
description: In dit artikel wordt beschreven hoe beheerders handmatig voorraadtransacties kunnen verzamelen (of het verzamelen annuleren) om problemen op te lossen die worden veroorzaakt door beschadigde verkoop- en transferordergegevens.
author: perlynne
ms.date: 08/19/2022
ms.topic: article
ms.search.form: WHSManualSalesLinePicking, WHSManualInventTransferLinePicking, InventTransPick, WHSLoadLineManualCorrection, WHSTroubleshootingSelfService
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: d2f89a7109060e69aca6a06eadaedc017728bbae
ms.sourcegitcommit: 0220be95c007c77ba3b73fed8ac68a3d72dc2884
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403653"
---
# <a name="manually-handle-sales-and-transfer-line-picking-exceptions"></a>Uitzonderingen voor orderverzameling op verkoop- en transferregels handmatig verwerken

[!include [banner](../includes/banner.md)]

Beheerders kunnen door handmatige verwerking van uitzonderingen voor orderverzameling van verkoop- en transferregels problemen oplossen die worden veroorzaakt door beschadigde verkoop- en transferordergegevens. Met deze informatie kunnen vertrouwde gebruikers handmatig voorraadtransacties verzamelen (of het verzamelen annuleren) die zijn gerelateerd aan verkoop- en transferorderregels terwijl magazijnprocessen al worden uitgevoerd.

De functionaliteit die hier wordt beschreven, mag alleen worden gebruikt wanneer het systeem de verwerking van de magazijnprocessen niet op de gebruikelijke manier kan voltooien. Standaard mogen alleen gebruikers met de rol systeembeheerder deze rol gebruiken. U kunt toegang tot deze rollen verlenen door de bevoegdheid *Verkoopregels handmatig verzamelen* toe te wijzen aan andere rollen zoals nodig is.

## <a name="turn-on-this-feature-for-your-system"></a>Deze functie inschakelen voor uw systeem

Voordat u de in dit artikel beschreven functies kunt gebruiken, moet u deze in het systeem inschakelen. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functies te controleren en in te schakelen. In het werkgebied **Functiebeheer** worden de functies met de volgende namen vermeld:

- *Handmatige orderverzamelactiviteit van verkoopregels voor beheerder of soortgelijke vertrouwde gebruikers*<br>(Vanaf Supply Chain Management versie 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld.)
- *Handmatige orderverzamelactiviteit van transferregels voor beheerder of soortgelijke vertrouwde gebruikers*

## <a name="correct-transactions-related-to-sales-or-transfer-order-lines"></a>Transacties corrigeren die betrekking hebben op verkoop- of transferorderregels

Met de volgende procedure corrigeert u transacties die zijn gerelateerd aan verkoop- of transferorderregels.

1. Volg een van de volgende stappen, afhankelijk van het type order dat u moet corrigeren:

    - Als u een transactie wilt corrigeren die is gerelateerd aan een verkooporder, gaat u naar **Warehouse Management \> Periodieke taken \> Opschonen \> Verkoopregels handmatig verzamelen**.
    - Als u een transactie wilt corrigeren die is gerelateerd aan een transferorder, gaat u naar **Warehouse Management \> Periodieke taken \> Opschonen \> Transferregels handmatig verzamelen**.

1. Gebruik op de pagina **Verkoopregels handmatig verzamelen** of **Transferregels handmatig verzamelen** de filters boven aan het raster om de gewenste regel te zoeken en selecteer vervolgens de doelorderregel in het bovenste raster.
1. Gebruik de tabbladen **Voorraadtransacties**, **Regels laden**, **Werkregels** en **Containerregels** in het onderste gedeelte om meer informatie over de geselecteerde regel weer te geven. De informatie op deze tabbladen geeft een basisoverzicht van de gerelateerde magazijnprocessen en hun status.
1. Selecteer in het actievenster **Orderverzamelen** om de geselecteerde orderregel te openen op de pagina **Orderverzamelen** voor voorraadtransacties. U kunt deze stap zelfs voltooien voor orderregels die al zijn vrijgegeven in het magazijn. (Orderregels die zijn vrijgegeven in het magazijn, kunnen meestal niet worden geopend op de pagina **Orderverzamelen**.)

    > [!NOTE]
    > Er worden mogelijk verschillende waarschuwingen weergegeven wanneer u de pagina **Orderverzamelen** opent. Voer de aanbevolen actie uit voor deze waarschuwingen. U kunt bijvoorbeeld een waarschuwing ontvangen over orderregels die aan magazijnwerk zijn gekoppeld. In dit geval heeft het zin om te proberen het werk te annuleren door de standaardfunctionaliteit [werk annuleren](cancel-warehouse-work.md) te gebruiken voordat u handmatige correcties uitvoert.

1. Selecteer de regel in het **transactieraster** en vervolgens **Orderverzamelregel toevoegen** op de werkbalk **Transacties**.
1. De geselecteerde regel wordt verplaatst naar het raster **Orderverzamelregels**. Stel de juiste waarden in voor kolommen met ontbrekende vereiste informatie. (Geef bijvoorbeeld de locatie en nummerplaat op waaruit het artikel moet worden opgehaald.)
1. Selecteer op de werkbalk **Orderverzamelregels** de optie **Alles verzamelen bevestigen**.

## <a name="correct-load-line-quantities"></a>Correcties van hoeveelheden op ladingregels

Met de volgende procedure kunt u de hoeveelheid op de ladingregel aanpassen.

1. Volg een van de volgende stappen, afhankelijk van het type order dat u moet corrigeren:

    - Als u een transactie wilt corrigeren die is gerelateerd aan een verkooporder, gaat u naar **Warehouse Management \> Periodieke taken \> Opschonen \> Verkoopregels handmatig verzamelen**.
    - Als u een transactie wilt corrigeren die is gerelateerd aan een transferorder, gaat u naar **Warehouse Management \> Periodieke taken \> Opschonen \> Transferregels handmatig verzamelen**.

1. Gebruik op de pagina **Verkoopregels handmatig verzamelen** of **Transferregels handmatig verzamelen** de filters boven aan het raster om de gewenste regel te zoeken en selecteer vervolgens de doelorderregel in het bovenste raster.
1. Selecteer op het tabblad **Ladingregels** in het onderste gedeelte de optie **Ladingregels handmatig corrigeren** op de werkbalk.
1. Controleer op de pagina **Ladingsregels handmatig corrigeren** in het raster **Voorraadtransacties** de voorraadtransacties die aan de geselecteerde ladingregel zijn gerelateerd.
1. Corrigeer in het bovenste raster zo nodig de hoeveelheden op de ladingregel in de volgende kolommen:

    - **Hoeveelheid gemaakt werk**
    - **Verzamelde hoeveelheid**
    - **Geplande hoeveelheid voor cross-docken**

    Alle wijzigingen die u in deze kolommen aan brengen, worden gevalideerd.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
