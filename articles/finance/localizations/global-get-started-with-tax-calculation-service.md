---
title: Aan de slag met belastingberekening
description: In dit artikel wordt uitgelegd hoe u belastingberekening instelt.
author: EricWangChen
ms.date: 10/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.custom: intro-internal
ms.search.form: TaxIntegrationTaxServiceParameters
ms.openlocfilehash: 42898823ffc366351c6f58f1fe9b924678ab4b49
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690378"
---
# <a name="get-started-with-tax-calculation"></a>Aan de slag met belastingberekening

[!include [banner](../includes/banner.md)]

In dit artikel vindt u informatie over hoe u aan de slag met het berekenen van belasting. De secties in dit artikel leiden u door het basisontwerp en de configuratiestappen in Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), Dynamics 365 Finance en Dynamics 365 Supply Chain Management. 

De configuratie omvat drie hoofdstappen.

1. In LCS installeert u de invoegtoepassing Belastingberekening.
2. Stel in RCS de functie Belastingberekening in. Deze instelling in niet specifiek voor een rechtspersoon. Deze kan worden gedeeld tussen rechtspersonen in Finance en Supply Chain Management.
3. In Finance en Supply Chain Management stelt u de parameters voor Belastingberekening in per rechtspersoon.

## <a name="high-level-design"></a>Basisontwerp

### <a name="runtime-design"></a><a name="runtime"></a> Runtime-ontwerp

De volgende afbeelding toont het basis-runtime-ontwerp van Belastingberekening. Aangezien Belastingberekening met meerdere Dynamics 365-toepassingen kan worden geïntegreerd, wordt in de afbeelding de integratie met Financiën als voorbeeld gebruikt.

1. Een transactie, zoals een verkoop- of inkooporder, wordt gemaakt in Financiën.
2. Financiën gebruikt automatisch de standaardwaarden van de btw-groep en de btw-groep voor artikelen.
3. Wanneer de knop **Btw** is geselecteerd voor de transactie, wordt de btw-berekening geactiveerd. Financiën verzendt vervolgens de nettolading naar de belastingberekeningsservice.
4. De belastingberekeningsservice matcht de nettolading met vooraf gedefinieerde regels in de btw-functie om tegelijkertijd een nauwkeurigere btw-groep en btw-groep voor artikelen te vinden.

    - Als de nettolading kan worden gematcht met de matrix **Toepasbaarheid belastinggroep**, wordt de waarde van de btw-groep overschreven met de waarde van de gematchte btw-groep in de toepasbaarheidsregel. Anders blijft de waarde van de btw-groep van Financiën worden gebruikt.
    - Als de nettolading kan worden gematcht met de matrix **Toepasbaarheid artikelbelastinggroep**, wordt de waarde van de artikelbelastinggroep overschreven met de waarde van de gematchte artikelbelastinggroep in de toepasbaarheidsregel. Anders blijft de waarde van de artikelbelastinggroep van Financiën worden gebruikt.

5. De service voor belastingberekening bepaalt de uiteindelijke belastingcodes door de intersectie van de btw-groep en de artikelbelastinggroep te gebruiken.
6. De service voor belastingberekening berekent de belasting op basis van de uiteindelijke belastingcodes die door de service zijn bepaald.
7. De service voor belastingberekening retourneert het resultaat van de belastingberekening aan Financiën.

![Runtime-ontwerp van de belastingberekening.](media/tax-calculation-runtime-logic.png)

### <a name="high-level-configuration"></a>Basisconfiguratie

De volgende stappen geven een basisoverzicht van het configuratieproces voor de service voor belastingberekening.

1. In LCS installeert u de invoegtoepassing **Belastingberekening** in uw LCS-project.
2. Maak in RCS de functie **Belastingberekening**.
3. Stel in RCS de functie **Belastingberekening** in:

    1. Selecteer de belastingconfiguratieversie.
    2. Maak belastingcodes.
    3. Maak een belastinggroep.
    4. Maak een belastinggroep voor artikelen.
    5. Optioneel: maak de toepasbaarheid van belastingroepen als u de standaard btw-groep wilt overschrijven die is ingevoerd vanuit de hoofdgegevens van de klant of leverancier.
    6. Optioneel: maak de toepasbaarheid van artikelgroepen als u de standaard btw-groep voor artikelen wilt overschrijven die is ingevoerd vanuit de artikelhoofdgegevens.

4. Voltooi en publiceer in RCS de functie **Belastingberekening**.
5. Selecteer in Financiën de gepubliceerde functie **Belastingberekening**.

Nadat u deze stappen hebt voltooid, worden de volgende instellingen automatisch gesynchroniseerd van RCS naar Financiën.

- Btw-codes
- Btw-groepen
- Btw-groepen voor artikel

In de overige secties van dit artikel vindt u meer gedetailleerde configuratiestappen.

## <a name="prerequisites"></a>Vereisten

Voordat u de resterende procedures in dit artikel kunt voltooien, moet aan de volgende vereisten zijn voldaan:<!--TO HERE-->

- U moet toegang tot uw LCS-account hebben en u moet een LCS-project hebben geïmplementeerd met een Tier 2-omgeving (of hoger) waarop versie 10.0.21 of hoger van Dynamics 365 wordt uitgevoerd.
- U moet een RCS-omgeving voor uw organisatie maken en u moet toegang tot uw account hebben. Zie [Overzicht Regulatory Configuration Service](rcs-overview.md) voor meer informatie over het maken van een RCS-omgeving.
- De volgende functies moeten zijn ingeschakeld in de werkruimte **Functiebeheer** van uw geïmplementeerde Finance- of Supply Chain Management-omgeving, op basis van uw bedrijfsbehoeften:

    - Service voor belastingberekening
    - Meerdere btw-registratienummers ondersteunen
    - Belasting in transferorder

- De volgende functies moeten zijn ingeschakeld in de werkruimte **Functiebeheer** van uw geïmplementeerde RCS-omgeving.

    - Globalisatiefuncties

- De volgende rollen moeten naar wens worden toegewezen aan de gebruikers in uw RCS-omgeving:

    - Ontwikkelaar elektronische rapportage
    - Ontwikkelaar van globaliseringsfunctie
    - Ontwikkelaar van belastingberekenfunctie
    - Functioneel consultant belastingberekenfunctie
    - Ontwikkelaar voor belastingservice

## <a name="set-up-tax-calculation-in-lcs"></a>Belastingberekening instellen in LCS

1. Aanmelden bij [LCS](https://lcs.dynamics.com)
2. Voltooi de configuratie voor de Microsoft Power Platform-integratie. Zie [Overzicht van invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor meer informatie.
3. Selecteer een van uw geïmplementeerde omgevingen en selecteer vervolgens **Een nieuwe invoegtoepassing installeren**.
4. Selecteer **Belastingberekening**.
5. Lees de algemene voorwaarden, ga hiermee akkoord en selecteer **Installeren**.

## <a name="set-up-tax-calculation-in-rcs"></a>Belastingberekening instellen in RCS

De stappen in deze sectie zijn niet gerelateerd aan een specifieke rechtspersoon. U hoeft deze procedure maar één keer uit te voeren en u kunt dit in elke rechtspersoon in RCS doen.

1. Meld u aan bij [RCS](https://marketing.configure.global.dynamics.com/).
2. Voeg in de werkruimte **Elektronische rapportage** een nieuwe configuratieprovider toe. Gebruik uw bedrijfsnaam als de naam van de provider. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.
3. Selecteer de configuratieprovider die u zojuist hebt gemaakt en selecteer **Instellen als actief**.
4. Selecteer de configuratieprovider **Microsoft** en selecteer vervolgens **Opslagplaatsen**.
5. Selecteer in het veld **Type** de optie **Globaal**.
6. Selecteer **Openen**.
7. Ga naar **Belastinggegevensmodel**, vouw de bestandsstructuur uit en selecteer vervolgens **Belastingconfiguratie**.
8. Selecteer de juiste [belastingconfiguratieversie](global-tax-calcuation-service-overview.md#versions) op basis van uw Finance-versie en selecteer vervolgens **Importeren**.
9. Selecteer in de werkruimte **Globalisatiefuncties** **Functies**, selecteer de tegel **Belastingberekening** en kies **Toevoegen**.

    > [!NOTE]
    > In versie 10.0.26 en hoger kunt u een demonstratiefunctie importeren voor de rechtspersoon **DEMF** voor demonstatiedoeleinden. Zie [Demonstratiegegevens voor functie importeren](tax-calculation-import-export-feature.md) voor meer informatie.

10. Selecteer een van de volgende functietypen:

    - **Nieuwe functie**: maak een functie-instelling met lege inhoud.
    - **Gebaseerd op bestaande functie**: maak een functie op basis van een bestaande functie en kopieer de inhoud uit de bestaande functie-instelling.

11. Geef een naam en beschrijving op voor de functie en selecteer **Functie maken**.

    Als de functie is gemaakt, wordt er automatisch een conceptversie van gemaakt. U kunt **Deze versie ophalen** om de conceptversie opnieuw te baseren op een willekeurige voltooide versie.

12. Selecteer de conceptversie van de functie en selecteer **Bewerken**. De pagina **Belastingberekening** wordt ingevuld.
13. Selecteer **Configuratieversie**. Als het goed is, wordt de configuratieversie weergegeven die u in stap 8 hebt geïmporteerd.

    Microsoft biedt een standaardbelastingconfiguratie voor belastingberekening. Met deze configuratie wordt aan de meeste vereisten voor belastingberekeningsgedrag voldaan. Deze wordt bijgewerkt op basis van marktfeedback. Als u de configuratie moet uitbreiden om aan specifieke vereisten te voldoen, raadpleegt u [Uitbreiding inbouwen in belastingservice](./tax-service-add-data-fields-tax-integration-by-extension.md) voor informatie over het genereren en selecteren van uw eigen belastingconfiguratie.

14. Nadat u **Configuratieversie** hebt geselecteerd, worden verschillende extra tabbladen weergegeven. Volg de volgorde die hier wordt weergegeven om de verplichte tabinstelling te voltooien.

    **Verplichte installatie**

    - **Belastingcodes**: onderhoud hoofdgegevens voor belastingcodes. Alle belastingcodes die op dit tabblad worden gemaakt, worden automatisch gesynchroniseerd met Finance wanneer u de huidige versie inschakelt.
    - **Belastinggroep**: definieer de hoofdgegevens van de belastinggroep en de belastingcodes onder de groep.
    - **Artikelbelastinggroep**: definieer de hoofdgegevens van de artikelbelastinggroep en de belastingcodes onder de groep.

    **Optionele instellingen**

    - **Toepasbaarheid belastinggroep**: definieer een matrix waarmee de belastinggroep wordt bepaald. Als er geen regels voor toepasbaarheid in deze matrix overeenkomen met het belastbare document van Dynamics 365, wordt voor de belastingberekening de standaardwaarde op de belastbare documentregel gebruikt.
    - **Toepasbaarheid artikelbelastinggroep**: definieer een matrix waarmee de artikelbelastinggroep wordt bepaald. Als er geen regels voor toepasbaarheid in deze matrix overeenkomen met het belastbare document van Dynamics 365, wordt voor de belastingberekening de standaardwaarde op de belastbare documentregel gebruikt.
    - **Toepasbaarheid belastingregistratienummer klant**: als u meerdere belastingregistratienummers voor één klant hebt, kan Belastingberekening automatisch het juiste belastingregistratienummer bepalen. In de matrix op dit tabblad definieert u de regels die moeten worden gebruikt om de bepaling te maken. Anders blijven Finance en Supply Chain Management het standaard belastingregistratienummer in belastingdocumenten voor verkooptransacties gebruiken.
    - **Toepasbaarheid belastingregistratienummer leverancier**: als u meerdere belastingregistratienummers voor één leverancier hebt, kan Belastingberekening automatisch het juiste belastingregistratienummer bepalen. In de matrix op dit tabblad definieert u de regels die moeten worden gebruikt om de bepaling te maken. Anders blijven Finance en Supply Chain Management het standaard belastingregistratienummer in belastingdocumenten voor inkooptransacties gebruiken.
    - **Toepasbaarheid lijstcode**: bepaal automatisch de waarde van het veld **Lijstcode** via flexibelere en configureerbare regels. In de matrix op dit tabblad definieert u de regels die moeten worden gebruikt om de bepaling te maken. Anders blijven Finance en Supply Chain Management de standaardcode in belastingdocumenten gebruiken.

15. Selecteer op het tabblad **Belastingcodes** de optie **Toevoegen** en voer de belastingcode en een beschrijving in.
16. Selecteer **Belastingcomponent**. De belastingcomponent is een groep methoden die is gedefinieerd in de vorige versie van de geselecteerde belastingconfiguratie. De volgende belastingcomponenten zijn beschikbaar:

    - Op nettobedrag
    - Op brutobedrag
    - Op hoeveelheid
    - Op marge
    - Belasting op belasting

17. Selecteer **Opslaan**. Er komen meer velden beschikbaar, op basis van de belastingcomponent die u hebt geselecteerd.
18. Gebruik de volgende opties om de aard van de belastingcode te identificeren:

    - Is vrijgesteld
    - Is gebruiksbelasting
    - Is terugboeking
    - Uitsluiten van berekening van basisbedrag

    Stel voor een scenario voor gebruiksbelasting één belastingcode met een positief belastingtarief in en markeer deze als **Is gebruiksbelasting**.

    Stel voor een terugboekingsscenario twee belastingcodes in, waarvan de ene een positief belastingtarief heeft en de andere een negatief belastingtarief, maar dezelfde tariefwaarde. Markeer de negatieve belastingcode als **Is terugboeking**. Zie [Mechanisme voor omgekeerde toeslagen van btw/GST-schema](emea-reverse-charge.md) voor meer informatie over de terugboekingsoplossing in Finance.

    Voor sommige belastingtypen die moeten worden uitgesloten van de berekening van het belastingbasisbedrag voor prijsinclusieve transacties (zoals invoerrechten in sommige landen of regio's) schakelt u het selectievakje **Uitsluiten van berekening van basisbedrag** in. Zie [Belasting berekenen bovenop de prijs wanneer Prijzen inclusief belastingen zijn ingeschakeld](global-exclude-from-tax-base-amount-calculation.md) voor meer informatie over deze parameter.

    Houd belastingtarieven en de belastingbedraglimieten voor deze belastingcode bij.

19. Herhaal stap 15 tot en met 18 om alle belastingcodes toe te voegen die vereist zijn.
20. Selecteer op het tabblad **Belastinggroep** de kolom **Belastinggroep**, voeg deze aan de matrix toe als de invoervoorwaarde en voeg vervolgens regels toe om de hoofdgegevens van de belastinggroep te onderhouden.

    Hier volgt een voorbeeld.

    | Belastinggroep    | Btw-codes           |
    | ------------ | ------------------- |
    | DEU_Dom | DEU_VAT19; DEU_VAT7 |
    | DEU_EU       | DEU_Exempt          |
    | BEL_Dom | BEL_VAT21; BEL_VAT6 |
    | BEL_EU       | BEL_Exempt          |

21. Selecteer op het tabblad **Artikelbelastinggroep** de kolom **Artikelbelastinggroep**, voeg deze aan de matrix toe als de invoervoorwaarde en voeg vervolgens regels toe om de hoofdgegevens van de belastinggroep te onderhouden.

    Hier volgt een voorbeeld.

    | Artikelbelastinggroep | Btw-codes                                    |
    | -------------- | -------------------------------------------- |
    | Vol           | DEU_VAT19; BEL_VAT21; DEU_Exempt; BEL_Exempt |
    | Gereduceerd        | DEU_VAT7; BEL_VAT6; DEU_Exempt; BEL_Exempt   |

22. Selecteer op het tabblad **Toepasbaarheid van belastinggroep** de kolommen die vereist zijn om de juiste belastinggroep te bepalen en selecteer vervolgens **Toevoegen**. Voer waarden voor elke kolom in of selecteer deze. Het veld **Belastinggroep** is de uiteindelijke uitvoer van deze matrix. Als dit tabblad niet is geconfigureerd, wordt de btw-groep op de transactieregel gebruikt.

    Hier volgt een voorbeeld.

    | Bedrijfsproces | Verzenden van | Zenden naar | Belastinggroep    |
    | ---------------- | --------- | ------- | ------------ |
    | Sales            | DEU       | DEU     | DEU_Dom |
    | Sales            | DEU       | FRA     | DEU_EU       |
    | Sales            | BEL       | BEL     | BEL_Dom |
    | Sales            | BEL       | FRA     | BEL_EU       |
    
    > [!NOTE]
    > Als de standaard btw-groep op uw belastbare documentregels correct is, laat u deze matrix leeg. Zie de sectie [Runtime-ontwerp](#runtime), eerder in dit artikel, voor meer informatie.

23. Selecteer op het tabblad **Toepasbaarheid van artikelbelastinggroep** de kolommen die vereist zijn om de juiste belastingcode te bepalen en selecteer vervolgens **Toevoegen**. Voer waarden voor elke kolom in of selecteer deze. Het veld **Artikelbelastinggroep** is de uiteindelijke uitvoer van deze matrix. Als dit tabblad niet is geconfigureerd, wordt de artikel-btw-groep op de transactieregel gebruikt.

    Hier volgt een voorbeeld.

    | Artikelcode | Belastinggroep voor artikel |
    | --------- | -------------- |
    | D0001     | Vol           |
    | D0003     | Gereduceerd        |

    > [!NOTE]
    > Als de standaard btw-groep voor artikelen op uw belastbare documentregels correct is, laat u deze matrix leeg. Zie de sectie [Runtime-ontwerp](#runtime), eerder in dit artikel, voor meer informatie.

    Zie [Logica voor bepaling van btw-groepen en item-btw-groepen](global-sales-tax-group-determination.md) voor meer informatie over de manier waarop belastingcodes worden bepaald in Belastingberekening.

24. Stel de toepasbaarheid van belastingregistratienummers voor klanten, belastingregistratienummers voor leveranciers en lijstcodes in op basis van de bedrijfsbehoeften.
25. Selecteer **Opslaan** en sluit de pagina.
26. Selecteer **Status wijzigen** \> **Voltooien**. Nadat de status is gewijzigd in **Voltooid**, kan de versie niet meer worden bewerkt.
27. Selecteer **Status wijzigen** \> **Publiceren**. Deze versie van de instelling van de belastingfunctie wordt naar de algemene opslagplaats gepusht en is zichtbaar voor elke rechtspersoon in Finance.

## <a name="set-up-tax-calculation-in-dynamics-365"></a>Belastingberekening instellen in Dynamics 365

Nadat u de installatie in RCS hebt voltooid, hebt u een gepubliceerde versie van de belastingfunctie. Voer de volgende stappen uit om Belastingberekening in te stellen in Finance.

De configuratie in deze sectie wordt per rechtspersoon uitgevoerd. U moet dit configureren voor elke rechtspersoon waarvoor u Belastingberekening wilt inschakelen in Finance.

1. Ga in Finance naar **Belasting** \> **Instellingen** \> **Belastingconfiguratie** \> **Parameters voor belastingberekening**.
2. Stel op het tabblad **Algemeen** de volgende velden in:

    - **De service voor belastingberekening inschakelen**: schakel dit selectievakje in om Belastingberekening voor de rechtspersoon in te schakelen. Als deze niet is ingeschakeld voor de huidige rechtspersoon, blijft de rechtspersoon de bestaande belastingengine gebruiken om belasting te bepalen en te berekenen.
    - **Functie-instellingen**: selecteer een gepubliceerde configuratie en versie van de belastingfunctie voor de rechtspersoon. Zie de vorige sectie van dit artikel voor meer informatie over het instellen en voltooien van een gepubliceerde belastingfunctie.
    - **Bedrijfsproces**: Selecteer de bedrijfsprocessen die u wilt inschakelen.

3. Definieer op het tabblad **Berekening** de verwachte afrondingsregel voor de rechtspersoon. Zie [Afrondingsregels voor belastingberekening](https://go.microsoft.com/fwlink/?linkid=2166988) voor meer informatie over de afrondingslogica.
4. Definieer op het tabblad **Foutafhandeling** de verwachte foutverwerkingsmethode voor de rechtspersoon. Er zijn drie opties beschikbaar:

    - Nee
    - Waarschuwing
    - Fout

    U kunt een foutverwerkingsmethode instellen voor elke resultaatcode in de sectie **Details**. Als sommige resultaatcodes niet worden gesynchroniseerd via de belastingberekeningsservice, kunt u ook een standaardmethode instellen in de sectie **Algemeen**.

5. Op het tabblad **Meerdere btw-registraties** kunt u afzonderlijk de btw-aangifte, de EU-verkooplijst en Intrastat intrekken om te werken met een scenario voor meerdere btw-registraties. Zie [Aangifte van meerdere btw-registraties](emea-reporting-for-multiple-vat-registrations.md) voor meer informatie over btw-aangiftes voor meerdere btw-registraties.
6. Sla de instellingen op en herhaal de vorige stappen voor elke extra rechtspersoon. Wanneer een nieuwe versie wordt gepublcieerd en u deze wilt toepassen, stelt u het veld **Functie-instellingen** in op het tabblad **Algemeen** van de pagina **Parameters voor belastingberekening** (zie stap 2).
