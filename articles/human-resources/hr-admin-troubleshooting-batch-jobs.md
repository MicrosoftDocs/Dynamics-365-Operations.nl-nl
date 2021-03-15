---
title: Prestaties optimaliseren door batchtaken na werktijd te plannen
description: In dit onderwerp wordt uitgelegd hoe u prestatieproblemen met Microsoft Dynamics 365 Human Resources kunt oplossen door de batchtaken met een lange uitvoeringsduur na werktijd in te plannen.
author: andreabichsel
manager: tfehr
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 219537aab2015469b6ca6ebed5c00af0190c5187
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112108"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Prestaties optimaliseren door batchtaken na werktijd te plannen

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