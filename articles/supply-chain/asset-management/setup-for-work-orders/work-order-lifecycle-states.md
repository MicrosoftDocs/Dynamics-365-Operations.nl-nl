---
title: Levenscyclusstatussen van werkorders
description: In dit onderwerp wordt uitgelegd hoe u levenscyclusstatussen van werkorders plant in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3bff0c7334a9e05c3f455ffc9b3c82863964785e
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215465"
---
# <a name="work-order-lifecycle-states"></a>Levenscyclusstatussen van werkorders


[!include [banner](../../includes/banner.md)]

 

Levenscyclusstatussen van werkorders bepalen de statussen die een werkorder kan doorlopen. Voorbeelden zijn **Gemaakt**, **Gepland**, **In uitvoering** en **Beëindigd**. Levenscyclusstatussen van werkorders kunnen handmatig worden bijgewerkt op een werkorder of automatisch worden bijgewerkt (bijvoorbeeld tijdens het plannen van de werkorder).

De levenscyclusstatussen van werkorders die nodig zijn voor uw werkorders moeten worden gekoppeld aan overeenkomende projectfasen op de pagina **Projectmanagement en boekhoudparameters** (**Projectmanagement en boekhouding** \> **Projectmanagement en boekhoudparameters**). U definieert eerst projectfasen in Projectmanagement en boekhouding. U stelt vervolgens levenscyclusstatussen van werkorders en levenscyclusmodellen van werkorders in Activabeheer in.

In de volgende tabel worden de opties in de secties **Werkorder** en **Planning** op het Sneltabblad **Algemeen** van de pagina **Levenscyclusstatus van werkorder** (**Activabeheer** \> **Instellen** \> **Werkorders** \> **Levenscyclusstatussen**).

![Pagina Levenscyclusstatus van werkorder](media/09-setup-for-work-orders.png)

| Optienaam                   | Beschrijving |
|-------------------------------|-------------|
| Actief                        | Stel deze optie in op **Ja** als de werkorder actief moet zijn in deze levenscyclusstatus. |
| Regel toevoegen                      | Stel deze optie in op **Ja** als werkordertaken kunnen worden toegevoegd aan een werkorder die zich in deze levenscyclusstatus bevindt. |
| Verwijderen                        | Stel deze optie in op **Ja** als de werkorder in deze levenscyclusstatus gewist kan worden. |
| Regel verwijderen                   | Stel deze optie in op **Ja** als werkordertaken kunnen worden verwijderd uit een werkorder die zich in deze levenscyclusstatus bevindt. |
| Plannen toestaan              | Stel deze optie in op **Ja** als een werkorder in deze levenscyclusstatus gepland kan worden. |
| Werkelijk begin instellen              | Stel deze optie in op **Ja** als de gebruiker moet worden gevraagd om een werkelijke begindatum en -tijd voor een werkorder te selecteren wanneer deze wordt bijgewerkt naar deze levenscyclusstatus. |
| Werkelijke einde instellen                | Stel deze optie in op **Ja** als de gebruiker moet worden gevraagd om een werkelijke begindatum en -tijd voor een werkorder te selecteren wanneer deze wordt bijgewerkt naar deze levenscyclusstatus. |
| Journalen boeken                 | Stel deze optie in op **Ja** als werkorderjournalen kunnen worden toegevoegd wanneer een werkorder wordt bijgewerkt naar deze levenscyclusstatus. Als er een fout optreedt tijdens het boeken van een journaal, wordt een bericht weergegeven en wordt de levenscyclusstatus van de werkorder bijgewerkt. Als u de journaalregels voor een werkorder wilt weergeven, selecteert u **Activabeheer** \> **Algemeen** \> **Werkorders** \> **Alle werkorders**, **Actieve werkorders**, of **Mijn actieve werkorders**, selecteert u de werkorder in de lijst en selecteert u vervolgens **Journalen**. Deze instelling van automatische werkorder-journaalboeking met een bepaalde levensduur is hetzelfde als wanneer u **Journalen boeken** selecteert op de pagina **Werkorder-journalen**.<p>**Opmerking:** als u deze optie op **Ja**instelt, worden journalen automatisch geboekt als er geen workflow voor goedkeuring is ingesteld. Als uw bedrijf de goedkeuringsinstellingen voor journalen gebruikt die zijn geconfigureerd op de pagina **Journaal-goedkeuring** (**Projectmanagement en boekhouding** \> **Instellingen** \> **Journalen** \> **Journaal-goedkeuring**), moet een manager of mede werker verbruiksregistraties valideren en boeken.</p> |
| Onderhoudscontrolelijst verwerken | Stel deze optie in op **Ja** als alle bijgevoegde onderhoudscontrolelijsten kunnen worden toegevoegd wanneer een werkorder wordt bijgewerkt naar deze levenscyclusstatus. Als onderdeel van deze verwerking worden alle tellerregistraties die in een onderhoudscontrolelijst zijn ingevoerd, geboekt en wordt het resultaat van de gehele onderhoudscontrolelijst geëvalueerd. Regels voor onderhoudscontrolelijsten met **Gehaalde** en **Mislukte** resultaten worden geëvalueerd en als er ten minste één regel uitvalt, wordt de gehele Onderhoudscontrolelijst gemarkeerd als **Mislukt** in Activabeheer. |
| Gereed                         | Stel deze optie in op **Ja** als de taakplanning van de werkorder voor alle werkordertaken die zijn gemaakt voor een werkorder automatisch moet worden bijgewerkt naar **Gereed** wanneer de werkorder wordt bijgewerkt naar deze levenscyclusstatus. |
| Begin                         | Stel deze optie in op **Ja** als de taakplanning van de werkorder voor alle werkordertaken die zijn gemaakt voor een werkorder automatisch moet worden bijgewerkt naar **Gestart** wanneer de werkorder wordt bijgewerkt naar deze levenscyclusstatus. |
| Einde                           | Stel deze optie in op **Ja** als de taakplanning van de werkorder voor alle werkordertaken die zijn gemaakt voor een werkorder automatisch moet worden bijgewerkt naar **Beëindigd** wanneer de werkorder wordt bijgewerkt naar deze levenscyclusstatus. |
| Planningsregels verwijderen         | Stel deze optie in op **Ja** als de taakplanning van de werkorder voor alle werkordertaken die zijn gemaakt voor een werkorder die al is gepland, automatisch moet worden bijgewerkt naar Gereed wanneer de werkorder wordt bijgewerkt naar deze levenscyclusstatus. Met andere woorden, de capaciteitsreserveringen voor het activum, de gerelateerde onderhoudswerknemer en bijbehorende tools worden verwijderd. U stelt deze optie bijvoorbeeld instellen op **Ja** voor de levenscyclus van werkorders met de naam **Geraamd.** Wanneer een werkorder vervolgens wordt hersteld naar deze levenscyclusstatus omdat herplanning is vereist, kan de planning worden verwijderd voor die werkorder. |

## <a name="set-up-project-stages-and-work-order-lifecycle-states"></a>Projectfasen en levenscyclusstatussen van werkorders instellen

1. Klik op **Projectmanagement en boekhouding** \> **Instellen** \> **Projectmanagement- en boekhoudingsparameters**.
2. Schakel in het tabblad **Projectfase** voor elke fase die u wilt gebruiken, het selectievakje in voor elk projecttype dat voor uw werkorders is vereist. De projecttypen definiëren regels over de toegestane financiële taken. Voorbeelden van financiële taken zijn het maken van een prognose, het maken van ramingen en het maken van beginsaldi.

    > [!IMPORTANT]
    > Als geen projectfase is geselecteerd voor een projecttype, maar de projectfase wordt gebruikt voor de levenscyclusstatus van werkorders, worden de werkorderprojecten niet op de juiste manier bijgewerkt.

3. Sluit de pagina **Projectmanagement en boekhoudingsparameters**.
4. Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Levenscyclusstatussen**.
5. Selecteer **Nieuw** om een levenscyclusstatus te maken.
6. Voer in het veld **Levenscyclusstatus** een id voor de levenscyclusstatus in.
7. Voer in het veld **Naam** een naam in.

    In het Sneltabblad **Details** wordt in het veld **Levenscyclusmodellen** het aantal levenscyclusmodellen van werkorders weergegeven die deze levenscyclusstatus gebruiken.

8. Selecteer in het Sneltabblad **Algemeen** in de sectie **Werkorder** de functies die beschikbaar moeten zijn voor deze levenscyclusstatus door de relevante opties in te stellen op **Ja**. Zie voor beschrijvingen van de opties de tabel eerder in dit onderwerp.
9. Selecteer in de sectie **Project** in het veld **Fase** de projectfase die aan deze levenscyclusstatus moet worden gerelateerd.
10. Stel in de sectie **Project** de optie **Activiteiten afsluiten** in op **Ja** als projectactiviteiten die aan elke werkordertaak zijn gekoppeld, automatisch moeten worden gesloten wanneer de werkorder zich in deze levenscyclusstatus bevindt.

    > [!NOTE]
    > Als u het nummer wilt weten van de projectactiviteit die aan een werkordertaak is gekoppeld, selecteert u **Activiteitenbeheer** \> **Algemene** \> **Werkorders** \> **Alle werkorders**, **Actieve werkorders** of **Mijn actieve werkorders**. Open de werkorder en selecteer vervolgens de werkordertaak. Het activiteitsnummer wordt weer gegeven in het veld **Activiteitsnummer** in de sectie **Project** in het tabblad **Algemeen** van het Sneltabblad **Regeldetails**.

11. In de sectie **Prognose** stelt u de optie **Uurprognose kopiëren**, **Artikelprognose kopiëren** en/of **Onkostenprognose kopiëren** in op **Ja** als projectprognoses voor werkorders automatisch moeten worden gekopieerd naar werkorderjournalen wanneer de werkorder zich in deze levenscyclusstatus bevindt.
12. Stel in sectie **Planning** een van de opties in op **Ja** als de planningsstatus voor werkordertaken moet worden bijgewerkt wanneer de werkorder zich in deze levenscyclusstatus bevindt. Zie de tabel eerder in dit onderwerp voor beschrijvingen van de opties **Gereed**, **Start**, **Einde** en **Planningsregels verwijderen**.

    > [!NOTE]
    > Als u het planningsregels wilt zien die aan werkordertaken zijn gekoppeld, selecteert u **Activiteitenbeheer** \> **Algemene** \> **Werkorders** \> **Alle werkorders**, **Actieve werkorders** of **Mijn actieve werkorders**. Open de werkorder, selecteer de werkordertaak op het Sneltabblad **Werkordertaken** en bekijk gerelateerde informatie over het Sneltabblad **Regeldetails**. In het veld **Status** op het tabblad **Planning** wordt de status van de werkordertaak weergegeven. Het veld **Status** kan op de volgende waarden worden ingesteld: **Gepland**, **Gereed**, **Gestart**, **Gestopt**en **Beëindigd**.

13. Selecteer in de sectie **Onderhoudsverzoeken** in het veld **Levenscyclusstatus** de levenscyclusstatus van het onderhoudsverzoek waarnaar gerelateerde onderhoudsverzoeken moeten worden bijgewerkt. Deze update wordt automatisch uitgevoerd. U kunt dit alleen doen als de status van de levenscyclusstatus van het onderhoudsverzoek is geselecteerd in het model voor de levenscyclusstatus van het onderhoudsverzoek dat wordt gebruikt voor het onderhoudsverzoek.
14. Stel in sectie **Activa** de optie **Activumstuklijst bijwerken** in op **Ja** als alle artikelen die op een werkorder worden gebruikt, automatisch moeten worden bijgewerkt op de pagina **Activumstuklijst** wanneer de werkorder wordt bijgewerkt met deze levenscyclusstatus. Deze instelling kan relevant zijn als bijvoorbeeld de levenscyclusstatus van de werkorder de werkorder als voltooid of beëindigd definieert.
15. In de sectie **Werkordergroep** stelt u de optie **Groepsverwijzing verwijderen** in op **Ja** als werkorders die zich in deze levenscyclusstatus bevinden, automatisch moeten worden verwijderd uit de werkordergroepen.
16. Selecteer in het Sneltabblad **Valideren** de validatietypen die in deze levenscyclusstatus moeten worden geactiveerd door de relevante opties op **Ja**in te stellen. Selecteer vervolgens in het veld **Type** voor elk validatietype dat u selecteert, het type bericht dat moet worden weer gegeven als verplichte velden, die zijn gerelateerd aan het validatietype, niet zijn gevalideerd. Als u **Fout**selecteert, wordt de status van de levenscyclusstatus van de werkorder geannuleerd totdat de gerelateerde verplichte velden op de werkorder zijn bijgewerkt.

    - De opties voor **Onderhoudsuitval**, **Onderhoudscontrolelijst**, **Probleemsymptomen**, **Probleemoorzaken** en **Probleemoplossingen** zijn gerelateerd aan de opties in de sectie **Verplicht** op de pagina **Werkordertypes** (**Activabeheer** \> **Instellingen** \> **Werkorders** \> **Werkordertypes**). Als u deze validaties wilt activeren, moeten de gerelateerde opties ook op **Ja** zijn ingesteld op het werkordertype dat voor de werkorder wordt gebruikt.
    - Als de optie **Onderhoudscontrolelijst** is ingesteld op **Ja** voor de levenscyclusstatus waarin een werkorder wordt bijgewerkt, wordt validatie uitgevoerd om te controleren of regels voor onderhoudscontrolelijsten die zijn gemarkeerd als **Verplicht**, zijn geregistreerd als **Gecontroleerd** of **Niet van toepassing**. Als geen van deze registraties is uitgevoerd op de verplichte regels, wordt een informatief, fout- of waarschuwingsbericht weergegeven wanneer de werkorder wordt bijgewerkt tot deze levenscyclusstatus.
    - Als de optie **Toegezegde kosten** is ingesteld op **Ja** voor de levenscyclusstatus waaraan een werkorder wordt bijgewerkt, wordt het totale bedrag aan toegezegde kosten (het totale bedrag aan onkosten dat de rechtspersoon heeft toegezegd te betalen) berekend voor elke werkordertaak. Een bericht wordt weergegeven als het toegezegde kostenbedrag groter dan 0 (nul) is. U selecteert de typen kostentoezeggingen die worden opgenomen in het Sneltabblad **Kostentoezeggingen** in het tabblad **Kostenbeheer** van de pagina **Projectmanagement- en boekhoudparameters** (**Projectmanagement en boekhouding** \> **Instellingen** \> **Projectmanagement- en boekhoudparameters**).
    - Als de optie **Onderhoudsuitval** is ingesteld op **Ja** voor de levenscyclusstatus waaraan een werkorder wordt bijgewerkt, wordt de tijdige validatie van de uitvaltijd uitgevoerd op het activum dat aan de werkorder is gekoppeld. Als er een tijdregistratie voor onderhoud is uitgevoerd maar er is geen registratie **Beëindigd**, wordt een bericht weergegeven wanneer de werkorder wordt bijgewerkt tot deze levenscyclusstatus.
    - Als de standaard projectinstellingen niet alle fasen bevatten die u nodig hebt voor de instellingen van het Activabeheer, kunt u door de gebruiker gedefinieerde projectfasen instellen in het tabblad **Projectfase** van de pagina **Projectmanagement- en boekhoudparameters**. In de volgende afbeelding ziet u het tabblad **Projectfase** op de pagina **Projectmanagement- en boekhoudparameters**.

    ![Pagina Projectfasen instellen voor diverse projecttypen](media/10-setup-for-work-orders.png)

> [!NOTE]
> Als de levenscyclusstatus waarvoor u een werkorder bijwerkt inactief is, worden journalen die aan de werkorder zijn gekoppeld, maar die nog niet zijn geboekt, automatisch verwijderd. Hierdoor kunnen ongebruikte gegevens automatisch worden opgeruimd. (Een levenscyclusstatus is niet actief als de optie **Actief** voor deze optie is ingesteld op **Nee** in het Sneltabblad **Algemeen** van de pagina **Levenscyclusstatus van werkorders**.)
>
> Als u een werkorder echter zodanig instelt dat hij inactief is, worden journalen die aan de werkorder zijn gekoppeld, maar die nog niet zijn geboekt, **niet** automatisch verwijderd. (Als u een werk order handmatig wilt deactiveren, selecteert u **Activabeheer** \> **Algemene** \> **Werkorders** \> **Alle werkorders** of **Actieve werkorders**. Open de werkorder en schakel over naar de **Koptekst**-weergave. Selecteer in het Sneltabblad **Algemeen** **Bewerken** en stel vervolgens de optie **Actief** in op **Nee**.)

## <a name="relations-among-work-order-lifecycle-models-work-order-types-and-work-order-lifecycle-states"></a>Relaties tussen levenscyclusmodellen van werkorders, werkordertypes en levenscyclusstatus van werkorders.

Levenscyclusmodellen verwijzen naar workflows en levenscyclusstatussen worden in sequentiële volgorde geselecteerd in een levenscyclusmodel. Er worden levenscyclusmodellen ingesteld voor werkordertypen. Met werkordertypen wordt de grootte of omvang van workflows en werkprocessen bepaald. **Onderhoud**, dat een standaard werkordertype is, is bijvoorbeeld mogelijk gerelateerd aan een levenscyclusmodel voor werkorders met vele levenscyclusstatussen. U kunt daarentegen een werkordertype **Corrigerend** hebben, dat wordt gebruikt voor werkorders die nog niet zijn gepland, of voor werkorders waarvoor de taak is voltooid voordat de werkorder wordt gemaakt vanwege een urgente situatie. Dit type werkorder is mogelijk gerelateerd aan een levenscyclusmodel van een werkorder model met slechts enkele levenscyclussen.

De reden voor het gebruik van typen is dat wanneer een type wordt gedefinieerd voor bijvoorbeeld een werkorder of een activum, de gerelateerde werkprocessen (levenscyclusstatussen) automatisch worden gedefinieerd. Zie [Werkordertypes](../setup-for-work-orders/work-order-types.md) voor meer informatie over het instellen van werkordertypes.

> [!NOTE]
> De levenscyclusstatussen, levenscyclusmodellen en types zijn ook van toepassing op functionele locaties, activa en onderhoudsverzoeken, naast werkorders.

In de volgende afbeelding ziet u de relatie tussen werkordertypen, levenscyclusmodellen en levenscyclusstatussen.

![Pagina Werkordertype vergeleken met pagina Levenscyclusmodellen van werkorder](media/11-setup-for-work-orders.png)

## <a name="work-order-lifecycle-models"></a>Levenscyclusmodellen van werkorder

Nadat u de levenscyclusstatussen voor werkorders hebt gemaakt die vereist zijn voor uw werkorders, kunnen deze worden onderverdeeld in levenscyclusmodellen. U moet minimaal één standaard levenscyclusmodel maken.

1. Selecteer **Activabeheer** \> **Instellingen** \> **Werkorders** \> **Levenscyclusmodellen**.
2. Selecteer **Nieuw** om een levenscyclusmodel te maken.
3. Voer in het veld **Levenscyclusmodel** de id van het levenscyclusmodel in.
4. Voer in het veld **Naam** een naam in.

    In het Sneltabblad **Details** toont het veld **Levenscyclusstatussen** het aantal levenscyclusstatussen die in dit levenscyclusmodel zijn geselecteerd. Het veld **Werkordertypes** bevat het aantal typen werkordertypes dat gebruikmaakt van dit levenscyclusmodel.

5. Ga naar het sneltabblad **Levenscyclusstatussen** en selecteer de levencyclusstatussen die moet worden opgenomen in het levenscyclusmodel:

    - Als u een levenscyclusstatus wilt opnemen in het levenscyclusmodel, selecteert u deze in de sectie **Resterende levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-rechts ![Pijl-rechts](media/12-setup-for-work-orders.png) om deze te verplaatsen naar de sectie **Geselecteerde levenscyclusstatussen**.
    - Als u alle beschikbare levenscyclusstatussen in het levenscyclusmodel wilt opnemen, selecteert u de knop **Alle beschikbare statussen selecteren** ![Alle beschikbare statussen selecteren](media/13-setup-for-work-orders.png). Alle levenscyclusstatussen worden verplaatst naar de sectie **Geselecteerde levenscyclusstatussen**.
    - Als u een levenscyclusstatus uit het levenscyclusmodel wilt verwijderen, selecteert u deze in de sectie **Geselecteerde levenscyclusstatussen** en selecteert u vervolgens de knop Pijl-links ![Pijl-links](media/14-setup-for-work-orders.png) om deze te verplaatsen naar de sectie **Resterende levenscyclusstatussen**.

6. Selecteer **Updates van levenscyclusstatussen** om de levenscyclusstatussen te definiëren die een geselecteerde levenscyclusstatus kunnen volgen.
7. Selecteer in het Sneltabblad **Updates** in het veld **Geplande status** de levenscyclusstatus die altijd moet worden geselecteerd voor een werkorder waarvoor u de werkorderplanning hebt voltooid, ongeacht de vorige levenscyclusstatus van de werkorder.
8. Selecteer in het veld **Niet-geplande levenscyclusstatus** de levenscyclusstatus die altijd moet worden geselecteerd voor een werkorder als de werkorderplanning wordt verwijderd.
9. Sla het levenscyclusmodel voor de werkorder op.

![Pagina Levenscyclusmodellen van werkorder](media/15-setup-for-work-orders.png)
