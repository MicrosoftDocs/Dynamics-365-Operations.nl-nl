---
title: Financiële rapporten weergeven en ontwerpen
description: Dit artikel bevat oefeningen waarin wordt uitgelegd hoe u financiële rapporten voor Microsoft Dynamics 365 Finance kunt weergeven en maken.
author: jcart1106
manager: AnnBe
ms.date: 10/02/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReportingSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 10814
ms.assetid: cd5f6483-c09b-4c2d-9336-d22eb6ab6e4f
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97895081293d9ee5a82a718e0644bebdaa0f2777
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686240"
---
# <a name="view-and-design-financial-reports"></a>Financiële rapporten weergeven en ontwerpen

[!include [banner](../includes/banner.md)]

Dit artikel bevat oefeningen waarin wordt uitgelegd hoe u financiële rapporten voor Microsoft Dynamics 365 Finance kunt weergeven en maken. Financiële rapportage bestaat uit een weergave-ervaring in de toepassing en een ClickOnce-rapportontwerper waarmee u financiële rapporten kunt maken en bewerken.

## <a name="exercise-1-generate-and-explore-a-default-financial-report"></a>Oefening 1: Een standaard financieel rapport genereren en controleren

Voor deze oefening genereert en controleert u een bestaand standaardrapport. Dit rapport bevat alle rekeningen en ook rekeningeigenschappen (kenmerken) voor de rekeningen. U zoomt in op transactiedetails, u past dimensiefilters toe en u wijzigt de valuta in het rapport. Eerst werken we de weergavevolgorde van dimensies voor financiële rapportage bij. Hiermee kunt u bepalen hoe de dimensies niet alleen tijdens het ontwerpen en weergeven van financiële rapporten worden weergegeven.

1. Ga naar **Financiële dimensieconfiguratie voor het integreren van toepassingen** onder **Dimensies van rekeningschema** in het grootboek.
2. Verplaats de dimensies zodat ze in de volgende volgorde staan:

    1. Hoofdrekening
    2. Bedrijfseenheid
    3. Kostenplaats
    4. Departement

    > [!NOTE]
    > De dimensies kunnen in de volgorde blijven die ze momenteel hebben.

3. Sla de dimensieconfiguratie op. Vervolgens genereren we een rapport en controleren de gegevens in het rapport.
4. Ga naar **Financiële rapporten** onder **Query's en rapporten** in het grootboek.
5. Selecteer de rij voor het rapport met de naam **GB-details: standaard**.
6. Selecteer **Bewerken**.

    > [!NOTE]
    > U wordt gevraagd de ClickOnce-rapportontwerper te downloaden en u aan te melden. Meld u aan met uw referenties.

7. Wijzig het basisjaar in 2012 en selecteer **Genereren**. Wanneer een rapport van de rapportontwerper wordt gegenereerd, wordt het op een nieuw browsertabblad geopend. U kunt het rapport op het nieuwe browsertabblad controleren of u kunt naar het oorspronkelijke browsertabblad gaan en het rapport daar openen door het in de lijst **Financiële rapporten** te selecteren.
8. Selecteer in het geopende rapport een van de bedragen waarvoor u wilt inzoomen op de rekeningdetails van het rapport.
9. Als u in de rekeningdetails bent, selecteert u een rekening met gegevens en **zoomt u in op rapporttransactieniveau**. Op het rapporttransactieniveau kunt u de eigenschappen (kenmerken) zien die in het ontwerp van dit rapport zijn opgenomen. Afhankelijk van de transactie en de rekening kunnen sommige of alle kenmerken worden weergegeven.
10. Sluit het rapporttransactieniveau.
11. Selecteer dezelfde of een andere rekening en **open boekstuktransacties**. Boekstuktransacties worden gefilterd op periode, jaar en rekening + de dimensiecombinatie van de geselecteerde rekening. Vanuit boekstuktransacties kunt u ervoor kiezen andere gegevens over de transactie te controleren.
12. Sluit boekstuktransacties. In een financieel rapport kunt u ervoor kiezen de gegevens voor een andere periode en een ander jaar of met andere kenmerken en dimensies toegepast weer te geven. Dit doet u met behulp van **Rapportopties**.
13. Selecteer **Rapportopties**.
14. Selecteer **Een dimensiefilter toevoegen** en kies **Bedrijfseenheid**.
15. Typ 001 in het veld en selecteer **OK**. In het rapport worden nu alleen de gegevens weergegeven voor de bedrijfseenheid 001. Dit is een gepersonaliseerde weergave van het rapport en anderen mogen deze niet weergeven.
16. Sluit het gefilterde rapport. Financiële rapporten kunnen in elke valuta worden weergegeven die aan de toepassing is toegevoegd.
17. Selecteer **Valuta** en selecteer vervolgens **EUR**. Het rapport wordt nu in Euro weergegeven. Alle valutacodes of valutasymbolen die zijn opgenomen in het rapportontwerp, worden in de toegepaste valuta weergegeven. Als er geen valutasymbool is gedefinieerd voor een valuta, wordt het valutasymbool niet weergegeven.
18. Sluit het rapport **GB-details**.
19. Sluit **Report Designer**.

## <a name="exercise-2-add-additional-account-properties-to-a-report-design"></a>Oefening 2: Aanvullende rekeningeigenschappen toevoegen aan een rapportontwerp
In deze oefening wijzigt u een bestaand standaardrapport. U werkt beide rijdefinities bij om alle rekeningen op te nemen en u werkt de kolomdefinitie bij om rekeningkenmerken op te nemen. Zodra de updates zijn voltooid, genereert u het nieuw gemaakte rapport en controleert u het rapport. Wij beginnen in de lijst met financiële rapporten.

1. Ga naar **Financiële rapporten** onder Query's en rapporten in het grootboek.
2. Selecteer de rij voor het rapport met de naam **Samengevatte proefbalans: standaard**.
3. Selecteer **Bewerken**. **Samengevatte proefbalans: standaard** wordt in de rapportontwerper geopend.
4. Selecteer **Bestand** en vervolgens **Opslaan als** en geef het rapport de naam Gedetailleerde proefbalans met kenmerken.

    > [!NOTE]
    > Elke keer wanneer een nieuw rapport in rapportontwerper wordt gemaakt, wordt de lijst met financiële rapporten bijgewerkt.

5. Selecteer in de rapportdefinitie het rijdefinitiepictogram om **Proefbalans: standaardrijdefinitie** te openen.
6. Sla de rijdefinitie op als **Gedetailleerde proefbalans met kenmerken**.
7. Selecteer met de cursor op rij 50 **Bewerken** en vervolgens **Rijen invoegen van dimensies**. Met Rijen invoegen van dimensies kunt u kiezen welke dimensies u in uw rijdefinitie wilt hebben. Voor deze oefening gaan we de rijdefinitie met Hoofdrekening maken.
8. Zorg ervoor dat **Hoofdrekening** alle en-tekens bevat en selecteer **OK**. De rijdefinitie bevat nu alle hoofdrekeningen voor rechtspersoon USMF.
9. Schuif omlaag naar rij 11110 en verwijder rij 11110.
10. Selecteer in rij 11080 **--- (Onderstrepingstekenbedragen)**.
11. Typ in rij 11140 **Totaal van alle rekeningen** in kolom B.
12. Selecteer in kolom C **TOT** in de vervolgkeuzelijst.
13. Typ **50:11080** in kolom D.
14. **Sla** de rijdefinitie op. De rijdefinitie bevat nu alle rekeningen plus een totaalrij om alle rekeningen samen te voegen. Vervolgens werken we de kolomdefinitie bij om extra rekeningkenmerken op te nemen.
15. Selecteer in de rapportdefinitie **Gedetailleerde proefbalans met kenmerken** de kolomdefinitiepictogram om de kolomdefinitie **Samengevatte proefbalans: standaard** te openen.
16. Sla de kolomdefinitie op als **Gedetailleerde proefbalans met kenmerken**. De kolomdefinitie bevat financiële gegevenskolommen, een omschrijvingskolom en berekeningskolommen. We gaan kenmerkkolommen toevoegen aan de kolomdefinitie om extra details over de rekeningen op te geven.
17. De volgende kenmerken worden aan de kolomdefinitie toegevoegd:

    - Journaalnummer
    - Journaalomschrijving
    - Transactiedatum
    - Gemaakt door
    - Laatst gewijzigd door

18. Selecteer in kolom I **ATTR** als kolomtype. Selecteer vervolgens **Journaalnummer** als kenmerkcategorie.
19. Blijf kolommen toevoegen voor de resterende kenmerken.
20. Voeg in de rij **Koptekst 2** omschrijvingen toe voor elk van de nieuwe kolommen die zijn toegevoegd.
21. Sla de kolomdefinitie op. Nu de rijdefinitie en kolomdefinitie zijn bijgewerkt, moeten we ze aan de rapportdefinitie toevoegen.
22. Selecteer in de rapportdefinitie **Gedetailleerde proefbalans met kenmerken** Gedetailleerde proefbalans met kenmerken voor zowel de rijdefinitie als de kolomdefinitie.
23. Wijzig het basisjaar in **2012**.
24. **Sla** de rapportdefinitie op en **genereer** deze. Zodra het rapport is gegenereerd en geopend, kunt u het rapport controleren zoals u in de eerste oefening hebt gedaan. Zoom in op verschillende rekeningen om te zien hoe de aanvullende kenmerken worden weergegeven.
25. Sluit het rapport **Gedetailleerde proefbalans met kenmerken**.
26. Sluit **Report Designer**.

## <a name="exercise-3-create-a-multidimensional-report-using-a-reporting-tree"></a>Oefening 3: Een multidimensionaal rapport maken met een rapportagestructuur
Voor deze oefening wijzigt u een bestaand standaardrapport. U maakt een rapportagestructuur en voegt deze aan een rapportdefinitie toe om een kostenplaats/afdelingsinkomensoverzicht te maken. Zodra de updates zijn voltooid, genereert u de kostenplaats/afdelingsinkomensoverzicht en controleert u het rapport met de rapportagestructuur. Wij beginnen in de lijst met financiële rapporten.

1. Ga naar **Financiële rapporten** onder Query's en rapporten in het grootboek.
2. Selecteer de rij voor het rapport met de naam **Inkomensoverzicht: standaard**.
3. Selecteer **Bewerken**. **Inkomensoverzicht: standaard** wordt in de rapportontwerper geopend.
4. Wijs in het menu **Bestand** naar **Nieuw** en klik vervolgens op **Rapporteringsstructuurdefinitie**.
5. Klik in het menu **Bewerken** op **Rapporteringseenheden invoegen uit dimensies**.
6. Schakel selectievakjes voor alle dimensies uit, behalve **Kostenplaats**.
7. Klik op het veld **Van dimensie** voor het dimensietype Kostenplaats, typ **007** en druk vervolgens op de Tab-toets. Typ in het veld **Naar dimensie** **018**.
8. **Sla** de resulterende structuur met de naam **Kostenplaatsen per afdeling** op. Nu de rapportagestructuur is gemaakt, wijzigt u de rapportagestructuur om drie nieuwe rollup-eenheden op te nemen; Marketing, Bewerkingen en Detailhandel.
9. Klik in het menu **Venster** op **Kostenplaatsen per afdeling**. (Als de rapportagestructuur is gesloten, selecteert u deze in de rapportagestructuurdefinities in het navigatievenster.)
10. Klik op eenheid nummer twee, **Handelsbeurzen**, en klik vervolgens op het pictogram **Rapportage-eenheid invoegen** .
11. Dubbelklik op de entiteitkolom in de lege rij en selecteer **USMF**.
12. Typ **Marketing** in kolom B en C.
13. Klik op eenheid nummer vijf, **Servicebewerkingen**, en klik met de rechtermuisknop. Selecteer **Rapportage-eenheid invoegen**.
14. Herhaal stap 11.
15. Typ **Bewerkingen** in kolom B en C.
16. Klik op eenheid nummer twaalf, **Vestiging** en klik met de rechtermuisknop. Selecteer **Rapportage-eenheid invoegen**.
17. Herhaal stap 11.
18. Typ **Detailhandel** in kolom B en C. U ziet dat de eenheden Marketing, Bewerkingen en Detailhandel op hetzelfde niveau als de huidige rollup-eenheden worden weergegeven. De nieuwe eenheden worden vervolgens georganiseerd. Rapportage-eenheden worden georganiseerd door met de rechtermuisknop te klikken; door niveau te verhogen en te verlagen of door te slepen en neer te zetten.
19. Controleer of eenheid drie, **Handelsbeurzen** actief is en klik met de rechtermuisknop.
20. Selecteer **Rapportage-eenheid niveau verlagen**. De eenheid wordt nu weergegeven als een onderliggend element van **Marketing**.
21. Klik op eenheid vier, **Marketing Campagne** en klik met de rechtermuisknop.
22. Selecteer **Rapportage-eenheid niveau verlagen**.
23. Klik op **Servicebewerkingen** in de grafische weergave. Houd de linkermuisknop ingedrukt terwijl u de eenheid omhoog sleept naar **Bewerkingen**. Laat de linkermuisknop los om de eenheid in de rollup Bewerking neer te zetten. Herhaal dit voor **Productie, Kwaliteitscontrole, Logistiek, Inkoop en Beheer**.
24. Maak van **Vestiging** **Super**, **Winkelcentrum** en **Online** onderliggende elementen van **Detailhandel** door het niveau ervan te verhogen of te verlagen en ze te slepen en neer te zetten.
25. Sla de resulterende reorganisatie op. Nu hebben we de rapportagestructuur gemaakt en ingedeeld en kan deze aan de rapportdefinitie worden toegevoegd.
26. Selecteer in het menu **Venster** **Inkomensoverzicht: standaard** om de rapportdefinitie te openen.
27. Klik op de pijl van de vervolgkeuzelijst **Structuurtype** en selecteer **Rapportagestructuur**.
28. Klik op de pijl van de vervolgkeuzelijst Structuur en selecteer **Kostenplaatsen per afdeling**.
29. Wijzig het basisjaar in **2012**, **sla** de wijzigingen op en **genereer** het rapport. Nadat het rapport is gegenereerd en geopend, kunt u het rapport controleren.
30. Selecteer de vervolgkeuzelijst **Rapportagestructuur** om de rapportage-eenheden weer te geven. U kunt ook inzoomen op een rij van het rapport om alle saldi voor alle eenheden van de rapportagestructuur te bekijken.
31. Sluit **Inkomensoverzicht: standaard**.
32. Sluit **Report Designer**.

## <a name="exercise-4-create-a-consolidated-report-using-an-organization-hierarchy"></a>Oefening 4: Een geconsolideerd rapport maken met een organisatiehiërarchie
Voor deze oefening wijzigt u een bestaand standaardrapport. U voegt een organisatiehiërarchie in de rapportdefinitie toe om een geconsolideerd inkomensoverzicht en een balans te maken. Zodra de updates zijn voltooid, genereert u de het geconsolideerde rapport en controleert u het rapport met de rapportagestructuur. Wij beginnen in de lijst met financiële rapporten.

1. Ga naar **Financiële rapporten** onder Query's en rapporten in het grootboek.
2. Selecteer de rij voor het rapport met de naam **Balans en inkomensoverzicht naast elkaar: standaard**.
3. Selecteer **Bewerken**. **Balans en inkomensoverzicht naast elkaar: standaard** wordt in de rapportontwerper geopend.
4. Selecteer **Bestand** &gt; **Opslaan als** en geef het rapport de naam **Geconsolideerde balans en inkomensoverzicht naast elkaar**.
5. Wijzig het basisjaar in 2012.
6. Klik op de pijl van de vervolgkeuzelijst Structuur en selecteer **Organisatiehiërarchieën**.
7. Klik op de pijl van de vervolgkeuzelijst Structuur en selecteer **Contoso-holdings**.
8. Sla de wijzigingen op en genereer het rapport. Indien gevraagd, selecteert u alle rapportage-eenheden. Nadat het rapport is gegenereerd en geopend, kunt u het rapport controleren.
9. Selecteer **Rapportopties**.
10. Selecteer **Een dimensiefilter toevoegen** en kies **Afdeling**.
11. Typ **022** in het veld en selecteer **OK**.
12. Sluit het gefilterde rapport.
13. Selecteer de vervolgkeuzelijst **Rapportagestructuur** om de rapportage-eenheden weer te geven. U kunt ook inzoomen op een rij van het rapport om alle saldi voor alle eenheden van de rapportagestructuur te bekijken.
14. Sluit **Geconsolideerde balans en inkomensoverzicht naast elkaar**.
15. Sluit **Report Designer**.

## <a name="exercise-5-create-a-side-by-side-departmental-report"></a>Oefening 5: Een afdelingsrapport naast elkaar maken
In deze oefening maakt u een nieuw rapport. Het rapport is een afdelingsinkomensoverzicht naast elkaar. U gebruikt een bestaande rijdefinitie, maar maakt een nieuwe rapportdefinitie en een nieuwe kolomdefinitie die dimensiefilters gebruikt. Wij beginnen in de lijst met financiële rapporten.

1. Ga naar **Financiële rapporten** onder Query's en rapporten in het grootboek.
2. Selecteer **Nieuw**. Rapportontwerper wordt geopend met een lege rapportdefinitie. Uw eerste taak bestaat eruit de kolomdefinitie te maken.
3. Maak een nieuwe kolomdefinitie door te klikken op **Bestand**, **Nieuw** en vervolgens op **Kolomdefinitie**.
4. Selecteer in **kolom A** **DESC** voor het kolomtype.
5. Selecteer in **Kolom B** **FD** voor het kolomtype.
6. Dubbelklik in het veld **Dimensiefilter**.
7. Dubbelklik in het venster **Dimensie** op de kolom **Afdeling**.
8. Klik in de sectie Persoon of bereik van het dialoogvenster op de **ellips** voor het veld **Van** om een lijst van afdelingen weer te geven.
9. Selecteer afdeling **022**, **Verkoop en Marketing** en klik vervolgens op **OK**.
10. Herhaal stap 5 tot 8 voor afdelingen 23-25.
11. Typ in de rij **Koptekst 2** voor elke FD-kolom de volgende afdelingsomschrijvingen:

    - Kolom B – Verkoop en marketing
    - Kolom C - Bewerkingen
    - Kolom D – Financiën
    - Kolom E – IT

12. Sla de kolomdefinitie als Afdelingen naast elkaar op. Omdat we een bestaande rijdefinitie gebruiken, kan de rapportdefinitie nu worden gewijzigd om gebruik te maken van de nieuwe kolomdefinitie en de bestaande rijdefinitie.
13. Selecteer in het menu **Venster** **Nieuwe rapportdefinitie** om de rapportdefinitie te openen.
14. Selecteer **Inkomensoverzicht - Standaard** als de rijdefinitie en **Afdelingen naast elkaar** als de kolomdefinitie.
15. Sla de rapportdefinitie op als **Afdelingsinkomensoverzicht naast elkaar**.
16. Wijzig het basisjaar in **2012**.
17. Wijzig het detailniveau in **Financieel, rekening en transactie**.
18. **Sla** uw wijzigingen op en **genereer** ze. Nadat het rapport is gegenereerd en geopend, kunt u het rapport controleren.

## <a name="additional-resources"></a>Aanvullende bronnen
[Financiële rapportage](../../../finance/general-ledger/financial-reporting-getting-started.md)

[Financiële rapporten weergeven](../../../finance/general-ledger/view-financial-reports.md)

[Dynamics 365 Finance-blog](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog)
