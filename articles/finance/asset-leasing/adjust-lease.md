---
title: Leases aanpassen
description: In dit onderwerp wordt uitgelegd hoe u een lease kunt aanpassen. Aanpassingen kunnen nodig zijn als de leasetermijnen worden gewijzigd, de lease wordt verlengd of andere omstandigheden veranderen.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 32d99d9e90b65f7cac74176d21fa4b053ae8f62c
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130750"
---
# <a name="adjust-leases"></a>Leases aanpassen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u een lease kunt aanpassen. Aanpassingen kunnen nodig zijn als de leasetermijnen worden gewijzigd, de lease wordt verlengd of andere omstandigheden veranderen. Het leasen van activa voldoet aan de richtlijnen die de Accounting Standards Codification Topic 842 (ASC 842) en International Financial Reporting Standard 16 (IFRS 16) bieden over leasewijzigingen. In ASC 842-20-15-1 wordt een wijziging in de lease gedefinieerd als elke wijziging in de voorwaarden van een contract waardoor een wijziging in de omvang of de interpretatie van de lease wordt veroorzaakt. In IFRS 39 van IFRS 16 wordt aangegeven dat een leasenemer de leaseverplichtingen moet herwaarderen, zodat deze wijzigingen in de leasebetalingen weerspiegelen.

Voor organisaties die zich houden aan ASC 842 of IFRS 16, wordt een lease aangepast om een wijziging in de contante waarde van de toekomstige minimale leasebetalingen (PVFMLP) aan te geven. Als de PVFMLP toeneemt, is de gemaakte journaalpost een debetpost voor het activumaccount met gebruiksrecht en een creditpost voor het leaseverplichtingenaccount om het verschil tussen de nieuwe PVFMLP en de vorige PVFMLP aan te geven. Als de PVFMLP afneemt, is de journaalpost voor het verschil een debetbedrag voor het leaseverplichtingenaccount en een creditbedrag voor het RoU-activumaccount.

Als door de correctie het RoU-activum onder 0 (nul) zakt, wordt het restbedrag bijgeschreven bij de winst op de boekingsrekening voor de leasewijziging die is opgegeven op de pagina **Leaseboekingsrekeningen**. De systeem geeft deze transacties en andere correctieposten weer, zoals classificatiewijzigingen, initiële directe kosten, leasebonussen, vooruitbetalingen en ontmantelingskosten die voortvloeien uit leasewijzigingen.

Voor specifieke richtlijnen voor het aanpassen van leasetransacties, raden we u aan IFRS 16 en ASC 842 te bekijken.

## <a name="lease-adjustment-wizard"></a>Wizard Leasecorrectie

Voer de volgende stappen uit om een lease aan te passen. Met de gewijzigde gegevens worden de leaseschema's bijgewerkt nadat u hebt geboekt via de wizard **Leasecorrectie**. U kunt op elk moment uw werk opslaan en de wizard sluiten en later teruggaan om uw werk te hervatten.

Volg deze stappen om de wizard **Leasecorrectie** te openen vanuit het leaseoverzicht.

1. Ga naar **Activa leasen \> Leases \> Leaseoverzicht**. 
2. Selecteer de lease die u wilt aanpassen en vervolgens de **wizard Correctie**.
3. Volg de aanwijzingen in de wizard om de vereiste wijzigingen in te voeren.

Als u de wizard **Leasecorrectie** wilt openen vanaf de pagina **Leasecorrecties**, gaat u als volgt te werk voor een correctie die al wordt uitgevoerd.

1.  Ga naar **Lease \> Leases \> Leasecorrecties**.
2.  Selecteer een lease met de correctiestatus **In uitvoering** en selecteer vervolgens de **wizard Correctie**.
3.  Voer de juiste datums in de velden **Begindatum wijziging** en **Boekingsdatum** in.
4.  Selecteer **Volgende**.

    De lease wordt nu toegevoegd aan de pagina **Leasecorrecties**, waar u de nieuwe informatie kunt invoeren.

    Nadat de lease is gecorrigeerd, zijn de velden voor gebruiksrechten van toepassing. Als er geen initiële directe kosten, leasebonussen, vooruitbetalingen of ontmantelingskosten aan de gewijzigde lease worden gekoppeld, moet u de desbetreffende velden leeg laten. De oorspronkelijke bedragen zijn niet van toepassing op de bijgewerkte lease. 

    Een leaseverstrekker biedt bijvoorbeeld een bonus van USD 1.000 om een leaseverlenging te accepteren. Wanneer u in dit geval de lease corrigeert met de verlenging, voert u **1000** in het veld **Leasebonussen voortvloeiend uit de correctie** in.

    Op de regels voor het betalingsschema worden nu alle betalingen van de maand en latere maanden in het veld **Begindatum van wijziging** weergegeven. Aangezien wijzigingen mogelijk zijn, kunnen regels van het betalingsschema niet beginnen voordat de wijziging ingaat. Als u betalingsschemaregels van vóór de begindatum van de wijziging wilt weergeven, gaat u naar de pagina **Historie van leaseversie**.

8.  Selecteer **Volgende**.

    De volgende pagina bevat belangrijke details over de verwachte leasecorrectie, zoals de boekwaarden van de leaseverplichtingen vóór de wijziging en de nieuwe verwachte leaseverplichtingen na de wijziging. Op de pagina wordt ook een voorbeeld weergegeven van de journaalboeking voor de verwachte leasecorrectie.

9.  Selecteer **Indienen bij werkstroom** om de leasecorrectie bij het werkstroomsysteem in te dienen als de leasecorrectiewerkstroom actief is en de correctie nog niet is goedgekeurd. Zie [Leasecorrectiewerkstromen gebruiken](use-create-lease-wrkflw.md) voor meer informatie over hoe u de leasecorrectiewerkstroom kunt gebruiken.

    > [!NOTE]
    > Op dit punt worden de correctievariabelen opnieuw berekend om te verifiëren dat er geen transacties in de lease zijn geboekt sinds het correctieoverzicht en de correctiejournaalboeking voor het eerst zijn berekend. Als waarden worden gewijzigd, wordt het correctieoverzichtsraster bijgewerkt en kunt u de informatie controleren voordat u de leasecorrecties opnieuw indient in het werkstroomsysteem.

10. Als een werkstroom niet actief is of als de leasecorrectie is goedgekeurd, selecteert u **Voltooien** om de wijzigingen te verwerken en de boeking in het correctiejournaal te plaatsen.

    > [!NOTE] 
    > Op dit punt worden de correctievariabelen opnieuw berekend om te verifiëren dat er geen transacties in de lease zijn geboekt sinds het correctieoverzicht en de correctiejournaalboeking voor het eerst zijn berekend. Als er waarden worden gewijzigd, wordt het correctieoverzichtsraster bijgewerkt en kunt u de wijzigingen beoordelen voordat u **Voltooien** selecteert. Als de werkstroom actief is en de leasecorrectie is goedgekeurd, wordt door wijzigingen in het correctieoverzicht de goedkeuringsstatus teruggezet op **Niet ingediend**. In dit geval moet u de leasecorrectie opnieuw bij het werkstroomsysteem indienen.

    Op de pagina **Leasecorrecties** is de correctiestatus nu ingesteld op **Voltooid**.

    Op de pagina **Leasecorrecties** kunt u nog steeds de sneltabbladen **Correctieoverzicht** en **Voorbeeld van correctieboeking** weergeven. De leasegegevens en datumgegevens worden weergegeven in de versiehistorie van die lease.

    Er wordt nu een nieuwe leaseversie en een nieuwe set schema's gemaakt op basis van de gewijzigde informatie. 

13. Als u de nieuwe schema's wilt weergeven, gaat u naar de lease en selecteert u **Boeken**.
14. Als u het zojuist gegenereerde betalingsschema wilt weergeven, selecteert u **Betalingsschema**.
15. Als u het nieuwe afschrijvingsschema voor de leaseverplichtingen wilt weergeven dat is gegenereerd op basis van de nieuwe informatie, sluit u de pagina **Betalingsschema** en opent u de pagina **Afschrijvingsschema**.
16. Als u het zojuist gegenereerde afschrijvingsschema voor het activum wilt weergeven, opent u de pagina **Afschrijvingsschema voor activa** via de pagina **Boekdetails**.
17. Selecteer **Journalen \> Activaleasejournaal** om de correctieboeking in het journaal weer te geven.

## <a name="cancel-a-lease-adjustment"></a>Een leasecorrectie annuleren

Als u een leasecorrectie die in uitvoering is, wilt verwijderen, gaat u als volgt te werk.

1.  Ga naar **Lease \> Leases \> Leasecorrecties**.
2.  Selecteer de leasecorrectie die in uitvoering is om te annuleren.
3.  Selecteer **Correctie annuleren**. 
4.  Selecteer **OK**.

    > [!NOTE] 
    > Als u In de wizard **Leasecorrectie** de optie **Annuleren** selecteert, kunt u de meest recente wijziging die u in de wizard hebt voltooid, terugdraaien, maar u verwijdert geen correctie die in uitvoering is.

## <a name="use-the-lease-adjustment-workflow"></a>De werkstroom voor leasecorrectie gebruiken

In deze sectie wordt uitgelegd hoe u de werkstroom voor leasecorrectie moet gebruiken. Met de werkstroom voor leasecorrecties kunt u leasecorrecties consistent beheren door een reeks goedkeuringsstappen aan te geven en deze toe te wijzen aan specifieke gebruikers die een leasecorrectie goedkeuren voordat deze definitief wordt. Nadat de leasecorrectie is goedgekeurd in de werkstroom, kunt u de wizard **Leasecorrectie** gebruiken om de leasecorrectie te voltooien.

1.  Als u een leasecorrectie wilt indienen voor goedkeuring, gaat u naar **Lease \> Leases \> Leasecorrecties**.
2.  Selecteer de lease-id van de leasecorrectie en vervolgens de **wizard Correctie**.
3.  Selecteer **Indienen voor goedkeuring** op de laatste pagina van de wizard.
4.  Voer een opmerking over de correctie in en selecteer **OK**.

    De werkstroomstatus wordt gewijzigd in **In afwachting van goedkeuring** en alle velden in de wizard zijn vergrendeld, zodat ze niet meer kunnen worden gewijzigd.

5.  Als u de leasecorrectie wilt goedkeuren, gaat u naar **Lease \> Leases \> Leasecorrecties**.
6.  Selecteer de lease-id van de leasecorrectie en controleer de sneltabbladen **Correctieoverzicht** en **Voorbeeld van correctieboeking**.
7.  Selecteer **Werkstroom \> Goedgekeurd**.

    Op de pagina **Leasecorrecties** is de werkstroomstatus nu ingesteld op **Goedgekeurd**. Op dit moment is de leasecorrectie gereed om te worden geboekt via de boeking in het correctiejournaal.

8.  Als u wilt doorgaan met de verwerking van de leasecorrectie en de correctieboeking wilt plaatsen, gaat u naar **Lease \> Leases \> Leasecorrecties**.
9.  Selecteer de lease-id van de leasecorrectie en vervolgens de **wizard Correctie**.
10. Selecteer **Volgende** totdat u de laatste pagina van de wizard hebt bereikt en selecteer **Voltooien**.

De boekwaarden van de lease worden automatisch opnieuw berekend om ervoor te zorgen dat de goedgekeurde correctievariabelen actueel zijn. Als er wijzigingen zijn, wordt de goedkeuringsstatus teruggezet op **Concept** en moet u de leasecorrectie opnieuw bij het werkstroomsysteem indienen

## <a name="view-lease-versions"></a>Leaseversies weergeven

Als een lease is gecorrigeerd, kunt u de verschillende versies ervan weergeven. U kunt ook de historische schema's en eerdere leasegegevens weergeven.

1. Selecteer op de pagina **Leaseoverzicht** de lease en vervolgens in het actievenster **Historie van leaseversie**.

    Als de geselecteerde lease is gecorrigeerd, worden op de pagina **Historie van leaseversie** de verschillende versies weergegeven. De oorspronkelijke lease wordt aangeduid met **1** en de volgende versies hebben een oplopende numerieke volgorde.

    Voor een geselecteerde leaseversie kunt u de financiële dimensies, contractgegevens, locatie en betalingsschemaregels weergeven.

2. Als u historische planningen wilt weergeven, opent u de gewijzigde lease op de pagina **Leaseoverzicht**, selecteert u het gewenste boek en vervolgens in het actievenster **Historie van boekversie**.
3. Selecteer op de pagina **Boekversie** een versie en een schema om weer te geven.
