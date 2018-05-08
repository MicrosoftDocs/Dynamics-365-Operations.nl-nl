---
title: De functionaliteit van Microsoft Dynamics 365 for Talent uitbreiden
description: Als u Microsoft PowerApps hebt gemaakt, kunt u die toepassingen starten via koppelingen in Microsoft Dynamics 365 for Talent.
author: rschloma
manager: AnnBe
ms.date: 03/21/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-28
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 72d4ff5e1311005d3bf43a13e28208cd9b3d1457
ms.openlocfilehash: 51eb4288f5b6c732755007c1dcd8c4db090ccc0a
ms.contentlocale: nl-nl
ms.lasthandoff: 03/07/2018

---
# <a name="extend-the-functionality-of-microsoft-dynamics-365-for-talent"></a>De functionaliteit van Microsoft Dynamics 365 for Talent uitbreiden

[!include [banner](includes/banner.md)]

Als u Microsoft PowerApps hebt gemaakt, kunt u die toepassingen starten via koppelingen in Microsoft Dynamics 365 for Talent. Als u toegang tot uw toepassingen wilt instellen, moet u bepaalde informatie instellen in Talent op een configuratiepagina die u opent vanuit het werkgebied **Systeembeheer**.

## <a name="configuring-embedded-powerapps-within-talent"></a>Ingesloten PowerApps in Talent configureren
Gebruik de pagina **Ingesloten Microsoft PowerApps instellen** om Talent-pagina's te configureren om PowerApps-toepassingen te starten. U opent de pagina **Ingesloten Microsoft PowerApps instellen** door het werkgebied **Systeembeheer** en vervolgens het tabblad **Koppelingen** te openen en **Microsoft PowerApps** te selecteren in de groep **Instellingen**. 

De volgende gegevens worden ingevoerd of ingesteld op deze pagina: 

 -  Een beschrijvende naam of id voor elke PowerApps-toepassing.
 -  Een unieke id (GUID) voor elke toepassing die u aan een Talent-pagina toevoegt. De app-id is beschikbaar op de PowerApps-site [powerapps.com](http://powerapps.com/). 
 -  De pagina waarop gebruikers een toepassing of rapport kunnen openen. Niet alle Talent-pagina's ondersteunen ingesloten PowerApps en Power BI-rapporten. 

 > [!NOTE]
 >  Voer in plaats van de weergavenaam die boven aan de pagina wordt weergegeven de interne naam van de pagina in. U vindt de interne naam door de betreffende pagina te openen en met de rechtermuisknop op de pagina te klikken. Wanneer het menu wordt geopend, beweegt u de muisaanwijzer over het item **Formuliergegevens**. De interne formuliernaam wordt weergegeven naast het item **Formuliergegevens** in het menu.
 
-   Geef op vanuit welk formulierbesturingselement de toepassing contextgegevens kan ophalen. Een toepassing kan bijvoorbeeld gegevens over een werknemer gebruiken. Als u de pagina **Werknemer** invoert in het veld **Context**, wordt de pagina **Werknemer** geopend wanneer u de toepassing start. U bent niet verplicht om iets in te voeren in het veld **Context**. 
-   Stel de grootte in van het dialoogvenster waarin de PowerApps-toepassing wordt uitgevoerd. De dialoogvensters worden aangewezen als klein of groot om de gebruikersinterface te optimaliseren wanneer uw toepassing respectievelijk op een telefoon of een groter apparaat wordt uitgevoerd. 


U kunt ook opgeven voor welke rechtspersonen een toepassing beschikbaar wordt of u kunt deze beschikbaar maken voor alle rechtspersonen. Standaard zijn uw PowerApps-toepassingen beschikbaar voor alle rechtspersonen.

## <a name="opening-an-application"></a>Een toepassing openen
Wanneer u ingesloten PowerApps-toepassingen hebt geconfigureerd, worden er koppelingen naar de opgegeven toepassingen toegevoegd aan de pagina's in Talent. Klik op een koppeling om een toepassing te openen. 



