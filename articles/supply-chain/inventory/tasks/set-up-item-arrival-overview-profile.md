---
title: Een ontvangstoverzichtsprofiel instellen voor een artikel
description: Dit artikel is gericht op de instelling van een profiel van aankomstoverzicht.
author: yufeihuang
ms.date: 07/30/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WMSArrivalOverviewProfile
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yufeihuang
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8517710f5d0be1859f86449152712d950281769a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8872002"
---
# <a name="set-up-an-item-arrival-overview-profile"></a>Een ontvangstoverzichtsprofiel instellen voor een artikel

[!include [banner](../../includes/banner.md)]

Dit artikel is gericht op de instelling van een profiel van aankomstoverzicht. Het profiel van aankomstoverzicht is een verzameling regels die wordt toegepast wanneer de aankomstoverzichtspagina door een gebruiker wordt geopend. U kunt deze procedure gebruiken in het demobedrijf USMF. Deze procedure wordt meestal uitgevoerd door een ontvangstadministrateur.

1. Ga in het navigatievenster naar **Modules > Voorraadbeheer > Instellingen > Distributie > Aankomstoverzichtsprofielen**.
2. Selecteer **Nieuw**. Omdat u bijna altijd in hetzelfde magazijn zult werken waar volledige vrachtwagenladingen worden gelost, kunt u het beste een aankomstoverzichtsprofiel maken om het proces van het registreren van ontvangen artikelen te vereenvoudigen.  
3. Typ een waarde in het veld **Naam aankomstoverzichtsprofiel**.
4. Selecteer een optie in het veld **Regels tonen**. Selecteren welke regels voor de ontvangsten worden weergegeven:  

    - **Alle**: alle regels weergeven, onafhankelijk van de status.   
    - **In uitvoering**: regels weergeven voor ontvangsten waarvan de voortgang Volledig of Gedeeltelijk is. Dit betekent dat voor elke regel ofwel de volledige hoeveelheid of een deel daarvan in een ontvangstjournaal is geregistreerd.   
    - **Niet volledig**: regels weergeven voor ontvangsten waarvan de voortgang Geen of Gedeeltelijk is. Dit betekent dat voor elke regel niets of een gedeelte van de hoeveelheid in een ontvangstjournaal is geregistreerd.  

5. Vouw de sectie **Aankomstopties** uit of samen.
6. Typ een waarde in het veld **Dagen vooruit**. Hiermee wordt een filter ingesteld om de ontvangstregels weer te geven waarvan de ontvangst in de komende dagen wordt verwacht (afhankelijk van het getal dat u instelt).  
7. Typ een waarde in het veld **Dagen terug**. Hiermee wordt een filter ingesteld om de ontvangstregels weer te geven waarvan de ontvangst een aantal dagen vóór vandaag werd verwacht.  
8. Typ een waarde in het veld **Magazijnen**. Filteren op een of meer magazijnen.  
9. Selecteer een waarde in het veld **Leveringsmethode**. Dit stelt een filter in om alleen de ontvangstregels met deze leveringsmethode weer te geven.  
10. Selecteer WHS in het veld **Naam**.
11. Selecteer magazijn 24 in het veld **Magazijn**. Dit is het standaardmagazijn dat voor geregistreerde ontvangstregels wordt gebruikt die dit profiel gebruiken.  
12. Selecteer **Baydoor** in het veld **Locatie**. Dit is de standaardlocatie die voor geregistreerde ontvangstregels wordt gebruikt die dit profiel gebruiken.  
13. Vouw de sectie **Aankomstquerygegevens** uit of samen.
14. Selecteer Vestiging 2 in het veld **Beperken tot vestiging**. Dit stelt een filter in om alleen de ontvangstregels met deze site weer te geven.  
15. Stel de optie **Inkooporders** in op **Ja**. Regels vanuit inkooporders selecteren.  
16. Stel de optie **overboekingsorders** in op **Ja**. Regels vanuit overboekingsorders selecteren.  
17. Selecteer **Opslaan**.
18. Sluit de pagina.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
