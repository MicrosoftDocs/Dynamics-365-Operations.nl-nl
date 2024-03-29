---
title: SQL Server Reporting Services configureren voor on-premises implementaties
description: Dit artikel biedt informatie over het configureren van SQL Server Reporting Services (SSRS) voor een on-premises implementatie.
author: PeterRFriis
ms.date: 06/23/2017
ms.topic: article
ms.prod: dynamics-365
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: peterfriis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.custom: 55651
ms.assetid: ''
ms.service: ''
ms.openlocfilehash: 9acb681ce07c3a7da82a630c7a87a4271a411b51
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275407"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a>SQL Server Reporting Services configureren voor on-premises implementaties

[!include [banner](../includes/banner.md)]

Volg de stappen in dit artikel om SQL Server Reporting Services (SSRS) te configureren voor uw implementatie van Microsoft Dynamics 365 Finance + Operations (on-premises).

1. Open de toepassing Reporting Services Configuration Manager.
2. Laat de standaard **servernaam**, gewoonlijk de naam van de huidige computer, en de **Naam van rapportserverexemplaar** **MSSQLSERVER** staan.
3. Klik op **Verbinden**.

    [![Configuratie verbinding Reporting Services.](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)

4. Klik op het tabblad **Serviceaccount** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![Tabbald Serviceaccount.](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)

5. Klik op het tabblad **Webservice-URL** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![Tabblad Webservice-URL.](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)

6. Klik op het tabblad **Database** en controleer of **Databasenaam** en **Referentie-instellingen** overeenkomen met de volgende afbeelding.

    > [!NOTE]
    > U moet een nieuwe database maken. Klik hiertoe op **Database wijzigen** en vervolgens controleert u of de naam van de nieuwe database als volgt luidt: **DynamicsAxReportServer**.

    [![Tabblad Database.](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)

7. Klik op het tabblad **Webportal-URL** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    > [!NOTE]
    > Klik op **Toepassen** om de Portal te maken en correct te configureren.

    [![Tabblad Webportal-url.](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)

    Nadat de Portal is geconfigureerd, komt het tabblad **Webportal** overeen met de volgende afbeelding.

    [![Tabblad Webportal.](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)

8. Klik op de URL van de rapporten om de webportal SQL Server Reporting Services weer te geven.
9. Wanneer u zich in de portal bevindt, maakt u een nieuwe map met de naam **Dynamics**.

    [![Dynamics-map.](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)

10. Klik in **Reporting Services Configuration Manager** op het tabblad **E-mailinstellingen** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![Tabblad E-mailinstellingen.](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)

11. Klik op het tabblad **Uitvoeringsaccount** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![Tabblad Uitvoeringsaccount.](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)

    Wijzig de standaardinstellingen op het tabblad **Coderingssleutels** niet.

    [![Tabblad Coderingssleutel.](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)

12. Klik op het tabblad **Abonnementen instellen** en controleer of de instellingen overeenkomen met de volgende afbeelding.

    [![tabblad Abonnementen instellen.](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)

    Wijzig de standaardinstellingen op het tabblad **Implementatie horizontaal schalen** niet.

    [![Tabblad Implementatie horizontaal schalen.](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)

    Wijzig de standaardinstellingen op het tabblad **Power BI-integratie** niet.

    [![Tabblad Power BI-integratie.](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)

13. Klik op **Afsluiten** om de **Reporting Services Configuration Manager** te sluiten.

    [![Reporting Services Configuration Manager sluiten.](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
