---
title: Voorbereiden op go-live van Human Resources
description: Deze pagina bevat richtlijnen voor de voorbereiding op een go-live met Dynamics 365 Human Resources.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1cbf6d1e5bf1716bc602b335e0b0a57dd52bb983
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8855226"
---
# <a name="prepare-for-human-resources-go-live"></a>Voorbereiden op go-live van Human Resources

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../includes/peap-2.md)]

In dit artikel wordt beschreven hoe u voorbereidingen treft om live te gaan met een Dynamics 365 Human Resources-project met behulp van Microsoft Dynamics Lifecycle Services (LCS). 

In deze afbeelding worden de fasen van het go-live-proces weergegeven. 

![Go-live-proces.](./media/hr-admin-go-live-prepare-process.png)

In de volgende tabel worden alle stappen in het proces weergegeven, de verwachte duur en degene die verantwoordelijk is voor de actie.

| Fase | Actie | Duur/wanneer | Wie | Opmerkingen |
| --- | --- | --- | --- |--- |
| 1 | Go-live-datum in LCS bijwerken | Uiterlijk 2-3 maanden van tevoren | Partner/klant | De mijlpaaldatums moeten up-to-date worden gehouden en doorlopend worden bijgewerkt. |
| 2 | Controlelijst invullen en verzenden | Nadat acceptatietesten door gebruiker (UAT) zijn voltooid | Partner/klant | Volg de instructies die worden geleverd in [Go-live-beoordeling van FastTrack](hr-admin-go-live-prepare.md#fasttrack-go-live-assessment). |
| 3 | Projectbeoordeling (FastTrack) | FastTrack Architect* | Architect verschaft een beoordeling na ontvangst van de controlelijst en blijft verder controleren totdat vragen zijn opgehelderd en eventuele oplossingen zijn gevonden. |
| 4 | Projectworkshop (FastTrack) | FastTrack Architect* | |
| 5 | Gegevenspakketten importeren | Is afhankelijk van het project | Partner/klant | Volg de instructies in [Overzicht gegevensbeheer](../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).|
| 6 | Gereed voor productie | Nadat alle vorige stappen zijn uitgevoerd | Partner/klant | Partner/klant kan de controle over de productieomgeving overnemen.|
| 7 | Cutover-activiteiten | Is afhankelijk van het project | Partner/klant | |
| 8 | Go-live | Is afhankelijk van het project | Klant | |

> [!IMPORTANT]
> * Stap 3 en 4 worden alleen uitgevoerd voor klanten die in aanmerking komen voor FastTrack.

## <a name="completing-the-lcs-methodology"></a>De LCS-methodologie voltooien

Een belangrijke mijlpaal in elk implementatieproject is de cutover naar de productieomgeving. Het proces voor het uitvoeren van een stap bestaat uit twee delen: 

- De werkelijke werkzaamheden uitvoeren, zoals een geschiktheids-/hiaatanalyse of acceptatietesten door de gebruiker (UAT). 
- De corresponderende stap in de LCS-methodologie als voltooid markeren. 

Het is raadzaam de stappen in de methodologie te voltooien terwijl u de implementatie uitvoert. Wacht niet tot het laatste moment. Het is voor de klant het beste om een solide implementatie te hebben. 

## <a name="uat-for-your-solution"></a>UAT voor uw oplossing

Tijdens de UAT-fase moet u alle bedrijfsprocessen die u hebt geïmplementeerd en alle aanpassingen die u hebt aangebracht, testen in een Sandbox-omgeving in het implementatieproject. Houd bij het voltooien van de UAT-fase rekening met het volgende als u zeker wilt zijn van een succesvolle go-live: 

- We raden u aan uw UAT-proces te starten met een schone omgeving waarin de gegevens uit uw GOLD-configuratie vóór het begin van het UAT-proces naar de omgeving worden gekopieerd. Wij raden u aan de productieomgeving als uw GOLD-omgeving te gebruiken totdat u live gaat, waarna de omgeving een productieomgeving wordt.
- Testcases omvatten het gehele bereik van vereisten. 
- Test met behulp van gemigreerde gegevens. Deze moeten gegevens zoals werknemers, taken en posities omvatten. Neem ook beginsaldi op, zoals verlof- en verzuimtoerekeningen. Neem tot slot openstaande transacties op, zoals huidige inschrijvingen voor vergoedingen. Voer testen met alle typen gegevens uit, zelfs als de gegevensset niet is voltooid. 
- Test met behulp van de juiste beveiligingsrollen (standaardrollen en aangepaste rollen) die aan gebruikers zijn toegewezen. 
- Zorg ervoor dat de oplossing voldoet aan alle bedrijfsspecifieke en sectorspecifieke wettelijke vereisten. 
- Documenteer alle functies en verkrijg goedkeuring en meld u af bij de klant. 

## <a name="mock-go-live"></a>Go-live simulatie

Voorafgaand aan uw go-live, moet u een simulatie go-live uitvoeren om de stappen die nodig zijn voor de cutover van uw legacy-systemen naar het nieuwe systeem te testen. U moet een go-live simulatie uitvoeren in een sandbox-omgeving en alle stappen in uw cutover-plan opnemen.

- We raden u aan de productieomgeving als GOLD-configuratieomgeving te gebruiken tot de go-live.
- Zorg ervoor dat u over een sterk governanceproces beschikt om de productieomgeving te beschermen tegen onbedoelde transacties of updates voorafgaand aan de go-live.
- Wanneer u klaar bent om UAT of de go-live simulatie uit te voeren, vernieuwt u de sandbox-omgeving vanuit de productieomgeving. Zie [Een exemplaar kopiëren](hr-admin-setup-copy-instance.md) voor meer informatie.
- Test elke stap van uw cutover-plan in de sandbox-omgeving en valideer vervolgens de sandbox-omgeving door steekproefcontroles uit te voeren of tests uit te voeren vanuit uw UAT-scripts in de omgeving.
  - Tests moeten alle gegevensmigraties omvatten, inclusief transformaties die nodig zijn voor de go-live.
  - Het proces moet een oefen-cutoff van eventuele legacy-systemen omvatten.
  - Zorg ervoor dat u integratie-cutoverstappen of externe systeemstappen opneemt in uw cutover-simulatie.
- Als u problemen ondervindt tijdens de cutover-simulatie, kan een tweede simulatie nodig zijn. Daarom raden we u aan twee cutover-simulaties in uw projectplan te plannen.

## <a name="fasttrack-go-live-assessment"></a>Go-live-beoordeling van FastTrack

Klanten die zijn gekwalificeerd voor FastTrack en werken met FastTrack Solution Architect, voeren een go-live-evaluatie uit met Microsoft FastTrack. Zie  [Microsoft FastTrack](/dynamics365/fasttrack/) voor meer informatie. 

Ongeveer acht weken vóór go-live zal het FastTrack-team u vragen een [Go-live-controlelijst](https://go.microsoft.com/fwlink/?linkid=2146013) in te vullen.

De projectmanager of een belangrijk projectlid moet de go-live-controlelijst invullen tijdens de pre-go-live fase van het project. De controlelijst wordt normaal gesproken vier tot zes weken vóór de voorgestelde go-live-datum ingevuld wanneer de UAT is voltooid of bijna is voltooid. 

Wanneer u de go-live-controlelijst hebt ingevuld, verzendt u deze per e-mail naar uw FastTrack Solution Architect. Neem altijd een belangrijke belanghebbende van de klant en de implementatiepartner in het e-mailbericht op. 

Nadat u de controlelijst hebt ingediend, zal uw FastTrack Solution Architect het project beoordelen en een beoordeling geven waarin de mogelijke risico's, de beste methoden en aanbevelingen worden beschreven voor een succesvolle go-live van het project. In sommige gevallen kan de oplossingsarchitect risicofactoren markeren en vragen om een oplossingsplan. 

## <a name="see-also"></a>Zie ook

[Veelgestelde vragen over go-live](hr-admin-go-live-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
