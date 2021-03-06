---
title: Prestaties optimaliseren door batchtaken na werktijd te plannen
description: In dit onderwerp wordt uitgelegd hoe u prestatieproblemen met Microsoft Dynamics 365 Human Resources kunt oplossen door de batchtaken met een lange uitvoeringsduur na werktijd in te plannen.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a5aeaeb7311d87a154882b7058b6da430900bd56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053462"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Prestaties optimaliseren door batchtaken na werktijd te plannen

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Uitgeven

De prestaties van Microsoft Dynamics 365 Human Resources kunnen problemen ondervinden als langlopende batchtaken tijdens normale werktijden worden uitgevoerd.

## <a name="resolution"></a>Oplossing

Plan de volgende batchtaken in na werktijd. We raden ook aan de frequentie te evalueren van batchtaken die regelmatig worden uitgevoerd. Verminder zo mogelijk het herhalingspatroon van de batchtaak. In veel gevallen is de standaardfrequentie voldoende.

De volgende batchtaken kunnen beter 's nachts of na werktijd worden uitgevoerd. Controleer ook de tijdzone voor deze herhalende batchtaken. Er zijn batchtaken die mogelijk een andere tijdzone gebruiken.

| Batchtaak | Standaard herhalingspatroon |
| --- | --- |
| Batchtaakhistorie opschonen | 1 keer per maand |
| Exportfasering opschonen | 1 keer per dag |
| Gemist synchronisatieverzoek Common Data Service-integratie | 1 keer per dag |
| Systeemtaak voor databasecompressie die regelmatig moet worden uitgevoerd buiten kantooruren | 1 keer per dag |
| Systeemtaak voor opnieuw samenstellen van de database-index die regelmatig moet worden uitgevoerd buiten kantooruren | 1 keer per dag |

1. Selecteer in Human Resources de optie **Systeembeheer**.

2. Zoek in de **Zoek**-balk naar een van de bovenstaande batchtaken.

3. Selecteer **Uitvoeren op de achtergrond** en selecteer **Terugkeerpatroon**.

   ![Stel terugkeerpatroon in](media/talent-batch-history-cleanup-recurrence.png)

4. Geef onder **Terugkeerpatroon definiëren** de **Begindatum** en **Begintijd** op die buiten werktijd of in het weekend vallen. Selecteer **Geen einddatum**. 

   ![Definieer begindatum en -tijd van het terugkeerpatroon](media/talent-batch-history-cleanup-define-recurrence.png)

5. Selecteer **OK**.

6. Wijzig zo nodig andere parameters onder **Uitvoeren op de achtergrond** en selecteer vervolgens **OK**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Prestaties optimaliseren met automatische opschoningstaken](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]