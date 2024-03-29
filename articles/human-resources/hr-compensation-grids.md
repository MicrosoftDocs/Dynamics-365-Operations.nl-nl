---
title: Compensatierasters instellen
description: Compensatierasters worden gebruikt om de salarisstructuren voor plannen voor vaste compensatie weer te geven of te onderhouden.
author: twheeloc
ms.date: 01/03/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HRCCompGrid, HRCCompGridView, HcmCompensationWorkspace
audience: Application User
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9119c15cf80b9ebb9bed83ac438f24249aa4aa2f
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/04/2022
ms.locfileid: "8691668"
---
# <a name="set-up-compensation-grids"></a>Compensatierasters instellen


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Compensatierasters worden gebruikt om de salarisstructuren voor plannen voor vaste compensatie weer te geven of te onderhouden. Compensatierasters kunnen worden gedeeld over meerdere plannen of worden gekopieerd bij het maken van een nieuw compensatieplan.  Voordat u een compensatieraster maakt, moet u de Niveaus en Referentiepunten instellen. In dit voorbeeld wordt een nieuw Cijfertype van compensatieraster gemaakt met demogegevens voor de Niveaus en Referentiepunten. Het bedrijf van de demogegevens dat wordt gebruikt om deze procedure te maken is USMF.


## <a name="set-up-information-about-the-compensation-grid"></a>Information over het compensatieraster instellen
1. Ga naar **Personeel** > **Compensatie** > **Vaste compensatie** > **Compensatierasters**.
2. Klik op **Nieuw**.
3. Typ een waarde in het veld **Raster**.
4. Typ een waarde in het veld **Beschrijving**.
5. Selecteer een optie in het veld **Type**.
6. Typ of selecteer een waarde in het veld **Referentie**-instelling.
7. Typ of selecteer een waarde in het veld **Valuta**.
8. Voer een datum in het veld **Begindatum** in.

## <a name="add-levels-to-the-compensation-structure"></a>Niveaus toevoegen aan de compensatiestructuur
1. Klik op **Compensatiestructuur**.
2. Markeer in de lijst de geselecteerde rij.
3. Typ of selecteer een waarde in het veld **Niveau**.
4. Klik op **Nieuw**.
5. Markeer in de lijst de geselecteerde rij.
6. Typ of selecteer een waarde in het veld **Niveau**.
7. Klik op **Nieuw**.
8. Markeer in de lijst de geselecteerde rij.
9. Typ of selecteer een waarde in het veld **Niveau**.
10. Klik op **Nieuw**.
11. Markeer in de lijst de geselecteerde rij.
12. Typ of selecteer een waarde in het veld **Niveau**.
13. Klik op **Nieuw**.
14. Markeer in de lijst de geselecteerde rij.
15. Typ of selecteer een waarde in het veld **Niveau**.

## <a name="fill-in-the-compensation-structure-with-values"></a>De compensatiestructuur vullen met waarden
1. Markeer in de lijst de geselecteerde rij.
    * Op dit moment kunnen de compensatiewaarden handmatig in elk veld in de tabel worden ingevoerd, of kunt u de functie Groepsgewijs wijzigen gebruiken om eenvoudig meerdere velden in te vullen en basisberekeningen uit te voeren.  
2. Klik op **Groepsgewijs wijzigen**.
    * Voor dit raster passen we eerst de waarde voor het middelpunt van eerste vlak toe op alle velden in de tabel. Dit wordt de basis voor de compensatiematrix.  
3. Selecteer een optie in het veld **Correctietype**.
4. Voer in het veld **Aanpassingsbedrag** een getal in.
5. Selecteer of deselecteer alle rijen in de lijst.
6. Klik op **Toepassen op raster**.
    * Nu gebruiken we de functie Groepsgewijs wijzigen om de bedragen in elk volgend niveau te verhogen met een bepaald percentage of bedrag. In dit voorbeeld krijgt elk cijfer een afstand van 12,5% tussen hun middelpunten.  
7. Selecteer een optie in het veld **Correctietype**.
8. Voer in het veld **Aanpassingsbedrag** een getal in.
9. Zoek en selecteer de gewenste record in de lijst.
10. Klik op **Toepassen op raster**.
    * Nu gebruiken we de functie Groepsgewijs wijzigen om de minimum- en maximumreferentiepunten voor elk niveau te corrigeren. Dit voorbeeld gebruikt een afstand van 50% zodat het minimumreferentiepunt met -20% worden gecorrigeerd en het maximumreferentiepunt met +20% wordt aangepast.  
11. Voer in het veld **Aanpassingsbedrag** een getal in.
12. Typ of selecteer een waarde in het veld **Referentiepunt**.
13. Selecteer of deselecteer alle rijen in de lijst.
14. Klik op **Toepassen op raster**.
15. Voer in het veld **Aanpassingsbedrag** een getal in.
16. Typ of selecteer een waarde in het veld **Referentiepunt**.
17. Selecteer of deselecteer alle rijen in de lijst.
18. Klik op **Toepassen op raster**.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
