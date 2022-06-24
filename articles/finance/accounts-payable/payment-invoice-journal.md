---
title: Een betalingsschema toepassen op het factuurjournaal
description: In dit artikel wordt beschreven hoe u een betaling aan het leveranciersfactuurjournaal toevoegt.
author: sunfzam
ms.date: 01/31/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: twheeloc
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-08-30
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: f3ae08ea46be66dd8bf26f7f91bd73f6c5b9192f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863125"
---
# <a name="apply-a-payment-schedule-to-the-invoice-journal"></a>Een betalingsschema toepassen op het factuurjournaal

[!include [banner](../includes/preview-banner.md)]

In Microsoft Dynamics 365 Finance versie 10.0.25 wordt nu een betalingsschema ondersteund in het **Leveranciersfactuurjournaal**.

Als u deze functionaliteit wilt gebruiken, moet u de functie **Betalingsschema toepassen op factuurjournaal** in Functiebeheer inschakelen.

Als de functie is ingeschakeld, wordt een nieuw **Betalingsschema**-veld toegevoegd aan de pagina **Factuurjournaal**. Wanneer u een factuurjournaalregel maakt, wordt het veld **Betalingsschema** bijgewerkt op de pagina **Factuurjournaal** als de betalingsvoorwaarden worden beheerd voor de leverancier en de betalingsvoorwaarden worden geselecteerd in het betalingsschema.

U kunt overeenkomstig uw bedrijfsbehoefte het betalingsschema wijzigen dat wordt gebruikt. Tijdens het boeken van het leveranciersfactuurjournaal worden openstaande transacties voor leveranciers gemaakt volgens het betalingsschema.

 - Als u meerdere openstaande leverancierstransacties wilt bekijken die zijn gegenereerd op basis van het betalingsschema, gaat u naar **Leveranciers \> Facturen \> Openstaande leveranciersfacturen** en voert u het factuurnummer of de leveranciersrekening in.
 - Als u het betalingsschema wilt controleren of configureren, gaat u naar **Leveranciers \>Betalingsinstelling \> Betalingsschema**.
 - Als u de betalingsvoorwaarden wilt configureren en een betalingsschema wilt toewijzen, gaat u naar **Leveranciers \> Betalingsinstelling \> Betalingstermijnen**.
 - Als u de betalingsvoorwaarden voor een leverancier wilt beheren, gaat u naar **Leveranciers \> Alle leveranciers**, selecteert u de leveranciersrekening en stelt u vervolgens op het tabblad **Betaling** het veld **Betalingstermijnen** in.

De functie voor betalingsschema's is ook beschikbaar in het proces **Leveranciersfactuurregister**. Als een betalingsschema is geselecteerd in het facturenregisterjournaal, worden meerdere leverancierbetalingsregels **niet** gegenereerd wanneer het facturenregister wordt geboekt. De leveranciersbetalingsregels worden gegenereerd als de factuur wordt goedgekeurd.

## <a name="limitation"></a>Beperking

Als het betalingsschema op de factuurkoptekst staat, is er voor een leveranciersfactuur in behandeling een geavanceerde pagina waarmee gebruikers de betalingsregels kunnen bewerken. (Gebruikers kunnen bijvoorbeeld de vervaldatum en waarde voor elke betalingsregel bewerken.) Betalingsregels die worden gegenereerd op basis van het factuurjournaal, krijgen de waarde van het betalingsschema.

Deze functionaliteit is in een toekomstige versie beschikbaar voor het **Leveranciersfactuurjournaal** en **Facturen in behandeling**.
