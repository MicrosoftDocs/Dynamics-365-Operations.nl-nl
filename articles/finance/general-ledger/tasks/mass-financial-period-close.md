---
title: Massale sluiting van financiële periode
description: In dit onderwerp procedure ziet u hoe u een periode in de wachtstand plaatst of definitief afsluit voor meer dan één rechtspersoon tegelijk.
author: aprilolson
ms.date: 08/16/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCalendar, LedgerPeriodModuleAccessControlUpdate, SysLookupPicklist, LedgerFiscalCalendarPeriodStatus
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 54a5b16f731e850b468ea2e05e47b47774e45838
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826493"
---
# <a name="mass-financial-period-close"></a>Massale sluiting van financiële periode

[!include [banner](../../includes/banner.md)]

In dit onderwerp procedure ziet u hoe u een periode in de wachtstand plaatst of definitief afsluit voor meer dan één rechtspersoon tegelijk. Daarnaast ziet u hoe u een gebruikersgroep kunt blokkeren voor het boeken naar specifieke modules.

1. Ga in het navigatievenster naar **Modules > Grootboek > Afgesloten periode > Grootboekkalenders**. Merk op dat de getoonde lijst van rechtspersonen afhankelijk is van de fiscale kalender die is geselecteerd op de pagina. Alleen rechtspersonen die de geselecteerde fiscale kalender gebruiken, worden weergeven.
2. Selecteer **Bewerken**.
3. Selecteer de periode waarvan u de status wilt wijzigen.
4. Selecteer de rechtspersonen waarvan u de status wilt bijwerken. U kunt alle entiteiten snel selecteren door het selectievakje links boven in het raster in te schakelen.  
5. Selecteer **Moduletoegang bijwerken** om de toegang voor boeken naar een geselecteerde module te definiëren. U kunt de modulestatus ook één voor één bijwerken, door de records in het raster te bewerken. De knop is handig wanneer u snel meerdere rechtspersoonrecords wilt bijwerken.  
6. Selecteer in de module **Toepassing** de module waarvan u de status wilt bijwerken. Klik op **Selecteren**.
7. Selecteer bij **Toegangsniveau** een waarde: **Alle**, **Geen** of een specifieke gebruikersgroep. Klik op **Selecteren**. Alle geeft aan dat alle gebruikers met bewerkingsmachtiging naar de module kunnen boeken als de periode is geopend. Geen geeft aan dat gebruikers niet naar de module kunnen boeken als de periode open is. Een specifieke gebruikersgroep geeft aan dat alleen gebruikers in de groep naar de module mogen boeken als de periode is geopend.  
8. Selecteer **Bijwerken**.
9. Selecteer een andere periode waarvan u de status wilt bijwerken.
10. Selecteer de rechtspersonen waarvan u de periodestatus wilt bijwerken.
11. Selecteer **Periodestatus bijwerken** en stel de status in op **In wachtstand**, **Open** of **Definitief afgesloten**. **Open** geeft aan dat er naar de periode kan worden geboekt, mits de gebruiker toegang heeft. Bij **In wachtstand** kan er niet worden geboekt naar de periode, maar kan de periode wel worden heropend. Bij **Definitief afgesloten** is de periode afgesloten en kan deze niet meer worden geopend. Aanpassingen kunnen niet worden geboekt. Het is raadzaam om een periode pas op **Definitief afgesloten** in te stellen wanneer alle correcties en audits zijn voltooid.  
12. Selecteer **Bijwerken**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]