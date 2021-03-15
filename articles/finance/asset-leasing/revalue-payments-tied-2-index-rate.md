---
title: Leasebetalingen die zijn gekoppeld aan een indextarief herwaarderen
description: Dit onderwerp beschrijft de correctie die wordt uitgevoerd om de aansprakelijkheid voor een RoU-activum te leasen wanneer variabele leasebetalingen veranderen vanwege een wijziging in het indextarief.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2cbe54ad92aff2f8a85e47301635fe4b6819e9a7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5012056"
---
# <a name="revalue-lease-payments-that-are-linked-to-an-index-rate"></a>Leasebetalingen die zijn gekoppeld aan een indextarief herwaarderen

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft de correctie die wordt uitgevoerd op de leaseverplichting van een RoU-activum wanneer variabele leasebetalingen veranderen vanwege een wijziging in het indextarief. De leaseverplichtingen en het RoU-activum worden gecorrigeerd met de nieuwe betalingsbedragen. Onder Accounting Standards Codification Topic 842 (ASC 842), de standaard in algemeen geaccepteerde boekhoudprincipes in de V.S. (VS GAAP), veranderen alleen de variabele betalingen wanneer betalingen toenemen of afnemen vanwege een wijziging in het indextarief, tenzij er extra wijzigingen zijn in de kasstromen. Deze aanvullende wijzigingen kunnen een wijziging in de leasevoorwaarden omvatten die gerelateerd is aan rentetarieven. Zie ASC 842-10-55-225 en alinea 42(b) van International Financial Reporting Standard 16 (IFRS 16) voor meer informatie.

## <a name="adjust-lease-payments"></a>Leasebetalingen aanpassen

Volg deze stappen om leasebetalingen die zijn gekoppeld aan een indextarief te herwaarderen.

1. Als u het leaseindex herwaarderingsproces wilt uitvoeren, gaat u naar **Activa leasen \> Periodiek \> Herwaardering indextarief**.

    De pagina **Herwaardering indextarief** wordt weergegeven en toont alle eerdere herwaarderingsprocessen van de leaseindex die zijn uitgevoerd. De informatie op deze pagina bevat de proces-id die is gegenereerd op basis van de instelling van de nummerreeks, de rechtspersoon, het aantal leaseboeken dat is aangepast, de totale aansprakelijkheidscorrectie voor de IFRS 16-leases en de totale variabele betalingen die zijn gecorrigeerd voor de ASC 842-leases.

2. Als u de herwaardering wilt uitvoeren, selecteert u in het actievenster de optie **Herwaardering leaseindex**.

    Het dialoogvenster **Parameters indexherwaardering** wordt geopend. Hier kunt u filteren en selecteren welke leases, leasegroepen of andere criteria moeten worden gebruikt wanneer u de leases selecteert die u wilt herwaarderen. Daarnaast kunt u op het tabblad **Op de achtergrond uitvoeren** het herwaarderingsproces voor de index instellen zodat het in een batch wordt uitgevoerd.

4. Selecteer de filters voor het selecteren van leases die in het achtergrondproces moeten worden opgenomen en selecteer vervolgens **OK**.

    Het dialoogvenster **Herwaardering indextarief preview** wordt geopend en toont de leases die worden geherwaardeerd. Ook worden de activa en aansprakelijkheidscorrecties of de variabele betalingscorrecties weergegeven.
    
5. Als u wilt voorkomen dat leases worden geherwaardeerd, selecteert u de leases die **moeten** worden geherwaardeerd. Als u geen leases selecteert, worden alle leases geherwaardeerd. Wanneer u klaar bent, selecteert u **OK** om de leasebetalingen te herwaarderen.
6. Als u de transacties wilt weergeven die zijn gemaakt voor een specifiek indexherwaarderingsproces, selecteert u de proces-id en selecteert u vervolgens **Transacties**.

    Er wordt een dialoogvenster geopend waarin de details worden weergegeven van de transacties die zijn gemaakt tijdens de verwerking.

> [!NOTE]
> Alleen leases met een herwaarderingsdatum die op of voor de systeemdatum ligt, kunnen worden geherwaardeerd. Alle leases met een herwaarderingsdatum die later is dan de systeemdatum worden automatisch door het systeem genegeerd.

## <a name="asc-842-leases--index-revaluation"></a>ASC 842-leases: indexherwaardering

Als u het effect van het leaseherwaarderingsproces op ASC 842-leases wilt bekijken, opent u het betalingsschema voor een lease. Op de pagina worden alleen de variabele betalingen weergegeven die zijn uitgevoerd op of nadat de herwaarderingsdatum is gewijzigd vanwege de indexherwaardering. De aflossings- en afschrijvingsschema's blijven ongewijzigd. Wanneer u een factuur maakt met een variabele betaling, wordt de variabele betaling gedebiteerd van de boekingsrekening voor variabele betalingen. Het variabele betalingsbedrag wordt ook toegevoegd aan de creditpost die rechtstreeks naar de leverancier wordt geboekt of wordt geboekt naar rekening voor te betalen facturen, afhankelijk van de instellingen van het leaseboek.

De regels van het betalingsschema op de pagina Leasedetails worden automatisch bijgewerkt met een nieuwe regel die het nieuwe indextarief aangeeft. Daarnaast wordt in een kolom weergegeven of de regel handmatig of via het indexherwaarderingsproces is gemaakt.

## <a name="ifrs-16-leases--index-revaluation"></a>IFRS 16-leases: indexherwaardering

Als u het effect van het leaseherwaarderingsproces op IFRS 16-leases wilt bekijken, opent u de leasedetails voro een gewijzigde lease. De velden **Leasetermijn** en **Economische levensduur activum** zijn bijgewerkt om het tijdsverloop vanaf de begindatum of wijzigingsdatum tot aan de herwaarderingsdatum weer te geven. Daarnaast zijn de betalingsschemaregels bijgewerkt met de nieuwe betalingen op de lease, het nieuwe indextarief en de manier waarop de regel is gemaakt.

U kunt het nieuw gegenereerde betalingsschema bekijken dat begint op de herwaarderingsdatum en het totale bijgewerkte betalingsbedrag weergeeft. Er is ook een nieuw afschrijvingsschema voor de leaseverplichtingen en een schema voor activumafschrijvingen gemaakt om het aangepaste betalingsschema weer te geven.

De journaalboeking heeft de correctiejournaalpost automatisch geboekt naar de rekening voor de wijziging in de leasebetalingen die betrekking hebben op de indexherwaardering.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]