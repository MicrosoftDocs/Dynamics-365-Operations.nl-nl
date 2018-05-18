--- 
title: "Regels en beleid van de vergoedingsgeschiktheid definiëren"
description: Deze opname laat zien hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.
author: kherr75
manager: AnnBe
ms.date: 06/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 807e6a41d603a5327d713d1ab742cc0d961a7784
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="define-benefit-eligibility-rules-and-policies"></a>Regels en beleid van de vergoedingsgeschiktheid definiëren

[!include [task guide banner](../../includes/task-guide-banner.md)]

Deze opname laat zien hoe u geschiktheidsregels en beleid voor vergoedingen kunt maken en vervolgens regels kunt toewijzen aan vergoedingen.  

Het bedrijf van de demogegevens dat wordt gebruikt om deze registratie te maken is USMF.


## <a name="create-benefit-eligibility-policy-rule-type"></a>Regeltype van beleid om in aanmerking te komen voor een vergoeding maken
1. Ga naar Human resources > Vergoedingen > Geschiktheid > Regeltypen van beleid om in aanmerking te komen voor een vergoeding.
2. Klik op Nieuw.
3. Typ een waarde in het veld Regelnaam.
4. Typ een waarde in het veld Omschrijving.
5. Klik in het veld Querynaam op de vervolgkeuzeknop om de zoekopdracht te openen.
6. Klik in de lijst op de koppeling in de geselecteerde rij.
7. Klik op Opslaan.
8. Sluit de pagina.

## <a name="benefit-eligibility-policy"></a>Beleid om in aanmerking te komen voor een vergoeding
1. Ga naar Human resources > Vergoedingen > Geschiktheid > Beleid voor geschiktheid vergoedingen.
2. Selecteer een bestaand vergoedingsbeleid.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Schakel de uitbreiding van de secties Beleidsorganisaties om.  Hier kunt u organisaties toevoegen of verwijderen die u wilt opnemen in het beleid.
5. Vouw de sectie Beleidsregels uit of samen.
6. Zoek in de lijst de beleidsregel die eerder is gemaakt.
7. Klik op Beleidsregel maken.
8. Voer in het veld Ingangsdatum de datum in waarop u het beleid van kracht wilt laten worden.
    * Door ingangsdatums en einddatums in te stellen kunt u toekomstige wijzigingen aanbrengen in beleidsregels en terugkomen naar het beleid als u die wijzigingen van kracht wilt laten worden overbodig maken.  
9. 
    * Als u bijvoorbeeld wilt dat de regel alleen van toepassing is op verkoopmanagers, kunt u het WHERE-onderdeel gebruiken om te zeggen: Waar de positieomschrijving gelijk is aan Verkoopmanager.  U kunt via En en Of meerdere Where-instructies opnemen in de regel.  
10. Klik op OK.
11. Sluit de pagina.
12. Sluit de pagina.

## <a name="assign-rule-to-benefit"></a>Regel toewijzen aan vergoeding
1. Ga naar Human resources > Vergoedingen > Vergoedingen.
2. Zoek en selecteer de gewenste record in de lijst.
3. Klik in de lijst op de koppeling in de geselecteerde rij.
4. Vouw de sectie Geschiktheidsregels uit of samen.
5. Klik op Bewerken.
6. Selecteer in het veld geschiktheid de optie Op basis van regels uit de lijst.
7. Klik in het veld Regeltype op de vervolgkeuzeknop om de zoekopdracht te openen.
8. Zoek en selecteer in de lijst de regel die u eerder hebt gemaakt.
9. Klik in de lijst op de koppeling in de geselecteerde rij.
10. Klik op Opslaan.
11. Het formulier sluiten.


