---
title: Gegevens exporteren uit Attract en Onboard
description: Exporteer gegevens uit Dynamics 365 Talent Attract en Onboard.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: acdd93637385246f9c5c652cccdf2cbfb263cc33
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/23/2020
ms.locfileid: "2975929"
---
# <a name="export-data-from-attract-and-onboard"></a>Gegevens exporteren uit Attract en Onboard

[!include [banner](includes/banner.md)]

Zoals is aangekondigd in [Het buiten gebruik stellen van Dynamics 365 Talent: Attract- en Dynamics 365 Talent: Onboard-apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), stellen we Dynamics 365 Talent: Attract en Dynamics 365 Talent: Onboard buiten gebruik op 1 februari 2022. Om u te helpen bij de migratie naar een ander product, bieden beide apps nu mogelijkheden voor gegevensexport.

## <a name="export-data-from-attract"></a>Gegevens exporteren vanuit Attract

U kunt uw gegevens exporteren zonder de toegang tot uw omgeving te beperken. U kunt dit bijvoorbeeld doen voor testdoeleinden of om inzicht te krijgen in onze gegevensstructuur. Wanneer u klaar bent om te migreren, beperkt u de toegang tot uw Attract-omgeving met behulp van de instructies na deze procedure. Zorg dat u de gegevens opnieuw exporteert. 

1. Ga naar [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Selecteer onder **Gegevensexport** de optie **Een gegevensexport aanvragen**.

   ![[Een gegevensexport aanvragen vanuit Attract](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. Wanneer het berichtvenster **De aanvraag wordt verwerkt** wordt weergegeven, selecteert u **OK**. De gegevensexport kan 20 minuten in beslag nemen, afhankelijk van de grootte van de export.

4. Wanneer de export is voltooid, selecteert u de knop **Downloaden** ernaast. 

   >[!NOTE]
   >Alle gegevensexports zijn zeven dagen beschikbaar. Daarna vervalt de **Download**-koppeling.</br>
   
De download bevat een ZIP-bestand met uw Attract-gegevens, waaronder de volgende mappen:

| Mapnaam | Beschrijving |
| --- | --- |
| Beheerinstellingen | Configuraties van het Attract-beheercentrum. |
| Kandidaten | Alle kandidaten die aan banen of talentgroepen zijn toegevoegd. |
| E-mailsjablonen | Alle e-mailsjablonen die voor de omgeving zijn geconfigureerd. |
| Sjablonen voor baanaanbiedingspakketten | Alle sjablonen voor baanaanbiedingen die zijn gemaakt, plus de bijbehorende configuraties. |
| Regelsets voor baanaanbiedingen |  Alle regelsetbestanden die zijn geüpload voor aanbiedingsbeheer. |
| Sjablonen voor baanaanbiedingen | Alle sjablonen voor baanaanbiedingsdocumenten die voor de omgeving zijn gemaakt. |
| Vacatures | Alle aangemaakte banen. Verwijderde banen worden niet geëxporteerd. De submappen bevatten sollicitaties van kandidaten, met submappen voor bijlagen van sollicitaties en aanbiedingspakketten, indien van toepassing. |
| Vacaturesjablonen | Baanverwerkingssjablonen die in de omgeving zijn geconfigureerd. |
| Talentenpools | Alle gemaakte talentgroepen, lijsten van hun deelnemers en de kandidatenlijsten voor de talentgroepen. |
| Medewerkers | Lijst van alle medewerkers in de omgeving, plus hun rollen. |
| (basismap) | Een JSON-schemabestand waarin de gegevensstructuurvelden worden beschreven. |

### <a name="restrict-access-to-attract"></a>Toegang tot Attract beperken

Wanneer u klaar bent om te migreren, beperkt u de toegang van niet-beheerders tot de Attract-omgeving en exporteert u uw gegevens.

>[!IMPORTANT]
>Het beperken van de toegang tot de Attract-omgeving is permanent en kan niet ongedaan worden gemaakt. Sla deze stap over als u wilt dat niet-beheerders de toegang tot uw omgeving behouden.

1. Ga naar [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).

2. Om de toegang van niet-beheerders tot de Attract-omgeving te beperken, selecteert u onder **Toegang tot deze app beperken** de optie **Toegang nu beperken**. Door de toegang te beperken, wordt ook de publicatie van gepubliceerde actieve banen opgeheven.

   ![[Toegang van niet-beheerders tot Attract beperken](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. Wanneer u de waarschuwing **Dit is een permanente wijziging** ziet, selecteert u **Toegang beperken** om de toegang van gebruikers die geen beheerder zijn permanent te beperken vanuit deze omgeving. Als u deze stap nog niet wilt uitvoeren, selecteert u **Annuleren**.

   ![[Waarschuwing dat het beperken van de toegang een permanente wijziging is](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   >Beheerders blijven toegang houden tot de gegevensexport- en persoonlijke rapportpagina's wanneer u de toegang tot de Attract-omgeving hebt beperkt.

## <a name="export-data-from-onboard"></a>Gegevens exporteren vanuit Onboard

Wanneer u klaar bent, kunt u sjablonen, gidsen en kandidaatgegevens downloaden van Onboard.

1. Ga naar [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).

2. Selecteer onder **Gegevensexport** de optie **Een gegevensexport aanvragen**. 

   ![[Een gegevensexport aanvragen vanuit Onboard](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. Wanneer het berichtvenster **De aanvraag wordt verwerkt** wordt weergegeven, selecteert u **OK**. De gegevensexport kan 20 minuten in beslag nemen, afhankelijk van de grootte van de export.

4. Wanneer de export is voltooid, selecteert u de knop **Downloaden** ernaast. 

   ![[Gegevensexport downloaden van Onboard](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   >Uw gegevensexport is zeven dagen beschikbaar. Na zeven dagen vervalt de **Download**koppeling en moet u een nieuwe exportaanvraag indienen als u de gegevens opnieuw moet downloaden. Wanneer u een nieuwe gegevensexport start, vervallen eventuele bestaande downloads wanneer de nieuwe export is geslaagd.

De download is een ZIP-bestand dat het volgende bevat:

- Een map **Sjablonen** die uw Onboard-sjablonen in de Word-documentindeling bevat.

- Een map **Gidsen** die uw Onboard-gidsen in de Word-documentindeling bevat.

## <a name="see-also"></a>Zie ook

[Dynamics 365 Talent: Attract- en Dynamics 365 Talent: Onboard-apps buiten gebruik stellen](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)