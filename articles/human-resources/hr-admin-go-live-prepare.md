---
title: Voorbereiden op go-live van Human Resources
description: Deze pagina bevat richtlijnen voor de voorbereiding op een go-live met Dynamics 365 Human Resources.
author: rachel-profitt
manager: tfehr
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 59d7274c3b40e78209d90960c4514321b736876a
ms.sourcegitcommit: d66fd72342931fad25a696b251c05781280d36c4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/14/2020
ms.locfileid: "4011409"
---
# <a name="prepare-for-human-resources-go-live"></a>Voorbereiden op go-live van Human Resources

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u voorbereidingen treft om live te gaan met een Dynamics 365 Human Resources-project met behulp van Microsoft Dynamics Lifecycle Services (LCS). 

In deze afbeelding worden de fasen van het go-live-proces weergegeven. 

![Go-live-proces](./media/hr-admin-go-live-prepare-process.png)

In de volgende tabel worden alle stappen in het proces weergegeven, de verwachte duur en degene die verantwoordelijk is voor de actie.

| Fase | Actie | Duur/wanneer | Wie | Opmerkingen |
| --- | --- | --- | --- |--- |
| 1 | Go-live-datum in LCS bijwerken | Uiterlijk 2-3 maanden van tevoren | Partner/klant | De mijlpaaldatums moeten up-to-date worden gehouden en doorlopend worden bijgewerkt. |
| 2 | Controlelijst invullen en verzenden | Nadat acceptatietesten door gebruiker (UAT) zijn voltooid | Partner/klant | Volg de instructies die worden geleverd in [Go-live-beoordeling van FastTrack](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projectbeoordeling (FastTrack) | FastTrack Architect* | Architect verschaft een beoordeling na ontvangst van de controlelijst en blijft verder controleren totdat vragen zijn opgehelderd en eventuele oplossingen zijn gevonden. |
| 4 | Projectworkshop (FastTrack) | FastTrack Architect* | |
| 5 | Gegevenspakketten importeren | Is afhankelijk van het project | Partner/klant | Volg de instructies in [Overzicht gegevensbeheer](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities-data-packages).|
| 6 | Gereed voor productie | Nadat alle vorige stappen zijn uitgevoerd | Partner/klant | Partner/klant kan de controle over de productieomgeving overnemen.|
| 7 | Cutover-activiteiten | Is afhankelijk van het project | Partner/klant | |
| 8 | Go-live | Is afhankelijk van het project | Klant | |

> [!IMPORTANT]
> * Stap 3 en 4 worden alleen uitgevoerd voor klanten die in aanmerking komen voor FastTrack.

## <a name="completing-the-lcs-methodology"></a>De LCS-methodologie voltooien

Een belangrijke mijlpaal in elk implementatieproject is de cutover naar de productieomgeving. 

Om ervoor te zorgen dat de productieomgeving wordt gebruikt voor live bewerkingen, verstrekt Microsoft het productie-exemplaar alleen wanneer de implementatie de fase **Uitvoeren** nadert, nadat de vereiste activiteiten in de LCS-methodologie zijn voltooid. Zie de  [Dynamics 365-licentiehandleiding](https://go.microsoft.com/fwlink/?LinkId=866544) voor meer informatie over de omgevingen in uw abonnement. 

Klanten moeten de fasen **Analyse** , **Ontwerpen en ontwikkelen** en **Testen** in de LCS-methodologie uitvoeren vóór de knop  **Configureren**  om te vragen of de productieomgeving beschikbaar wordt. Als u een fase in LCS wilt voltooien, moet u eerst elke vereiste stap in die fase voltooien. Wanneer alle stappen in een fase zijn voltooid, kunt u de gehele fase voltooien. U kunt een fase later altijd opnieuw openen als u wijzigingen moet aanbrengen. Zie  [Lifecycle Services (LCS) voor klanten van Finance and Operations-apps](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs) voor meer informatie. 

Het proces voor het uitvoeren van een stap bestaat uit twee delen: 

- De werkelijke werkzaamheden uitvoeren, zoals een geschiktheids-/hiaatanalyse of acceptatietesten door de gebruiker (UAT). 
- De corresponderende stap in de LCS-methodologie als voltooid markeren. 

Het is raadzaam de stappen in de methodologie te voltooien terwijl u de implementatie uitvoert. Wacht niet tot het laatste moment. Klik niet zomaar op alle stappen om een productieomgeving te krijgen. Het is voor de klant het beste om een solide implementatie te hebben. 

## <a name="uat-for-your-solution"></a>UAT voor uw oplossing

Tijdens de UAT-fase moet u alle bedrijfsprocessen die u hebt geïmplementeerd en alle aanpassingen die u hebt aangebracht, testen in een Sandbox-omgeving in het implementatieproject. Houd bij het voltooien van de UAT-fase rekening met het volgende als u zeker wilt zijn van een succesvolle go-live: 

- Testcases omvatten het gehele bereik van vereisten. 
- Test met behulp van gemigreerde gegevens. Deze gegevens moeten hoofdgegevens zoals werknemers, taken en posities omvatten. Neem ook beginsaldi op, zoals verlof- en verzuimtoerekeningen. Neem tot slot openstaande transacties op, zoals huidige inschrijvingen voor vergoedingen. Voer testen met alle typen gegevens uit, zelfs als de gegevensset niet is voltooid. 
- Test met behulp van de juiste beveiligingsrollen (standaardrollen en aangepaste rollen) die aan gebruikers zijn toegewezen. 
- Zorg ervoor dat de oplossing voldoet aan alle bedrijfsspecifieke en sectorspecifieke wettelijke vereisten. 
- Documenteer alle functies en verkrijg goedkeuring en meld u af bij de klant. 

## <a name="fasttrack-go-live-assessment"></a>Go-live-beoordeling van FastTrack

Klanten die zijn gekwalificeerd voor FastTrack en werken met FastTrack Solution Architect, voeren een go-live-evaluatie uit met Microsoft FastTrack. Zie  [Microsoft FastTrack](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/fasttrack-dynamics-365-overview) voor meer informatie. 

Ongeveer acht weken vóór go-live zal het FastTrack-team u vragen een [Go-live-controlelijst](https://go.microsoft.com/fwlink/?linkid=2146013) in te vullen.

De projectmanager of een belangrijk projectlid moet de go-live-controlelijst invullen tijdens de pre-go-live fase van het project. De controlelijst wordt normaal gesproken vier tot zes weken vóór de voorgestelde go-live-datum ingevuld wanneer de UAT is voltooid of bijna is voltooid. 

Wanneer u de go-live-controlelijst hebt ingevuld, verzendt u deze per e-mail naar uw FastTrack Solution Architect. Neem altijd een belangrijke belanghebbende van de klant en de implementatiepartner in het e-mailbericht op. 

Nadat u de controlelijst hebt ingediend, zal uw FastTrack Solution Architect het project beoordelen en een beoordeling geven waarin de mogelijke risico's, de beste methoden en aanbevelingen worden beschreven voor een succesvolle go-live van het project. In sommige gevallen kan de oplossingsarchitect risicofactoren markeren en vragen om een oplossingsplan. 

## <a name="see-also"></a>Zie ook

[Veelgestelde vragen over go-live](hr-admin-go-live-faq.md)