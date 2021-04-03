---
title: Werkorders maken
description: In dit onderwerp wordt uitgelegd hoe u werkorders maakt in Activabeheer.
author: johanhoffmann
manager: tfehr
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 76306fb31e7e5297e6a5d64b97b5bd09b64349ee
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500569"
---
# <a name="creating-work-orders"></a>Werkorders maken

[!include [banner](../../includes/banner.md)]

Nadat u preventieve onderhoudstaken hebt gepland, is de volgende stap het maken van werkorders voor de taken. U kunt deze stap uitvoeren met een van de onderhoudsschema's. De geplande taken in een onderhoudsschema kunnen verschillende verwijzingstypen hebben, zoals beschreven in de volgende tabel.

| Verwijzingstype | Beschrijving |
|---|---|
| Onderhoudsplannen | Taken voor preventief onderhoud op basis van de typen onderhoudsplan *Tijd* of *Teller*. |
| Onderhoudsrondes | Taken voor preventief onderhoud met verschillende activa waarvoor een vergelijkbaar type onderhoud is vereist. |
| Onderhoudsverzoek | Een handmatig gemaakte aanvraag voor onderhoud of reparatie van een activum. Deze aanvraag kan worden geconverteerd naar een werkorder. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Werkorders maken op basis van uw onderhoudsschema

Volg deze stappen om werkorders te maken op basis van uw onderhoudsschema.

1. Open een van de volgende pagina's, afhankelijk van hoe u schema-artikelen voor uw werkorders wilt selecteren:

    - Alle onderhoudsschema's (**Activabeheer \> Beheerschema \> Alle onderhoudsschema's**)
    - Open onderhoudsschemaregels (**Activabeheer \> Beheerschema \> Alle onderhoudsschemaregels**)
    - Open onderhoudsschemagroepen (**Activabeheer \> Beheerschema \> Onderhoudsschemagroepen openen**)

1. Schakel in het raster het selectievakje in voor elke geplande onderhoudstaak waarvoor u een werkorder wilt maken. Selecteer vervolgens in het actievenster **Werkorder**.

    Het dialoogvenster **Werkorders maken** wordt weergegeven. Het veld **Prognose voor onderhoudsuren** toont het totaal aantal geraamde uren voor de geselecteerde regels.

    ![Dialoogvenster Werkorders maken](media/18-preventive-maintenance.png)

1. Geef in de sectie **Parameters** het aantal werkorders op dat u wilt maken. Een van de volgende opties selecteren:

    - **Eén werkorder per regel** – Eén werkorder per onderhoudsschemaregel maken.
    - **Eén werkorder per** – Werkorders maken die gegroepeerd zijn volgens de instellingen van de andere opties die beschikbaar worden wanneer u deze optie selecteert.

1. Selecteer in het veld **Werkordertype** het werkordertype dat u wilt gebruiken voor alle werkorders die u maakt.
1. Selecteer **OK** om de werkorders volgens uw instellingen te maken.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Werkorderregels groeperen die automatisch worden gemaakt terwijl een onderhoudsplan wordt uitgevoerd

[!INCLUDE [preview-banner-section](../../../includes/preview-banner-section.md)]

Met deze functie kunt u regels definiëren voor het groeperen van werkorderregels onder één werkorder wanneer het systeem is ingesteld om automatisch werkorders te genereren op basis van een onderhoudsplan. Eerder automatisch gegenereerde werkorders kunnen slechts één regel bevatten. U kunt werkorders nu echter wel groeperen op bijvoorbeeld activa, activatype of functionele locatie. (Handmatig gegenereerde werkorders konden al op deze manier worden gegroepeerd, zoals wordt beschreven in de vorige sectie van dit onderwerp.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Groepering inschakelen voor automatisch gegenereerde werkorders

Voordat u deze functie kunt gebruiken, moet deze zijn ingeschakeld in uw systeem. Beheerders kunnen gebruikmaken van de instellingen voor [functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) om de status van de functie te controleren en in te schakelen. Schakel in het werkgebied **Functiebeheer** de functie als volgt in:

- **Module:** *Activabeheer*
- **Functienaam:** *(Preview) Regels toepassen voor het groeperen van werkorders tijdens het uitvoeren van een onderhoudsplan*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Groepering instellen voor automatisch gegenereerde werkorders

Volg deze stappen om groepering in te stellen voor automatisch gegenereerde werkorders.

1. Ga naar **Activabeheer \> Instellen \> Preventief onderhoud \> Onderhoudsplannen**.
1. Volg deze stappen voor elk plan waarin u gegroepeerde werkorders wilt genereren:

    1. Selecteer het plan in het lijstvenster.
    1. Controleer op sneltabblad **Regels** of het selectievakje **Automatisch maken** op elke regel is ingeschakeld.

1. Ga naar **Activabeheer \> Periodiek \> Preventief onderhoud \> Onderhoudsplannen plannen**.
1. Geef in het dialoogvenster **Onderhoudsplannen plannen** in de sectie **Periode** de tijdshorizon op voor het plan (hoe ver vooruit moet worden gekeken bij het zoeken naar geplande onderhoudstaken om werk voor te genereren).
1. Stel de optie **Automatisch maken van werkorder vanuit schema** in op *Ja*.
1. Selecteer in het gedeelte **Werkorder** een van de volgende opties:

    - **Eén werkorder per regel** – Eén werkorder per onderhoudsschemaregel maken. (Deze optie biedt dezelfde functionaliteit die beschikbaar is wanneer de functie *Regels toepassen voor het groeperen van werkorders tijdens het uitvoeren van een onderhoudsplan* is uitgeschakeld.)
    - **Eén werkorder per** – Werkorders maken die gegroepeerd zijn volgens de instellingen van de andere opties die beschikbaar worden wanneer u deze optie selecteert.

1. Als u wilt dat de opties worden toegepast wanneer u slechts enkele van uw onderhoudsplannen uitvoert, voegt u op het tabblad **Op te nemen records** desgewenst filters toe, net als voor andere batchtaken in Microsoft Dynamics 365 Supply Chain Management.
1. Stel op het sneltabblad **Uitvoeren op achtergrond** desgewenst batch- en planningsopties in, op dezelfde manier als u doet voor andere batchtaken in Supply Chain Management.
1. Selecteer **OK** om de geselecteerde onderhoudsplannen uit te voeren en/of te plannen.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]