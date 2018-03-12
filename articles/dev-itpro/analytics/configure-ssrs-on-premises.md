---
title: SQL Server Reporting Services configureren voor een on-premises implementatie
description: Dit onderwerp biedt informatie over het configureren van SQL Server Reporting Services (SSRS) voor een on-premises implementatie.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a1f11641a2ec055cfaa0157ac9a40525daa4006
ms.contentlocale: nl-nl
ms.lasthandoff: 11/03/2017

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a>SQL Server Reporting Services configureren voor een on-premises implementatie

[!include[banner](../includes/banner.md)]

Gebruik de stappen in dit onderwerp voor het configureren van SQL Server Reporting Services (SSRS) voor uw implementatie van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises).

1. Open de toepassing Reporting Services Configuration Manager.
2. Laat de standaard **servernaam**, gewoonlijk de naam van de huidige computer, en de **Naam van rapportserverexemplaar** **MSSQLSERVER** staan. 
3. Klik op **Verbinden**.
   
   [![Configuratie verbinding Reporting Services](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)
   
4. Klik op het tabblad **Serviceaccount** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![Tabbald Serviceaccount](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)
    
5. Klik op het tabblad **Webservice-URL** en controleer of de instellingen overeenkomen met de volgende afbeelding. 

    [![Tabblad Webservice-URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png) 
    
6. Klik op het tabblad **Database** en controleer of **Databasenaam** en **Referentie-instellingen** overeenkomen met de volgende afbeelding. **Opmerking:** U moet een nieuwe database maken. Klik hiertoe op **Database wijzigen** en vervolgens controleert u of de naam van de nieuwe database als volgt luidt: **DynamicsAxReportServer**.

    [![Tabblad Database](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)
    
7. Klik op het tabblad **Webportal-URL** en controleer of de instellingen overeenkomen met de volgende afbeelding. **Opmerking:** Klik op **Toepassen** om de Portal te maken en correct te configureren.

    [![Tabblad Webportal-url](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)
    
  Nadat de Portal is geconfigureerd, komt het tabblad **Webportal** overeen met de volgende afbeelding.
    [![Tabblad Webportal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)
    
8. Klik op de URL van de rapporten om de webportal SQL Server Reporting Services weer te geven. 
9.  Wanneer u zich in de portal bevindt, maakt u een nieuwe map met de naam **Dynamics**.

    [![Dynamics-map](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)
    
10. Klik in **Reporting Services Configuration Manager** op het tabblad **E-mailinstellingen** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![Tabblad E-mailinstellingen](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)
    
11. Klik op het tabblad **Uitvoeringsaccount** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![Tabblad Uitvoeringsaccount](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)
    
  Wijzig niet de standaardinstellingen op het tabblad **Coderingssleutel**. [![Tabblad Coderingssleutel](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)
    
12. Klik op het tabblad **Abonnementen instellen** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![tabblad Abonnementen instellen](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)
    
  Wijzig niet de standaardinstellingen op het tabblad **Implementatie horizontaal schalen**. [![Tabblad Implementatie horizontaal schalen](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)
    
  Wijzig niet de standaardinstellingen op het tabblad **Power BI-integratie**. [![Tabblad Power BI-integratie](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png) 
    
13. Klik op **Afsluiten** om de **Reporting Services Configuration Manager** te sluiten.

    [![Reporting Services Configuration Manager sluiten](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)
    


