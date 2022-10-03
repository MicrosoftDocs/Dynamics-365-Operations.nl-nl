---
title: Configuratie voor Finance Insights
description: In dit artikel worden de configuratiestappen beschreven die ervoor zorgen dat uw systeem de mogelijkheden gebruikt die beschikbaar zijn in Finance Insights.
author: ShivamPandey-msft
ms.date: 09/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 05bf5fe5a5ff86bbf52ed58ee6b1e84c15bf2c1e
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573189"
---
# <a name="configuration-for-finance-insights"></a>Configuratie voor Finance Insights

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Finance Insights combineert de functionaliteit van Microsoft Dynamics 365 Finance met Dataverse, Azure en AI Builder, zodat u beschikt over krachtige prognosefuncties voor uw organisatie. In dit artikel worden de configuratiestappen beschreven die ervoor zorgen dat uw systeem de mogelijkheden gebruikt die beschikbaar zijn in Finance Insights. Om de procedures in dit artikel te kunnen uitvoeren, moet u toegang als Systeembeheerder en Systeemaanpasser hebben in het [Power Portal-beheercentrum](https://admin.powerplatform.microsoft.com/), systeembeheerdertoegang in Dynamics 365 Finance en toegang om omgevingen te maken in Microsoft Dynamics Lifecycle Services (LCS).

> [!NOTE]
> De volgende procedures voor het instellen van Finance Insights zijn geldig voor versies van Dynamics 365 Finance, versie 10.0.21 en hoger.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance implementeren

Ga als volgt te werk om de omgevingen te implementeren.

1. In LCS kunt u een Dynamics 365 Finance-omgeving maken of bijwerken. Voor de omgeving is app-versie 10.0.21 of hoger vereist.

    > [!NOTE]
    > De omgeving moet een omgeving met hoge beschikbaarheid (HA) zijn. (Dit type omgeving wordt ook wel een Tier-2-omgeving genoemd.) Zie [Omgevingsplanning](/fin-ops-core/fin-ops/imp-lifecycle/environment-planning) voor meer informatie.

2. Als u Finance Insights configureert in een sandbox-omgeving, moet u mogelijk productiegegevens naar die omgeving kopiëren om ervoor te zorgen dat voorspellingen werken. Het voorspellingsmodel gebruikt meerdere jaren aan gegevens om voorspellingen samen te stellen. De Contoso-demonstratiegegevens bevatten niet voldoende historische gegevens om het voorspellingsmodel op een adequate manier te trainen. 

## <a name="configure-your-azure-ad-tenant"></a>Uw Azure AD-tenant configureren

Azure Active Directory (Azure AD) moet worden geconfigureerd zodat deze kan worden gebruikt met Dataverse en de Microsoft Power Platform-toepassingen. Voor deze configuratie moet de rol **Projecteigenaar** of de rol **Omgevingsmanager** worden toegewezen aan de gebruiker in het veld **Projectbeveiligingsrol** in LCS.

Controleer of de volgende instellingen zijn voltooid:

- U hebt toegang tot **Systeembeheerder** en **Systeemaanpasser** in het Power Portal-beheercentrum.
- Er wordt een licentie voor Dynamics 365 Finance of equivalente licentie toegepast op de gebruiker die de invoegtoepassing voor Finance insights installeert.
- De volgende Azure AD-apps zijn geregistreerd in Azure AD.

    |  Toepassing                             | App-id                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP-microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |

    Als u wilt verifiëren of de toepassing is geregistreerd in Azure AD, controleert u de lijst **Alle toepassingen**. Zie [Ondernemingstoepassingen weergeven](/azure/active-directory/manage-apps/view-applications-portal) voor meer informatie.
  
    Als de toepassing niet is geregistreerd in Azure AD, neemt u contact op met de ondersteuning.
  
## <a name="configure-dataverse"></a>Dataverse configureren

Voer de volgende stappen uit om Dataverse voor Finance Insights te configureren.

- Open de omgevingspagina in LCS en controleer of de sectie **Power Platform-integratie** al is ingesteld.

    - Als Dataverse al is ingesteld, moet de naam van de Dataverse-omgeving worden weergegeven die is gekoppeld aan de Finance-omgeving.
    - Als Dataverse nog niet is ingesteld, selecteert u **Instellingen**. De instelling van de Dataverse-omgeving kan tot een uur duren. Wanneer de instelling is voltooid, moet de naam van de Dataverse-omgeving waarmee is gekoppeld in de Finance-omgeving worden weergegeven.
    - Als deze integratie is ingesteld met een bestaande Microsoft Power Platform-omgeving, neemt u contact op met de beheerder om te controleren of de gekoppelde omgeving niet uitgeschakeld is.

        Zie [De Power Platform-integratie inschakelen](../../fin-ops-core/dev-itpro/power-platform/enable-power-platform-integration.md) voor meer informatie. 

        Als u toegang wilt tot de Microsoft Power Platform-beheersite, gaat u naar <https://admin.powerplatform.microsoft.com/environments>.

## <a name="configure-the-finance-insights-add-in"></a>De invoegtoepassing Finance insights configureren

Als u de invoegtoepassing Finance Insights eerder hebt geïnstalleerd, moet u deze verwijderen voordat u de volgende procedure voltooit.

> [!NOTE]
> Als u de data lake-invoegtoepassing in LCS al hebt geïnstalleerd, gebruikt Finance Insights deze om gegevens op te slaan die nodig zijn voor voorspellingen. Als u de data lake-invoegtoepassing nog niet geïnstalleerd hebt in LCS, maakt de Finance insights-invoegtoepassing een beheerd data lake.

Voer de volgende stappen uit om de invoegtoepassing Finance insights te installeren.

1. Meld u aan bij LCS en selecteer vervolgens **Volledige details** onder de naam van de omgeving aan de rechterkant van de pagina.
2. Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
3. Selecteer de invoegtoepassing **Finance insights**.
4. Geef uw akkoord aan de algemene voorwaarden en selecteer **Installeren**.

Het kan enkele minuten duren voordat de invoegtoepassing is geïnstalleerd.

## <a name="one-last-thing"></a>Nog één ding...

Nadat de invoegtoepassing is geïnstalleerd, kan het tot een uur duren voordat u de Finance Insights-functies kunt inschakelen in het werkgebied **Functiebeheer** in Dynamics 365 Finance. Als u niet zo lang wilt wachten, kunt u het proces voor de **statuscontrole van Insights-inrichting** handmatig uitvoeren. 

1. Ga in Dynamics 365 Finance naar **Systeembeheer \> Instellingen \> Procesautomatisering**.
2. Zoek op het tabblad **Achtergrondprocessen** naar de **statuscontrole van Insights-inrichting** en selecteer **Bewerken**.
3. Stel het veld **Volgende uitvoerbewerking** in op 30 minuten voor de huidige tijd.

   Door deze wijziging moet het proces **statuscontrole voor Insights-inrichting** direct worden uitgevoerd.

   Nadat het proces van de **statuscontrole van Insights-inrichting** is uitgevoerd, kunt u Finance Insights-functies inschakelen in het werkgebied **Functiebeheer**.

> [!NOTE]
> Als het proces van **Statuscontrole voor Insights-inrichting** niet wordt uitgevoerd, gaat u naar **Systeembeheer** > **Query´s** > **Batchtaken**. Wijzig in het veld **Polling-systeem procesautomatisering** de waarde in **Wachtend** om het proces te starten. 
> 
## <a name="feedback-and-support"></a>Feedback en ondersteuning

Stuur een e-mail naar [Finance Insights (preview)](mailto:fiap@microsoft.com) als u feedback wilt geven of ondersteuning nodig hebt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
