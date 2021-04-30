---
title: Aan de slag met belastingberekening
description: In dit onderwerp wordt uitgelegd hoe u belastingberekening instelt.
author: wangchen
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: a90455a338067331a6a44cab36b578ed01ed56eb
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890293"
---
# <a name="get-started-with-the-tax-calculation-preview"></a>Aan de slag met de belastingberekening (preview)

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

In dit onderwerp vindt u informatie over hoe u aan de slag met het berekenen van belasting. Eerst wordt u door de configuratiestappen geleid in Microsoft Dynamics Lifecycle Services (LCS), Regulatory Configuration Service (RCS), Dynamics 365 Finance en Dynamics 365 Supply Chain Management. Vervolgens wordt gekeken naar het gemeenschappelijke proces voor het gebruik van de functies voor belastingberekening in Finance- en Supply Chain Management-transacties.

De configuratie omvat vier hoofdstappen:

1. Installeer Belastingberekening in LCS.
2. Stel in RCS de functie Belastingberekening in. Deze instelling in niet specifiek voor een rechtspersoon. Deze kan worden gedeeld tussen rechtspersonen in Finance en Supply Chain Management.
3. In Finance en Supply Chain Management stelt u de parameters voor Belastingberekening in per rechtspersoon.
4. In Finance en Supply Chain Management maakt u transacties, zoals verkooporders, en gebruikt u Belastingberekening om belastingen te bepalen en te berekenen.

## <a name="prerequisites"></a>Vereisten

Voordat u de procedures in dit onderwerp kunt voltooien, moet aan de volgende vereisten zijn voldaan:

- U hebt toegang tot uw LCS-account en u hebt een LCS-project geïmplementeerd met een Tier 2-omgeving (of hoger) waarop versie 10.0.18 of hoger van Dynamics 365 wordt uitgevoerd.
- U hebt toegang tot uw RCS-account.
- U hebt contact opgenomen met Microsoft om de flighting in te schakelen in uw geïmplementeerde Finance- of Supply Chain Management-omgeving.

## <a name="set-up-tax-calculation-in-lcs"></a>Belastingberekening instellen in LCS

1. Aanmelden bij [LCS](https://lcs.dynamics.com)
2. Voltooi de configuratie voor de Microsoft Power Platform-integratie. Zie [Overzicht van invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor meer informatie.
3. Selecteer een van uw geïmplementeerde niet-productieomgevingen en selecteer vervolgens **Een nieuwe invoegtoepassing installeren**.
4. Selecteer **Belastingberekening (preview)**.
5. Lees de algemene voorwaarden, ga hiermee akkoord en selecteer **Installeren**.

## <a name="set-up-tax-calculation-in-rcs"></a>Belastingberekening instellen in RCS

De stappen in deze sectie zijn niet gerelateerd aan een specifieke rechtspersoon. U hoeft deze procedure maar één keer uit te voeren en u kunt dit in elke rechtspersoon in RCS doen.

1. Meld u aan bij [RCS](https://marketing.configure.global.dynamics.com/).
2. Voeg in Finance in het werkgebied **Elektronische rapportage** een nieuwe configuratieprovider toe. Gebruik uw bedrijfsnaam als de naam van de provider. Zie [Configuratieproviders maken en deze als actief markeren](../../fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11.md) voor meer informatie.
3. Selecteer de configuratieprovider die u zojuist hebt gemaakt en selecteer **Instellen als actief**.
4. Selecteer de configuratieprovider **Microsoft** en selecteer vervolgens **Opslagplaatsen**.
5. Selecteer in het veld **Type** de optie **Globaal**.
6. Selecteer **Openen**.
7. Ga naar **Belastinggegevensmodel**, vouw de bestandsstructuur uit en selecteer vervolgens **Belastingconfiguratie**.
8. Selecteer de nieuwste versie en selecteer **Importeren**.
9. Ga terug naar het werkgebied **Globalisatiefuncties (preview)** en selecteer **Functies**, de tegel **Belastingberekening** en **Toevoegen**.
10. Selecteer een van de volgende functietypen:

    - **Nieuwe functie**: maak een functie-instelling met lege inhoud.
    - **Gebaseerd op bestaande functie**: maak een functie op basis van een bestaande functie en kopieer de inhoud uit de bestaande functie-instelling.

11. Geef een naam en beschrijving op voor de functie en selecteer **Functie maken**.

    Als de functie is gemaakt, wordt er automatisch een conceptversie van gemaakt.

12. Selecteer de conceptversie van de functie en selecteer **Bewerken**. De pagina **Belastingberekening** wordt ingevuld.
13. Selecteer **Configuratieversie**. Als het goed is, wordt de configuratieversie weergegeven die u in stap 8 hebt geïmporteerd.

    Microsoft biedt een standaardbelastingconfiguratie voor de invoegtoepassing voor belastingberekening. Met deze configuratie wordt aan de meeste vereisten voor belastingberekeningsgedrag voldaan. Deze wordt bijgewerkt op basis van marktfeedback. Als u de configuratie moet uitbreiden om aan specifieke vereisten te voldoen, raadpleegt u [Uitbreiding inbouwen in belastingservice](./tax-service-add-data-fields-tax-integration-by-extension.md) voor informatie over het genereren en selecteren van uw eigen belastingconfiguratie.

    Nadat u **Configuratieversie** hebt geselecteerd, worden verschillende extra tabbladen weergegeven:

    - **Belastingcodes**: dit tabblad is verplicht. Het wordt gebruikt om hoofdgegevens voor belastingcodes te onderhouden. Alle belastingcodes die op dit tabblad worden gemaakt, worden automatisch gesynchroniseerd met Finance wanneer u de huidige versie van de instelling van de belastingfunctie in de rechtspersoon inschakelt.
    - **Toepasbaarheid van belastingcodes**: dit tabblad is verplicht. Het wordt gebruikt om een matrix te definiëren die de belastingcode, belastinggroep en artikelbelastinggroep bepaalt. De belastingcode die wordt bepaald, wordt gebruikt om het belastingbedrag te berekenen. De waarden van de velden **Belastingcode**, **Belastinggroep** en **Artikelbelastinggroep** worden geretourneerd naar Finance.
    - **Toepasbaarheid van belastingregistratienummer voor klanten**: dit tabblad is optioneel. Als u meerdere belastingregistratienummers voor één klant hebt, kan Belastingberekening automatisch het juiste belastingregistratienummer bepalen. In de matrix op dit tabblad definieert u de regels die worden gebruikt om de bepaling te maken. Anders blijven Finance en Supply Chain Management het standaard belastingregistratienummer in belastingdocumenten voor verkooptransacties gebruiken.
    - **Toepasbaarheid van belastingregistratienummer voor leveranciers**: dit tabblad is optioneel. Als u meerdere belastingregistratienummers voor één leverancier hebt, kan Belastingberekening automatisch het juiste belastingregistratienummer bepalen. In de matrix op dit tabblad definieert u de regels die worden gebruikt om de bepaling te maken. Anders blijven Finance en Supply Chain Management het standaard belastingregistratienummer in belastingdocumenten voor inkooptransacties gebruiken.
    - **Toepasbaarheid van lijstcode**: dit tabblad is optioneel. Het kan helpen bij het automatisch bepalen van de waarde van het veld **Lijstcode** via flexibelere en configureerbare regels. In de matrix op dit tabblad kunt u de regels definiëren die worden gebruikt om de bepaling te maken. Anders blijven Finance en Supply Chain Management de standaardcode in belastingdocumenten gebruiken.

14. Selecteer op het tabblad **Belastingcodes** de optie **Toevoegen** en voer de belastingcode en een beschrijving in.
15. Selecteer **Belastingcomponent**. De belastingcomponent is een groep methoden die is gedefinieerd in de vorige versie van de geselecteerde belastingconfiguratie. De volgende belastingcomponenten zijn beschikbaar:

    - Op nettobedrag
    - Op brutobedrag
    - Op hoeveelheid
    - Op marge
    - Belasting op belasting

16. Selecteer **Opslaan**. Er komen meer velden beschikbaar, op basis van de belastingcomponent die u hebt geselecteerd.
17. Gebruik de volgende opties om de aard van de belastingcode te identificeren:

    - Is vrijgesteld
    - Is gebruiksbelasting
    - Is terugboeking
    - Uitsluiten van berekening van basisbedrag

    Stel voor een scenario voor gebruiksbelasting één belastingcode met een positief belastingtarief in en markeer deze als **Is gebruiksbelasting**.

    Stel voor een terugboekingsscenario twee belastingcodes in, waarvan de ene een positief belastingtarief heeft en de andere een negatief belastingtarief, maar dezelfde tariefwaarde. Markeer de negatieve belastingcode als **Is terugboeking**. Zie [Mechanisme voor omgekeerde toeslagen van btw/GST-schema](emea-reverse-charge.md) voor meer informatie over de terugboekingsoplossing in Finance.
    
    Voor sommige belastingtypen die moeten worden uitgesloten in de berekening van het belastingbasisbedrag voor prijsinclusieve transacties, zoals invoerrechten in sommige landen, schakelt u het selectievakje **Uitsluiten van berekening van basisbedrag** in.

    Houd belastingtarieven en de belastingbedraglimieten voor deze belastingcode bij.

18. Herhaal stap 14 tot en met 17 om alle belastingcodes toe te voegen die vereist zijn.
19. Selecteer op het tabblad **Toepasbaarheid van belastingcodes** de kolommen die vereist zijn om de juiste belastingcode te bepalen en selecteer vervolgens **Toevoegen**.
20. Voer waarden voor elke kolom in of selecteer deze. De velden **Belastingcode**, **Belastinggroep** en **Artikelbelastinggroep** zijn de uitvoer van deze matrix.
21. Herhaal stap 19 tot en met 20 om de toepasbaarheid van registratienummers voor klantbelastingen, registratienummers voor leveranciersbelastingen en lijstcodes in te stellen.
22. Selecteer **Opslaan** en sluit de pagina.
23. Selecteer **Status wijzigen** \> **Voltooien**. Nadat de status is gewijzigd in **Voltooid**, kan de versie niet meer worden bewerkt.
24. Selecteer **Status wijzigen** \> **Publiceren**. Deze versie van de instelling van de belastingfunctie wordt naar de algemene opslagplaats gepusht en is zichtbaar voor elke rechtspersoon in Finance.

## <a name="dynamics-365-setup"></a>Dynamics 365-instellingen

Nadat u de installatie in RCS hebt voltooid, zoals beschreven in de vorige sectie, hebt u een gepubliceerde versie van de belastingfunctie. Voer de volgende stappen uit om Belastingberekening in te stellen in Finance.

De configuratie in deze sectie wordt per rechtspersoon uitgevoerd. U moet dit configureren voor elke rechtspersoon waarvoor u Belastingberekening wilt inschakelen in Finance.

1. Ga in Finance naar **Belasting** \> **Instellingen** \> **Belastingconfiguratie** \> **Instellingen voor Belastingberekening (preview)**.
2. Stel op het tabblad **Algemeen** de volgende velden in:

    - **Belastingberekening inschakelen**: schakel dit selectievakje in om de invoegtoepassing Belastingberekening voor de rechtspersoon in te schakelen. Als deze niet is ingeschakeld voor de huidige rechtspersoon, blijft de rechtspersoon de bestaande belastingengine gebruiken om belasting te bepalen en te berekenen.
    - **Functie-instellingen**: selecteer een gepubliceerde configuratie en versie van de belastingfunctie voor de rechtspersoon. Zie de vorige sectie van dit onderwerp voor meer informatie over het instellen en voltooien van een gepubliceerde belastingfunctie.
    - **Bedrijfsproces**: Selecteer de bedrijfsprocessen die u wilt inschakelen.
    - **Aanpassing van belastingcode inschakelen**: stel deze optie in op **Ja** om aanpassingen in belastingcode in te schakelen op de pagina voor btw.

3. Definieer op het tabblad **Berekening** de verwachte afrondingsregel voor de rechtspersoon.
4. Definieer op het tabblad **Foutafhandeling** de verwachte foutverwerkingsmethode voor de rechtspersoon. Er zijn drie opties beschikbaar voor elke resultaatcode:

    - No
    - Waarschuwing
    - Fout

5. Sla de instellingen op.
6. Herhaal stap 1 tot en met 5 voor elke extra rechtspersoon.

## <a name="transaction-processing"></a>Transacties verwerken

Nadat u alle configuratieprocedures hebt voltooid, kunt u Belastingberekening gebruiken om de belasting in Finance te bepalen en te berekenen. De stappen voor het verwerken van transacties blijven hetzelfde. De volgende transacties worden ondersteund in versie 10.0.18 van Finance:

- Verkoopproces

    - Verkoopofferte
    - Verkooporder
    - Bevestiging
    - Orderverzamellijst
    - Pakbon
    - Verkoopfactuur
    - Creditnota
    - Retourorder
    - Kopteksttoeslag
    - Regeltoeslag

- Aankoopproces

    - Inkooporder
    - Bevestiging
    - Ontvangstlijst
    - Ontvangst van producten
    - Inkoopfactuur
    - Kopteksttoeslag
    - Regeltoeslag
    - Creditnota
    - Retourorder
    - Opdracht tot inkoop
    - Regeltoeslag opdracht tot inkoop
    - Offerteaanvraag
    - Kopteksttoeslag offerteaanvraag
    - Regeltoeslag offerteaanvraag

- Voorraadproces

    - Transferorder – verzenden
    - Transferorder - ontvangen