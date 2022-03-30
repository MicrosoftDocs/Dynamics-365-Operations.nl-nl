---
title: Certificaatnummers voor terugvorderbare TDS registreren
description: In dit onderwerp wordt uitgelegd hoe u de pagina Certificaten voor terugvordering kunt gebruiken om de nummers en datums voor TDS-certificaten te registreren die zijn ontvangen voor een bepaalde leverancier, klant of grootboek.
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 8fa4d1200818b4657b044a376ebb292426250ae1
ms.sourcegitcommit: 6dc2b877cf8ea9185a07964ec05c5ddb7a78471b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2022
ms.locfileid: "8407735"
---
# <a name="record-tds-recoverable-certificate-numbers"></a>Certificaatnummers voor terugvorderbare TDS registreren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u de pagina **Certificaten voor terugvordering** kunt gebruiken om de nummers en datums voor TDS-certificaten te registreren die zijn ontvangen voor een bepaalde leverancier, klant of grootboek. Als u de TDS-certificaatnummers en -datums die zijn geregistreerd voor TDS-transacties op deze pagina wilt bijwerken, gebruikt u de pagina **Certificaat bijwerken** (**Grootboek \> Periodiek \> Bronbelasting \> Certificaat bijwerken**). Wanneer u klaar bent met het bijwerken van TDS-certificaatnummers, sluit u deze.

Volg deze stappen om de certificaatnummers en -datums voor TDS te registreren.

1. Ga naar **Belasting \> Indirecte belasting \> Bronbelasting \> Certificaten voor terugvordering**.

    [![Pagina Certificaten voor terugvordering.](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png) 

2. Selecteer **TDS** in het veld **Belastingtype** op de pagina **Certificaten voor terugvordering**.
3. Selecteer **Nieuw** om een record te maken.
4. Voer in het veld **Certificaatnummer** het TDS-certificaatnummer in.
5. Selecteer in het veld **Rekeningtype** het type rekening waar het TDS-certificaat voor wordt ontvangen: **Leverancier**, **Klant** of **Grootboek**.
6. Selecteer in het veld **Rekening** het rekeningnummer van de leverancier, de klant of het grootboek, afhankelijk van het rekeningtype dat u hebt geselecteerd. Het veld **Naam** geeft de naam van de leveranciers-, klant- of grootboekrekening weer.
7. Voer in het veld **Certificaatbedrag** het bedrag in voor het TDS-certificaat.
8. Voer in het veld **Datum** de certificaatdatum in voor het certificaatnummer.
9. Selecteer **Aanvragen** om de pagina **Certificaattransacties te openen**, waar u de TDS-transacties kunt bekijken waarvoor het TDS-certificaatnummer en de TDS-datum zijn bijgewerkt. Deze informatie kan worden bijgewerkt op de pagina **Certificaat bijwerken** (**Belasting \> Aangiften \> Bronbelasting \> Certificaat bijwerken**).

    Op de pagina **Certificaat bijwerken** wordt de volgende informatie voor elke TDS-transactie weergegeven:

    - **Datum**: de boekingsdatum van de TDS-transactie.
    - **Boekstuk**: het boekstuknummer van de TDS-transactie.
    - **Bron**: de module waarin de TDS-transactie is gemaakt.
    - **Rekening**: het leveranciers-, klant- of grootboekrekeningnummer waarvoor de TDS-transactie is gemaakt.
    - **Naam**: de naam van de leveranciers-, klant- of grootboekrekening waarvoor de TDS-transactie is gemaakt.
    - **Bedrag**: het factuurbedrag waarover de TDS is berekend.
    - **Belastingbedrag**: het TDS-belastingbedrag dat voor de transactie is berekend.
    - **Certificaatdatum**: de datum van het TDS-certificaat die is bijgewerkt voor de TDS-transactie.
    - **Certificaatnummer**: het TDS-certificaatnummer dat is bijgewerkt voor de TDS-transactie.

10. Schakel op de pagina **Certificaten voor terugvordering** het selectievakje **Afgesloten** in om het TDS-certificaatnummer te sluiten nadat u het hebt bijgewerkt voor TDS-transacties op de pagina **Certificaat bijwerken**.

    Als u het selectievakje **Afgesloten** voor alle records op de pagina wilt inschakelen, selecteert u **Alles markeren**.

    > [!NOTE]
    > TDS-certificaatnummers waar het selectievakje **Afgesloten** voor is ingeschakeld, zijn niet beschikbaar op de pagina **Certificaat bijwerken**.
