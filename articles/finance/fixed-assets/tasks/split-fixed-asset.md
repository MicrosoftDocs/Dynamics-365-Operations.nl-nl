---
title: Een vast activum splitsen
description: In dit artikel wordt uitgelegd hoe u een percentage van één activumboek opsplitst naar een nieuw activumboek.
author: moaamer
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0d7fe30702717f960a42fb2a118e0d12587024f5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8880783"
---
# <a name="split-a-fixed-asset"></a>Een vast activum splitsen

[!include [banner](../../includes/banner.md)]

In dit artikel wordt uitgelegd hoe u een percentage van één activumboek opsplitst naar een nieuw activumboek. 

## <a name="create-a-new-fixed-asset"></a>Nieuwe vaste activa maken

1. Ga in het navigatievenster naar **Modules \> Vaste activa \> Vaste activa \> Vaste activa**.
2. Selecteer **Nieuw**.
3. Typ of selecteer een waarde in het veld **Groep vaste activa**. Noteer het vaste-activanummer om het later in het splitsingsproces te gebruiken.
4. Voer een waarde in het veld **Naam** in.
5. Het formulier sluiten.

## <a name="split-a-fixed-asset"></a>Een vast activum splitsen

Voordat een volledig afgeschreven activum wordt gesplitst, moet de status van het activaboek handmatig worden gewijzigd van **Afgesloten** in **Openstaand**. Deze stap is vereist omdat de status van het boek **Openstaand** moet zijn als u transacties voor het activum moet boeken (bijvoorbeeld voor een afboekingsverkoop). U moet ook de parameter **Meerdere transacties binnen één boekstuk toestaan** inschakelen op het tabblad **Algemeen** van de pagina **Grootboekparameters**. Nadat de boekingsstatus van het activum is gewijzigd en er meerdere transacties binnen één boekstuk zijn toegestaan, voert u de volgende stappen uit om het activum te splitsen.

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
