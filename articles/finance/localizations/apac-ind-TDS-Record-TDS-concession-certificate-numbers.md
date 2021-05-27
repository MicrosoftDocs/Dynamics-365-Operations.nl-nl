---
title: TDS-vrijstellingscertificaatnummers registreren
description: In dit onderwerp wordt uitgelegd hoe u de TDS-vrijstellingscertificaatnummers (belasting ingehouden op bron) vastlegt die aan leveranciers worden uitgegeven.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: f543adc8bab5ca224bdb672d6b3c282c2d8531d8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023136"
---
# <a name="record-tds-concession-certificate-numbers"></a>TDS-vrijstellingscertificaatnummers registreren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de TDS-vrijstellingscertificaatnummers (belasting ingehouden op bron) vastlegt die aan leveranciers worden uitgegeven.

1. Ga naar **Belasting \> Indirecte belastingen \> Bronbelasting \> Vrijstelling van bronbelasting**.
2. Selecteer in het veld **Belastingtype** de optie **TDS** om vrijstellingscertificaten voor het belastingtype TDS vast te leggen.
3. Selecteer **Alt+N** op het tabblad **Overzicht** om een regel te maken.

    [![Koptekst van de nieuwe regel](./media/apac-ind-TDS-34.png)](./media/apac-ind-TDS-34.png)

4. Selecteer in het veld **Bronbelastingcode** de TDS-belastingcode waarvoor de leveranciersvrijstellingscertificaten worden uitgegeven. In het veld **Bronbelastingcodenaam** wordt de naam van de TDS-belastingcode weergegeven.
5. Definieer in de velden **Begindatum** en **Einddatum** de geldigheidsduur voor het vrijstellingscertificaat dat de TDS-belastingcode gebruikt om TDS voor de leverancier op vrijstellingsbasis te berekenen.
6. Voer in het veld **Opmerkingen** eventuele opmerkingen in.
7. Voer in het veld **Sectie** de wettelijke sectiecode in waaronder het TDS-vrijstellingscertificaat wordt gebruikt.

    Als de sectiecode 197 is, wordt de waarde "A" weergegeven in zowel de kolom "Reden voor niet-inhouding/lagere inhouding" in Formulier 26Q als de kolom "Reden voor niet-inhouding/lagere inhouding/brutowinst (indien van toepassing)" in Formulier 27Q. Als de sectiecode 197A is, wordt op beide plaatsen de waarde "B" weergegeven.

8. Selecteer het sneltabblad **Certificaat** om TDS-vrijstellingscertificaatnummers voor leveranciers vast te leggen.
9. Selecteer in het veld **Leveranciersrekening** de leveranciersrekening waarvoor het TDS-vrijstellingscertificaat wordt uitgegeven.
10. Definieer in de velden **Begindatum** en **Einddatum** de geldigheidsduur voor het TDS-vrijstellingscertificaat.

    De berekening van TDS op vrijstellingsbasis is gebaseerd op de periode waarin het certificaat voor de leverancier wordt gemaakt.

11. Voer in het veld **Certificaat** het TDS-vrijstellingscertificaatnummer in.

    [![Sneltabblad Certificaat](./media/apac-ind-TDS-33.png)](./media/apac-ind-TDS-33.png)

12. Sluit de pagina.
