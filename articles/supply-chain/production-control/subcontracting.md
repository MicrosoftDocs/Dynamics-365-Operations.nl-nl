---
title: Werk uitbesteden
description: Dit onderwerp helpt u een procedure voor het uitbesteden van werk in de productie op te zetten in Dynamics 365 Supply Chain Management.
author: christophernread
manager: tfehr
ms.date: 09/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2018-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3e282e0676e53200b0993dd9cb2b52e08fe97dca
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4981451"
---
# <a name="subcontracting"></a>Werk uitbesteden

[!include [banner](../includes/banner.md)]

Dit onderwerp helpt u een procedure voor het uitbesteden van werk in de productie op te zetten in Microsoft Dynamics 365 Supply Chain Management. In het eerste deel van dit onderwerp wordt beschreven hoe u de gegevens instelt. In het tweede deel doorloopt u de stappen in de procedure.

## <a name="target-audience"></a>Doelgroep

In dit onderwerp leert u hoe u de uitbesteding van werk in productie instelt. U gebruikt bestaande gegevens in de rechtspersoon HQUS om de basisinstellingen voor een stroom uitbestedingsactiviteiten te configureren. De voorbeeldgegevens in de rechtspersoon HQUS omvatten onder andere instellingsparameters die vooraf zijn ingesteld ter ondersteuning van de stappen in deze procedure. Hoewel in de procedure belangrijke knelpunten en uitdagingen voor verschillende rollen aan bod komen, kan de systeembeheerder deze procedure voltooien.

## <a name="demo-scenario"></a>Demonstratiescenario

In de rechtspersoon HQUS worden geavanceerde luidsprekers geproduceerd. Tijdens het productieproces doorlopen de luidsprekers de volgende drie bewerkingsfasen.

- **Voormontage**: de luidsprekerkast wordt gemonteerd. Het materiaal voor de kast wordt in het magazijn geselecteerd voordat de fase wordt gestart.
- **Bekleding**: nadat de luidsprekerkast is gemonteerd, moet deze worden bekleed. Deze bewerking wordt voltooid door een leverancier (onderaannemer). De voorgemonteerde luidsprekerkast wordt met twee materialen verzonden naar de onderaannemer die de bekleding aanbrengt.
- **Afwerking**: als de voorgemonteerde luidsprekerkast is bekleed door de onderaannemer, wordt deze weer geretourneerd naar de rechtspersoon HQUS zodat de eindmontage van de luidspreker kan worden voltooid.

In de volgende afbeelding worden de drie bewerkingsfasen en de verbruikte materialen weergegeven.

![De bewerkingen Voormontage, Bekleding en Afwerking en de materialen die hierin worden verbruikt](./media/subcontract01_operations-materials.png)

## <a name="setup"></a>Instelling

Voordat u de procedure start, moet u de gegevens instellen.

### <a name="set-up-the-finished-product"></a>Het voltooide product instellen

In deze procedure wordt u door het proces voor het instellen van het vrijgegeven product D8100 Kast met bekleding gevoerd.

1. Selecteer **Productgegevensbeheer \> Producten \> Vrijgegeven producten** om de pagina **Vrijgegeven productdetails** te openen.
2. Voer in het snelfilterveld **D8100** in om het bestaande vrijgegeven product te vinden.

    ![Filteren op het vrijgegeven product D8100 op de pagina Vrijgegeven productdetails](./media/subcontract02_filtering-released-products.png)

3. Selecteer in het actievenster op het tabblad **Technicus** de optie **Route** om de pagina **Route** te openen.

    Op de pagina **Route** worden de acht routeversies voor vrijgegeven product D8100 weergegeven. De acht routeversies worden verdeeld over vier routes op locatie 1 en locatie 5. Route 000400 wordt gebruikt voor kostprijsberekening, route 00041 wordt gebruikt wanneer de bewerking Bekleding intern wordt afgehandeld en route 00042 wordt gebruikt wanneer de bewerking Bekleding een externe aangelegenheid is.

    ![Acht routeversies op de pagina Route](./media/subcontract03_route-page.png)

4. Selecteer in het bovenste deelvenster in het raster **Versies** routeversie **00042** voor locatie **5**.
5. Selecteer in het onderste deelvenster op het tabblad **Overzicht** bewerking **20** (**Cbnt CtSc**) in het raster.

    ![Bewerking 20 voor routeversie 00042 voor locatie 5 geselecteerd](./media/subcontract04_route-version-operation.png)

6. Selecteer het tabblad **Algemeen**.

    Het veld **Routetype** is ingesteld op **Leverancier**. Deze waarde geeft aan dat bewerking 20 (Cbnt CtSc) een uitbestede bewerking is.

    ![Het veld Routetype is ingesteld op Leverancier op het tabblad Algemeen](./media/subcontract05_general-tab.png)

7. Selecteer het tabblad **Resourcevereisten**.

    Capaciteiten worden gebruikt om een geschikte resource te vinden tijdens de productieplanning. Voor bewerking 20 (Cbnt CtSc) is een resource met twee capaciteiten, namelijk **Bekleding** en **Kasten met bekleding**, nodig.

    ![De capaciteiten Bekleding en Kasten met bekleding op het tabblad Resourcevereisten](./media/subcontract06_resource-requirements-tab.png)

8. Selecteer **Toepasselijke resources** om het dialoogvenster **Toepasselijke resources** te openen.

    Er worden drie resources gevonden die overeenkomen met de resourcevereisten voor de bewerking. Resources 8851 en 8852 zijn van het type **Leverancier**.

    ![Drie toepasselijke resources in het dialoogvenster Toepasselijke resources](./media/subcontract07_applicable-resources-dialog.png)

9. Selecteer **OK** om het dialoogvenster **Toepasselijke resources** te sluiten en terug te keren naar de pagina **Route**.
10. Sluit de pagina **Route** om terug te keren naar de pagina **Vrijgegeven productdetails**.

    ![Pagina Vrijgegeven productdetails](./media/subcontract08_released-product-details-page.png)

11. Selecteer in het actievenster op het tabblad **Technicus** de optie **Stuklijstversies** om de pagina **Stuklijstversies** te openen.

    Op de pagina **Stuklijstversies** worden de vier stuklijstversies voor vrijgegeven product D8100 weergegeven. Stuklijst 000040 wordt gebruikt voor kostprijsberekening en planning, stuklijst 000041 wordt gebruikt als de bewerking Bekleding intern wordt uitgevoerd en stuklijsten 000042 en 000043 worden gebruikt als de bewerking Bekleding wordt uitbesteed.

    Artikel S8050 is een product van het artikeltype **Service**. Dit artikel vertegenwoordigt het uitbestede werk.

    ![Vier stuklijstversies op de pagina Stuklijstversies](./media/subcontract09_bom-versions-page.png)

12. Selecteer op het sneltabblad **Stuklijstregels** de optie **Bewerken** om het dialoogvenster **Stuklijstregel bewerken** te openen.

    Wanneer een productieorder wordt gemaakt en geraamd voor vrijgegeven product D8100, wordt er automatisch een inkooporder gegenereerd voor artikel S8050. Deze inkooporder wordt gekoppeld aan de productieorder. Inkooporders worden automatisch gegenereerd als het veld **Regeltype** is ingesteld op **Leverancier** en de leverancierrekening voor de toeleverancier is geselecteerd. In dit geval is de leverancierrekening US-801.

    De stuklijstregel is verbonden met de bewerking Bekleding via het bewerkingsnummer (in dit geval 20).

    ![Dialoogvenster Stuklijstregel bewerken](./media/subcontract10_edit-bom-line-dialog.png)

### <a name="create-a-password-for-warehouse-workers"></a>Een wachtwoord maken voor magazijnmedewerkers

U moet een wachtwoord definiëren voor de magazijnmedewerkers die het handheld-apparaat gebruiken.

1. Selecteer **Magazijnbeheer \> Instellen \> Werknemer** om de pagina **Werkgebruikers** te openen.
2. Selecteer op het sneltabblad **Gebruikers** de rij voor gebruiker **51**.

    ![Pagina Werkgebruikers](./media/subcontract11_work-users-page.png)

3. Selecteer **Wachtwoord opnieuw instellen**.
4. Voer in de velden **Wachtwoord** en **Wachtwoord bevestigen** de waarde **1** in.
5. Selecteer **Wachtwoord instellen**.

## <a name="step-by-step-walkthrough"></a>Stapsgewijze procedure

**Scenario en achtergrond**

Er wordt een productieorder van 10 stuks gemaakt voor het product D8100, Kast met bekleding. De bekleding van de kasten is een uitbestede bewerking die wordt uitgevoerd door leverancier US-801 Perfecte bekledingen. De productieorder omvat drie bewerkingen. In de eerste fase wordt de kast intern voorgemonteerd. Het materiaal voor de voormontage wordt vrijgegeven voor orderverzamelen in het magazijn voor grondstoffen. Als de voormontage is voltooid, wordt de voorgemonteerde kast naar Perfecte bekledingen verzonden met twee materialen die vereist zijn voor de bekleding. Als de beklede kast weer terugkomt van de leverancier, wordt de eindmontage intern uitgevoerd voordat deze als voltooid wordt gerapporteerd.

1. Selecteer **Productiebeheer \> Productieorders \> Alle productieorders** om de pagina **Alle productieorders** te openen.
2. Selecteer in het actievenster de optie **Nieuwe productieorder** om het dialoogvenster **Productieorder maken** te openen.

    ![Dialoogvenster Productieorder maken](./media/subcontract12_create-production-order-dialog.png)

3. Selecteer in het veld **Artikelnummer** de optie **D8100**.
4. De velden met voorraaddimensies worden weergegeven wanneer u het artikelnummer hebt geselecteerd. Selecteer **Chroom** in het veld **Kleur**.

    Er wordt een berichtvenster weergegeven waarin u wordt gevraagd of de actieve versies voor de stuklijst en route moeten worden ingevoegd.

    ![Berichtvenster](./media/subcontract13_message-box.png)

5. Selecteer **Ja**. 

    In het dialoogvenster **Productieorder maken** worden de actieve versies van de stuklijst en route voor product D8100 automatisch geselecteerd in de velden **Stuklijstnummer** en **Routenummer**. In dit geval zijn stuklijst **000040** en route **000040** geselecteerd.
    
    > [!NOTE]
    > Zowel voor de stuklijst als voor de route wordt versie 000040 gebruikt voor kostprijsberekening en planning.

6. Selecteer **5** in het veld **Locatie**.
7. Selecteer **51** in het veld **Magazijn**.
8. Wijzig in de velden **Stuklijstnummer** en **Routenummer** de automatisch geselecteerde waarde in **000042**.

    > [!NOTE]
    > Voor de stuklijst en de route wordt versie 000042 gebruikt om de bekleding van de kast ui te besteden aan leverancier US-801.

    ![Ingestelde waarden in het dialoogvenster Productieorder maken](./media/subcontract14_create-production-order-dialog-set.png)

9. Selecteer **Maken** om de productieorder te maken en terug te keren naar de pagina **Alle productieorders**.

    ![Nieuwe productieorder op de pagina Alle productieorders](./media/subcontract15_new-production-order.png)

10. Selecteer in het actievenster op het tabblad **Productieorder** de optie **Raming** om het dialoogvenster **Raming** te openen.

    ![Dialoogvenster Raming](./media/subcontract16_estimate-dialog.png)

11. Selecteer **OK** om de raming te bevestigen en terug te keren naar de pagina **Alle productieorders**.

    > [!NOTE]
    > Wanneer de productieorder is geraamd, wordt de inkooporder voor serviceartikel S8050 gegenereerd voor leverancier US-801.

12. Klik in het actievenster op het tabblad **Productieorder** op de optie **Stuklijst** om de pagina **Stuklijst** te openen, waarop u de stuklijstregels voor de productieorder kunt bekijken.

    Voor serviceartikel S8050 bestaat er een verwijzing naar de inkooporder die is gegenereerd toen de productieorder werd geraamd.

    ![Stuklijstregels in de productieorder op de pagina Stuklijst](./media/subcontract17_production-order-bom-lines.png)

13. Sluit de pagina **Stuklijst** om terug te keren naar de pagina **Alle productieorders**.
14. Selecteer in het actievenster op het tabblad **Planning** de optie **Taken plannen** om het dialoogvenster **Taakplanning** te openen.
15. Geef de volgende waarden op:

    - Selecteer in het veld **Planningsrichting** de optie **Verder vanaf vandaag**.
    - Stel de optie **Eindige capaciteit** in op **Ja**.

    ![Dialoogvenster Taakplanning](./media/subcontract18_job-scheduling-dialog.png)

16. Selecteer **OK** om het dialoogvenster **Taakplanning** te sluiten en terug te keren naar de pagina **Alle productieorders**.
17. In het actievenster selecteert u op het tabblad **Planning** de optie **Gantt** om de pagina **Gantt-diagram - Bronweergave** te openen.

    Het Gantt-diagram biedt een visueel overzicht van hoe de productietaken zijn gepland voor de resources. De externe bewerking Bekleding bestaat uit drie taken: een verwerkingstaak, een transporttaak en een wachtrijtijdtaak.

    ![Gantt-diagram op de pagina Gantt-diagram - Bronweergave](./media/subcontract19_gantt-chart.png)

18. Sluit de pagina **Gantt-diagram - Bronweergave** om terug te keren naar de pagina **Alle productieorders**.
19. Selecteer in het actievenster op het tabblad **Productieorder** de optie **Vrijgave** om het dialoogvenster **Vrijgave** te openen.

    ![Dialoogvenster Vrijgave](./media/subcontract20_release-dialog.png)

20. Selecteer **OK** om het dialoogvenster **Vrijgave** te sluiten.
21. Selecteer **Productiebeheer \> Periodieke taken \> Vrijgeven aan magazijn \> Stuklijst en formuleregels automatisch vrijgeven** om het dialoogvenster **Stuklijst en formuleregels automatisch vrijgeven** te openen.

    ![Dialoogvenster Stuklijst en formuleregels automatisch vrijgeven](./media/subcontract21_auto-release-bom-formula-lines-dialog.png)

22. Selecteer **OK** om de taak Stuklijst en formuleregels automatisch vrijgeven uit te voeren.

    Met deze taak wordt verzamelwerk voor grondstoffen naar het magazijn vrijgegeven.

23. Selecteer **Productiebeheer \> Productieorders \> Alle productieorders** om de pagina **Alle productieorders** te openen.
24. Met het snelfilterveld kunt u de productieorder selecteren waaraan u hebt gewerkt.
25. Selecteer in het actievenster op het tabblad **Magazijn** de optie **Werkgegevens** om de pagina **Werk** te openen.

    Op de pagina worden twee soorten werk voor de orderverzameling van grondstoffen weergegeven. Het eerste werk is voor de materialen M8100 en M8101. De materialen worden verbruikt door bewerking 10. Het tweede werk is voor de materialen M8202 en M8250. Deze materialen worden verbruikt door bewerking 20, de uitbestede bewerking.

    ![Twee soorten werk voor orderverzameling van grondstoffen op de pagina Werk](./media/subcontract22_work-page.png)

26. Start de magazijn-app om het magazijnwerk voor bewerking 10 te starten.

    <!-- TBD – screen shots for processing pick work for the materials. -->

27. Selecteer **Productiebeheer \> Productieorders \> Alle productieorders** om de pagina **Alle productieorders** te openen.
28. Met het snelfilterveld kunt u de productieorder selecteren waaraan u hebt gewerkt.
29. Selecteer in het actievenster op het tabblad **Productieorder** de optie **Beginnen** om het dialoogvenster **Starten** te openen.
30. Geef op het tabblad **Algemeen** de volgende waarden op:

    - Selecteer in het veld **Van bewerkingsnummer** de optie **10**.
    - Selecteer in het veld **Tot bewerkingsnummer** de optie **10**.

    ![Ingestelde waarden op het tabblad Algemeen](./media/subcontract23_start-dialog.png)

31. Selecteer **OK** om het dialoogvenster **Starten** te sluiten en terug te keren naar de pagina **Alle productieorders**.

    De status van de productieorder is nu **Gestart**. De materialen voor bewerking 10 worden verbruikt door een automatische boeking van het orderverzamellijstjournaal. Het tijdverbruik voor bewerking 10 wordt verantwoord door een automatische boeking van een routekaartjournaal.

32. Start de magazijn-app om het magazijnwerk voor bewerking 20 te starten.

    <!-- TBD – screen shots for processing pick work for the materials. -->

33. Selecteer in het actievenster op het tabblad **Productieorder** de optie **Beginnen** om het dialoogvenster **Starten** te openen.
34. Geef op het tabblad **Algemeen** de volgende waarden op:

    - Selecteer in het veld **Van bewerkingsnummer** de optie **20**.
    - Selecteer in het veld **Tot bewerkingsnummer** de optie **20**.
    - Typ **10** in het veld **Hoeveelheid**.
    - Selecteer **Nee** in het veld **Orderverzamellijst nu boeken**.

    ![Ingestelde waarden op het tabblad Algemeen](./media/subcontract24_general-tab.png)

35. Selecteer **OK** om het dialoogvenster **Starten** te sluiten en terug te keren naar de pagina **Alle productieorders**.

    Er wordt een orderverzamellijst gemaakt voor de materialen die worden gebruikt voor de bewerking Bekleding en voor het serviceartikel. Het serviceartikel staat voor de kosten van de uitbestede bewerking.

36. In het actievenster selecteert u op het tabblad **Weergave** de optie **Orderverzamellijst** om de pagina **Orderverzamellijst** te openen.
37. Selecteer de orderverzamellijst die niet is geboekt en selecteer vervolgens het journaalnummer om de journaalregels weer te geven.

    ![Journaalregels op de pagina Orderverzamellijst](./media/subcontract25_picking-list.png)

38. Selecteer in het actievenster **Afdrukken** \> **Orderverzamellijst (rapport)** om het dialoogvenster **Orderverzamellijst (rapport)** te openen.
39. Stel de optie **Indeling van afleveringsbewijs gebruiken** in op **Ja**.

    ![Dialoogvenster Orderverzamellijst (rapport)](./media/subcontract26_picking-list-report-dialog.png)

40. Selecteer **OK** om een rapport **Orderverzamellijst** te genereren.

    In dit geval wordt een afleveringsbewijs van leverancier afgedrukt vanuit het productieorderverzamellijstjournaal. In het afleveringsbewijs wordt aangegeven welke materialen worden verzonden naar de leverancier die de bewerking Bekleding uitvoert.

    ![Orderverzamellijst (rapport)](./media/subcontract27_picking-list-report.png)

41. Sluit het rapport **Orderverzamellijst** om terug te keren naar de pagina **Orderverzamellijst**.
42. Selecteer in het actievenster de optie **Boeken** om het dialoogvenster **Journaal boeken** te openen.

    ![Dialoogvenster Journaal boeken](./media/subcontract28_post-journal-dialog.png)

43. Selecteer **OK** om het dialoogvenster **Journaal boeken** te sluiten.
44. Open de inkooporder.

    ![Pagina Inkooporder](./media/subcontract29_purchase-order-page.png)

45. Selecteer in het actievenster op het tabblad **Inkoop** de optie **Bevestigen**.
46. Selecteer **Boeken** om het dialoogvenster **Journaal boeken** te openen.
47. Selecteer **OK** om het dialoogvenster **Journaal boeken** te sluiten en terug te keren naar de pagina **Inkooporder**.
48. Wijzig de eenheidsprijs van **33** in **40**.

    ![Gewijzigde eenheidsprijs op de pagina Inkooporder](./media/subcontract30_unit-price.png)

49. Bevestig de inkooporder opnieuw.
50. Productontvangstbon.

    ![Dialoogvenster Productontvangstbon boeking](./media/subcontract31_posting-product-receipt-dialog.png)

51. Inkoopfactuur.
52. Werk de vereffeningsstatus bij.

    ![Pagina Leveranciersfactuur](./media/subcontract32_vendor-invoice-page.png)

53. Rapporteren als gereed.

    ![Dialoogvenster Rapporteren als gereed](./media/subcontract33_report-as-finished-dialog.png)

54. Einde.

    ![Dialoogvenster Einde](./media/subcontract34_end-dialog.png)

55. Kostenvergelijking.

    ![Kostenvergelijkingsdiagrammen](./media/subcontract35_cost-comparison-charts.png)

Ontbrekende instellingen in gegevens.
