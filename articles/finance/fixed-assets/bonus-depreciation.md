---
title: Bonusafschrijving
description: In dit artikel vindt u een overzicht van de functionaliteit voor bonusafschrijving.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f811b913f751a860c21fc120b15bac406281d7f8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827021"
---
# <a name="bonus-depreciation"></a>Bonusafschrijving

[!include [banner](../includes/banner.md)]

In dit artikel vindt u een overzicht van de functionaliteit voor bonusafschrijving.

Voor bonusafschrijving kunt u gedurende het eerste jaar waarin het activum in gebruik wordt genomen en wordt afgeschreven, extra bedragen of bonussen afschrijven. De bonusafschrijving moet vóór andere afschrijvingsberekeningen worden toegepast. Daarom is het beste om bonusafschrijving met boeken te gebruiken als de functionaliteit Boeken naar grootboek is uitgeschakeld. U kunt de optie **Transacties verwijderen die niet zijn geboekt naar grootboek** gebruiken om historische transacties te verwijderen voor boeken die niet naar het grootboek boeken. U kunt bonusafschrijving later in de levenscyclus van het activum aanpassen door afschrijvingstransacties te verwijderen die eerder zijn geboekt. 

U kunt bonusafschrijving met behulp van het voorstelproces berekenen of zelf transacties voor bonusafschrijving maken. U kunt geen transacties voor bonusafschrijving maken als er afschrijvingstransacties of correctietransacties voor afschrijving voor dat activumboek zijn.

Wanneer u met het voorstelproces de bonusafschrijving berekent, worden alle bestaande bonustransacties in de berekening van de basis opgenomen. De berekening omvat ook alle vorige bonusafschrijvingen die u handmatig voor de activa hebt ingevoerd. 

Als er meerdere bonusafschrijvingen voor een activum worden uitgevoerd, wordt rekening gehouden met prioriteit. Elke bonus vermindert de activabasis voor de volgende bonus. Er wordt in de activabasis voor berekeningen van de bonusafschrijving geen rekening gehouden met de restwaarde. De afschrijvingsconventie geldt niet voor de bonusafschrijving. 

Bepaalde eigendommen komen momenteel in de Verenigde Staten in aanmerking als Section 179-eigendom. Door de Section 179-inhouding te gebruiken, kunt de gehele kosten van een bepaald eigendom of een gedeelte van de kosten, tot een bepaald bedrag, terugbetaald krijgen. U kunt de kosten terugbetaald krijgen door de kosten af te trekken in het jaar dat u het eigendom in gebruik hebt genomen.

## <a name="example"></a>Voorbeeld
De volgende bonusafschrijvingen zijn gekoppeld aan een activumboek:

-   **Section 179:** 1.000,00, Prioriteit 1
-   **Liberty Zone:** 30 procent, Prioriteit 2

De kosten van de verwerving van de activa zijn 5.000,00. Wanneer de bonusafschrijving wordt berekend, is het eerste bedrag van de bonusafschrijving € 1.000,00 voor de Section 179-afschrijving. 

Het volgende bedrag van de bonusafschrijving, voor de afschrijving van de Liberty Zone, wordt als volgt berekend: 

Verwervingskosten – 1.000 (Section 179-afschrijving) x 30 procent = € 1.200 

Als het bedrag van de bonusafschrijving meer is dan de overige verwervingskosten, is het bedrag van de bonusafschrijving het resultaat van de bonusafschrijving of de resterende verwervingskosten, welk bedrag van de twee het laagst is. 

Als de resterende verwervingskosten 0 (nul) of minder zijn, worden er geen transacties voor bonusafschrijving gegenereerd. 

Wanneer bonusafschrijving met behulp van het voorstelproces wordt berekend, wordt er een transactie voor bonusafschrijving voor alle van toepassing zijnde bonusafschrijvingsrecords berekend die aan het activumboek zijn gekoppeld. 

U kunt net zoveel bonusafschrijvingsrecords maken als u wilt. Als u deze records toewijst aan een activagroepsboek, worden deze records op het activumboek toegepast. 

Bonusafschrijving wordt als een percentage of een vast bedrag ingevoerd. Wanneer u afschrijvingsvoorstellen boekt, worden transacties voor bonusafschrijving los van de afschrijvingstransacties naar het boek geboekt.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]