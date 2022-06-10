---
title: Voorraadboeking
description: In dit onderwerp wordt het tabblad Voorraadboeking op de pagina Voorraadboekingsprofiel uitgelegd.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783366"
---
# <a name="inventory-posting"></a>Voorraadboeking

Het tabblad **Voorraad** op de pagina **Voorraadboekingsprofielen** wordt gebruikt om te bepalen hoe voorraadtransacties naar het grootboek worden geboekt. Voorraadtransacties zijn transacties die niet op basis van verkooporders, inkooporders of productieorders worden gemaakt. Met voorraadtransacties worden de fysieke en financiële updates tegelijkertijd naar de voorraad geboekt. Eén uitzondering is transferorders die fysieke en financiële updates scheiden wanneer u de voorraad verzend en ontvangt.

In de volgende tabel vindt u enkele voorbeelden van voorraadtransacties.

| Transactietype | Ontvangst of uitgifte | Fysieke boeking, financiële boeking of beide | Description |
|---|---|---|---|
| Mutatie | Beide | Beide | <p>Een mutatiejournaal is een voorraadjournaal dat u kunt gebruiken om voorraad toe te voegen of te verwijderen. Het mutatiejournaal werkt als een voorraadcorrectiejournaal. Eén belangrijk verschil is echter dat de hoofdrekening wordt opgegeven waarmee de journaalregel wordt tegengeboekt.</p><p>Met het mutatiejournaal worden beginsaldi en eenmalige correcties ingevoerd die in rekening moeten worden gebracht. Het mutatiejournaal wordt bijvoorbeeld gebruikt wanneer voorraad wordt verwijderd voor een verkoopmonster.</p><p>Als het journaal wordt geboekt, worden de fysieke en financiële updates tegelijkertijd uitgevoerd.</p><p>Positieve hoeveelheden op de journaalregels vertegenwoordigen ontvangsten en negatieve hoeveelheden vertegenwoordigen uitgiften.</p> |
| Voorraadcorrectie | Beide | Beide | Een voorraadcorrectiejournaal wordt gebruikt om voorraad toe te voegen of te verwijderen. Er mag geen tegenrekening worden geselecteerd. Alleen de rekeningen die zijn opgegeven op de pagina **Voorraadboekingsprofiel** worden gebruikt om de grootboekpost bij te werken. |
| Overboeking (journaal) | Beide | Beide | <p>Met een overboekingsjournaal wordt voorraad van de ene naar de andere locatie verplaatst (met behulp van opslagdimensies). De productgegevens van een voorraadtransactie worden bijgewerkt met nieuwe product- of traceringsdimensies.</p><p>Met een overboekingsjournaal wordt één regel gemaakt voor de verplaatsing van een artikel. Deze regel heeft velden 'van' en 'naar' voor de voorraaddimensies. Met elke regel in een overboekingsjournaal worden twee voorraadtransacties gemaakt. Er wordt één transactie gemaakt voor de 'van'-voorraaddimensies. Dit is de uitgifte en heeft een negatieve hoeveelheid. De andere transactie wordt gemaakt voor de 'naar'-voorraaddimensies. Dit is de ontvangst en heeft een positieve hoeveelheid.</p><p>Met overboekingsjournalen wordt mogelijk geen boekstuk gemaakt als de voorraadverplaatsing als een niet-financiële overboeking wordt beschouwd. Voorraaddimensies die verschillen voor de waarden 'van' en 'naar', worden niet gemarkeerd met de optie **Financiële voorraad** op de pagina **Opslagdimensiegroep** of **Traceringsdimensiegroep**. Als de optie **Financiële voorraad** bijvoorbeeld niet is gemarkeerd voor de dimensie **Locatie** en u de voorraad van de ene naar de andere locatie hebt verplaatst in dezelfde locatie en hetzelfde magazijn, wordt er geen boekstuk gemaakt.</p><p>Overboekingsjournalen verschillen van transferorders omdat er geen documenten voor de verplaatsing zijn. Het bijwerken wordt in één transactie uitgevoerd door het journaal te boeken. Met een transferorder kunnen daarentegen orderverzamel- en verzenddocumenten worden gegenereerd, waarbij twee updates nodig zijn om de transactie te verwerken.</p> |
| Zending van transferorder | Probleem | Beide | <p>Wanneer u een nieuwe transferorder maakt, heeft elke combinatie van een regel en een voorraaddimensie twee voorraadtransacties: één voor de transferorderverzending en één voor de ontvangst van de transferorder. Als u de transferorder verzendt, worden er twee voorraadtransacties bijgewerkt en worden er twee extra voorraadtransacties gemaakt voor de transit van goederen, voor in totaal vier voorraadtransacties.</p><ol><li>De eerste voorraadtransactie wordt gebruikt om het artikel te verwijderen uit het bronmagazijn en de bronlocatie. De uitgiftestatus van deze transactie is **Verkocht** om aan te geven dat het artikel niet meer beschikbaar is in het magazijn.</li><li>De tweede voorraadtransactie wordt gebruikt om het artikel toe te voegen aan het transitmagazijn dat is geselecteerd voor het magazijn waaruit het artikel wordt overgebracht. De ontvangststatus van deze transactie is **Ingekocht**.</li><li>De derde voorraadtransactie is voor de overboeking van het transitmagazijn naar het doelmagazijn. De uitgiftestatus van deze transactie is **Fysiek gereserveerd**. Met deze status wordt gegarandeerd dat het artikel niet door een ander proces kan worden verbruikt terwijl het nog in transit is.</li><li>De vierde voorraadtransactie is voor de ontvangst van goederen in het doelmagazijn. De ontvangststatus van deze transactie is **Besteld**.</li></ol> |
| Transferorder ontvangst | Ontvangst | Beide | Wanneer een transferorder wordt ontvangen in het doelmagazijn, wordt de voorraadstatus van de voorraadtransactie in het transitmagazijn (nummer 3 in het voorgaande voorbeeld) gewijzigd in **Verkocht** en wordt de voorraadstatus van de voorraadtransactie voor het doelmagazijn gewijzigd in **Ingekocht**. |
| Stuklijsten | Beide | Beide | U kunt een stuklijstjournaal gebruiken om een product gereed te melden en de grondstoffen te verbruiken die tijdens het proces zijn verbruikt zonder een productieorder te gebruiken. Een stuklijstjournaal bevat doorgaans ten minste één positieve regel voor het eindproduct en één of meer negatieve regels voor de grondstoffen die worden verbruikt. De eindproductregel is een ontvangst in de voorraad, terwijl de negatieve regels uitgiften van de voorraad voor de grondstoffen zijn. Wanneer u een stuklijstjournaal maakt, is de eerste regel de stuklijstkoptekst en de volgende regels die worden toegevoegd, zijn de stuklijstregels. |
| Wijziging aan voorraadeigendom | Beide | Beide | Het wijzigingsjournaal van het voorraadeigendom wordt gebruikt om het eigendom van geconsigneerde voorraad van de leverancier te wijzigen in uw organisatie. Wijzigingsjournalen van voorraadeigendom lijken op journalen voor voorraadoverboeking, in zoverre dat twee voorraadtransacties zijn gerelateerd aan elke combinatie van een regel en een voorraaddimensie. Met één voorraadtransactie wordt de voorraad van de leverancier in de dimensie **Eigendom** verwijderd, en met de andere voorraadtransactie wordt het artikel toegevoegd aan de rechtspersoon in de dimensie **Eigendom**. |
| Artikelontvangst | Ontvangst | Fysiek | Met een artikelontvangstjournaal wordt de ontvangststatus van de voorraad gewijzigd in **Geregistreerd**. Dit journaal wordt meestal gebruikt voor de inkooporderontvangst van goederen en verkooporderretouren. |
| Productie-invoer | Ontvangst | Fysiek | Een productie-invoerjournaal lijkt op een artikelontvangstjournaal. Productie-invoer wordt gebruikt om eindproducten van een productieorder in het magazijn te ontvangen. Wanneer het journaal wordt geboekt, wordt de status van de voorraadtransactie gewijzigd in **Geregistreerd**. |
| Tellen | Beide | Beide | Een tellingsjournaal wordt gebruikt om de hoeveelheid artikelen te registreren die zijn geteld voor een specifieke combinatie van voorraaddimensies. Voorraadtransacties worden gemaakt wanneer de regel van het journaal een telverschil heeft. Een regel met een hogere getelde hoeveelheid veroorzaakt een ontvangst in de voorraad. Een regel met een lagere getelde hoeveelheid veroorzaakt een uitgifte in de voorraad. Regels waarvan de getelde hoeveelheid overeenkomt met de verwachte hoeveelheid hebben geen voorraadtransacties. |
| Telling labels | Niet van toepassing | Niet van toepassing | Een labeltellingsjournaal wordt gebruikt om voorraadlabels bij te houden die zijn toegewezen en gebruikt in een volledige voorraadtelling. U kunt het journaal gebruiken om een labelnummer toe te wijzen aan een specifieke combinatie van een artikel en een voorraaddimensie, en om de status van dat label bij te houden tijdens een volledige voorraad. Met labeltellingsjournalen worden geen voorraadtransacties gemaakt. |
| Kwaliteitsorders | Probleem | Fysiek | <p>Een kwaliteitsorder wordt gebruikt om testresultaten voor een bepaalde partij in de voorraad te registreren. Elke kwaliteitsorder is gerelateerd aan een bestaande voorraadtransactie of een deel van een voorraadtransactie.</p><p>Met een kwaliteitsorder wordt in twee situaties een nieuwe voorraadtransactie gegenereerd:</p><ul><li>De kwaliteitsorder wordt gemarkeerd als **Destructieve test** op het tabblad **Algemeen**.</li><li>De kwaliteitsorder wordt gemarkeerd als **In quarantaine bij validatiefout** op het tabblad **Algemeen** en de test slaagt niet voor de validatie. In dit geval worden twee voorraadtransacties gemaakt. Met de ene voorraadtransactie wordt het artikel uit de oorspronkelijke combinatie van voorraaddimensie en locatie verwijderd, en met de andere wordt het artikel toegevoegd aan het quarantainemagazijn.</li></ul> |
| Quarantaineorders | Beide | Beide | <p>De voorraadtransacties van een quarantaineorder zijn vergelijkbaar met die van een transferorder. Er wordt een quarantainemagazijn gebruikt om de voorraad bij te houden. Er zijn twee ontvangsttransacties en twee uitgiftetransacties.</p><p>Wanneer u de order in eerste instantie maakt, worden er twee transacties gemaakt. De ontvangsttransactie heeft de status **Besteld** voor het quarantainemagazijn dat is gekoppeld aan het magazijn waar het artikel zich bevindt. De uitgiftetransactie heeft de status **In bestelling** voor het magazijn waarin het artikel is opgeslagen.</p><p>Wanneer u de quarantaineorder start, worden er twee extra transacties gemaakt en worden de bestaande transacties bijgewerkt. De status van de ontvangsttransactie voor het quarantainemagazijn wordt gewijzigd in **Ontvangen** en de status van de uitgiftetransactie voor het opslagmagazijn wordt gewijzigd in **Ingehouden**.</p><p>De twee nieuwe transacties worden gebruikt om de uiteindelijke verplaatsing terug naar het opslagmagazijn aan te geven. De ontvangsttransactie heeft de status **Besteld** voor het opslagmagazijn en die uitgiftetransactie heeft de status **Fysiek gereserveerd** voor het quarantainemagazijn.</p><p>Wanneer u een quarantaineorder als gereed rapporteert, wordt met deze bewerking de fysieke update van de quarantaineorder vertegenwoordigd. De ontvangststatus in het opslagmagazijn wordt gewijzigd in **Ontvangen**.</p><p>Wanneer u de quarantaineorder beëindigt, wordt met deze bewerking de financiële update van de quarantaineorder vertegenwoordigd. De status van de uitgiftetransacties wordt gewijzigd in **Verkocht** en de status van de ontvangsttransacties wordt gewijzigd in **Ingekocht**.</p><p>U kunt de quarantaineorder ook buiten gebruik stellen. Met deze bewerking wordt het artikel uit de voorraad verwijderd. Wanneer u een quarantaineorder buiten gebruik stelt, blijven er slechts drie transacties over. De ontvangsttransactie voor het opslagmagazijn wordt verwijderd en de status van de resterende ontvangsttransactie wordt gewijzigd in **Ingekocht**. De status van de twee uitgiftetransacties wordt gewijzigd in **Verkocht**. Deze bewerking is een fysieke en financiële update voor de order.</p> |

## <a name="fixed-receipt-price-posting"></a>Boeking van vaste ontvangstprijs

Met vaste ontvangstprijs kunt u standaardkosten voor een product gebruiken. Het is een alternatief voor het selecteren van de optie **Standaardkosten** op de pagina **Artikelmodelgroep** voor een artikel. Het belangrijkste verschil wanneer u een vaste ontvangstprijs gebruikt, is dat de kostprijs die momenteel is geconfigureerd, voor het artikel wordt gebruikt wanneer de ontvangst naar de voorraad wordt geboekt. Er is geen kostprijsherwaarderingsproces voor een vaste ontvangstprijs. Wanneer een financiële update wordt geboekt, wordt de huidige kostprijs gebruikt bij het boeken. Als de kostprijs die bij ontvangst wordt gebruikt en de factuur verschillen, wordt het verschil geboekt naar de winst- en verliesrekeningen van de vaste ontvangstprijs.

Als u desgewenst een vaste ontvangstprijs voor een product wilt gebruiken, moet u de volgende configuratie voltooien:

- Schakel het selectievakje **Fysieke voorraad boeken** in op de pagina **Artikelmodelgroep** voor het artikel dat is geselecteerd op de voorraadtransactieregel.
- Schakel het selectievakje **Vaste ontvangstprijs** op de pagina **Artikelmodelgroep** in.
- Geef op de pagina **Voorraadboekingsprofiel** de hoofdrekeningen voor de volgende boekingstypen op:

    - Winstrekening vaste ontvangstprijs
    - Verliesrekening vaste ontvangstprijs

Zie [Vaste ontvangstprijs](/supply-chain/cost-management/fixed-receipt-price.md) voor meer informatie.

## <a name="catch-weight-posting"></a>Catch weight-boeking

Catch weight-producten worden vaak gebruikt in bedrijfstakken zoals de voedselindustrie waarin het gewicht en/of de grootte van producten iets varieert. Catch weight-producten gebruiken twee maateenheden: een voorraadeenheid en een catch weight-eenheid. Het gewicht van voorraad wanneer deze een magazijn binnenkomt kan afwijken van het gewicht van de voorraad als deze het magazijn verlaat. Met de verwerking van catch weight-producten wordt de voorraad aangepast.

Als er een afwijking is in catch weight, worden de verschillen geboekt naar de rekeningen die zijn opgegeven in de velden **Catch weight-verlies** en **Catch weight-winst** op de pagina **Voorraadboekingsprofiel**. Meestal wordt in beide velden dezelfde hoofdrekening opgegeven.

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen en zijn voorbeeldhoofdrekeningen en omschrijvingen opgenomen.

- De kolom Debet/Credit? geeft aan of de transactie meestal debet- of credittransacties betreft. In sommige gevallen kan de transactie debet- of credittransacties boeken.
- De kolom "Vereffeningsrekening" geeft aan of het boekingstype een vereffeningsrekening is. Met andere woorden: het bedrag dat op deze rekening wordt geboekt, wordt automatisch teruggeboekt wanneer een latere transactie wordt geboekt.
- De kolom "P/F" geeft het type boeking aan. "P" staat voor fysieke boeking en "F" staat voor financiële boeking.
- De kolom "Volgen" geeft aan of de hoofdrekening voor het boekingstype gewoonlijk hetzelfde is als de hoofdrekening voor een ander boekingstype. Met name wordt het boekingstype aangegeven dat doorgaans voor de boeking wordt gebruikt.

> [!NOTE]
> De hoofdrekeningen en hoofdrekeningnamen in de tabel zijn suggesties. Het is raadzaam om samen met uw accountant te bepalen wat de beste configuratie is voor uw bedrijfsbehoeften.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | P/F | Volgen | Description |
|---|---|---|---|---|---|---|---|---|
| Verliesrekening variabel gewicht | 510520 | Voorraadcorrectie | Onkosten | | Nr. | Beide | Winstrekening variabel gewicht | Deze rekening wordt gebruikt wanneer u een voorraadtransactie maakt waarbij het catch weight-bedrag lager is. |
| Winstrekening variabel gewicht | 510520 | Voorraadcorrectie | Onkosten | | Nr. | Beide | Verliesrekening variabel gewicht | Deze rekening wordt gebruikt wanneer u een voorraadtransactie maakt waarbij het catch weight-bedrag hoger is. |

Zie voor meer informatie over catch weight-producten [Informatie over catch weight-artikelen](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) en [Verwerking van catch weight-producten bij magazijnbeheer](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Boeking van overboeking van voorraad naar vaste activa

Het voorraad naar vaste-activajournaal (**Vaste activa** \> **Journalen** \> **Voorraad naar vaste-activajournaal**) wordt gebruikt om artikelen uit de voorraad te verplaatsen en deze te converteren naar vaste activa. Zie [Integratie vaste activa](/fixed-assets/fixed-asset-integration.md) voor meer informatie.

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen en zijn voorbeeldhoofdrekeningen en omschrijvingen opgenomen.

- De kolom Debet/Credit? geeft aan of de transactie meestal debet- of credittransacties betreft. In sommige gevallen kan de transactie debet- of credittransacties boeken.
- De kolom "Vereffeningsrekening" geeft aan of het boekingstype een vereffeningsrekening is. Met andere woorden: het bedrag dat op deze rekening wordt geboekt, wordt automatisch teruggeboekt wanneer een latere transactie wordt geboekt.
- De kolom "P/F" geeft het type boeking aan. "P" staat voor fysieke boeking en "F" staat voor financiële boeking.
- De kolom "Volgen" geeft aan of de hoofdrekening voor het boekingstype gewoonlijk hetzelfde is als de hoofdrekening voor een ander boekingstype. Met name wordt het boekingstype aangegeven dat doorgaans voor de boeking wordt gebruikt.

> [!NOTE]
> De hoofdrekeningen en hoofdrekeningnamen in de tabel zijn suggesties. Het is raadzaam om samen met uw accountant te bepalen wat de beste configuratie is voor uw bedrijfsbehoeften.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | P/F | Volgen | Description |
|---|---|---|---|---|---|---|---|---|
| Probleem met vaste activa | 180100 | Materiële vaste activa | Activum | Credit | Nr. | Beide | Niet van toepassing | Deze rekening wordt gebruikt wanneer u een voorraad naar een vaste-activajournaal overboekt om een artikel uit de voorraad te verwijderen en te converteren naar een vast activum. |

## <a name="moving-average-posting"></a>Boeking van zwevend gemiddelde

Het zwevende gemiddelde is een permanente kostprijsberekeningsmethode die is gebaseerd op het gemiddeldeprincipe. De kosten voor voorraaduitgiften worden niet gewijzigd wanneer de inkoopkosten worden gewijzigd. Het verschil wordt gekapitaliseerd en is gebaseerd op een proportionele berekening. Het overblijvende bedrag zijn onkosten.

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen met voorbeeldhoofdrekeningen en omschrijvingen.

- De kolom Debet/Credit? geeft aan of de transactie meestal debet- of credittransacties betreft. In sommige gevallen kan de transactie debet- of credittransacties boeken.
- De kolom "Vereffeningsrekening" geeft aan of het boekingstype een vereffeningsrekening is. Met andere woorden: het bedrag dat op deze rekening wordt geboekt, wordt automatisch teruggeboekt wanneer een latere transactie wordt geboekt.
- De kolom "P/F" geeft het type boeking aan. "P" staat voor fysieke boeking en "F" staat voor financiële boeking.
- De kolom "Volgen" geeft aan of de hoofdrekening voor het boekingstype gewoonlijk hetzelfde is als de hoofdrekening voor een ander boekingstype. Met name wordt het boekingstype aangegeven dat doorgaans voor de boeking wordt gebruikt.

> [!NOTE]
> De hoofdrekeningen en hoofdrekeningnamen in de tabel zijn suggesties. Het is raadzaam om samen met uw accountant te bepalen wat de beste configuratie is voor uw bedrijfsbehoeften.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | P/F | Volgen | Description |
|---|---|---|---|---|---|---|---|---|
| Prijsverschil voor zwevend gemiddelde | 510600 | Prijsverschil voor zwevend gemiddelde | Onkosten | Beide | Nr. | Beide | Niet van toepassing | Deze rekening wordt gebruikt wanneer er een verschil is in de kosten tussen de ontvangst en de factuur. |
| Herwaardering voor zwevend gemiddelde | 510610 | Herwaardering zwevend gemiddelde | Onkosten | Beide | Nr. | Beide | Niet van toepassing | Deze rekening wordt gebruikt als u de kosten van het zwevend gemiddelde van een product aanpast. |

## <a name="sample-posting-profile-configuration"></a>Voorbeeldconfiguratie van boekingsprofiel

In de volgende tabel ziet u voorbeelden van de standaardboekingstypen met voorbeeldhoofdrekeningen en omschrijvingen.

| Boekingstype | Voorbeeld van hoofdrekening | Voorbeeld van hoofdrekeningnaam | Rekeningtype | Debet/Credit? | Vereffeningsrekening | P/F | Volgen | Description |
|---|---|---|---|---|---|---|---|---|
| Voorraaduitgifte | 140100 | Materiaalvoorraad | Activum | Credit | Nr. | Beide | Voorraadontvangst | Deze rekening wordt gebruikt wanneer een voorraadtransactie die wordt geboekt een uitgifte (negatieve hoeveelheid) is en die niet is gerelateerd aan verkoop, inkoop of productie. De tegenrekening voor deze rekening is de rekening Voorraaduitgave, verlies. Deze rekening vertegenwoordigt doorgaans de voorraad op de balans. |
| Voorraaduitgave, verlies | 510100 | Winst en verlies van voorraad | Onkosten | Debet | Nr. | Beide | Voorraaduitgave, winst | Deze rekening wordt gebruikt wanneer een voorraadtransactie die wordt geboekt een uitgifte (negatieve hoeveelheid) is en die niet is gerelateerd aan verkoop, inkoop of productie. De tegenrekening voor deze rekening is de rekening Voorraaduitgifte. |
| Voorraadontvangst | 140100 | Materiaalvoorraad | Activum | Debet | Nr. | Beide | Voorraaduitgifte | Deze rekening wordt gebruikt wanneer een voorraadtransactie die wordt geboekt een ontvangst (positieve hoeveelheid) is en die niet is gerelateerd aan verkoop, inkoop of productie. De tegenrekening voor deze rekening is de rekening Voorraaduitgave, winst. Deze rekening vertegenwoordigt doorgaans de voorraad op de balans. |
| Voorraaduitgave, winst | 510100 | Winst en verlies van voorraad | Onkosten | Credit | Nr. | Beide | Voorraaduitgave, verlies | Deze rekening wordt gebruikt wanneer een voorraadtransactie die wordt geboekt een ontvangst (positieve hoeveelheid) is en die niet is gerelateerd aan verkoop, inkoop of productie. De tegenrekening voor deze rekening is de rekening Voorraadontvangst. |
| Inter-unit te betalen | 231500 | Inter-unit crediteuren | Aansprakelijkheid | Debet | Nr. | Beide | | Deze rekening wordt gebruikt wanneer de voorraad wordt overgeboekt tussen voorraaddimensies zoals locaties, en de kosten van een artikel per site verschillen. |
| Inter-unit te ontvangen | 131500 | Inter-unit debiteuren | Activum | Credit | Nr. | Beide | | Deze rekening wordt gebruikt wanneer de voorraad wordt overgeboekt tussen voorraaddimensies zoals locaties, en de kosten van een artikel per site verschillen. |
