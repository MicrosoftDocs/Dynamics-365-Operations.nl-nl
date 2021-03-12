---
title: Een journaalboeking maken met een sjabloon
description: Geboekte journaalboekstuk kunnen als boekstuksjablonen worden opgeslagen en toegepast in een nieuw journaalboekstuk.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 234cfb98cc07f6c8c81821584e4e1d509d033477
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4988569"
---
# <a name="create-a-journal-entry-using-template"></a>Een journaalboeking maken met een sjabloon

[!include [banner](../../includes/banner.md)]

Geboekte journaalboekstuk kunnen als boekstuksjablonen worden opgeslagen en toegepast in een nieuw journaalboekstuk. Bij deze procedure wordt het demobedrijf USMF gebruikt.

1. Ga naar **Navigatievenster > Modules > Grootboek > Journaalboekingen > Algemene journalen**.
2. Klik in het **actievenster** op **Nieuw**. Deze procedure start met het maken en boeken van een journaalboekstuk, maar elk eerder geboekt journaalboekstuk kan als sjabloon worden opgeslagen.  
3. Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.
4. Zoek en selecteer het gewenste record in de lijst.
5. Klik in de lijst op de koppeling in de geselecteerde rij.
6. Klik op **Regels**.
7. Typ een waarde in het veld **Rekeningtype**.
8. Typ een waarde in het veld **Beschrijving**.
9. Typ een waarde in het veld **Debet**.
10. Klik op **Nieuw**.
11. Typ een waarde in het veld **Rekeningtype**.
12. Typ een waarde in het veld **Beschrijving**.
13. Typ een waarde in het veld **Debet**.
14. Klik op **Nieuw**.
14. Geef in het veld **Rekening** de gewenste waarden op.
15. Typ een waarde in het veld **Beschrijving**.
16. Voer in het veld **Credit** een waarde in om het boekstuk in balans te brengen.
17. Klik in het **actievenster** op **Boeken**.
18. Klik op **Functies**.
19. Klik op **Boekstuksjabloon opslaan**.
20. In deze procedure wordt uitgegaan van een sjabloontype **Procent**. Klik op OK.
    - Procent: de bedragen in het boekstuk worden omgezet in percentagefactoren, waardoor elk bedrag kan worden toegepast als de sjabloon voor het boekstuk wordt geselecteerd.
    - Bedrag: de werkelijke bedragen worden opgeslagen en toegepast.  
21. Klik op **Algemene journalen**.
22. Klik op **Nieuw**.
23. Klik in het veld **Naam** op de vervolgkeuzeknop om de zoekopdracht te openen.
24. Klik in de lijst op de koppeling in de geselecteerde rij.
25. Klik op **Regels**.
26. Klik op **Functies**.
27. Klik op **Boekstuksjabloon selecteren**.
28. Zoek de sjabloon die u eerder hebt gemaakt. Klik op **OK**. Mogelijk moet u op **Vorige stap** klikken en vervolgens de juiste sjabloon selecteren als andere sjablonen bestaan.  
29. Voer in het veld **Bedrag** het bedrag in dat op het boekstuk moet worden toegepast. Het veld **Bedrag** wordt alleen weergegeven als de boekstuksjabloon van het type Procent is.  
30. Klik op **OK**.

