---
title: Dienstverbandverificatie i9-verificatie
description: Volgens de Immigration Reform and Control Act moeten Amerikaanse werkgevers de arbeidsbevoegdheidsstatus van nieuwe werknemers controleren.
author: ShielaSogge
ms.date: 01/10/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: HcmWorker, HcmPersonIdentificationNumber, Hcmi9Document
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea77f112413a5b7d5c96768ad46fdb361023bd84
ms.sourcegitcommit: 27475081f3d2d96cf655b6afdc97be9fb719c04d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/12/2022
ms.locfileid: "7964878"
---
# <a name="employment-verification-i9-verification"></a>Dienstverbandverificatie i9-verificatie

[!include [banner](../../../includes/banner.md)]

Volgens de Immigration Reform and Control Act moeten Amerikaanse werkgevers de arbeidsbevoegdheidsstatus van nieuwe werknemers controleren. Deze procedure doorloopt de stappen van het registreren van de benodigde documenten voor I-9-verificatie. Gebruik het bedrijf USMF voor deze procedure.

1. Ga naar **Human Resources \> Medewerkers \> Werknemers**.
2. Gebruik de snelfilter om records te zoeken. Filter bijvoorbeeld op het veld **Naam** met een waarde van **Vince**.
3. Selecteer de werknemer. Selecteer bijvoorbeeld **Vince Prado**.
4. Selecteer het sneltabblad **Persoonlijke gegevens**.
5. Selecteer **Identificatienummers**.
6. Selecteer **Nieuw**.
7. Selecteer het identificatietype dat u registreert. Selecteer bijvoorbeeld **Paspoort**.
8. Voer een waarde in het veld **Nummer** in.
9. Selecteer **Ja** in het veld **Primair**.
10. Voer in het veld **Omschrijving** een korte omschrijving van de identificatierecord in.
11. Selecteer bij **Uitgevende instantie** de instantie die de vorm van identificatie voor de werknemer heeft uitgegeven. Selecteer bijvoorbeeld **Overheid**.
12. Voer de datum in waarop de uitgevende instantie de vorm van identificatie voor de werknemer heeft uitgegeven. Voer bijvoorbeeld de datum **15-02-2015** (15 februari 2011) in.
13. Voer de datum in waarop de vorm van identificatie verloopt. Voer bijvoorbeeld de datum **15-02-2021** (15 februari 2021) in.
14. Selecteer **Opslaan**.
15. Sluit de pagina.
16. Selecteer het tabblad **Aanstelling**.
17. Selecteer **I-9**.
18. Selecteer **Nieuw**.
19. Selecteer een optie in het veld **Werkvergunningen**.

    Als de werknemer geen Amerikaans staatsburger is, moet u het vreemdelingen- of toelatingsnummer van de werknemer opgeven.

20. Selecteer de optie **GroupListA**.

    De lijst die u selecteert is afhankelijk van welke vorm van identificatie de werknemer heeft opgegeven. Een werknemer moet één document uit Lijst A of één document uit zowel Lijst B als Lijst C verstrekken. Als de werknemer bijvoorbeeld een paspoort heeft verstrekt, kunt u Lijst A selecteren. Als de werknemer echter alleen een rijbewijs en identiteitskaart heeft opgegeven, moet u Lijst B en Lijst C selecteren.

21. Selecteer in het veld **I-9-documenttype** het type document dat de werknemer heeft verstrekt.
22. Typ of selecteer een waarde in het veld **Documentnummer**.
23. Selecteer **Opslaan**.

[!INCLUDE[footer-include](../../../../../includes/footer-banner.md)]
