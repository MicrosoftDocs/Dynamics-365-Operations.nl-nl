---
title: Vast geplande orders
description: In dit onderwerp wordt uitgelegd hoe u geplande orders kunt fiatteren. Wanneer geplande orders worden gefiatteerd, worden ze omgezet in werkelijke inkooporders, transferorders of productieorders.
author: ChristianRytt
ms.date: 04/22/2021
ms.search.form: ReqTransPo, ReqTransFirmLog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-04-22
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 7e3a86e2aa0e7182f7f9e853b9e8667e677a8ad6
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/09/2022
ms.locfileid: "8102708"
---
# <a name="firm-planned-orders"></a>Vast geplande orders

[!include [banner](../../includes/banner.md)]

Geplande orders moeten worden *gefiatteerd* (dat wil zeggen, worden vrijgegeven) als onderdeel van het hoofdplanningsproces. Wanneer geplande orders worden gefiatteerd, worden ze omgezet in werkelijke inkooporders, transferorders of productieorders. Deze orders worden ook wel *vrijgegeven orders* of *openstaande orders* genoemd.

U kunt geplande orders op drie manieren fiatteren:

- **Handmatige fiatteren**: selecteer specifieke geplande orders in een lijst en start het proces vervolgens handmatig.
- **Automatisch fiatteren**: definieer een standaard time fence voor de fiattering voor behoefteplanningsgroepen, afzonderlijke artikelen en combinaties van artikelen en hoofdplannen. Tijdens de uitvoering van de hoofdplanning worden geplande orders vervolgens automatisch gefiatteerd als de orderdatum binnen de opgegeven time fence voor fiattering valt.
- **Op query's gebaseerde fiattering**: Definieer een query om geplande orders te selecteren op basis van de eigenschappen van deze orders. U kunt een batchtaak instellen om de query uit te voeren en overeenkomende orders regelmatig te fiatteren.

In dit onderwerp wordt elke methode uitgebreid beschreven.

## <a name="enable-the-features-that-are-described-in-this-topic"></a><a name="enable-features"></a>De functies inschakelen die in dit onderwerp worden beschreven

De meeste geplande orderfuncties zijn beschikbaar in alle standaardinstallaties van Microsoft Dynamics 365 Supply Chain Management die gebruikmaken van Planningsoptimalisatie. Enkele functies die in dit onderwerp worden beschreven, moeten echter worden ingeschakeld in Functiebeheer voordat u ze kunt gebruiken.

### <a name="turn-parallelized-firming-of-planned-orders-on-or-off"></a>Parallel fiatteren van geplande orders in- of uitschakelen

Parallel fiatteren zorgt voor een sneller fiatteringsproces door dit proces parallel te laten verlopen voor meerdere threads. Deze benadering kan handig zijn wanneer een groot aantal geplande orders moet worden gefiatteerd. Als u deze functionaliteit wilt gebruiken, moet de functie *Parallelle fiattering van geplande orders* voor het systeem zijn ingeschakeld. Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld. Vanaf Supply Chain Management 10.0.25 is deze functie verplicht en deze functie kan niet worden uitgeschakeld. Als u een versie ouder dan 10.0.25 gebruikt, kunt u deze functionaliteit in- of uitschakelen door naar [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) te gaan en te zoeken naar de functie *Parallelle fiattering van geplande orders*.

### <a name="enable-planned-order-firming-with-filtering"></a>Fiatteren van geplande orders inschakelen met filtering

Via fiatteren van geplande orders met filtering kunt u logische criteria definiëren om geplande orders te selecteren die moeten worden gefiatteerd. U kunt ook een voorbeeld bekijken van de geplande orders die zijn geselecteerd, het proces uitvoeren op de achtergrond en/of dit proces als een batchtaak plannen.

Vanaf Supply Chain Management versie 10.0.25 is deze functie standaard ingeschakeld. Beheerders kunnen deze functionaliteit in- of uitschakelen door te zoeken naar de functie *Parallelle fiattering van geplande orders* in de werkruimte [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="enable-auto-firming-for-planning-optimization"></a>Automatische fiattering voor Planningsoptimalisatie inschakelen

Met automatische fiattering kunt u tijdens de time fence voor fiattering geplande orders fiatteren als onderdeel van het hoofdplanningsproces. Automatische fiattering wordt altijd ondersteund voor de planningsengine die in Supply Chain Management is geïntegreerd. Als u de functie echter ook wilt gebruiken met Planningsoptimalisatie, moet u de functie inschakelen.

Als u deze functionaliteit beschikbaar wilt maken in uw systeem, gaat u naar [Functiebeheer](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) en schakelt u de functie *Automatisch fiatteren voor Planningsoptimalisatie* in. (Vanaf Supply Chain Management versie 10.0.21 is deze functie standaard ingeschakeld.)

## <a name="manually-firm-planned-orders"></a>Geplande orders handmatig fiatteren

Als u geplande orders handmatig wilt fiatteren, kunt u de geplande orders zoeken en selecteren die u wilt fiatteren. Vervolgens start u handmatig het fiatteringsproces.

1. [Open een willekeurige lijstpagina met geplande orders](approved-planned-order.md#view-planned-orders).
1. Gebruik het veld **Filteren**, het veld **Plannen** en de kolomkoppen om de lijst te filteren en te sorteren zodat u de geplande orders kunt vinden die u zoekt.
1. Schakel het selectievakje in voor elke geplande order die u wilt fiatteren. Als u alle geplande orders op de pagina wilt fiatteren die op dat moment op de pagina worden weergegeven (op basis van de filters die u hebt toegepast), slaat u deze stap over.
1. Selecteer een van de volgende knoppen in het actievenster:

    - **Fiatteren**: hiermee worden alleen de geselecteerde geplande orders gefiatteerd.
    - **Alle fiatteren**: alle geplande orders die op dit moment op de pagina worden weergegeven, worden gefiatteerd (op basis van de filters die u hebt toegepast), ongeacht de selectievakjes die zijn ingeschakeld. Deze optie kan handig zijn als u een groot aantal geplande orders wilt fiatteren.

1. Stel in het dialoogvenster **Fiatteren** op het sneltabblad **Parameters** de volgende velden in. (Veel van deze velden nemen de standaardwaarden over van het tabblad **Standaardupdate** op de pagina **Parameters van hoofdplanning**.)

    - **Markering bijwerken**: selecteer het beleid voor het markeren van de voorraad dat moet worden gebruikt bij het fiatteren van geplande orders.
    - **Fiatteren beëindigen bij fout**: stel deze optie in op *Ja* om het fiatteren van alle geselecteerde geplande orders te stoppen als er een fout optreedt in een van deze orders. Deze optie moet worden ingesteld op *Nee* als de optie **Fiattering parallel uitvoeren** is ingesteld op *Ja*.
    - **Fiattering parallel uitvoeren**: deze optie is alleen beschikbaar als de functie [*Geplande orders parallel fiatteren*](#enable-features) is ingeschakeld in uw systeem en als u twee of meer geplande orders voor fiattering hebt geselecteerd. Stel de optie in op *Ja* om de fiatteringsprocessen parallel uit te voeren. Met parallel fiatteren kunnen de prestaties worden verbeterd.
    - **Aantal threads**: deze optie is alleen beschikbaar als de functie [*Geplande orders parallel fiatteren*](#enable-features) is ingeschakeld in uw systeem en als u de optie **Parallel fiatteren** hebt ingesteld op *Ja*. Voer het aantal threads in dat moet worden gebruikt om het fiatteringsproces parallel uit te voeren. Zie [De prestaties van de hoofdplanning verbeteren](../master-planning-performance.md#number-of-threads) voor advies over het gebruik van deze optie in de hoofdplanning.

        > [!NOTE]
        > Met de waarde *0* (nul) in het veld **Aantal threads** verhoogt de uitvoeringstijd van de hoofdplanning. Het is daarom raadzaam de waarde in dit veld in te stellen op een waarde hoger dan 0.

    - **Groeperen op leverancier**: stel deze optie in op *Ja* om geplande inkooporders te groeperen en één inkooporder per leverancier te maken tijdens het fiatteren. U kunt ook één inkooporder maken met een regel voor elke geplande order.
    - **Groeperen op inkopersgroep**: stel deze optie in op *Ja* als u geplande inkooporders wilt groeperen en één inkooporder wilt maken waarin de leverancier en inkopersgroep worden gecombineerd. Als u deze optie wilt gebruiken, moet u ook de optie **Groeperen op leverancier** instellen op *Ja*.
    - **Groeperen op inkoopovereenkomst**: stel deze optie in op *Ja* om geplande inkooporders met dezelfde leverancier als bestaande inkoopovereenkomsten te groeperen en één inkooporder per inkoopovereenkomst te maken. Deze optie wordt automatisch ingeschakeld als **Groeperen op leverancier** is ingeschakeld. Als u **Groeperen op inkoopovereenkomst** wilt gebruiken, moet **Inkoopovereenkomst zoeken** zijn ingesteld op *Ja* op de pagina **Parameters van hoofdplanning**.
    - **Groeperen op periode** (in het gedeelte **Inkooporders**): selecteer de periode waarvoor u geplande inkooporders wilt groeperen. Als u deze optie wilt gebruiken, moet u ook de optie **Groeperen op leverancier** inschakelen.
    - **Groeperen op periode** (in het gedeelte **Transferorders**): selecteer de periode waarvoor u geplande transferorders wilt groeperen. De orders worden gegroepeerd op basis van de waarden **Van magazijn** en **Naar magazijn**.

    > [!NOTE]
    > Door elk van de opties 'Groeperen op' wordt elke geplande order geconverteerd naar een regel in de afzonderlijke inkooporder die het resultaat is van de groepering.

    ![Sneltabblad Parameters in het dialoogvenster Fiattering.](./media/manual-firming.png "Sneltabblad Parameters in het dialoogvenster Fiattering")

1. Stel de taak op het sneltabblad **Op de achtergrond uitvoeren** zo in dat deze in de batchmodus wordt uitgevoerd. Het heeft echter geen zin een terugkerend schema in te stellen wanneer u de fiattering handmatig uitvoert. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management. Bij handmatige fiattering worden bij de batchtaak echter alleen de op dat moment geselecteerde geplande orders verwerkt. Bij de batchtaak worden orders die niet aan de filters voldoen die op dat moment op de pagina zijn toegepast, niet verwerkt.
1. Selecteer **OK** om de instellingen toe te passen en de gefiatteerde orders te genereren.

## <a name="auto-firm-planned-orders"></a>Geplande orders automatisch fiatteren

Met automatische fiattering kunt u geplande orders fiatteren als onderdeel van het hoofdplanningsproces. U kunt een standaard time fence voor de fiattering definiëren voor behoefteplanningsgroepen, afzonderlijke artikelen en combinaties van artikelen en hoofdplannen. Tijdens de uitvoering van de hoofdplanning worden geplande orders vervolgens automatisch gefiatteerd als de orderdatum binnen de opgegeven time fence voor fiattering valt. Bij geplande orders die worden gegenereerd via Planningsoptimalisatie en de geïntegreerde hoofdplanningsbewerking wordt de orderdatum (dat wil zeggen, de begindatum) anders verwerkt.

> [!NOTE]
> Geplande inkooporders kunnen alleen automatisch worden gefiatteerd als de artikelen zijn gekoppeld aan een leverancier.
> 
> Afgeleide orders (dat wil zeggen, uitbestede inkooporders) die worden gefiatteerd, hebben de status *Wordt gecontroleerd* als Wijzigingen bijhouden is ingeschakeld.

> [!IMPORTANT]
> Voordat de functie die in deze sectie wordt beschreven, kan worden gebruikt met Planningsoptimalisatie, moet de functie [*Automatische fiattering voor planningsoptimalisatie*](#enable-features) zijn ingeschakeld in het systeem, zoals aan het begin van dit onderwerp is beschreven. Automatische fiattering kan altijd worden gebruikt met de geïntegreerde hoofdplanningsengine.

### <a name="auto-firming-with-planning-optimization-vs-the-built-in-planning-engine"></a>Automatisch fiattering met Planningsoptimalisatie versus de geïntegreerde planningsengine

Zowel Planningsoptimalisatie als de geïntegreerde planningsengine kunnen voor het automatisch fiatteren van geplande orders worden gebruikt. Er zijn echter enkele belangrijke verschillen. Bij Planningsoptimalisatie wordt bijvoorbeeld de orderdatum (dat wil zeggen, de begindatum) gebruikt om te bepalen welke geplande orders moeten worden gefiatteerd, terwijl bij de geïntegreerde planningsengine de behoeftedatum (dat wil zeggen, de einddatum) wordt gebruikt. In de volgende tabel krijgt u een overzicht van de verschillen.

| Functie | Planningsoptimalisatie | Geïntegreerde planningsengine |
|---|---|---|
| **Datumbasis** | Automatische fiattering is gebaseerd op de orderdatum (begindatum). | Automatische fiattering is gebaseerd op de behoeftedatum (einddatum). |
| **Levertijd** | Omdat de orderdatum (begindatum) de fiattering activeert, hoeft u geen rekening te houden met de doorlooptijd als onderdeel van de time fence voor fiattering. | Om te garanderen dat orders tijdig worden gefiatteerd, moet de time fence voor fiattering langer zijn dan de levertijdtijd. |
| **Orders voor de huidige week** | Als u alle orders wilt fiatteren die in de huidige week moeten beginnen, moet de time fence voor fiattering één week zijn. | Als u alle orders wilt fiatteren die in de huidige week moeten beginnen, moet de time fence voor fiattering de levertijd plus één week zijn. |

### <a name="set-up-auto-firming-and-the-firming-time-fence"></a>Automatisch fiatteren en de time fence voor fiatteren instellen

U kunt automatische fiattering inschakelen door een geautomatiseerde time fence voor fiatteren toe te wijzen aan de relevante behoefteplanning, zoals verderop in deze sectie wordt beschreven. Als automatische fiattering niet is ingeschakeld voor behoefteplanning of als de planning wordt gestart vanaf een specifieke pagina, zoals de pagina **Nettobehoeften** voor een vrijgegeven product, wordt het automatische fiatteringsproces overgeslagen.

Voor de opties voor groeperen en markeren voor automatische fiattering worden de waarden gebruikt van het tabblad **Standaardupdate** op de pagina **Parameters hoofdplanning**.

De time fence voor automatische fiattering wordt gedefinieerd door het aantal dagen dat u invoert voor de relevante behoefteplanning. U kunt de time fence voor automatisch fiatteren inschakelen en op de volgende manieren beheren:

- Als u de standaard time fence voor fiattering voor een behoefteplanningsgroep wilt definiëren, gaat u naar **Hoofdplanning \> Instellingen \> Behoefteplanning \> Behoefteplanningsgroepen** en selecteert u een behoefteplanningsgroep. Voer vervolgens op het sneltabblad **Overige** in het veld **Time fence automatische fiattering (dagen)** het aantal dagen in.
- Als u de time fence voor fiattering wilt overschrijven die voor de Ga naar Vrijgegeven producten van productgegevensbeheer om de vaste time fence te overschrijven die is gedefinieerd voor de behoefteplanningsgroep voor een bepaald artikel is gedefinieerd, gaat u naar **Productgegevensbeheer \> Vrijgegeven producten**. Selecteer op de actiepagina **Plannen** en selecteer vervolgens **Artikelbehoefteplanning**. Selecteer op het tabblad **Algemeen** de optie **Time fence overschrijven** en voer vervolgens in het veld **Time fence automatische fiattering (dagen)** het aantal dagen in.
- Als u de gedefinieerde time fence voor fiattering voor de behoefteplanningsgroep en artikelbehoefteplanning voor een specifiek hoofdplan wilt overschrijven, gaat u naar **Hoofdplanning \> Instellingen \> Hoofdplannen** en selecteert u een hoofdplan. Stel vervolgens op het sneltabblad **Time fence in dagen** de optie **Fiattering** in op *Ja* om het aantal dagen in te voeren.

Als u alle eerder genoemde time fences instelt op *0* (nul), wordt automatisch fiatteren uitgeschakeld voor de relevante gedekte artikelen.

## <a name="firm-planned-orders-by-using-a-query"></a>Geplande orders fiatteren met behulp van een query

Met op een query gebaseerde fiattering kunt u fiattering plannen op basis van criteria die vooraf zijn gedefinieerd. In tegenstelling tot automatische fiattering kunnen bij op query's gebaseerde fiattering verschillende subsets van orders op verschillende tijdstippen worden gefiatteerd. Bovendien kunt u handmatige of geautomatiseerde bewerkingen gebruiken om verschillende typen geplande orders te fiatteren. U kunt ook een voorbeeld bekijken van de gefiatteerde orders die zijn geselecteerd op basis van uw instellingen. U kunt daarom bevestigen dat de selectie voldoet aan uw verwachtingen.

U kunt automatische fiattering combineren met op query gebaseerde fiattering. Een op een query gebaseerd fiatteringstaak heeft bijvoorbeeld een time fence in de toekomst die langer is dan de time fence voor een overeenkomende configuratie voor automatische fiattering van de behoefte. Daarom worden met de op een query gebaseerde fiatteringstaak de geplande orders verwerkt voordat de automatische fiattering wordt geactiveerd. U kunt dit gedrag gebruiken als u orders voor specifieke leveranciers anders wilt plannen dan orders voor vergelijkbare producten van andere leveranciers.

> [!IMPORTANT]
> Voordat de functie die in deze sectie wordt beschreven, kan worden gebruikt, moet de functie [*Fiatteren van geplande orders met filtering*](#enable-features) zijn ingeschakeld in het systeem, zoals aan het begin van dit onderwerp is beschreven.

Volg deze stappen om een geplande order te fiatteren met behulp van het op een query gebaseerd fiatteringsproces.

1. Ga naar **Hoofdplanning \> Hoofdplanning \> Uitvoeren \> Fiatteren van geplande orders**.
1. Stel in het dialoogvenster **Fiatteren van geplande orders** op het sneltabblad **Parameters** de basisopties voor verwerking, markering en groepering in. Deze opties werken op dezelfde manier als in het dialoogvenster **Fiattering**. (Zie de vorige sectie voor omschrijvingen.) Stel vervolgens in de sectie **Plannen** de volgende velden in die uniek zijn voor het dialoogvenster **Fiatteren van geplande orders**.

    - **Plannen**: selecteer het hoofdplan dat moet worden toegepast tijdens het fiatteren van de geplande orders die met behulp van deze query worden gevonden.
    - **Time fence voor fiattering dagen vooruit**: selecteer hoe ver in de toekomst de verschillende vereisten en andere overwegingen moeten worden berekend op basis van de hoofdplanning.
    - **Time fence voor fiattering dagen terug**: selecteer hoe ver in het verleden de verschillende vereisten en andere overwegingen moeten worden berekend op basis van de hoofdplanning.

    ![Sneltabblad Parameters in het dialoogvenster Fiatteren van geplande orders.](./media/planned-order-firming-main-1.png "Sneltabblad Parameters in het dialoogvenster Fiatteren van geplande orders")

1. Als u wilt opgeven welke records in de order moeten worden opgenomen, selecteert u de knop **Filteren** op het sneltabblad **Op te nemen records**. Er wordt een standaard querydialoogvenster weergegeven, waarin u selectiecriteria, sorteercriteria en joins kunt definiëren. De velden werken op dezelfde manier als bij andere typen query's in Supply Chain Management. De velden hier zijn alleen-lezen en bevatten waarden die betrekking hebben op de query.

    ![Sneltabblad Op te nemen records in het dialoogvenster Fiatteren van geplande orders.](./media/planned-order-firming-main-2.png "Sneltabblad Op te nemen records in het dialoogvenster Fiatteren van geplande orders")

1. Selecteer **Voorbeeld** om een voorbeeld te bekijken van de inhoud van de gefiatteerde order, op basis van de instellingen tot nu toe. De lijst met geplande orders die worden gefiatteerd, wordt als een bericht weergegeven. U kunt vervolgens de gewenste instellingen aanpassen totdat in het voorbeeld de gefiatteerde order wordt weergegeven die u wilt.

    ![Voorbeeld van een weergave van een gefiatteerde order.](./media/planned-order-firming-preview.png "Voorbeeld van een weergave van een gefiatteerde order")

    > [!WARNING]
    > Met deze functie worden alle geplande orders gefiatteerd die aan de filtercriteria voldoen. Als het fiatteren van geplande orders niet goed wordt ingesteld, kunnen er veel ongewenste inkoop-, transfer- en productieorders worden gemaakt. Voordat u doorgaat, moet u altijd de knop **Voorbeeld** gebruiken om de records te valideren die worden opgenomen.

1. Stel op het sneltabblad **Op de achtergrond uitvoeren** de taak zo in dat deze in de batchmodus wordt uitgevoerd en/of stel een terugkerende planning in. De velden werken op dezelfde manier als bij andere typen [achtergrondtaken](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) in Supply Chain Management.
1. Selecteer **OK** om de instellingen toe te passen en de gefiatteerde orders te genereren.

## <a name="track-firmed-orders"></a>Gefiatteerde orders volgen

Volg deze stappen om een geplande order te volgen die is gefiatteerd.

1. [Open een willekeurige lijstpagina met geplande orders](approved-planned-order.md#view-planned-orders).
1. Open of selecteer de geplande order die u wilt volgen.
1. Selecteer in het actievenster op het tabblad **Weergeven** in de groep **Weergeven** de optie **Fiatteringshistorie**.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
