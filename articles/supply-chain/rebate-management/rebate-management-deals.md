---
title: Deals voor kortingbeheer
description: In dit onderwerp wordt beschreven hoe u deals voor kortingbeheer maakt. Met deals worden verschillende methoden en basissen voor het berekenen van kortingen en royalty's bestuurd. Zij bevatten regels voor opname en uitsluiting.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TAMRebateDeal
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: 7ba42df021eddccbae389321b38828c7a92e50c8
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020502"
---
# <a name="rebate-management-deals"></a>Deals voor kortingbeheer

[!include [banner](../includes/banner.md)]

Deals voor kortingbeheer worden gebruikt om verschillende methoden en basissen voor het berekenen van kortingen en royalty's te besturen. Zij bevatten regels voor opname en uitsluiting. Er zijn drie typen deals voor kortingsbeheer: klantkortingen, klantroyalty's en leverancierskortingen. Alle drie de typen hebben soortgelijke instellingen. In dit onderwerp wordt aangegeven waar de verschillen liggen.

## <a name="create-a-deal"></a>Een deal maken

1. Ga naar **Kortingsbeheer \> Deals voor kortingbeheer \> Alle deals voor kortingsbeheer**. Op de lijstpagina **Alle eals voor kortingsbeheer** kunt u van alle drie de typen deals maken en gebruiken.

    U kunt ook een van deze stappen uitvoeren. In alle gevallen bevat de lijstpagina die wordt weergegeven dezelfde instellingen als de lijstpagina **Alle deals voor kortingsbeheer**, maar deze is gefilterd om deals van slechts één type weer te geven.

    - Ga naar **Kortingsbeheer \> Deals voor kortingsbeheer \> Deals voor klantkortingen** om alleen deals voor klantkorting te maken.
    - Ga naar **Kortingsbeheer \> Deals voor kortingsbeheer \> Deals voor klantroyalty** om alleen deals voor klantroyalty te maken.
    - Ga naar **Kortingsbeheer \> Deals voor kortingsbeheer \> Deals voor leverancierskortingen** om alleen deals voor leverancierskorting te maken.

1. Selecteer **Nieuw** in het actievenster.
1. Stel in het dialoogvenster **Nieuwe deal maken** de volgende velden in:

    - **Deal voor kortingsbeheer**: als u een [nummerreeks hebt ingesteld](rebate-management-parameters.md) voor kortingsdeals, wordt dit veld automatisch ingesteld op een unieke, door het systeem gegenereerde id. Voer anders een unieke id in.
    - **Beschrijving**: voer een beschrijving van de deal in.
    - **Module**: selecteer het type partner waarop de deal van toepassing is (*Klant* of *Leverancier*). Afhankelijk van de pagina waar u bent begonnen, wordt dit veld mogelijk automatisch ingesteld op basis van het geselecteerde type deal. In dat geval is het veld alleen-lezen.
    - **Type**: selecteer het type deal (*Korting* of *Royalty*). Afhankelijk van de pagina waar u bent begonnen, wordt dit veld mogelijk automatisch ingesteld op basis van het geselecteerde type deal. In dat geval is het veld alleen-lezen.
    - **Afstemmen met**: selecteer hoe de deal moet worden berekend en afgestemd:

        - *Deal*: er moet een enkele korting worden verwerkt voor alle kortingen en inhoudingen in de deal.
        - *Regel*: kortingen moeten worden verwerkt voor elke regel in een deal.

    - **Boekingsprofiel**: selecteer het [boekingsprofiel](rebate-management-posting.md) dat moet worden gebruikt voor transacties waarop de deal van toepassing is. Dit veld is alleen beschikbaar wanneer het veld **Afstemmen met** is ingesteld op *Deal*. Als het is ingesteld op *Regel*, wijst u het profiel later toe voor elke regel die u aan de deal toevoegt.
    - **Boekingsprofiel voor garantie**: selecteer het [boekingsprofiel](rebate-management-posting.md) dat moet worden gebruikt voor garantietransacties. Boekingsprofielen zijn alleen vereist voor garantietransacties als de garantie van toepassing is op een royalty. Anders wordt, hoewel een boekingsprofiel niet verplicht is, een fout weergegeven wanneer garanties worden geboekt als er geen boekingsprofiel is opgegeven. Dit veld is alleen beschikbaar wanneer het veld **Type** is ingesteld op *Royalty*. 
    - **Kortingsuitvoer**: selecteer hoe de korting of royalty moet worden betaald:

        - *Financieel*: genereer een vrije-tekstcreditnota of debetnota voor leveranciers, zodat bedragen later kunnen worden betaald of ontvangen. Houd er rekening mee dat het **wel** mogelijk is voorzieningen te gebruiken voor kortingen waarbij deze optie is geselecteerd. Dit is de enige beschikbare optie wanneer het veld **Type** is ingesteld op *Royalty*.
        - *Artikel*: genereer een verkooporder voor artikelen volgens de instellingen van de deal. Op deze verkooporder wordt een prijs van 0 (nul) toegewezen aan elk artikel. Houd er rekening mee dat het **niet** mogelijk is voorzieningen te gebruiken voor kortingen waarbij deze optie is geselecteerd.

    - **Kortingsvaluta**: selecteer de valuta die moet worden gebruikt wanneer de korting, inhouding of royalty wordt betaald.
    - **Documentnotities**: voer indien nodig notities in over de deal.
    - **Cumulatieve garantie**: u kunt deze optie alleen instellen op *Ja* als het veld **Type** is ingesteld op *Royalty*. Deze optie is van invloed op de berekening van betalingen met gegarandeerde inhoudingen. Dit is een voorbeeld:

        - De garantie van de deal is de verkoop van een waarde die leidt tot een betaling van $ 10.000 per kwartaal.
        - De organisatie die de goederen verkoopt, verkoopt een waarde die leidt tot een inhoudingsbetaling $ 12.000 in kwartaal 1. Het resultaat is een royalty van $ 12000 die wordt betaald, met aftrek van de garantie van $ 10.000.
        - Als de optie **Cumulatieve garantie** is ingesteld op *Ja*, zijn de extra $ 2000 aan royalty's die in kwartaal 1 zijn betaald, van toepassing op kwartaal 2. Daarom ontvangt de klant gegarandeerd $ 8000 (de garantie van $ 10.000 min de extra betaling van $ 2000).
        - In kwartaal 2 registreert u verkopen die in een royalty van $ 5000 resulteren.
        - Het systeem geeft een betaling van $ 3000 aan (de garantie van $ 8000 min de $ 5000 aan betaalde royalty's).
        - Als de optie **Cumulatieve garantie** is ingesteld op *Nee*, wordt elk kwartaal de volledige $ 10.000 gegarandeerd. Deze garantie komt overeen met de voorgestelde betaling van $ 5000 betaling in kwartaal 2 (de garantie van $ 10.000 min de betaalde royalty's van $ 5000).

1. Selecteer **OK** om de deal te maken en het dialoogvenster te sluiten.

Met deze procedure maakt u het koptekstniveau van de nieuwe deal. Vervolgens voegt u regels toe aan de deal.

## <a name="add-lines-to-a-deal"></a>Regels toevoegen aan een deal

Nadat u een deal hebt gemaakt zoals beschreven in de vorige sectie, kunt u deze openen vanuit de lijstpagina. U kunt vervolgens regels toevoegen om de klanten of leveranciers, artikelen, tijdsbestekken, een basis en berekeningsmethoden voor de deal aan te geven. Een deal kan één of meerdere regels hebben. Als een deal meerdere regels heeft, zijn deze over het algemeen van hetzelfde type of zijn aan deze regels dezelfde parameters gekoppeld. Totdat u regels aan een deal toevoegt, doet de deal niets.

1. Open de juiste lijstpagina voor kortingsdeals, zoals beschreven in de vorige sectie.
1. Zoek en open de deal waarmee u wilt werken.
1. Selecteer op het sneltabblad **Kortingsbeheer** een van de volgende knoppen om een dealregel aan het raster toe te voegen:

    - **Regel toevoegen**: voeg een nieuwe lege dealregel toe.
    - **Regel kopiëren**: als een bestaande dealregel lijkt op de dealregel die u wilt toevoegen, kunt u deze knop selecteren om een kopie van de regel toe te voegen. De nieuwe dealregel bevat alle instellingen van de gerelateerde details voor kortingsbeheer. Vervolgens kunt u de instellingen bewerken. U kunt bijvoorbeeld doorgaans de artikelrelatie en het kortingspercentage bijwerken.

1. Stel de volgende velden in op de nieuwe dealregel:

    - **Kortingsbeheernummer**: als u een [nummerreeks hebt ingesteld](rebate-management-parameters.md) voor kortingbeheernummers, wordt dit veld automatisch ingesteld op een unieke, door het systeem gegenereerde id. Voer anders een unieke id in.
    - **Type**: het type deal waarop de regel van toepassing is (*Korting* of *Royalty*). De waarde wordt uit de koptekst gekopieerd en kan niet worden gewijzigd.
    - **Beschrijving**: voer een beschrijving van de dealregel in.
    - **Bedrijf**: selecteer het bedrijf (rechtspersoon) waarop de dealregel van toepassing is. Tijdens de verwerking kunnen gebruikers alleen dealregels verwerken die zijn toegewezen aan het bedrijf dat ze momenteel gebruiken. De lijstpagina **Deals voor klantkortingen** biedt een weergave voor meerdere bedrijven op basis van de beveiligingstoegang van de gebruiker. U kunt kortingen echter alleen bewerken en verwerken voor het bedrijf dat u momenteel gebruikt.
    - **Rekeningcode**: selecteer het bereik van klanten of leveranciers waarop de dealregel van toepassing is:

        - *Tabel*: de dealregel is van toepassing op een specifieke klant of leverancier.
        - *Groep*: de dealregel is van toepassing op een groep klanten of leveranciers. Zie [Groepen voor kortingsbeheer](rebate-management-groups.md) voor meer informatie over het instellen van groepen.
        - *Alle*: de dealregel is van toepassing op alle klanten of leveranciers.

    - **Rekeningrelatie** Als u *Tabel* hebt geselecteerd in het veld **Rekeningcode**, selecteert u de klant of leverancier waarop de deal betrekking heeft. Als u *Groep* hebt geselecteerd, selecteert u de klanten- of leveranciersgroep. Als u *Alle* hebt geselecteerd, is dit veld niet beschikbaar.
    - **Artikelcode**: selecteer het bereik van artikelen waarop de dealregel van toepassing is:

        - *Tabel*: de dealregel is van toepassing op een specifiek artikel.
        - *Groep*: de dealregel is van toepassing op een groep artikelen. Zie [Groepen voor kortingsbeheer](rebate-management-groups.md) voor meer informatie over het instellen van groepen.
        - *Alle*: de dealregel is van toepassing op alle artikelen.

    - **Artikelrelatie** Als u *Tabel* hebt geselecteerd in het veld **Artikelcode**, selecteert u het artikel waarop de dealregel betrekking heeft. Als u *Groep* hebt geselecteerd, selecteert u de artikelgroep. Als u *Alle* hebt geselecteerd, is dit veld niet beschikbaar.
    - **(Parameters voor voorraadbeheer)**: geef in de resterende velden op de dealregel waarden op voor de voorraadbeheerparameters die worden gebruikt om de artikelen te definiëren die in de deal worden opgenomen (zoals artikelgrootte, kleur, stijl, locatie en magazijn). Als u dimensies wilt toevoegen of verwijderen, selecteert u **Dimensies weergeven** in het actievenster.

1. Selecteer **Opslaan** in het actievenster.
1. Als u de set artikelen waarop een kortingsregel van toepassing is verder wilt beperken, selecteert u de regel en selecteert u vervolgens op het sneltabblad **Kortingsbeheer** de optie **Filteren** om een standaard dialoogvenster **Query** te openen.
1. Stel voor elke dealregel die u toevoegt de berekeningsdetails en andere details in op het sneltabblad **Details kortingsbeheer**, zoals wordt beschreven in de volgende sectie.

## <a name="add-rebate-management-details-to-a-deal-line"></a>Details van kortingsbeheer toevoegen aan een dealregel

Voor elke regel in uw deal moet u details instellen op het sneltabblad **Details kortingsbeheer**. Selecteer eerst de dealregel op het sneltabblad **Kortingsbeheer**. Stel vervolgens waarden in voor die dealregel met behulp van de verschillende tabbladen op het sneltabblad **Details kortingsbeheer**. In de volgende subsecties wordt beschreven hoe u elk tabblad gebruikt.

### <a name="settings-on-the-general-tab"></a>Instellingen op het tabblad Algemeen

Op het tabblad **Algemeen** van het sneltabblad **Details kortingsbeheer** kunt u de berekeningsmethode en basis voor de geselecteerde dealregel instellen. Deze instellingen bepalen of een minimum aankoop nodig is, de boekingsprofielen die aan de dealregel zijn gekoppeld en de details van de berekening. In de volgende tabel worden de velden beschreven die beschikbaar zijn.

| Veld | Beschrijving |
|---|---|
| Berekeningsmethode | Selecteer de methode die moet worden gebruikt wanneer de geselecteerde dealregel wordt gecombineerd met andere dealregels (*Getrapt*, *Cumulatief*, *Opvolgend* of *Totaal*). De waarde van dit veld kan de resultaten van uw kortingsberekeningen aanzienlijk beïnvloeden. Zie de sectie [Berekeningsmethoden voor dealregels](#calc-methods) verderop in dit onderwerp voor een volledige beschrijving van elke methode en voorbeelden die laten zien hoe dit van invloed is op de kortingsberekening. |
| Basis | Selecteer of de korting wordt toegepast op basis van de hoeveelheid (het totale aantal eenheden dat wordt gekocht of verkocht) of de waarde (de totale prijs van gekochte of verkochte goederen). |
| Transactietype | <p>Selecteer het punt in het proces waarop de berekening moet worden uitgevoerd:</p><ul><li>*Order*: gebruik de bestelde hoeveelheid of waarde als basis voor de berekening.</li><li>*Geleverd*: gebruik de geleverde hoeveelheid of waarde als basis voor de berekening.</li><li>*Factuur*: gebruik de gefactureerde hoeveelheid of waarde als basis voor de berekening.</li></ul> |
| Eenheid | Als u *Hoeveelheid* hebt geselecteerd in het veld **Basis**, selecteert u de eenheid waarin de hoeveelheid moet worden opgegeven. |
| Minimumbedrag | Voer het minimumbedrag in dat per periode moet worden betaald. U kunt een negatieve waarde invoeren om negatieve kortingsbedragen toe te staan als creditnota's de verkoop voor de periode overschrijden. |
| Kortingsreductieprincipe | Selecteer het [kortingsreductieprincipe](rebate-reduction-principle.md) dat geldt voor de dealregel. |
| Variantnummer | Als de dealregel van toepassing is op een artikel dat varianten heeft, selecteert u de variant waarop de dealregel van toepassing is. |
| Basis voor leverancierskortingen | <p>Dit veld wordt alleen weergegeven voor leverancierskortingen (oftewel deals waarbij het veld **Module** is ingesteld op *Leverancier*). Selecteer de basis voor de leverancierskorting:</p><ul><li>*Inkooporder*: de korting die de leverancier ontvangt, is gebaseerd op de hoeveelheid of waarde op de inkooporder.</li><li>*Verkooporder*: de leverancier ontvangt pas een korting nadat de goederen zijn verkocht. De korting wordt gebaseerd op de hoeveelheid of waarde op de verkooporder.</li></ul> |
| Prijsbasis | <p>Dit veld wordt alleen weergegeven voor leverancierskortingen (deals waarbij het veld **Module** is ingesteld op *Leverancier*). Als u *Verkooporder* hebt geselecteerd in het veld **Basis voor leverancierskortingen**, selecteert u de prijsbasis die van toepassing is:</p><ul><li><p>*FIFO*: de periodieke taak **FIFO-inkoopprijs berekenen** moet worden uitgevoerd om de korting te berekenen. (Als u de taak wilt uitvoeren, gaat u naar **Kortingsbeheer \> Periodieke taken \> FIFO-inkoopprijs berekenen**.) Een FIFO-regel (First In, First Out) wordt gebruikt om de waarde te berekenen van de voorraad die wordt verkocht. Deze waarde wordt vervolgens gebruikt om de leverancierskortingen te berekenen. Dit is een voorbeeld:</p><ul><li>**Verkochte voorraad:** 1000 eenheden van $ 3,00 per stuk = $ 3000</li><li>**Huidige inkoopprijs, gebaseerd op FIFO**: $ 2,00</li><li>**Werkberekening**: *verkochte eenheden* × *Huidige inkoopprijs* = 1000 × $ 2,00 = $ 2000</li></ul></li><li><p>*Laatste inkoopprijs*: de waarde van de laatste inkooptransactie wordt gebruikt om de leverancierskortingen te berekenen. Dit is een voorbeeld:</p><ul><li>**Verkochte voorraad:** 1000 eenheden van $ 3,00 per stuk = $ 3000</li><li>**Laatste inkoopprijs:** $ 2,00</li><li>**Werkberekening**: *verkochte eenheden* × *Laatste inkoopprijs* = 1000 × $ 2,00 = $ 2000</li></ul></li><li><p>*Gemiddelde inkoopprijs*: de waarde gewogen gemiddelde voor de laatste *X* maanden wordt gebruikt om de leverancierskortingen te berekenen. Als u deze optie selecteert, moet u het aantal maanden invoeren in het veld **Aantal maanden** (dat alleen beschikbaar is als het veld **Prijsbasis** is ingesteld op *Gemiddelde inkoopprijs*). Dit is een voorbeeld:</p><ul><li>**Verkochte voorraad:** 1000 eenheden van $ 3,00 per stuk = $ 3000</li><li>**Gemiddelde inkoopprijs**: $ 2,00</li><li>**Werkberekening**: *verkochte eenheden* × *Gemiddelde inkoopprijs* = 1000 × $ 2,00 = $ 2000</li></ul></li><li><p>*Verkoopprijs*: de verkoopprijs wordt gebruikt om de leverancierskortingen te berekenen. Dit is een voorbeeld:</p><ul><li>**Verkochte voorraad:** 1000 eenheden van $ 3,00 per stuk = $ 3000</li><li>**Gemiddelde inkoopprijs**: $ 2,00</li><li>**Werkberekening**: *verkochte eenheden* × *Verkoopprijs* = 1000 × $ 3,00 = $ 3000</li></ul></li></ul> |
| Aantal maanden | Dit veld wordt alleen weergegeven voor leverancierskortingen (deals waarbij het veld **Module** is ingesteld op *Leverancier*). Als u in het veld *Prijsbasis* de optie **Gemiddelde inkoopprijs** hebt geselecteerd, voert u het aantal maanden in dat moet worden gebruikt. |
| Boekingsprofiel | Selecteer het [boekingsprofiel](rebate-management-posting.md) dat geldt voor de geselecteerde dealregel. Dit profiel wordt alleen gebruikt wanneer het veld **Afstemmen met** in de koptekst van de deal is ingesteld op *Regel*. Als het veld **Afstemmen met** is ingesteld op *Deal*, wordt altijd gebruikgemaakt van het boekingsprofiel dat is ingesteld op de koptekst van de deal. Als geen boekingsprofiel is ingesteld voor de dealregel;, wordt gebruikgemaakt van het boekingsprofiel dat is ingesteld op de koptekst van de deal. |
| Boekingsprofiel voor garantie | Dit veld werkt net als het veld **Boekingsprofiel**, maar is alleen van toepassing op royalty's. |
| Type betaling | Het betalingstype voor het boekingsprofiel dat voor de deal is geselecteerd. |
| Btw inbegrepen | Selecteren of de transactie inclusief btw is. Of btw is inbegrepen is alleen relevant als het veld **Basis** is ingesteld op *Waarde*. Het factuurbedrag wordt gebruikt als het bedrag inclusief btw. Als de kortingsberekening wordt gebaseerd op een percentage, wordt het kortingspercentage in het systeem vermenigvuldigd met het bedrag inclusief btw. Bij de berekening wordt de btw-waarde van de dealregel gebruikt. |
| Creditnota's opnemen | <p>Stel deze optie in op *Ja* om creditnota's op te nemen in de kortingsberekening.</p><p>Als u deze optie instelt op *Ja*, varieert het effect, afhankelijk van de waarde van het veld **Transactietype**:</p><ul><li>Als het veld **Transactietype** is ingesteld op *Factuur*, wordt bij de berekening rekening gehouden met creditnota's. Dit is de gebruikelijke configuratie.</li><li>Als het veld **Transactietype** is ingesteld op *Order*, wordt bij de berekening rekening houden met zowel verkooporders met negatieve waarden als openstaande geretourneerde orders.</li></ul> |
| Kortingsbedrag | Stel deze optie in op *Ja* als u de berekening wilt baseren op het gereduceerde bedrag van het artikel of de artikelen wanneer dealregelkortingen worden gegeven. |
| Alleen betaalde facturen | Stel deze optie in op *Ja* als bij de berekening alleen rekening moet worden gehouden met volledig betaalde facturen. (Dit wil zeggen dat kortingen niet worden berekend voor gedeeltelijk betaalde facturen.) Deze optie is alleen beschikbaar als het veld **Transactietype** is ingesteld op *Factuur*. |
| Vrije tekst opnemen | Stel deze optie in op *Ja* om vrije-tekstgfacturen op te nemen in de berekening. Vrije-tekstfacturen kunnen alleen worden opgenomen voor dealregels waarbij het veld **Artikelcode** is ingesteld op *Alle*. |
| Vereffeningskorting opnemen | Stel deze optie in op *Ja* om de korting te verminderen met de eerste vereffeningskorting. Er wordt aangenomen dat de organisatie de eerste vereffeningskorting neemt. Stel deze optie in op *Nee* om de vereffeningskorting later te gebruiken. |
| Documentnotities | Voer notities in die moeten worden gebruikt als transactietekst op journaalregels voor kortingstransacties. |

### <a name="settings-on-the-dates-tab"></a>Instellingen op het tabblad Datums

Met de instellingen op het tabblad **Datums** op het sneltabblad **Details kortingsbeheer** definieert u de frequentie en timing van de berekeningen die zijn opgegeven op het tabblad **Algemeen**. Deze bepalen hoe berekeningen plaatsvinden tijdens de verwerkingstijd.

Op dit tabblad kunt u opgeven voor welk datumbereik de geselecteerde dealregel geldt en welke berekeningsfrequentie wordtg gehanteerd. U kunt ook opgeven of de garantie moet worden geboekt en wanneer.

Gebruik de knoppen op de werkbalk om datumregels aan het raster toe te voegen of uit het raster te verwijderen. Als er meerdere datumregels zijn, mogen de geldige datumbereiken elkaar niet overlappen. Als dit wel het geval is, wordt er een foutbericht weergegeven wanneer u de deal probeert op te slaan.

In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke datumregel.

| Veld | Beschrijving |
|---|---|
| Begindatum | Voer de eerste datum in waarop de datumregel van toepassing is. Als datums 'van' en 'tot' worden opgegeven in de koptekst van de deal, worden deze gebruikt als standaardwaarden voor elke nieuwe datumregel. |
| Einddatum | Voer de laatste datum in waarop de datumregel van toepassing is. Als datums 'van' en 'tot' worden opgegeven in de koptekst van de deal, worden deze gebruikt als standaardwaarden voor elke nieuwe datumregel. |
| Per | Geef op hoe vaak de dealregel moet worden berekend. Geef hier een geheel getal op en selecteer vervolgens een eenheid in het veld **Cumuleren per**. Stel, als u de berekening om de week wilt uitvoeren, bijvoorbeeld het veld **Per** in op *2* en het veld **Cumuleren per** op *Weken*. |
| Cumuleren per | Selecteer de eenheid die van toepassing is op de instelling **Per**. Selecteer *Levensduur* om de berekening uit te voeren op de volledige levensduur van de dealregel. Selecteer *Aangepaste periode* om een periode te selecteren die in het grootboek is gedefinieerd. In dit geval moet u ook het veld **Periodetype** instellen. |
| Periodetype | Dit veld is alleen beschikbaar wanneer het veld **Cumuleren per** is ingesteld op *Aangepaste periode*. De waarden die kunnen worden geselecteerd, zijn afkomstig uit de periodetypen die in het grootboek zijn gedefinieerd. |
| Eerste dag van de week | Geef op hoe de weken worden geïdentificeerd voor de periode. Dit veld is alleen beschikbaar wanneer het veld **Cumuleren per** is ingesteld op *Weken*. |
| Vorderen per | Geef op hoe vaak kortingsbedragen voor de dealregel kunnen worden gevorderd. Geef hier een geheel getal op en selecteer vervolgens een eenheid in het veld **Vorderen per**. |
| Vorderen door | Selecteer de eenheid die van toepassing is op de instelling **Vorderen door**. Selecteer *Levensduur* om vorderingen slechts één keer toe te staan tijdens de hele levensduur van de dealregel. Selecteer *Aangepaste periode* om een periode te selecteren die in het grootboek is gedefinieerd. In dit geval moet u ook het veld **Type vorderingsperiode** instellen. |
| Type vorderingsperiode | Dit veld is alleen beschikbaar wanneer het veld **Vorderen per** is ingesteld op *Aangepaste periode*. De waarden die kunnen worden geselecteerd, zijn afkomstig uit de periodetypen die in het grootboek zijn gedefinieerd. |
| Verwerken bij boeking | Schakel dit selectievakje in als de vorderingsregel tijdens het boeken moet worden verwerkt. Deze optie is alleen beschikbaar voor transactieregels waarbij het veld **Transactietype** op het tabblad **Algemeen** is ingesteld op *Geleverd* of *Factuur*. Bij voorzieningen wordt de voorziening geboekt wanneer de leveringsnota of factuur wordt gegenereerd. |
| Garantie per | Dit veld is alleen van toepassing op royaltydeals. Geef op hoe vaak de garantie van de royalty's moet worden berekend tijdens de periode die wordt gedefinieerd door de instelling **Cumuleren per**. Geef hier een geheel getal op en selecteer vervolgens een betalingstijd in het veld **Garantie betaald**. |
| Garantie betaald | <p>Dit veld is alleen van toepassing op royaltydeals. De frequentie van de garantieberekening wordt hierbij gedefinieerd in combinatie met het veld **Garantie per**. Selecteer een van de volgende waarden:</p><ul><li><p>*Begin van periode*: de garantie wordt betaald aan het begin van de overeenkomstperiode die is gedefinieerd voor de datumregel. De volledige garantie wordt eerst verwerkt. Alleen de waarde van royalty's die hoger zijn dan het gegarandeerde bedrag wordt als royalty geboekt. Dit is een voorbeeld:</p><ul><li>**Minimum garantie**: $ 10.000 gedurende twee maanden.</li><li>**Maand 1**: $ 10.000 zijn geboekt als garantie en $ 0 als royalty's.</li><li>**Maand 2**: $ 2000 zijn geboekt als royalty's en $ 0 als garanties.</li><li>**Werkberekening**: *Resterende garantie* – *Royalty's geboekt* = $0 – $ 2000 = -$ 2000.</li></ul><p>Omdat een royaltybetaling van $ 2000 is vereist, wordt een journaal gemaakt voor $ 2000.</p><p>**Opmerking**: de garantie moet worden berekend en geboekt samen met de inhoudingsvoorziening voor de eerste periode.</p></li><li><p>*Einde periode*: de garantie wordt pas betaald aan het einde van de inhoudingsovereenkomst, zoals gedefinieerd op de datumregel. Dit is een voorbeeld:</p><ul><li>**Minimum garantie**: $ 10.000 gedurende twee maanden.</li><li>**Maand 1**: $ 5000 zijn geboekt als royalty's en er is een journaal gemaakt.</li><li>**Maand 2**: $ 7000 zijn geboekt als royalty's en er is een journaal gemaakt.</li><li>**Werkberekening**: omdat de royalty's hoger zijn dan het garantiebedrag, wordt $ 0 geboekt naar de garantie.</li></ul><p>**Opmerking**: de garantie moet alleen samen met de inhoudings- en kortingstransactie worden berekend en geboekt voor de laatste periode.</p></li></ul> |
| Garantie minimum | Dit veld is alleen van toepassing op royaltydeals. Voer het minimumbedrag van de garantie voor een royalty in. Gebruik hiervoor de valuta die in de koptekst van de overeenkomst is gedefinieerd. |

### <a name="settings-on-the-lines-tab"></a>Instellingen op het tabblad Regels

Op het tabblad **Regels** van het sneltabblad **Details kortingsbeheer** kunt u de berekeningsregels voor de geselecteerde dealregel definiëren. Elke berekeningsregel legt een hoeveelheids- of waardedrempel vast en een gerelateerd compensatiebedrag of gerelateerde artikelen. In het veld **Basis** op het tabblad **Algemeen** wordt aangegeven of elke berekeningsregel is gebaseerd op een hoeveelheid of een waarde.

Gebruik de knoppen op de werkbalk om berekeningsregels aan het raster toe te voegen of uit het raster te verwijderen. U kunt elk gewenst aantal berekeningsregels hebben. Als er echter meerdere berekeningregels zijn, mogen de hoeveelheids- of waardebereiken 'tot' en 'van' elkaar niet overlappen.

In de volgende tabel worden de velden beschreven die beschikbaar zijn voor elke berekeningsregel.

| Veld | Beschrijving |
|---|---|
| Van hoev./waarde | Voer de minimumhoeveelheid of -waarde in waarvoor de berekeningsregel geldt. |
| Tot hoev./waarde | Voer de maximumhoeveelheid of -waarde in waarvoor de berekeningsregel geldt. |
| Methode voor kortingbeheer | <p>Dit veld is alleen beschikbaar voor deals waarbij het veld **Kortingsuitvoer** in de koptekst is ingesteld op *Financieel*. Selecteer de berekeningsmethode voor de korting:</p><ul><li>*Vast*: er wordt een vaste prijs voor de regel gebruikt.</li><li>*Percentage*: er wordt een percentage van het verkoopbedrag gebruikt.</li><li>*Tarief*: er wordt een vast prijsbedrag per order gebruikt.</li></ul><p>**Belangrijk**: het wordt dringend aangeraden dezelfde methode te gebruiken voor elke berekeningsregel op het tabblad **Regels**. Maak een nieuwe dealregel als een nieuwe methode is vereist. U kunt de knop **Regel kopiëren** op het sneltabblad **Kortingsbeheer** gebruiken om een nieuwe dealregel te maken op basis van een bestaande dealregel.</p><p>**Opmerking**: als het veld **Kortingsuitvoer** is ingesteld op *Artikel*, is dit veld altijd ingesteld op *Vast*. Zie de tekst die op deze tabel volgt voor meer informatie over het opgeven van de artikelen. |
| Bedrag voor kortingbeheer | Dit veld is alleen beschikbaar voor deals waarbij het veld **Kortingsuitvoer** in de koptekst is ingesteld op *Financieel*. Voer het bedrag in dat moet worden gebruikt om de korting te berekenen op basis van de methode die u hebt geselecteerd in het veld **Methode voor kortingbeheer**. |

Zoals is vermeld in de vorige tabel, moet u voor transacties waarbij het veld **Kortingsuitvoer** in de koptekst is ingesteld op *Artikel*, de artikelen opgeven die worden opgegeven voor elke berekeningsregel op het tabblad **Regels**. Volg deze stappen om de artikelen op te geven.

1. Maak op het tabblad **Regels** de vereiste berekeningsregel als deze niet bestaat, en selecteer deze.
1. Als de deal niet is opgeslagen nadat u de berekeningsregel hebt gemaakt, selecteert u **Opslaan** in het actievenster.
1. Selecteer op het tabblad **Regels** de optie **Artikelen**.
1. Gebruik op de pagina **Artikelen** de knoppen in het actievenster om artikelen aan het raster toe te voegen of om artikelen waar nodig te verwijderen. Stel voor elke rij de volgende velden in:

    - **Artikelnummer**: selecteer het artikel dat wordt geleverd.
    - **(Overige dimensies)**: als u meer dimensies moet gebruiken om het artikel te definiëren (bijvoorbeeld artikelconfiguratie, grootte, kleur, stijl, locatie of magazijn), geeft u deze op. Als u beschikbare dimensies wilt toevoegen of verwijderen, selecteert u **Dimensies weergeven** in het actievenster.
    - **hoeveelheid**: voer de hoeveelheid in die wordt verstrekt nadat de drempel voor de geselecteerde berekeningsregel is voldaan.
    - **Eenheid**: selecteer de eenheid waarin de waarde **Hoeveelheid** is opgegeven.
    - **Meerdere**: dit veld werkt in combinatie methet veld **Hoeveelheid**. Stel bijvoorbeeld voor een artikelregel het veld **Hoeveelheid** in op *2* en het veld **Meerdere** op *100*. Als u vervolgens een totale verkooporderhoeveelheid van 150 hebt, zijn twee van de artikelen gratis (twee per 100).

### <a name="settings-on-the-inventory-dimensions-tab"></a>Instellingen op het tabblad Voorraaddimensies

Op het tabblad **Voorraaddimensies** op het sneltabblad **Details kortingsbeheer** worden alle beschikbare dimensiewaarden weergegeven voor het product dat is opgegeven voor de geselecteerde dealregel. De lijst bevat dimensies die niet worden weergegeven op het sneltabblad **Kortingsbeheer**. U kunt alleen waarden bewerken voor de dimensies die van toepassing zijn op het geselecteerde product.

U kunt meer dimensies toevoegen aan het raster op het sneltabblad **Kortingsbeheer** door **Dimensies weergeven** te selecteren in het actievenster.

## <a name="calculation-methods-for-deal-lines"></a><a name="calc-methods"></a>Berekeningsmethoden voor dealregels

Telkens wanneer u gegevens voor een van uw dealregels instelt, zoals in het vorige gedeelte wordt beschreven, moet u de berekeningsmethode voor die regel selecteren. In deze sectie wordt elke berekeningsmethode uitgelegd en worden voorbeelden gegeven die laten zien hoe met elke methode de totale korting voor orders en dealregels wordt berekend. In deze voorbeelden zijn de orders en dealregels identiek. Alleen de berekeningsmethoden verschillen.

### <a name="stepped-calculation-method"></a>Berekeningsmethode Getrapt

Bij de getrapte berekeningsmethode wordt stap voor stap berekend hoe elke dealregel incrementeel bijdraagt aan de korting totdat de verkoophoeveelheid of -waarde is bereikt. De stappen kunnen worden gebaseerd op de hoeveelheid of de waarde van de verkochte goederen, afhankelijk van de instelling van het veld **Basis** op het tabblad **Algemeen** van het sneltabblad **Details kortingsbeheer**.

Een dealregel wordt bijvoorbeeld zo ingesteld dat het veld **Berekeningsmethode** wordt ingesteld op *Getrapt* en het veld **Basis** op *Waarde*. Er worden berekeningregels opgenomen met de volgende kortingen:

- **Regel A**: 10 procent tot aan $ 1000
- **Regel B**: 25 procent tot aan $ 2500

Als de waarde van de gekochte of verkochte goederen $ 2000 bedraagt, wordt de resulterende korting van $ 350 als volgt berekend:

- **Korting (A)**: *Drempel (A)* × *Percentage (A)* = $ 1000 × 10 procent = $ 100
- **Korting (B)**: (*Waarde verkocht* – *Drempel (A)*) × *Percentage (B)* = ($ 2000 – $ 1000) × 25 procent = $ 250
- **Totale korting**: *Korting (A)* + *Korting (B)* = $ 100 + $ 250 = $ 350

Als het veld **Basis** is ingesteld op *Hoeveelheid* in plaats van *Waarde*, werkt de getrapte berekeningsmethode op dezelfde manier. De eerste stap wordt gebruikt voor de geïdentificeerde hoeveelheid tot de tweede stap wordt bereikt. De tweedestap wordt vervolgens gebruikt voor alle hoeveelheid boven de eerste stap, totdat de derde stap wordt bereikt. Dit proces doorloopt vervolgens alle volgende stappen.

### <a name="cumulative-calculation-method"></a>Berekeningsmethode Cumulatief

Voor de cumulatieve berekeningsmethode wordt slechts één berekeningsregel gebruikt om de korting te berekenen. Als meerdere berekeningregels beschikbaar zijn voor de dealregel, wordt de berekeningsregel met de hoogste waarde of hoogste hoeveelheid die wordt bereikt, gebruikt voor de gehele hoeveelheid of waarde. Net als bij de andere berekeningsmethoden wordt voor de cumulatieve methode de instelling van het veld **Basis** op het tabblad **Algemeen** van het sneltabblad **Kortingsbeheer** gebruikt om te bepalen of de verkoophoeveelheid of de verkoopwaarde wordt gebruikt om de kortingen te berekenen.

Een dealregel wordt bijvoorbeeld zo ingesteld dat het veld **Berekeningsmethode** wordt ingesteld op *Cumulatief* en het veld **Basis** op *Waarde*. Er worden berekeningregels opgenomen met de volgende kortingen:

- **Regel A**: 10 procent tot aan $ 1000
- **Regel B**: 25 procent tot aan $ 2500

Als de waarde van de gekochte of verkochte goederen $ 2000 bedraagt, gebruikt de berekening alleen regel B. De resulterende korting van $ 500 wordt als volgt berekend:

- **Totale korting**: *Waarde verkocht* × *Korting (B)* = $ 2000 × 25 procent = $ 500

### <a name="rolling-calculation-method"></a>Berekeningsmethode Opvolgend

Met de opvolgende berekeningsmethode worden alle mogelijke berekeningsregels voor de deal berekend. Als er meerdere berekeningregels zijn en er meer dan één wordt bereikt, worden alle berekeningregels gebruikt die worden bereikt, maar zijn de bovenste drempels van toepassing op elk percentage. Net als bij de andere berekeningsmethoden wordt voor de opvolgende methode de instelling van het veld **Basis** op het tabblad **Algemeen** van het sneltabblad **Kortingsbeheer** gebruikt om te bepalen of de verkoophoeveelheid of de verkoopwaarde wordt gebruikt om de kortingen te berekenen.

Een dealregel wordt bijvoorbeeld zo ingesteld dat het veld **Berekeningsmethode** wordt ingesteld op *Opvolgend* en het veld **Basis** op *Waarde*. Er worden berekeningregels opgenomen met de volgende kortingen:

- **Regel A**: 10 procent tot aan $ 1000
- **Regel B**: 25 procent tot aan $ 2500

Als de waarde van de gekochte of verkochte goederen $ 2000 bedraagt, wordt de resulterende korting van $ 600 als volgt berekend:

- **Korting (A)**: *Drempel (A)* × *Percentage (A)* = $ 1000 × 10 procent = $ 100
- **Korting (B)**: *Waarde verkocht* × *Percentage (B)* = $ 2000 × 25 procent = $ 500
- **Totale korting**: *Korting (A)* + *Korting (B)* = $ 100 + $ 500 = $ 600

### <a name="total-calculation-method"></a>Berekeningsmethode Totaal

Voor de berekeningsmethode totaal worden alle berekeningsregels gebruikt om de korting te berekenen. De totale hoeveelheid wordt toegepast om de korting te berekenen voor elke berekeningsregel die wordt bereikt, en elke berekeningsregel past het percentage van deze toe op het volledige bedrag. Net als bij de andere berekeningsmethoden wordt voor de totale methode de instelling van het veld **Basis** op het tabblad **Algemeen** van het sneltabblad **Kortingsbeheer** gebruikt om te bepalen of de verkoophoeveelheid of de verkoopwaarde wordt gebruikt om de kortingen te berekenen.

Een dealregel wordt bijvoorbeeld zo ingesteld dat het veld **Berekeningsmethode** wordt ingesteld op *Totaal* en het veld **Basis** op *Waarde*. Er worden berekeningregels opgenomen met de volgende kortingen:

- **Regel A**: 10 procent tot aan $ 1000
- **Regel B**: 25 procent tot aan $ 2500

Als de waarde van de gekochte of verkochte goederen $ 2000 bedraagt, wordt de resulterende korting van $ 700 als volgt berekend:

- **Korting (A)**: *Waarde verkocht* × *Percentage (A)* = $ 2000 × 10 procent = $ 200
- **Korting (B)**: *Waarde verkocht* × *Percentage (B)* = $ 2000 × 25 procent = $ 500
- **Totale korting**: *Korting (A)* + *Korting (B)* = $ 200 + $ 500 = $ 700
