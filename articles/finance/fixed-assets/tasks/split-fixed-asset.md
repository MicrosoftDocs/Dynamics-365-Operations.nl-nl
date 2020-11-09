---
title: Een vast activum splitsen
description: In dit onderwerp wordt uitgelegd hoe u een percentage van één activumboek opsplitst naar een nieuw activumboek.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40703622bc8c7a21451d31e7606596c5edbe90f7
ms.sourcegitcommit: 51e626675b0130fa32a84ce2d9119b68ea928018
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4000288"
---
# <a name="split-a-fixed-asset"></a>Een vast activum splitsen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een percentage van één activumboek opsplitst naar een nieuw activumboek. Het gebruikt de accountantsrol en USMF-demogegevens.

## <a name="create-a-new-fixed-asset"></a>Nieuwe vaste activa maken

1. Ga in het navigatievenster naar **Modules \> Vaste activa \> Vaste activa \> Vaste activa**.
2. Selecteer **Nieuw**.
3. Typ of selecteer een waarde in het veld **Groep vaste activa**. Noteer het vaste-activanummer om het later in het splitsingsproces te gebruiken.
4. Voer een waarde in het veld **Naam** in.
5. Het formulier sluiten.

## <a name="split-a-fixed-asset"></a>Een vast activum splitsen

Voordat een volledig afgeschreven activum wordt gesplitst, moet de status van het activaboek handmatig worden gewijzigd van **Afgesloten** in **Openstaand**. Deze stap is vereist omdat de status van het boek **Openstaand** moet zijn als u transacties voor het activum moet boeken (bijvoorbeeld voor een afboekingsverkoop). Nadat de status van het activaboek is gewijzigd, voert u de volgende stappen uit om het activum te splitsen.

1. Zoek en selecteer in de lijst de koppeling naar het vaste activum om te splitsen.
2. Selecteer **Boeken**. Selecteer het boek dat u wilt opsplitsen naar het nieuwe activum.
3. Selecteer **Functies**.
4. Selecteer **Vast activum splitsen**.
5. Typ of selecteer een waarde in het veld **Naar vaste activa**.
6. Selecteer in het veld **Boeken** de vervolgkeuzeknop om de zoekopdracht te openen.
7. Voer in het veld **Transactiedatum** een datum in.
8. Voer een getal in het veld **Percentage** in.
9. Typ of selecteer een waarde in het veld **Journaalnaam**.
10. Selecteer **OK**.

## <a name="post-the-journal-transaction"></a>De journaaltransactie boeken

1. Ga in het navigatievenster naar **Modules \> Vaste activa \> Journaalboekingen \> Vaste-activajournaal**.
2. Selecteer in de lijst het journaal dat met het splitsingsproces is gemaakt.
3. Selecteer **Regels**

    - Controleer de gemaakte journaalregels.
    - Een bijboekingscorrectietransactie wordt gemaakt voor het oorspronkelijke activum om de waarde te verlagen door het percentage dat is opgegeven tijdens het opsplitsingsproces.
    - Een bijboekingstransactie wordt gemaakt voor het nieuwe activum voor hetzelfde bedrag.

4. Selecteer **Boeken**.
