---
title: Instellen van gegevens voor TDS-groep, PAN en TAN voor klanten en leveranciers
description: In dit onderwerp wordt uitgelegd hoe u gegevens kunt instellen over de TDS-groep (belasting ingehouden op bron), het permanente rekeningnummer (PAN) en het belastingrekeningnummer (TAN) voor leveranciers en klanten.
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
ms.openlocfilehash: b736838f1743a39d1f899f2679a31a2c0fe9a2b31e03b29d22af821314f329c9
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6745743"
---
# <a name="tds-group-pan-and-tan-information-setup-for-vendors-and-customers"></a>Gegevens instellen voor TDS-groep, PAN en TAN voor klanten en leveranciers

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u gegevens kunt instellen over de TDS-groep (belasting ingehouden op bron), het permanente rekeningnummer (PAN) en het belastingrekeningnummer (TAN) voor leveranciers en klanten.

1. Ga naar **Leveranciers \> Leveranciers \> Alle leveranciers** of **Klanten \> Klanten \> Alle klanten**.

    [![Pagina Alle leveranciers.](./media/apac-ind-TDS-55.png)](./media/apac-ind-TDS-55.png)

2. Selecteer in het actievenster **Nieuw** om een leverancier of klant te maken en voer de vereiste gegevens in. U kunt ook een bestaande leverancier of klant selecteren.
3. Stel op het sneltabblad **Factuur en levering** in de sectie **Bronbelasting** de optie **Bronbelasting berekenen** in op **Ja** om bronbelasting, TDS (belasting ingehouden op bron) of TCS (belasting geïnd aan bron) voor de leverancier of klant te berekenen.
4. TDS voor een inkoopfactuur wordt berekend op basis van de standaard-TDS-groep die voor de leverancier of klant is gedefinieerd. Selecteer de standaardgroep voor TDS in het veld **TDS-groep**.

    > [!NOTE]
    > Wanneer u een TDS-groep selecteert in het veld **TDS-groep**, worden de velden van de **Bronbelastinggroep** en de **TCS-groep** niet meer beschikbaar.

5. Selecteer in de sectie **PAN-gegevens** van het sneltabblad **Belastinginformatie** in het veld **Status** de status van het permanente rekeningnummer voor de leverancier of klant:

    - **Niet beschikbaar**: de leverancier of klant heeft geen PAN.
    - **Ontvangen**: de leverancier of klant heeft een PAN.
    - **Aangevraagd**: de leverancier of klant heeft een PAN aangevraagd.
    - **Ongeldig**: de leverancier of klant heeft een PAN, maar deze is niet geldig.

6. Als u **Ontvangen** hebt geselecteerd in het veld **Status** om aan te geven dat de leverancier of klant een PAN heeft, voert u de PAN in het veld **Nummer** in. De PAN moet bestaan uit vijf alfabetische tekens, vervolgens vier numerieke tekens en daarna één alfabetisch teken. Dit is een voorbeeld: **ABCDE1260A**.
7. Als u **Aangevraagd** hebt geselecteerd in het veld **Status** om aan te geven dat de leverancier of klant een PAN heeft aangevraagd, voert u het verwijzingsnummer in het veld **Verwijzingsnummer** in.
8. Selecteer in het veld **Soort belastingplichtige** de soort belastingplichtige waar de leverancier of klant toe hoort:

    - Bedrijf
    - HUF
    - Firma
    - Afzonderlijk
    - AOP
    - BOI
    - Lokale dienst
    - Andere

    [![Sneltabblad Belastinginformatie.](./media/apac-ind-TDS-56.png)](./media/apac-ind-TDS-56.png)

9. Selecteer vervolgens in het actievenster op het tabblad **Leverancier** in de groep **Registratie** de optie **Registratie-id's** om de pagina **Adressen beheren** te openen.
10. Selecteer op de pagina **Adressen beheren** op het sneltabblad **Belastinginformatie** de optie **Toevoegen** of **Bewerken** om de pagina **Belastinginformatie beheren** te openen, waar u de belastingregistratie-invoer kunt onderhouden.
11. Voer op de pagina **Belastinginformatie beheren** op het sneltabblad **Bronbelasting** in het veld **Belastingrekeningnummer (TAN)** het TAN in. De TAN moet bestaan uit vier alfabetische tekens, vervolgens vijf numerieke tekens en daarna één alfabetisch teken. Dit is een voorbeeld: **AFGH54821T**.
12. Sluit de pagina.
