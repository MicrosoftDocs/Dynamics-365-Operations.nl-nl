--- 
title: " Door machine learning aangestuurde productaanbevelingen configureren"
description: Deze procedure vernieuwt de gegevens in de Entiteitopslag die wordt gebruikt door het leersysteem van de machine dat productaanbevelingen genereert, en schakelt productaanbevelingen op POS-clients in.
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: c51c5f82efb50db1e238f4046506920975f33218
ms.contentlocale: nl-nl
ms.lasthandoff: 07/28/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a> Door machine learning aangestuurde productaanbevelingen configureren

[!include[task guide banner](../includes/task-guide-banner.md)]

Deze procedure vernieuwt de gegevens in de Entiteitopslag die wordt gebruikt door het leersysteem van de machine dat productaanbevelingen genereert, en schakelt productaanbevelingen op POS-clients in. Deze procedure gebruikt het demobedrijf USRT.

1. Ga naar Systeembeheer > Instellingen > Entiteitopslag.
2. Zoek en selecteer de gewenste record RetailSales in de lijst.
3. Klik op Vernieuwen.
4. Klik op OK.
5. Sluit de pagina.
6. Ga naar Detailhandel en commerce > Instelling van hoofdkantoor > Parameters > Detailhandelparameters.
7. Klik op het tabblad Machine Learning.
8. Selecteer Ja in het veld Productaanbevelingen inschakelen.
    * Als u het bericht "Kan de aanbevelingsmodellen niet ophalen" ziet, komt dat doordat u de entiteitopslag zeer onlangs hebt vernieuwd en het systeem mogelijk niet gereed is met het assimileren van de nieuwe gegevens. Wacht 2-3 uur en probeer het opnieuw.  
9. Klik op Opslaan.
10. Sluit de pagina.


