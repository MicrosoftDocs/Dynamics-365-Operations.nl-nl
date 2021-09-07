---
title: Ontvangsten en verzendingen voor Intrastat boeken
description: Dit onderwerp biedt een voorbeeld dat laat zien hoe u ontvangsten en verzendingen voor Intrastat kunt boeken.
author: andosip
ms.date: 8/23/2021
ms.topic: article
audience: Application User
ms.reviewer: kfender
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: f7bd1811fd0e580a6b6655244c689268915d320e
ms.sourcegitcommit: 72a82e9aeabbdecf57e1aee72975c63eba75143a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/24/2021
ms.locfileid: "7414782"
---
# <a name="post-arrivals-and-dispatches-for-intrastat"></a>Ontvangsten en verzendingen voor Intrastat boeken

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een voorbeeld dat laat zien hoe u ontvangsten en verzendingen voor Intrastat kunt boeken. In het voorbeeld wordt de rechtspersoon **ITCO** gebruikt.

## <a name="setup"></a>Instelling

1. De laatste versie van de volgende ER-configuraties (Elektronische Rapportage) importeren:

    - Intrastat-model
    - Intrastat-rapport
    - Intrastat (IT)

    Meer informatie is te vinden in [ER-configuraties downloaden uit de algemene opslagplaats van de configuratieservice](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

2. Leg in Microsoft Dynamics 365 Finance de volgende nummerreeksen vast als doorlopend: **Gene\_397**, **Acco\_16403**, **Gene\_407** en **PUR\_EU**.

    1. Ga naar **Organisatiebeheer** > **Nummerreeksen** > **Nummerreeksen**.
    2. Selecteer een van de nummerreekscodes in het raster.
    3. Selecteer **Bewerken** in het actievenster.
    4. Stel in het gedeelte **Instellingen** in het sneltabblad **Algemeen** de optie **Doorlopend** in op **Ja**.
    5. Selecteer **Opslaan** in het actievenster.

3. Stel een adres voor het magazijn in.

    1. Ga naar **Magazijnbeheer** &gt; **Instellen** &gt; **Magazijn** &gt; **Magazijnen**.
    2. Selecteer in de lijst magazijn **11**.
    3. Selecteer in het sneltabblad **Adres** de optie **Toevoegen**.
    4. Voer in het dialoogvenster **Nieuw** **Adres** in het veld **Naam** **of** **Beschrijving** de waarde **Hoofd** in.
    5. Selecteer in het veld **Land/regio** de waarde **ITA (Italië)**.
    6. Selecteer in het veld **Stad** de stad **Aprilia**.
    7. Selecteer **OK**.

4. Transactiecodes instellen.

    1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Transactiecodes**.
    2. Selecteer **Nieuw** en stel een transactiecode in voor eigenschapsoverdrachten.

        - Voer in het veld **Transactiecode** de waarde **1** in.
        - Vul in het veld **Naam** de **Eigenschapsoverdracht** in.

    3. Selecteer **Nieuw** en stel een transactiecode in voor retouren.

        - Voer in het veld **Transactiecode** de waarde **2** in.
        - Voer in het veld **Naam** **Retourneren van goederen** in.

5.  Parameters voor buitenlandse handel instellen.

    1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Parameters buitenlandse handel**.
    2. Selecteer in het tabblad **Intrastat** in het sneltabblad **Algemeen** in het veld **Transactiecode** de waarde **1**.
    3. Selecteer in het veld **Creditnota** de waarde **2**.
    4. Selecteer in het veld **Aangifteperiode verkoop** de waarde **Maandelijks**.
    5. Selecteer in het veld **Aangifteperiode aankoop** de waarde **Maandelijks**.
    6. Selecteer in het sneltabblad **Elektronische rapportage** in het veld **Toewijzing bestandsindeling** de waarde **Intrastat (IT)**.
    7. Selecteer in het veld **Toewijzing rapportindeling** de waarde **Intrastat-rapport**.
    8. Selecteer in het sneltabblad **Hiërarchie van basisproductcodes** in het veld **Categoriehiërarchie** de optie **Intrastat**.
    9. Stel in het sneltabblad **Statistische waarde** de optie **Statistische gegevens afdrukken en exporteren** in op **Ja**.
    10. Controleer in het tabblad **Eigenschappen land/regio** of de volgende regels aanwezig zijn.

        | **Land/regio voor partij** | **Intrastat-code** | **Valuta** | **Land-/regiotype** |
        |--------------------------|--------------------|--------------|-------------------------|
        | ITA                      | IT                 | EUR          | Binnenlands                |
        | SMR                      | SM                 | EUR          | Speciaal binnenlands        |

    11. Selecteer **Nieuw** in de werkbalk om een volgende regel aan te maken.

        | **Land/regio voor partij** | **Intrastat-code** | **Valuta** | **Land-/regiotype** |
        |--------------------------|--------------------|--------------|-------------------------|
        | DNK                      | DK                 | DKK          | EU                      |

6. Btw-vrijstellingsnummers instellen.

    1. Ga naar **Btw** > **Instellen** > **Btw** > **Btw-nummers belastingvrijstelling**.
    2. Selecteer **Nieuw** in het actievenster om de volgende regels aan te maken.

        | **Land/regio** | **Btw-nummer** | **Bedrijfsnaam** |
        |--------------------|-----------------------|------------------|
        | DEU                | DE3456789012          | UE LEVERANCIER        |
        | DNK                | DK0987654321          | Klant ER      |

7. Het adres van de leverancier instellen.

    1. Ga naar **Leveranciers** &gt; **Leveranciers** &gt; **Alle leveranciers**.
    2. Selecteer **UE leverancier** in het raster.
    3. Selecteer in het sneltabblad **Adressen** de optie **Toevoegen**.
    4. Voer in het dialoogvenster **Nieuw adres** in het veld **Naam of beschrijving** de waarde **Duitsland** in.
    5. Selecteer in het veld **Land/regio** de waarde **DEU**.
    6. Selecteer **OK** om het nieuwe adres aan te maken.
    7. Selecteer in het sneltabblad **Factuur en levering**, in het gedeelte **Btw** in het veld **Btw-nummer belastingvrijstelling** de optie **Alle** en selecteer vervolgens **DE1234567890**.
    8. Selecteer **Opslaan** in het actievenster.

8. Klantadressen instellen.

    1. Ga naar **Debiteuren** > **Klanten** > **Alle klanten**.
    2. Selecteer **ITCO-000001** in het raster.
    3. Selecteer in het sneltabblad **Adressen** de optie **Bewerken**.
    4. Voer in het dialoogvenster **Nieuw adres** in het veld **Naam of beschrijving** de waarde **San Marino** in.
    5. Selecteer in het veld **Land/regio** de waarde **SMR**.
    6. Selecteer **OK** om het nieuwe adres aan te maken.
    7. Selecteer in het sneltabblad **Factuur en levering** in het veld **Factuur** in het veld **Factuuraccount** de waarde **ITCO-000001**.
    8. Selecteer in het veld **Nummerreeksgroep** **IT\_VENDOM**.
    9. Selecteer **Opslaan** in het actievenster en sluit de pagina.
    10. Selecteer op de pagina **Alle klanten** in het raster **ITCO-000002**.
    11. Selecteer in het sneltabblad **Adressen** de optie **Toevoegen**.
    12. Voer in het dialoogvenster **Nieuw adres** in het veld **Naam of beschrijving** de waarde **Denemarken** in.
    13. Selecteer in het veld **Land/regio** de waarde **DNK**.
    14. Selecteer **OK** om het nieuwe adres aan te maken.
    15. Selecteer in het sneltabblad **Verkoopdemografie** in het veld **Valuta** de waarde **DKK**.
    16. Selecteer in het sneltabblad **Factuur en levering** , in het gedeelte **Btw** in het veld **Btw-groep** de optie **IT\_PUREU**.
    17. Selecteer in het veld **Btw-nummer belastingvrijstelling** de optie **Alle** en selecteer vervolgens **DK0987654321**.
    18. Selecteer **Opslaan** in het actievenster.

9. De categoriehiërarchie instellen.

    1. Ga naar **Productgegevensbeheer** > **Instellingen** > **Categorieën en kenmerken** > **Categoriehiërarchieën**.
    2. Selecteer **Intrastat** in het raster.
    3. Selecteer in het actievenster de optie **Nieuw categorieknooppunt**.
    4. Voer in het veld **Naam** de **Dienst** in.
    5. Voer in het veld **Code** de waarde **123456** in.
    6. Selecteer **Opslaan** in het actievenster.

10. Stel producten in.

    1. Ga naar **Productgegevensbeheer** > **Producten** > **Vrijgegeven producten**.
    2. Selecteer **ARTIKEL** in het raster.
    3. Selecteer in het veld **Aankoop** in het gedeelte **Administratie** in het veld **Leverancier** de optie **ITCO-000001**.
    4. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de waarde **\[100 200 30\] speaker**.
    5. Selecteer in het gedeelte **Oorsprong** in het veld **Land/regio** de waarde **DEU**.
    6. Selecteer **BE** in het veld **Provincie**.
    7. Voer in het sneltabblad **Voorraad beheren** in het gedeelte **Nettogewichtmetingen** in het veld **Nettogewicht** de waarde **5** in.
    8. Selecteer **Opslaan** in het actievenster.
    9. Selecteer op de pagina **Vrijgegeven producten** in het raster **Soort dienst**.
    10. Selecteer in het sneltabblad **Buitenlandse handel** in het gedeelte **Intrastat** in het veld **Basisproduct** de waarde **\[123456\] Service**.
    11. Selecteer **Opslaan** in het actievenster.

11. Transportmethoden instellen.

    1. Ga naar **Belasting** > **Instellingen** > **Buitenlandse handel** > **Transportmethoden**.
    2. Selecteer **Nieuw** in het actievenster om de volgende transportmethoden aan te maken.

        | **Transport** | **Beschrijving** |
        |---------------|-----------------|
        | 1             | Weg            |
        | 2             | Vliegtuig             |

12. Een leveringsmethode instellen.

    1. Ga naar **Inkoop en sourcing** > **Instellingen** > **Distributie** > **Leveringsmethoden**.
    2. Selecteer **Nieuw** in het actievenster.
    3. Voer in het veld **Leveringsmethode** de waarde **1** in.
    4. Voer in het veld **Beschrijving** de optie **Vrachtwagen** in.
    5. Selecteer in het sneltabblad **Buitenlandse handel** in het veld **Transport** de waarde **1 Weg**.
    6. Selecteer **Opslaan** in het actievenster.

13. Leveringsvoorwaarden instellen.

    1. Ga naar **Leveranciers** > **Instellingen** > **Leveringsvoorwaarden**.
    2. Selecteer in de lijst **CFR**.
    3. Selecteer in het sneltabblad **Algemeen** de optie **1** in het veld **Intrastat code**.

## <a name="post-arrivals-for-intrastat"></a>Ontvangsten voor Intrastat boeken

### <a name="purchase-goods-by-using-a-purchase-order"></a>Goederen inkopen met behulp van een inkooporder

Dit gedeelte van het voorbeeld laat zien hoe u een inkooporder gebruikt om goederen (artikelen) te kopen uit landen binnen de Europese Unie (EU).

1. Ga naar **Leveranciers** > **Inkooporders** > **Alle inkooporders**.
2.  Selecteer **Nieuw** in het actievenster.
3.  Ga in het dialoogvenster **Inkooporder maken** naar het sneltabblad **Leveranciersaccount** en selecteer **UE leverancier**.
4.  Selecteer in het veld **Taal** in het sneltabblad **Administratie** de optie **it**.
5.  Selecteer **OK**.
6.  Controleer in de weergave **Koptekst** in het sneltabblad **Buitenlandse** **handel** of het veld **Transactiecode** ingesteld is op **1**.
7.  Controleer of het veld **Land van oorsprong/bestemming** ingesteld is op **RM**.
8.  Selecteer in het sneltabblad **Levering** in het gedeelte **Levering** in het veld **Leveringsmethode** de optie **1**.
9.  Selecteer **CFR** in het raster **Leveringsvoorwaarden**.
10. Selecteer in het tabblad **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **Artikel**.
11. Selecteer **1** in het veld **Locatie**.
12. Selecteer **11** in het veld **Magazijn**.
13. Typ **10** in het veld **Hoeveelheid**.
14. Voer in het veld **Eenheidsprijs** **100** in.
15. Selecteer in het sneltabblad **Instellingen**, in de sectie **Btw** in het veld **Btw-groep item** de optie **22%EU**.
16. Selecteer in het actievenster in het tabblad **Inkoop** in de groep **Acties** de optie **Bevestigen**.
17. Selecteer in het actievenster op het tabblad **Factuur** in de groep **Genereren** de optie **Factuur**.
18. Selecteer in het actievenster **Standaardgegevens**.
19. Selecteer **Bestelde hoeveelheid** in het veld **Standaardhoeveelheid voor regels** en selecteer vervolgens **OK**.
20. Voer **0001** in het sneltabblad **Koptekst leveranciersfactuur** in, in het gedeelte **Factuuridentificatie** in het veld **Nummer**.
21. Selecteer in de sectie **Factuurdata** in het veld **Factuurdatum** de optie **09-07-2021**.
22. Als u de factuur wilt boeken, selecteert u **Boeken** vanuit het actievenster.

### <a name="purchase-services-by-using-a-vendor-invoice"></a>Inkoopservices met behulp van een leveranciersfactuur

Dit gedeelte van het voorbeeld laat zien hoe u een leveranciersfactuur gebruikt om diensten te kopen uit landen binnen de Europese Unie (EU).

1. Ga naar **Leveranciers** > **Facturen** > **Factuurjournaal**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het veld **Naam** de optie **VEND\_EUINV**.
4. Selecteer **Regels** in het actievenster.
5. Voer in het veld **Datum** de waarde **09-07-2021** in.
6. Selecteer **Leverancier** in het veld **Accounttype**.
7. Selecteer **UE leverancier** in het veld **Account**.
8. Selecteer in het veld **Factuurdatum** de waarde **09-07-2021**.
9. Voer in het veld **Factuur** de waarde **ITA-0004** in.
10. Typ **120000** in het veld **Krediet** in.
11. Selecteer in het veld **Tegenrekening** **type** de optie **Grootboek**.
12. Selecteer in het veld **Tegenrekening** de optie **110130**.
13. Selecteer in het veld **Btw-groep** de optie **IT\_PUREU**.
14. Selecteer in het veld **Btw-groep item** de optie **22%EU**.
15. Voer een van deze stappen uit in het tabblad **Buitenlandse handel**:

    1. Selecteer in het veld **Transactiecode** de waarde **1**.
    2. Selecteer **2 Lucht** in het veld **Transport**.
    3. Selecteer in het veld **Basisproduct** de waarde **\[123456\]-dienst**.
    4. Selecteer in het veld **Land/regio** de waarde **ITA**.
    5. Selecteer **LAZ** in het veld **Provincie**.
    6. Selecteer in het veld **Land van oorsprong/bestemming** de optie **LT**


16. Selecteer **Boeken** in het actievenster.
17. Een Intrastat-aangifte voor ontvangsten aanmaken.

    1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
    2. Selecteer in het actievenster de optie **Overboeken**.
    3. Stel in het dialoogvenster **Intrastat (overboeking)** de optie **Leveranciersfactuur** in op **Ja**.
    4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal vervolgens te bekijken.

   ![Pagina Intrastat-journaal, tabblad Overzicht.](media/ita_intrastat_journal_vendor_invoice.png)

18. Controleer het tabblad **Algemeen** voor de inkooporder.

    ![Regeldetails van Intrastat-journaal voor inkooporder](media/ita_intrastat_journal_purchase_order_line_details.png)

19. Controleer het tabblad **Algemeen** voor de leveranciersfactuur.

    ![Regeldetails van Intrastat-journaal voor leveranciersfactuur](media/ita_intrastat_journal_vendor_invoice_line_details.png)

20. Intrastat-rapportgegevens voor ontvangsten genereren.

    1. Selecteer in het actievenster **Uitvoer** > **Rapport**.
    2. Selecteer in het dialoogvenster **Intrastat-rapport** in de sectie **Datum** in het veld **Begindatum** de waarde **01-07-2021**.
    3. Selecteer in het veld **Einddatum** de waarde **31-07-2021**.
    4. Stel in het gedeelte **Exportopties** de opties **Bestand genereren** en **Rapport genereren** in op **Ja**.
    5. Voer in het veld **Bestandsnaam** de waarde **Bestand ontvangsten** in.
    6. Voer in het veld **Bestandsnaam rapport** de waarde **Rapport ontvangsten** in.
    7. Selecteer **Ontvangsten** in het veld **Richting**.
    8. Voer in het veld **Referentienummer** de waarde **123456** in.
    9. Selecteer **OK** om het Intrastat-rapport en het Intrastat-bestand te genereren en ze te controleren.

    In de volgende afbeelding ziet u een voorbeeld van een Intrastat-rapport.

    ![Intrastat-ontvangstenrapport.](media/ita_intrastat_arrivals_report.png)

    In de volgende afbeelding ziet u een voorbeeld van een Intrastat-bestand.

    ![Intrastat-ontvangstenbestand.](media/ita_intrastat_arrivals_file.png)

## <a name="post-dispatches-for-intrastat"></a>Verzendingen voor Intrastat boeken

### <a name="sell-goods-by-using-a-sales-order"></a>Goederen verkopen met behulp van een verkooporder

Dit gedeelte van het voorbeeld laat zien hoe u een verkooporder gebruikt om goederen (artikelen) te verkopen naar landen binnen de Europese Unie (EU).

1. Ga naar **Klanten** > **Orders** > **Alle verkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde **ITCO-000002**.
4. Selecteer **OK**.
5. Selecteer in de weergave **Koptekst** in het sneltabblad **Levering** in het gedeelte **Overige leveringsinfo** voor de **Leveringsmethode** de optie **1 Vrachtwagen**.
6. Selecteer **CFR** in het raster **Leveringsvoorwaarden**.
7. Selecteer in de weergave **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **ARTIKEL**.
8. Typ **50** in het veld **Hoeveelheid**.
9. Selecteer **1** in het veld **Locatie**.
10. Selecteer **11** in het veld **Magazijn**.
11. Voer in het veld **Eenheidsprijs** **250** in.
12. Selecteer in het sneltabblad **Regeldetails** in het tabblad **Instellingen** in de sectie **Btw** in het veld **Btw-groep artikel** de optie **22%EU**.
13. Selecteer **Opslaan** in het actievenster.
14. Selecteer vervolgens in het actievenster in het tabblad **Factuur** in de groep **Genereren** de optie **Factuur** om de factuur voor de bestelling aan te maken.
15. Selecteer in het dialoogvenster **Factuur boeken** in het sneltabblad **Parameters** in de sectie **Parameters** in het veld **Hoeveelheid** de optie **Alle**.
16. Selecteer in het sneltabblad **Instellingen** in het veld **Factuurdatum** de optie **09-07-2021**.
17. Selecteer **OK**.
18. Controleer de regels in het Intrastat-journaal.

    1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
    2. Selecteer in het actievenster de optie **Overboeken**.
    3. Stel in het dialoogvenster **Intrastat (overboeking)** de optie **Klantfactuur** in op **Ja**.
    4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal te bekijken. De creditnotatransactie is gemarkeerd als een correctie en heeft een negatief factuurbedrag.

        ![Pagina Intrastat-journaal](media/ita_intrastat_journal_sales_order.png)

        ![Regeldetails van Intrastat-journaal voor verkooporder](media/ita_intrastat_journal_sales_order_line_details.png)

### <a name="return-goods-by-using-a-credit-note"></a>Goederen retourneren met behulp van een creditnota

Dit gedeelte van het voorbeeld laat zien hoe u een creditnota gebruikt om goederen (artikelen) te retourneren vanuit landen binnen de Europese Unie (EU).

1. Ga naar **Klanten** > **Orders** > **Alle verkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde **ITCO-000002**.
4. Selecteer **OK**.
5. Selecteer in de weergave **Koptekst** in het sneltabblad **Levering** in het gedeelte **Overige leveringsinfo** voor de **Leveringsmethode** de optie **1 Vrachtwagen**.
6. Selecteer **CFR** in het raster **Leveringsvoorwaarden**.
7. Selecteer in het sneltabblad **Buitenlandse handel** in het veld **Transactiecode** de waarde **2**.
8. Selecteer in het tabblad **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **ARTIKEL**.
9. Voer **10** in het veld **Hoeveelheid** in.
10. Selecteer **1** in het veld **Locatie**.
11. Selecteer **11** in het veld **Magazijn**.
12. Voer in het veld **Eenheidsprijs** **250** in.
13. Selecteer in het sneltabblad **Regeldetails** in het tabblad **Instellingen** in de sectie **Btw** in het veld **Btw-groep artikel** de optie **22%EU**.
14. Selecteer in de sectie **Geretourneerde bestelling** in het veld **Partij-ID retourneren** de partij die u eerder hebt aangemaakt.
15. Selecteer **Opslaan** in het actievenster.
16. Selecteer vervolgens in het actievenster in het tabblad **Factuur** in de groep **Genereren** de optie **Factuur** om de factuur voor de bestelling aan te maken.
17. Selecteer in het sneltabblad **Parameters** in het gedeelte **Parameter** in het veld **Hoeveelheid** de optie **Alle**.
18. Selecteer in het dialoogvenster **Factuurboeking** in het sneltabblad **Instellingen** in het veld **Factuurdatum** de datum **09-07-2021**.
19. Selecteer **OK** om de factuur te boeken.
20. Controleer de regels in het Intrastat-journaal.

    1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
    2. Selecteer in het actievenster de optie **Overboeken**.
    3. Stel in het dialoogvenster **Intrastat (overboeking)** de optie **Klantfactuur** in op **Ja**.
    4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal te bekijken. De creditnotatransactie is gemarkeerd als een correctie en heeft een negatief factuurbedrag.

    ![Creditnota Intrastat-journaal](media/ita_intrastat_journal_credit_note.png)

    ![Regeldetails van Intrastat-journaal voor creditnota](media/ita_intrastat_journal_credit_note_line_details.png)

### <a name="sell-goods-to-san-marino-by-using-a-sales-order"></a>Goederen aan San Marino verkopen met behulp van een verkooporder

Dit gedeelte van het voorbeeld laat zien hoe u een verkooporder gebruikt om goederen (artikelen) te verkopen naar San Marino.

1. Ga naar **Klanten** > **Orders** > **Alle verkooporders**.
2. Selecteer **Nieuw** in het actievenster.
3. Selecteer in het dialoogvenster **Verkooporder maken** in het veld **Klantaccount** de waarde **ITCO-000001**.
4. Selecteer **OK**.
5. Selecteer in de weergave **Koptekst** in het sneltabblad **Levering** in het gedeelte **Overige leveringsinfo** voor de **Leveringsmethode** de optie **1**.
6. Selecteer **CFR** in het raster **Leveringsvoorwaarden**.
7. Selecteer in het tabblad **Regels** in het sneltabblad **Verkooporderregels** in het veld **Artikelnummer** de waarde **ARTIKEL**.
8. Typ **30** in het veld **Hoeveelheid**.
9. Selecteer **1** in het veld **Locatie**.
10. Selecteer **11** in het veld **Magazijn**.
11. Voer in het veld **Eenheidsprijs** **200** in.
12. Selecteer **Opslaan** in het actievenster.
13. Selecteer vervolgens in het actievenster in het tabblad **Factuur** in de groep **Genereren** de optie **Factuur** om de factuur voor de bestelling aan te maken.
14. Selecteer in het sneltabblad **Parameters** in het gedeelte **Parameter** in het veld **Hoeveelheid** de optie **Alle**.
15. Selecteer in het dialoogvenster **Factuurboeking** in het sneltabblad **Instellingen** in het veld **Factuurdatum** de datum **09-07-2021**.
16. Selecteer **OK** om de factuur te boeken.
17. Controleer de regels in het Intrastat-journaal.

    1. Ga naar **Belasting** > **Aangiften** > **Buitenlandse handel** > **Intrastat**.
    2. Selecteer in het actievenster de optie **Overboeken**.
    3. Stel in het dialoogvenster **Intrastat (overboeking)** de optie **Klantfactuur** in op **Ja**.
    4. Selecteer **OK** om de transacties over te boeken en het Intrastat-journaal te bekijken.

   ![Intrastat-journaal voor San Marino](media/ita_intrastat_journal_sales_order_san_marino.png)

   ![Regeldetails van Intrastat-journaal voor San Marino](media/ita_intrastat_journal_sales_order_san_marino_line_details.png)

18. Een Intrastat-aangifte voor verzendingen aanmaken.

    1. Ga naar **Belasting** &gt; **Aangiften** &gt; **Buitenlandse handel** &gt; **Intrastat**.
    2. Selecteer **Uitvoer** &gt; **Rapport** in het actievenster.
    3. Selecteer in het dialoogvenster **Intrastat-rapport** in de sectie **Datum** in het veld **Begindatum** de waarde **01-07-2021**.
    4. Selecteer in het veld **Einddatum** de waarde **31-07-2021**.
    5. Stel in het gedeelte **Exportopties** de opties **Bestand genereren** en **Rapport genereren** in op **Ja**.
    6. Voer in het veld **Bestandsnaam** de waarde **Bestand verzendingen** in.
    7. Voer in het veld **Bestandsnaam rapport** de waarde **Rapport verzendingen** in.
    8. Selecteer **Verzendingen** in het veld **Richting**.
    9. Voer in het veld **Referentienummer** de waarde **98754** in.
    10. Selecteer **OK** om het Intrastat-rapport en het Intrastat-bestand te genereren en controleer ze.

        In de volgende afbeelding ziet u een voorbeeld van een uitgeprint Intrastat-rapport.

        ![Intrastat-rapport](media/ita_intrastat_report_for_dispatches.png)

        In de volgende afbeelding ziet u een voorbeeld van een uitgeprint Intrastat-bestand.

        ![Intrastat-bestand voor verzendingen](media/ita_intrastat_file_for_dispatches.png)
