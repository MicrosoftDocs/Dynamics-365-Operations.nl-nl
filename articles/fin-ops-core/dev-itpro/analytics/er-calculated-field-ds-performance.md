---
title: De prestaties van ER-oplossingen verbeteren door BEREKEND VELD-gegevensbronnen met parameters toe te voegen
description: In dit onderwerp wordt uitgelegd hoe u de prestaties van ER-oplossingen (elektronische rapportage) kunt verbeteren door BEREKEND VELD-gegevensbronnen met parameters toe te voegen.
author: NickSelin
manager: AnnBe
ms.date: 09/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: c63d64774b5b97a562da20655400078ed47c5675
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569220"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>De prestaties van ER-oplossingen verbeteren door BEREKEND VELD-gegevensbronnen met parameters toe te voegen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u [prestatietraceringen](trace-execution-er-troubleshoot-perf.md) van uitgevoerde [ER-indelingen (elektronische rapportage)](general-electronic-reporting.md) kunt gebruiken om de prestaties te verbeteren door een gegevensbron **Berekend veld** met parameters te configureren.

Als onderdeel van het proces van het ontwerpen van ER-configuraties om elektronische documenten te genereren, definieert u de methode die wordt gebruikt om gegevens uit de toepassing te halen en deze in te voeren in de gegenereerde uitvoer. Door een ER-gegevensbron van het type **Berekend veld** met parameters te ontwerpen, kunt u het aantal databaseaanroepen verminderen en de tijd en kosten van het verzamelen van de details van het uitvoeren van de ER-indeling aanzienlijk beperken.

## <a name="prerequisites"></a>Vereisten

- Als u de voorbeelden in dit onderwerp wilt voltooien, moet u toegang hebben tot een van de volgende [rollen](../sysadmin/tasks/assign-users-security-roles.md):

    - Ontwikkelaar elektronische rapportage
    - Functioneel consultant elektronische rapportage
    - Systeembeheerder

- Het bedrijf moet worden ingesteld op **DEMF**.
- Volg de stappen in [bijlage 1](#appendix1) van dit onderwerp om de onderdelen van de Microsoft ER-voorbeeldoplossing te downloaden die vereist zijn om de voorbeelden in dit onderwerp te voltooien.
- Volg de stappen in [bijlage 2](#appendix2) van dit onderwerp om de minimale set ER-parameters te configureren die nodig is om het ER-framework te gebruiken om de prestaties van de Microsoft ER-voorbeeldoplossing te verbeteren.

## <a name="import-the-sample-er-solution"></a>De ER-voorbeeldoplossing importeren

Stel dat u een ER-oplossing moet ontwerpen om een nieuw rapport te genereren waarin leverancierstransacties worden weergegeven. Op dit moment kunt u de transacties voor een geselecteerde leverancier vinden op de pagina **Leverancierstransacties** (ga naar **Leveranciers** \> **Leveranciers** \> **Alle leveranciers**, selecteer een leverancier en selecteer in het actievenster op het tabblad **Leverancier** in de groep **Transacties** de optie **Transacties**). U wilt echter alle leverancierstransacties tegelijk in één elektronisch document in XML-indeling hebben. Deze oplossing bestaat uit verschillende ER-configuraties met het vereiste gegevensmodel, de modeltoewijzing en indelingscomponenten.

De eerste stap is om de ER-voorbeeldoplossing te importeren om een leverancierstransactierapport te genereren.

1. Meld u aan bij het exemplaar van Microsoft Dynamics 365 Finance dat wordt ingericht voor uw bedrijf.
2. In dit onderwerp maakt en wijzigt u configuraties voor het voorbeeldbedrijf **Litware, Inc.** Zorg ervoor dat deze configuratieprovider is toegevoegd aan uw exemplaar van Finance en als actief is gemarkeerd. Zie [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.
3. Selecteer in het werkgebied **Elektronische rapportage** de tegel **Rapportconfiguraties**.
4. Importeer op de pagina **Configuraties** de ER-configuraties die u als vereiste hebt gedownload in Finance, in de volgende volgorde: gegevensmodel, modeltoewijzing, indeling. Volg deze stappen voor elke configuratie:

    1. In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.
    2. Selecteer **Bladeren** en selecteer het juiste bestand voor de ER-configuratie in XML-indeling.
    3. Selecteer **OK**.

![Geïmporteerde configuraties op de pagina Configuraties](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>De ER-voorbeeldoplossing controleren

### <a name="review-the-model-mapping"></a>De modeltoewijzing controleren

1. Vouw op de pagina **Configuraties** in de configuratiestructuur **Prestatieverbeteringsmodel** uit en selecteer **Prestatieverbeteringstoewijzing**.
2. Selecteer **Ontwerper** in het actievenster.
3. Selecteer **Ontwerper** op de pagina **Model aan gegevensbrontoewijzing** in het actievenster.

    Deze ER-modeltoewijzing is ontworpen om de volgende acties uit te voeren:

    - De lijst met leverancierstransacties ophalen die zijn opgeslagen in de tabel VendTrans (gegevensbron **Trans**).
    - Voor elke transactie uit de tabel VendTable de record van een leverancier ophalen waarvoor de transactie is geboekt (gegevensbron **\#Vend**).

    > [!NOTE]
    > De gegevensbron **\#Vend** wordt geconfigureerd om de bijbehorende leveranciersrecord op te halen met behulp van de bestaande veel-op-één-relatie **\@.'\>Relations'.VendTable\_AccountNum**.

    Met de modeltoewijzing in deze configuratie wordt het basisgegevensmodel geïmplementeerd voor elke ER-indeling die voor dit model is gemaakt en in Finance wordt uitgevoerd. Dat betekent dat de inhoud van de gegevensbron **Trans** wordt weergegeven voor ER-indelingen zoals abstracte gegevensbronnen van het type **model**.

    ![Gegevensbron Trans op de pagina Ontwerper modeltoewijzing](media/er-calculated-field-ds-performance-mapping-1.png)

4. Sluit de pagina **Ontwerper modeltoewijzing**.
5. Sluit de pagina **Model aan gegevensbrontoewijzing**.

### <a name="review-format"></a>Indeling controleren

1. Vouw op de pagina **Configuraties** in de configuratiestructuur **Prestatieverbeteringsmodel** uit en selecteer **Prestatieverbeteringsindeling**.
2. Selecteer **Ontwerper** in het actievenster.
3. Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** de optie **Uitvouwen/Samenvouwen**.
4. Vouw de items **Model**, **Gegevens** en **Transactie** uit.

    Deze ER-indeling is ontworpen om een rapport voor leverancierstransacties in XML-indeling te genereren.

    ![Indelingsgegevensbronnen en geconfigureerde bindingen van indelingselementen op de pagina Indelingsontwerper](media/er-calculated-field-ds-performance-format.png)

5. Sluit de pagina **Indelingsontwerper**.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>De ER-voorbeeldoplossing uitvoeren om de uitvoering te traceren

Stel dat u klaar bent met het ontwerpen van de eerste versie van de ER-oplossing. U wilt deze nu testen in de oplossing in uw Finance-exemplaar en de uitvoeringsprestaties analyseren.

### <a name="turn-on-the-er-performance-trace"></a>De ER-prestatietracering inschakelen

1. Selecteer het bedrijf **DEMF**.
2. Volg de stappen in [De ER-prestatietracering inschakelen](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) om een prestatietracering te genereren terwijl er een ER-indeling wordt uitgevoerd.

    ![Dialoogvenster voor gebruikersparameters](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>De ER-indeling uitvoeren

1. Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.
2. Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Indeling voor prestatieverbetering**.
3. Selecteer **Uitvoeren** in het actievenster.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>De prestatietracering gebruiken om modeltoewijzingsprestaties te analyseren

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Prestatieverbeteringstoewijzing**.
2. Selecteer **Ontwerper** in het actievenster.
3. Selecteer **Ontwerper** op de pagina **Modeltoewijzingen** in het actievenster.
4. Selecteer op de pagina **Ontwerper modeltoewijzing** in het actievenster de optie **Prestatietracering**.
5. Selecteer de meest recente tracering die is gegenereerd en selecteer vervolgens **OK**.

Nieuwe informatie is nu beschikbaar voor bepaalde gegevensbronitems van de huidige modeltoewijzing:

- De werkelijke tijd die is besteed aan het ophalen van gegevens met behulp van de gegevensbron
- Dezelfde tijd uitgedrukt als een percentage van de totale tijd die is besteed aan het uitvoeren van de gehele modeltoewijzing

![Details over de uitvoeringstijd op de pagina Ontwerper modeltoewijzing](./media/er-calculated-field-ds-performance-mapping-2.png)

In het raster **Prestatiestatistieken** ziet u dat de gegevensbron **Trans** de tabel VendTrans één keer aanroept. De waarde **\[265\]\[Q:265\]** van de gegevensbron **Trans** geeft aan dat 265 leverancierstransacties uit de toepassingstabel zijn opgehaald en naar het gegevensmodel zijn geretourneerd.

In het raster **Prestatiestatistieken** ziet u ook dat de huidige modeltoewijzing databaseaanvragen dupliceert wanneer de gegevensbron **\#Vend** wordt uitgevoerd. Deze duplicatie vindt plaats om de volgende redenen:

- De leverancierstabel wordt twee keer aangeroepen voor elk van de 265 herhaalde leverancierstransacties, voor een totaal van 530 aanroepen:

    - Er wordt één oproep gedaan om het rekeningnummer van de leverancier in te voeren.
    - Er wordt één oproep gedaan om de naam van de leverancier in te voeren.

- De leverancierstabel wordt aangeroepen voor elke herhaalde leverancierstransactie, hoewel de opgehaalde transacties slechts voor vijf leveranciers zijn geboekt. Van de 530 aanroepen zijn er 525 duplicaten. In de volgende afbeelding ziet u het bericht dat u ontvangt over dubbele oproepen (databaseaanvragen).

![Bericht over dubbele databaseaanvragen op de pagina Ontwerper modeltoewijzing](./media/er-calculated-field-ds-performance-mapping-2a.png)

Van de totale uitvoeringstijd voor modeltoewijzingen (circa acht seconden), ziet u dat meer dan 80 procent (ongeveer zes seconden) is besteed aan het ophalen van waarden uit de VendTable-toepassingstabel. Dit percentage is te hoog voor twee kenmerken van vijf leveranciers, vergeleken met het volume gegevens in de VendTrans-toepassingstabel.

Als u het aantal aanroepen wilt beperken dat wordt uitgevoerd om de leveranciersgegevens voor elke transactie te verkrijgen en om de prestaties van de modeltoewijzing te verbeteren, kunt u caching gebruiken voor de gegevensbron **\#Vend**.

> [!NOTE]
> De gegevensbron **Trans\\\#Vend** wordt tijdens runtime in de cache opgeslagen in het bereik van de huidige transactie van de gegevensbron **Trans**.

Door de gegevensbron **\#Vend** in de cache op te slaan, verlaagt u het aantal dubbele aanroepen van 525 naar 260, maar verwijdert u de duplicatie niet volledig. Als u de duplicatie volledig wilt elimineren, kunt u een nieuwe gegevensbron met parameters configureren voor het type **Berekend veld**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>De modeltoewijzing verbeteren op basis van informatie uit de uitvoeringstracering

### <a name="change-the-logic-of-the-model-mapping"></a>De logica van de modeltoewijzing wijzigen

Volg deze stappen om caching en een gegevensbron van het type **Berekend veld** te gebruiken om dubbele oproepen naar de database te voorkomen.

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Prestatieverbeteringstoewijzing**.
2. Selecteer **Ontwerper** in het actievenster.
3. Selecteer **Ontwerper** op de pagina **Modeltoewijzingen** in het actievenster.
4. Voer op de pagina **Ontwerper modeltoewijzing** de volgende stappen uit om een gegevensbron van het type **Tabelrecords** toe te voegen om toegang te krijgen tot records in de VendTable-toepassingstabel:

    1. Vouw in het deelvenster **Typen gegevensbronnen** het item **Dynamics 365 for Operations** uit en selecteer **Tabelrecords**.
    2. Selecteer **Basis toevoegen**.
    3. Voer in het dialoogvenster in het veld **Naam** de tekst **Vend** in.
    4. Voer in het veld **Tabel** de waarde **VendTable** in.
    5. Selecteer **OK**.

5. U kunt alleen parameteraanroepen naar gegevensbronnen van het type **Berekend veld** uitvoeren als deze gegevensbronnen zich in een container bevinden. Voer daarom de volgende stappen uit om een gegevensbron van het type **Lege container** toe te voegen voor een nieuwe gegevensbron met parameters van het type **Berekend veld**:

    1. Vouw in het deelvenster **Typen gegevensbronnen** het item **Algemeen** uit en selecteer **Lege container**.
    2. Selecteer **Basis toevoegen**.
    3. Voer in het dialoogvenster in het veld **Naam** de tekst **Box** in.
    3. Selecteer **OK**.

    ![Gegevensbron Box op de pagina Ontwerper modeltoewijzing](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Voer de volgende stappen uit om een gegevensbron met parameters toe te voegen voor het type **Berekend veld**:

    1. Selecteer **Box** in het deelvenster **Gegevensbronnen**.
    2. Vouw in het deelvenster **Typen gegevensbronnen** het item **Functies** uit en selecteer **Berekend veld**.
    3. Selecteer **Toevoegen**.
    4. Voer in het dialoogvenster in het veld **Naam** de tekst **Vend** in.
    5. Selecteer **Formule bewerken**.
    6. Selecteer op de pagina **Formuleontwerper** de optie **Parameters** om de parameters op te geven die moeten worden opgegeven wanneer deze gegevensbron wordt aangeroepen.
    7. Selecteer **Nieuw** in het dialoogvenster **Parameters**.
    8. Voer in het veld **Naam** de waarde **parmVendAccNumber** in.
    9. Selecteer in het veld **Type** de optie **Tekenreeks**.
    10. Selecteer **OK**.
    11. Voer in het veld **Formule** de waarde **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))** in.
    12. Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.
    13. Klik op **OK** om de nieuwe gegevensbron toe te voegen.

7. Voer de volgende stappen uit om de toegevoegde gegevensbron te markeren als in cache opgeslagen tijdens de uitvoering:

    1. Selecteer **Box\\Vend** in het deelvenster **Gegevensbronnen**.
    2. Selecteer **Cache**.

    > [!NOTE]
    > De gegevensbron **Box\\Vend** wordt tijdens runtime in de cache opgeslagen in het bereik van alle leverancierstransacties van de gegevensbron **Trans**.

8. Voer de volgende stappen uit om de geneste gegevensbron **Trans\\\#Vend** bij te werken zodat deze de gegevensbron **Box\\Vend** gebruikt:

    1. Vouw **Trans** uit in het deelvenster **Gegevensbronnen**.
    2. Selecteer de gegevensbron **Trans\\\#Vend** en selecteer vervolgens **Bewerken** \> **Formule bewerken**.
    3. Voer op de pagina **Formuleontwerper** in het veld **Formule** de waarde **Box.Vend(\@.AccountNum)** in.
    4. Selecteer **Opslaan** en sluit de pagina **Formuleontwerper**.
    5. Selecteer **OK** om de wijzigingen in de geselecteerde gegevensbron te voltooien.

9. Selecteer **Opslaan**.

    ![Gegevensbron Vend op de pagina Ontwerper modeltoewijzing](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Sluit de pagina **Ontwerper modeltoewijzing**.
11. Sluit de pagina **Modeltoewijzingen**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>De gewijzigde versie van de ER-modeltoewijzing voltooien

1. Op de pagina **Configuraties** op het sneltabblad **Versies** selecteert u versie **1.2** van de configuratie **Toewijzing voor prestatieverbetering**.
2. Selecteer **Status wijzigen** \> **Voltooien** en **OK**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>De gewijzigde ER-oplossing uitvoeren om de uitvoering te traceren

Herhaal de stappen uit het gedeelte [De ER-indeling uitvoeren](#run-format) eerder in dit onderwerp om een nieuwe prestatietracering te genereren.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>De prestatietracering gebruiken om aanpassingen in de modeltoewijzing te analyseren 

1. Selecteer op de pagina **Configuraties** in de configuratiestructuur het item **Prestatieverbeteringstoewijzing**.
2. Selecteer **Ontwerper** in het actievenster.
3. Selecteer **Ontwerper** op de pagina **Modeltoewijzingen** in het actievenster.
4. Selecteer op de pagina **Ontwerper modeltoewijzing** in het actievenster de optie **Prestatietracering**.
5. Selecteer de meest recente tracering die is gegenereerd en selecteer vervolgens **OK**.

Door uw aanpassingen in de modeltoewijzing worden er geen dubbele query's meer uitgevoerd in de database. Het aantal aanroepen naar databasetabellen en gegevensbronnen voor deze modeltoewijzing is ook beperkt.

![Traceringsgegeven op de pagina Ontwerper modeltoewijzing 1](./media/er-calculated-field-ds-performance-mapping-5.png)

De totale uitvoeringstijd is ongeveer 20 keer verlaagd (van ongeveer 8 seconden tot ongeveer 400 milliseconden). Hierdoor zijn de prestaties van de hele ER-oplossing verbeterd.

![Traceringsgegeven op de pagina Ontwerper modeltoewijzing 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Bijlage 1: De componenten van de Microsoft ER-voorbeeldoplossing downloaden

U moet de volgende bestanden downloaden en lokaal opslaan.

| Bestand                                        | Inhoud |
|---------------------------------------------|---------|
| Versie 1 prestatieverbeteringsmodel     | [Voorbeeldconfiguratie van model voor ER-gegevens](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Versie 1.1 toewijzing voor prestatieverbetering | [Voorbeeldconfiguratie van ER-modeltoewijzing](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Versie 1.1 indeling voor prestatieverbetering  | [Voorbeeldconfiguratie van ER-indeling](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Bijlage 2: Het ER-raamwerk configureren

Voordat u het ER-raamwerk kunt gebruiken om de prestaties van de Microsoft ER-voorbeeldoplossing te verbeteren, moet u de minimale set ER-parameters configureren.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>ER-parameters configureren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Parameters van elektronische rapportage**.
3. Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Algemeen** de optie **Ontwerpmodus inschakelen** in op **Ja**.
4. Stel op het tabblad **Bijlagen** de volgende parameters in:

    - Selecteer in het veld **Configuraties** het type **Bestand** voor het bedrijf **DEMF**.
    - Selecteer in de velden **Taakarchief**, **Tijdelijk**, **Basislijn** en **Overige** het type **Bestand**.

Meer informatie over het configureren van ER-parameters vindt u in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Een ER-configuratieprovider activeren

Elke ER-configuratie die wordt toegevoegd, wordt gemarkeerd als het eigendom van een ER-configuratieprovider. De ER-configuratieprovider die is geactiveerd in de werkruimte **Elektronische rapportage** wordt hiervoor gebruikt. Daarom moet u een ER-configuratieprovider activeren in de werkruimte **Elektronische rapportage** voordat u ER-configuraties gaat toevoegen of bewerken.

> [!NOTE]
> Alleen de eigenaar van een ER-configuratie kan de configuratie bewerken. Daarom moet een geschikte ER-configuratieprovider worden geactiveerd in de werkruimte **Elektronische rapportage**, voordat een ER-configuratie kan worden bewerkt.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>De lijst met ER-configuratie providers bekijken

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.
3. Op de tabelpagina **Configuratieproviders** heeft elke providerrecord een unieke naam en een unieke URL. Bekijk de inhoud van deze pagina. Als er al een record bestaat voor **Litware, Inc.**, kunt u de volgende procedure, [Een nieuwe ER-configuratieprovider toevoegen](#ActivateProvider), overslaan.

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Een nieuwe ER-configuratieprovider toevoegen

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Verwante koppelingen** de tegel **Configuratieproviders**.
3. Selecteer **Nieuw** op de pagina **Configuratieproviders**.
4. Voer in het veld **Naam** de tekst **Litware, Inc.** in.
5. Voer in het veld **Internetadres** de tekst `https://www.litware.com` in.
6. Selecteer **Opslaan**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Een ER-configuratieprovider activeren

1. Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.
2. Selecteer op de pagina **Lokalisatieconfiguraties** in de sectie **Configuratieproviders** de tegel **Litware, Inc.** en selecteer **Instellen als actief**.

Meer informatie over ER-configuratieproviders vindt u in [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Aanvullende bronnen

- [Overzicht van elektronische rapportage](general-electronic-reporting.md)
- [De uitvoering van ER-indelingen traceren om prestatieproblemen op te lossen](trace-execution-er-troubleshoot-perf.md)
- [Ondersteuning van parameteraanroepen voor ER-gegevensbronnen van het type Berekend veld](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]