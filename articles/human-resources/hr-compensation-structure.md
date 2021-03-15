---
title: Een compensatiestructuur ontwikkelen
description: Dit artikel begeleidt u bij het maken van een vastecompensatieplan en het registreren van werknemers voor het plan via geschiktheidsregels.
author: andreabichsel
manager: tfehr
ms.date: 02/10/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: DefaultDashboard, HcmCompensationWorkspace, HcmCompFixedPlansPart, HRMCompFixedPlanTable, HRMCompCreateGridDialog, HRCCompGridView, HRMCompEligibility,  HRCCompGrid
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a5e7ef2021e41c13b82523f2dc6a1b09bd1ba9f
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115891"
---
# <a name="develop-a-compensation-structure"></a>Een compensatiestructuur ontwikkelen

Dit artikel begeleidt u bij het maken van een vastecompensatieplan en het registreren van werknemers voor het plan via geschiktheidsregels. In dit artikel, dat van toepassing is op managers voor compensatie en vergoedingen, worden de USMF-voorbeeldgegevens gebruikt.

## <a name="create-a-fixed-compensation-plan"></a>Een vast compensatieplan maken

1. Selecteer **Compensatiebeheer**.

2. Selecteer **Vastecompensatieplannen**.

3. Selecteer **Nieuw**.

4. Voer een waarde in het veld **Plan** in.

5. Voer een waarde in het veld **Beschrijving** in.

6. Voer een datum in het veld **Begindatum** in.

7. Selecteer in het veld **Type** of het vastecompensatieplan van het type **Schaal**, **Schijf** of **Stap** is.

8. Het selectievakje **Aanbeveling toegestaan** fungeert als standaardwaarde voor eventuele acties die aan dit plan in een procesgebeurtenis worden toegevoegd. Met Aanbeveling toegestaan kunt u het berekende richtlijnbedrag overschrijven bij het verwerken van de compensatie.

9. Met het veld **Tolerantie voor buiten bereik** kunt u opgeven hoe u compensatiebedragen wilt verwerken die buiten het opgegeven bereik van de compensatiestructuur voor het opgegeven niveau vallen. Als u het veld **Tolerantie voor buiten bereik** instelt op **Geen**, kunt u elk gewenst compensatiebedrag gebruiken. **Zachte tolerantie** waarschuwt gebruikers als het compensatiebedrag minder is dan het minimale of meer dan het maximale referentiepuntbedrag voor dat niveau. Gebruikers kunnen de waarschuwing negeren en verdergaan. **Harde tolerantie** genereert een fout als de compensatie van een werknemer buiten de minimum- en maximumreferentiepunten voor het niveau ligt en wordt de compensatie automatisch aangepast om binnen het bereik te vallen.

10. Met het veld **Huurregel** wordt de compensatie van een werknemer tijdens een procesgebeurtenis berekend. Een **huurregel** van het type **Percentage** berekent een verhoging die evenredig is voor de duur dat de werknemer in dienst is in de cyclus.

11. Typ een waarde in het veld **Valuta**.

12. Typ of selecteer een waarde in het veld **Conversie van loontarief**.

13. Vouw de sectie **Bereikgebruiksmatrix** uit. Voeg desgewenst bereikgebruikrecords toe om werknemers sneller naar hun middelpunt toe te krijgen en ze af te remmen voor het bereiken van het maximum van hun bereik.

14. Selecteer **Opslaan**. Hierdoor wordt de knop **Compensatie instellen** ingeschakeld en kunt u doorgaan met het definiëren van uw compensatiestructuur voor het plan.

15. Selecteer **Compensatie instellen**. U kunt een van de volgende drie methoden gebruiken om een compensatiestructuur te maken:

    - Maak een geheel nieuwe structuur door een set referentiepunten te selecteren en de niveaus toe te voegen om uw eigen structuur te maken.
    - Kopieer een compensatiestructuur van een bestaand plan als beginpunt en wijzig deze voor het nieuwe plan.
    - Selecteer een bestaand compensatieraster. Als een ander plan al gebruikmaakt van het compensatieraster, worden eventuele wijzigingen in het raster ook doorgevoerd in het andere plan.

16. Selecteer **Nieuwe matrix maken op basis van bestaande compensatiematrix**.

17. Typ of selecteer een waarde in het veld **Uit raster kopiëren**. Desgewenst kunt u de naam van het nieuwe compensatieraster wijzigen die u maakt door het geselecteerde raster te kopiëren.

18. Selecteer **OK**.

19. Selecteer **Groepsgewijs wijzigen**. Met **Groepsgewijs wijzigen** kunt u de bedragen van de compensatiematrix onderhouden door een percentage of een vlakke bedragverhoging toe te passen op één of meerdere niveaus of referentiepunten.

20. Voer in het veld **Aanpassingsbedrag** een getal in.

21. Selecteer of deselecteer alle rijen in de lijst.

22. Klik op **Toepassen op raster**.

23. Sluit de pagina. Nadat u de compensatiestructuur hebt gemaakt, kunt u selecteren welke referentiepunten u wilt gebruiken als controlepunt voor het vastecompensatieplan. Het controlepunt wordt gebruikt om de comparatio van een werknemer te berekenen.

24. Typ of selecteer een waarde in het veld **Controlepunt**.

25. Sluit de pagina.

## <a name="create-an-eligibility-rule-for-the-fixed-compensation-plan"></a>Maak een geschiktheidsregel voor het vastecompensatieplan

U kunt een vastecompensatieplan toewijzen aan een werknemer totdat u geschiktheidsregels voor het plan hebt gedefinieerd.  

1. Selecteer **Geschiktheidsregels**.

2. Selecteer **Nieuw**.

3. Typ of selecteer een waarde in het veld **Geschiktheid**.

4. Voer een waarde in het veld **Beschrijving** in.

5. Voer een datum in het veld **Begindatum** in. Zowel vaste- als variabele-compensatieplannen maken gebruik van geschiktheidsregels. Selecteer in het veld **Type** het type plan.

6. Typ of selecteer een waarde in het veld **Plannen**. Selecteer de criteria waaraan een werknemer moet voldoen om in aanmerking te komen voor het compensatieplan. Mogelijke criteria zijn:

    - **Departement**
    - **Vakbond**
    - **Locatie** (**Compensatieregio**)
    - **Functie**
    - **Functie**
    - **Taaktype**
    - **Compensatieniveau**
    
    De werknemer moet aan alle criteria voldoen om in aanmerking te komen voor het compensatieplan. Als u geen criteria opgeeft, komen alle werknemers in aanmerking voor het compensatieplan. Als een werknemer niet voldoet aan de criteria die in de regel voor geschiktheid worden opgegeven, of er geen regel voor geschiktheid voor een compensatieplan is opgegeven, wordt het compensatieplan niet in de zoekopdracht weergegeven als u een vastecompensatierecord voor een werknemer maakt.

7. Sluit de pagina.

8. Sluit de pagina.



[!INCLUDE[footer-include](../includes/footer-banner.md)]