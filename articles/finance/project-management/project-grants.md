---
title: Projectsubsidies
description: In dit onderwerp wordt uitgelegd hoe u een subsidie maakt of wijzigt.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: f4f7d347dab9f02fc474656e2f4cfba8e374480d
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282820"
---
# <a name="project-grants"></a>Projectsubsidies

[!include [banner](../includes/banner.md)]

Een subsidie is een schenking van geld voor een specifiek doel of project. Gewoonlijk zijn er beperkingen op hoe een subsidie kan worden uitgegeven. In Projectbeheer en boekhouding kunt u subsidies invoeren en bijhouden en hun relaties met projecten en projectcontracten definiëren. In dit formulier kunt u bijvoorbeeld de volgende taken uitvoeren:

- Koppel subsidies aan projecten en financieringsbronnen via koppelingen naar de pagina's **Project** en **Projectcontractgegevens**.
- Voer wijzigingen in een subsidie in en houdt ze bij terwijl deze van de ene status naar de andere wordt verplaatst.
- Voer kosten, vereiste bedragen en toegekende bedragen in en houdt deze bij.
- Maak hoofdsubsidies en koppel hieraan subsubsidies.

U kunt een subsidie maken door alle details in te voeren in een nieuwe registratie of u kunt de details kopiëren op basis van een bestaande subsidie.

## <a name="create-a-new-grant"></a>Een nieuwe subsidie maken

1. Ga naar **Projectbeheer en boekhouding** \> **Subsidies** \> **Subsidies**.
2. Selecteer **Nieuw** \> **Subsidie**.
3. Voer op de pagina Subsidiegegevens op het sneltabblad **Algemeen** in het veld **Subsidie-id** een alfanumerieke id voor de subsidie in.
4. Geef in het veld **Subsidienaam** een unieke naam voor de subsidie op.
5. Voeg in het veld **Omschrijving** details toe over de nieuwe subsidie.

    De meeste andere velden op de pagina zijn optioneel en u kunt zo weinig of zoveel informatie invoeren als u wilt.

    De volgende lijst bevat de informatie die is opgegeven op elk sneltabblad van de pagina Subsidiegegevens:

    - **Algemeen**: voer de naam, de status, de omschrijving, het doel en het bedrag van de subsidie in.
    - **Contactgegevens**: voer details in over de personeelsleden, de afdeling die de subsidie beheert en over de subsidieklant of organisatie die de subsidie uitkeert. U kunt ook aangeven of uw organisatie een doorgeeftentiteit is die de subsidie ontvangt en deze vervolgens aan een andere ontvanger doorgeeft. Selecteer **Toevoegen** om contactgegeven toe te voegen, zoals telefoonnummers en e-mailadressen voor de organisatie die de subsidie uitkeert.
    - **Datums en deadlines**: voer datums in die aan de subsidie en de subsidieaanvraag zijn gekoppeld. Voorbeelden zijn de vervaldatum van de toepassing, de verzenddatum en de datum waarop de subsidie wordt goedgekeurd of afgewezen.
    - **Gekoppelde projecten en projectcontracten**: u kunt alleen informatie over dit sneltabblad invoeren als het veld **Subsidiestatus** op het sneltabblad **Algemeen** is ingesteld op **Actief** of **Toegewezen**. Maak een keuze uit de volgende opties om de gerelateerde taak te voltooien:

        - **Financieringsbron toevoegen**: een nieuwe financieringsbron toevoegen voor de subsidie. U kunt meteen alle gegevens invoeren, of u kunt de standaardgegevens gebruiken en deze later bijwerken.
        - **Projectcontract toevoegen**: projectcontractgegevens toevoegen of bijwerken.
        - **Project toevoegen**: projectgegevens toevoegen of bijwerken.

    - **Instellen**: details invoeren over overeenkomende fondsen, als deze informatie verplicht is. Veel organisaties die subsidies verlenen, vereisen dat ontvangers een bepaalde bedrag eigen geld of middelen uitgeeft in overeenstemming met het bedrag dat in de subsidie wordt toegekend. In het **veld Lokaal project of tracerings-id** kunt u een id invoeren die verschilt van de project-id.

        > [!NOTE]
        > Als een deel van de subsidie aan een andere organisatie wordt toegekend, stelt u de optie **Subsusidiegever** in op **Ja**. Voor subsidies die in de Verenigde Staten worden toegekend, kunt u opgeven of een subsidie onder het mandaat van een staat of onder een federaal mandaat wordt toegekend.

    - **Verminderingsdetails**: voeg informatie toe over hoe vaak subsidiefondsen kunnen worden opgenomen, gefactureerd of uitgegeven in of werk deze bij.

## <a name="create-a-new-grant-from-a-copy"></a>Een nieuwe subsidie maken op basis van een kopie

1. Ga naar **Projectbeheer en boekhouding** \> **Subsidies** \> **Subsidies**.
2. Selecteer **Nieuw** \> **Kopie van subsidie**.
3. Voer een alfanumerieke id en een naam in voor de nieuwe subsidie en selecteer vervolgens **OK**.
4. Controleer op de pagina Subsidiegegevens de details van de gekopieerde subsidie en breng de vereiste wijzigingen aan. De meeste velden op de pagina zijn optioneel.

## <a name="view-or-modify-grant-details"></a>Subsidiegegevens weergeven of wijzigen

1. Ga naar **Projectbeheer en boekhouding** \> **Subsidies** \> **Subsidies**.
2. Selecteer de subsidie die aangepast moet worden.
3. Selecteer in het actievenster op het tabblad **Subsidie** in de groep **Onderhouden** de optie **Bewerken**.
4. Controleer de subsidiegegevens en breng eventueel vereiste wijzigingen aan.
