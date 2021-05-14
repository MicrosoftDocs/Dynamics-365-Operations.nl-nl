---
title: Veelgestelde vragen over financiële rapportage
description: In dit onderwerp vindt u antwoorden op eerdere vragen van andere gebruikers over financiële rapportage.
author: jiwo
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 023354b0e2973f63411bf81cbeb0344333c49112
ms.sourcegitcommit: d63e7e0593084a61362a6cad3937b1fd956c384f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923020"
---
# <a name="financial-reporting-faq"></a>Veelgestelde vragen over financiële rapportage 

Dit onderwerp biedt antwoorden op veelgestelde vragen over financiële rapportage. 

## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Hoe beperk ik de toegang tot een rapport met structuurbeveiliging?

In het volgende voorbeeld ziet u hoe u de toegang tot een rapport beperkt in de structuurbeveiliging.

Het USMF-demobedrijf heeft een balansrapport waartoe niet alle gebruikers van Financiële rapportage toegang moeten krijgen. Als u de toegang wilt beperken, kunt u structuurbeveiliging gebruiken om de toegang tot één rapport te beperken, zodat alleen bepaalde gebruikers toegang hebben tot het rapport. Volg deze stappen om de toegang te beperken: 

1. Meld u aan bij Financial Reporter Report Designer.
2. Maak een nieuwe structuurdefinitie. Ga naar **Bestand > Nieuw > Structuurdefinitie**.
3. Dubbelklik op de regel **Samenvatting** in de kolom **Beveiliging van eenheid**.
4. Klik op **Gebruikers en groepen**.  
5. Selecteer de gebruikers of groepen die toegang tot dit rapport moeten hebben. 
6. Selecteer **Opslaan**.
7. Voeg in de rapportdefinitie uw nieuwe structuurdefinitie toe.
8. Selecteer **Instelling** in de structuurdefinitie. Selecteer onder **Rapporteringseenheden selecteren** de optie **Alle eenheden opnemen**.

## <a name="how-do-i-identify-which-accounts-do-not-match-my-balances"></a>Hoe bepaal ik welke rekeningen niet met mijn saldi overeenkomen?

Als u een niet-salderend rapport hebt, kunt u het volgende doen om die rekeningen en afwijkingen te identificeren. 

**Financial Reporter Report Designer**
1. Maak een nieuwe rijdefinitie in Financial Reporter Report Designer. 
2. Selecteer **Bewerken > Rijen invoegen uit dimensies**.
3. Selecteer **MainAccount**.  
4. Selecteer **OK**.
5. Sla de rijdefinitie op.
6. Een nieuwe kolomdefinitie maken
7. Maak een nieuwe rapportdefinitie.
8. Selecteer **Instellingen** en schakel deze optie uit.  
9. Genereer het rapport. 
10. Exporteer het rapport naar Microsoft Excel.

**Dynamics 365 Finance** 
1. Ga in Dynamics 365 Finance naar **Grootboek > Query's en rapporten > Proefbalans**.
2. Stel de volgende parameters in:
   - **Begindatum**: voer het begin van het boekjaar in.
   - **Einddatum**: voer de datum in waarvoor u het rapport genereert.
   - **Financiële dimensie**: stel dit veld in op **Hoofdrekening ingesteld**.
 3. Selecteer **Berekenen**.
 4. Exporteer het rapport naar Microsoft Excel.

U kunt de gegevens nu uit het Excel-rapport in Financial Reporter kopiëren naar het proefbalansrapport zodat u de kolommen **Eindsaldo** kunt vergelijken.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]