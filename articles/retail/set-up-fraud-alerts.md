---
title: Fraudewaarschuwingen van callcenters instellen en gebruiken
description: Dit onderwerp wordt beschreven hoe u regels instelt om klantenservice medewerkers van potentieel frauduleuze informatie te waarschuwen wanneer bestellingen zijn verwerkt. U kunt speciale codes definiëren die automatisch of handmatig worden gebruikt om verdachte orders in de wachtstand te zetten.
author: josaw1
manager: AnnBe
ms.date: 05/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: SalesPostingHistory, MCRHoldCodeTrans
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 79103
ms.assetid: e342af8d-7498-4d20-8483-ab368429c578
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 13b6a18750e79a17c7f6034780922c64b12390e2
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "361493"
---
# <a name="set-up-and-work-with-call-center-fraud-alerts"></a>Fraudewaarschuwingen van callcenters instellen en gebruiken

[!include [banner](includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u criteria en regels instelt om mogelijk frauduleuze verkooporders in de wachtstand te plaatsen voor verder onderzoek. De fraudecontrolefunctie wordt gebruikt om de geldigheid van de gegevens in een verkooporder te bepalen. Als de informatie in de verkooporder dubieus lijkt op basis van de fraudecriteria en -regels van een organisatie, kan de order door een beheerder in de wachtstand worden geplaatst voor nader onderzoek. In dit geval kan de order niet worden vrijgegeven naar het magazijn voor verdere verwerking totdat de blokkering is gewist.

> [!NOTE]
> Deze functie kan alleen worden gebruikt met de functie voor verkooporderverwerking voor het detailhandelcallcenterkanaal.

## <a name="turning-on-the-fraud-check-feature"></a>De functie voor fraudecontrole inschakelen

Als u de fraudecontrolefunctie wilt gebruiken, moet u de optie **Ordervoltooiing inschakelen** in het kanaal op **Ja** instellen wanneer het callcenterkanaal wordt [gedefinieerd](https://docs.microsoft.com/dynamics365/unified-operations/retail/set-up-order-processing-options). Wanneer ordervoltooiing is ingeschakeld, moeten callcentergebruikers **Gereed** selecteren op de pagina van de verkooporder voor alle verkooporders die worden gemaakt. De actie Gereed opent de pagina **Overzicht van verkooporder**. Nadat gebruikers de vereiste betalingsgegevens op de pagina **Overzicht van verkooporder** hebben ingevoerd, selecteren ze **Indienen** om de order te voltooien. Wanneer de order wordt verzonden, wordt de fraudecontrolefunctie geactiveerd en worden regels die actief in het systeem zijn, automatisch gevalideerd.

Callcentergebruikers kunnen verkooporders ook handmatig in de wachtstand plaatsen voor fraudecontrole, voordat ze **Indienen** selecteren. Als u handmatig een verkooporder op de pagina **Overzicht van verkooporder** in de wachtstand wilt plaatsen, selecteert u **Blokkeren** \> **Handmatige fraudewachtstand**. Vervolgens wordt u gevraagd een opmerking in te voeren om uit te leggen waarom u de order in de wachtstand plaatst. Deze opmerking wordt weergegeven in de workbench [orderwachtstanden](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) om context te bieden aan de gebruiker die orders controleert die in de wachtstand staan om te bepalen of de order moet worden vrijgegeven.

Naast het configureren van de optie **Ordervoltooiing inschakelen** in het kanaal moet u de fraudecontrolefunctie configureren in de callcenterparameters. Ga naar **Detailhandel** \> **Afzetkanaalinstellingen** \> **Instellingen van callcenter** \> **Parameters van callcenter**. Stel op de pagina **Parameters van callcenter** op het tabblad **Blokkeringen** de optie **Fraudecontrole** in op **Ja**.

Op het tabblad **Blokkeringen** moet u ook de [wachtstandcodes](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds) definiëren die worden toegepast op een order die handmatig of automatisch in de wachtstand wordt geplaatst voor fraudecontrole. Stel de wachtstandcodes in de velden **Handmatige wachtstandcode voor fraude** en **Wachtstandcode voor fraude** in. Mogelijk vindt u het nuttig twee unieke wachtstandcodes te maken, zodat gebruikers die in de workbench Blokkeringen werken eenvoudig kunnen filteren en onderscheid kunnen maken tussen automatische en handmatige wachtstanden.

Wil de fraudecontrolefunctie goed werken, dan moet u ook het veld **Minimale score** instellen. Elk fraudecriterium en elke regel die zijn gedefinieerd in het systeem heeft een score. Wanneer een verkooporder wordt gecontroleerd op fraudeovereenkomsten en er een of meer overeenkomsten worden gevonden, worden de scores opgeteld om de order een totale fraudescore te geven. Als de totale fraudescore voor een order hoger is dan de waarde van het veld **Minimale score**, wordt de order automatisch in de wachtstand geplaatst. U kunt desgewenst de overige scoregerelateerde velden op het tabblad **Blokkeringen** gebruiken om de e-mailscore, postcodescore en uitgebreide postcodescore te definiëren. Als u voor een van deze statische fraudecriteria geen score opgeeft wanneer u ze definieert op de pagina **Statische fraudegegevens**, geeft het systeem ze een score met behulp van de standaardscores die u opgeeft op het tabblad **Blokkeringen** van de pagina **parameters van callcenter**.

Gebruik tot slot het veld **Type fraudeopmerking** om het documenttype op te geven dat moet worden gebruikt wanneer gebruikers opmerkingen invoeren wanneer ze een order handmatig in de wachtstand plaatsen voor fraudecontrole. Meestal wordt dit veld ingesteld op **Opmerking**.

## <a name="defining-fraud-criteria-and-rules"></a>Fraudecriteria en regels definiëren

Het systeem verwijst naar twee soorten fraudecriteria om te controleren of een order in de wachtstand moet worden geplaatst voor fraudebeoordeling:

- **Statische fraudegegevens** gebruikt een specifieke waarde, zoals een telefoonnummer dat in een lijst met geblokkeerde nummers is geplaatst of een e-mailadres dat is gemarkeerd omdat bekend is dat het eerder is gebruikt voor frauduleuze transacties. Als u statische fraudegegevens wilt instellen, gaat u naar **Detailhandel** \> **Afzetkanaalinstellingen** \> **Instellingen van callcenter** \> **Fraude** \> **Statische fraudegegevens**. Op de pagina **Statische fraudegegevens** kunt u fraudecriteria handmatig of via gegevensimport toevoegen. Scores worden gekoppeld aan de frauduleuze informatie. Als de fraudecontrolefunctie is ingeschakeld, wordt elke verkooporder die wordt ingevoerd, vergeleken met de statische gegevens. Als de gegevens worden gevonden in het factureringsadres van de klant of het leveringsadres dat is gekoppeld aan de orderkop, of als de gegevens worden gevonden in de leveringsadressen die zijn gekoppeld aan regels in die verkooporder, worden de scores van alle overeenkomsten opgeteld en vergeleken met de waarde **Minimale score** om te bepalen of de order in de wachtstand moet worden geplaatst.
- **Frauderegels** bestaan uit door de gebruiker gedefinieerde variabelen en de voorwaarden die zijn gedefinieerd voor die variabelen. Als regels wilt maken, gaat u naar **Detailhandel** \> **Afzetkanaalinstellingen** \> **Instellingen van callcenter** \> **Fraude** \> **Regels**. Met frauderegels kan een bedrijf een complexere regelset configureren die **AND**- of **OR**-instructies kan bevatten voor het evalueren van meerdere voorwaarden. Een gebruiker wil bijvoorbeeld dat alle orders voor klanten die behoren tot een bepaalde klantgroep en die een specifiek product hebben besteld, in de wachtstand worden geplaatst voor fraudecontrole. In dit geval worden de voorwaarden voor het valideren van de klant en de producten gedefinieerd op de pagina **Regels**, en wordt een AND-voorwaarde gebruikt. Een order wordt vervolgens alleen in de wachtstand geplaatst als beide voorwaarden waar zijn en als de scorewaarde die aan deze regel wordt toegewezen, plus de scorewaarde van andere regels waarmee de order overeenkomt, ertoe leidt dat de totale fraudescore van de order de waarde **Minimale score** overschrijdt die is gedefinieerd op de pagina **Parameters van callcenter**.

> [!NOTE]
> Meerdere regels of te complexe regels hebben invloed op de systeemprestaties wanneer verkooporders worden ingediend. De functie voor fraudecontrole is niet geoptimaliseerd voor het verwerken van grote hoeveelheden statische fraudegegevens en veel actieve regels. Houd er rekening mee dat elke regel wordt geëvalueerd wanneer callcentergebruikers **Indienen** selecteren tijdens verkooporderinvoer. De regels worden geëvalueerd op basis van de verkooporderkoptekst en alle orderregels. De verwerking duurt langer bij een groter aantal regels en complexere regelinstructies. Als een order een groot aantal regelartikelen en een groot aantal actieve regels en statische gegevensitems bevat, kan dit automatische proces van beoordeling en validering van alle gegevens en het berekenen van een fraudescore de prestaties sterk beïnvloeden. Organisaties die deze functie gebruiken, moeten altijd testen of de verwerkingstijd van orderindiening acceptabel is voordat ze wijzigingen toepassen op regels of statische fraudecriteria toepassen op de productieomgeving.

## <a name="identifying-orders-that-are-on-hold-for-fraud-review"></a>Orders identificeren die in de wachtstand staan voor fraudecontrole

Als callcentergebruikers een verkooporder indienen en de order voldoet aan de fraudecriteria of -regels en als de score groter is dan het minimum, ontvangen de gebruikers een waarschuwing dat de order in de wachtstand is geplaatst. Gebruikers kunnen dit bericht sluiten omdat dit alleen ter informatie dient. Gebruikers kunnen deze informatie desgewenst aan de klant communiceren. Het bedrijf moet het protocol bepalen dat gebruikers in deze situatie volgen.

De order wordt opgeslagen, maar de vlag **Niet verwerken** wordt ervoor ingesteld. Deze vlag zorgt ervoor dat de order kan niet worden vrijgegeven aan het magazijn. Op elk gewenst moment kunnen gebruikers de instelling van de vlag **Niet verwerken** weergeven voor een verkooporder op de pagina **Gedetailleerde status**. Deze pagina kan worden geopend vanuit de pagina's **Alle verkooporders** en **Klantenservice**. Het systeem werkt ook de waarde van het veld **Gedetailleerde status** voor de order bij in **Fraudewachtstand**.

Als u de orders wilt weergeven en beheren die in de wachtstand staan voor fraudecontrole, gaat u naar **Detailhandel** \> **Klanten** \> **Orderwachtstanden**. Selecteer op de pagina **Orderwachtstanden** een item in de lijst en klik vervolgens op **Orderwachtstand** om een gedetailleerdere weergave te zien met informatie over de reden voor de blokkering. Op het sneltabblad **Fraudedetails** ziet u de systematische fraudecriteria die als overeenkomst zijn gevonden voor de order en de scores die zijn toegepast. Als de order handmatig in de wachtstand is geplaatst, kunt u eventuele opmerkingen beoordelen die zijn ingevoerd door de gebruiker die de order in de wachtstand plaatste door te kijken naar het gedeelte **Fraudenotities** op het sneltabblad **Notities**.

Zie voor meer informatie over hoe u werkt met orders in de wachtstand [Orderwachtstanden](https://docs.microsoft.com/dynamics365/unified-operations/retail/work-with-order-holds).
