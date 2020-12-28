---
title: Een conformiteit maken en verwerken
description: In dit onderwerp wordt het beheer van non-conformiteiten, op basis van een bestaande kwaliteitsorder, beschreven.
author: perlynne
manager: tfehr
ms.date: 08/07/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bf20ed737707b7cf99023e3c78489caf4a68eab
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425707"
---
# <a name="create-and-process-a-conformance"></a>Een conformiteit maken en verwerken

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt het beheer van non-conformiteiten, op basis van een bestaande kwaliteitsorder, beschreven. U kunt deze registratie in het demobedrijf USMF uitvoeren en u kunt de voorgestelde waarden gebruiken. Doorgaans wordt deze procedure uitgevoerd door een kwaliteitsbewakingsmedewerker.  Voer als vereiste de instructies in [De kwaliteit van goederen inspecteren](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md) uit. Om de goedkeuring van een niet-conformering te verwerken moet aan de gebruiker die de taakregistratie uitvoert, een "Naam"-waarde zijn toegewezen op de pagina Gebruikers. Om de documentnotities te gebruiken moet de gebruiker ook Documentverwerking geactiveerd hebben in de gebruikersopties.


## <a name="select-a-quality-order"></a>Een kwaliteitsorder selecteren
1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Periodieke taken > Kwaliteitsbeheer > Kwaliteitsorders**.
2. Selecteer in de lijst de kwaliteitsorder die is gemaakt in [De kwaliteit van goederen inspecteren](https://github.com/MicrosoftDocs/Dynamics-365-Operations/blob/master/articles/supply-chain/inventory/tasks/inspect-quality-goods.md).  

## <a name="create-a-nonconformance"></a>Een non-conformiteit maken
1. Selecteer **Query's** in het actievenster.
2. Selecteer **Non-conformiteiten**.
3. Selecteer **Nieuw**.
4. Selecteer in de vervolgkeuzelijst van het veld **Probleemtype** het probleem dat tijdens het inspectieproces is aangetroffen.  
5. Selecteer **OK**.

## <a name="approvereject-a-nonconformance"></a>Een non-conformiteit goedkeuren/afwijzen
1. Selecteer **Functies**.
2. Selecteer **Non-conformiteit goedkeuren**. Keur voor dit voorbeeld de niet-conformering goed. Goedgekeurde non-conformiteiten kunnen aan gerelateerde bewerkingen worden gekoppeld om werk vast te leggen dat is uitgevoerd als onderdeel van de verwerking van de non-conformiteit en, zoals in dit onderwerp, de verwerking van correctiebehandeling.  
3. Selecteer **Ja**.

## <a name="create-a-correction-action"></a>Een correctieactie maken
1. Selecteer **Correcties**.
2. Selecteer **Nieuw**.
3. Selecteer in het veld **Personeelsnummer** van de nieuwe rij de gewenste record in de vervolgkeuzelijst.
4. Klik op **Selecteren**.
5. Selecteer **Bijvoegen**. Maak een notitie over de correctie. In dit voorbeeld is de actie contact met de leverancier op te nemen om de non-conformiteit te bespreken.  
6. Selecteer **Nieuw**.
7. Selecteer **Opmerking**. Afhankelijk van de rapportinstelling kunnen verschillende documenttypen worden afgedrukt in de rapporten die gerelateerd zijn aan beheer van non-conformiteiten.  
8. Typ een waarde in het veld **Beschrijving**.
9. Sluit de pagina.

## <a name="maintain-a-correction"></a>Een correctie onderhouden
1. Selecteer **Als voltooid markeren**.
2. Selecteer **OK**.
3. Sluit de pagina.

## <a name="close-a-nonconformance"></a>Een niet-conformering sluiten
1. Selecteer **Functies**.
2. Selecteer **Non-conformiteit afsluiten**.
3. Selecteer **Ja**.
4. Sluit de pagina's.
