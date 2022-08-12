---
title: Overzicht van Verkoop en marketing
description: Met Verkoop en marketing kunt u verschillende typen gegevens in de verkoopstroom opvragen, opslaan en gebruiken. Hierbij gaat het om gegevens zoals het oorspronkelijke verkoopinitiatief, toekomstige opvolgingsacties en extra verkopen.
author: Henrikan
ms.date: 07/25/2019
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "92303"
- intro-internal
ms.assetid: 65ca9992-bbfa-4224-bf0e-067a25c7e6a4
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25b87f45e43350f6c5e6ea775ebc3fcd74ec5187
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103795"
---
# <a name="sales-and-marketing-overview"></a>Overzicht van Verkoop en marketing

[!include [banner](../includes/banner.md)]

Met Verkoop en marketing kunt u verschillende typen gegevens in de verkoopstroom opvragen, opslaan en gebruiken. Hierbij gaat het om gegevens zoals het oorspronkelijke verkoopinitiatief, toekomstige opvolgingsacties en extra verkopen.

## <a name="marketing"></a>Marketing

U kunt marketingcampagnes en -activiteiten gebruiken om relaties met potentiële klanten te vinden en op te bouwen, zodat initiële interacties zich kunnen ontwikkelen tot verkooprelaties. In het volgende processtroomdiagram ziet u het bedrijfsproces voor marketing. [![Bedrijfsproces voor marketing.](./media/marketing01.jpg)](./media/marketing01.jpg)

### <a name="relationships"></a>Relaties

In verkoop en marketing kunnen de initiële interacties die u hebt met potentiële klanten plaatsvinden in verschillende situaties. Zo vindt u bijvoorbeeld mogelijk een potentiële klant terwijl u een beurs bijwoont of krijgt u een mogelijke lead bij een klant nadat uw organisatie een campagne voor bulkpost heeft uitgevoerd. Het is zeer belangrijk dat u de stroom van de entiteit van een partij begrijpt voordat die partij een klant wordt. In de volgende afbeelding ziet u de stroom van entiteitsrelaties als een potentiële klant een werkelijke klant wordt. [![SalesandMarketing01.](./media/salesandmarketing01.jpg)](./media/salesandmarketing01.jpg)

### <a name="campaigns"></a>Campagnes

Een campagne is gericht op de contactpersonen van prospects, potentiële klanten, verkoopkansen en klanten die zijn geselecteerd voor deelname aan de campagne. In Supply Chain Management kunt u verschillende typen campagnes maken, zoals telemarketing-, mailing- en e-mailcampagnes, om uw klantenpotentieel te maximaliseren. Als uw campagne vordert en u positieve reacties ontvangt, kunt u het verkoopproces beginnen met de geadresseerden die positief hebben gereageerd op de campagne.

## <a name="sales"></a>Verkoop
U gebruikt de verkoopfunctionaliteit om offertes te maken, meerverkoop en kruisverkoop uit te voeren bij nieuwe en bestaande klanten, verkooporders te genereren en verkoopfacturen op te stellen voor klanten. In het volgende processtroomdiagram ziet u het bedrijfsproces voor verkoop. [![Bedrijfsproces voor verkoop.](./media/sales01.jpg)](./media/sales01.jpg)

### <a name="sales-quotations"></a>Verkoopoffertes

U maakt verkoopoffertes om klanten een aanbieding te doen van de goederen of diensten die u zult leveren. Een klant kan een offerte aanvragen of u kunt een offerte maken als reactie op een verzoek van een potentiële of bestaande klant. Wanneer de klant de verkoopofferte goedkeurt, kunt u deze converteren naar een verkooporder.

### <a name="up-sellcross-sell"></a>Meerverkoop/bijverkoop

Meer- en kruisverkoop zijn technieken voor het verkopen van producten bij het invoeren van een order voor een klant. Bij meerverkoop wordt een ander product voorgesteld in plaats van het huidige product. Bij kruisverkoop wordt een product voorgesteld naast het huidige product. Wanneer u productlijsten instelt, kunt u specifieke regels opstellen om aan te geven wanneer een product moet worden voorgesteld als een product voor bij- of meerverkoop.

### <a name="sales-orders"></a>Verkooporders

Als u een nieuwe verkooporder maakt, moet u het type verkooporder selecteren dat u wilt maken. U hebt vijf opties. **Opmerking:** nadat u een verkooporder hebt gemaakt, kan elk ordertype worden gewijzigd, behalve het type **Artikelbehoeften** als de verkooporder de status **Geleverd** heeft.

| Type verkooporder  | Beschrijving                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Journaal           | Gebruik dit type als concept voor een verkooporder. Dit type heeft geen effect op de voorradige hoeveelheden en genereert geen artikeltransacties.                                                                                                                                                                    |
| Abonnement      | Gebruik dit type voor terugkerende orders. Als de order is gefactureerd, wordt de orderstatus automatisch ingesteld op een openstaande order. De gefactureerde geleverde hoeveelheid en de resterende leveringen worden bijgewerkt. U kunt dit verkoopordertype niet gebruiken als u de functionaliteit voor magazijnbeheer gebruikt. |
| Verkooporder       | Gebruik dit type wanneer een klant een order heeft geplaatst of bevestigd.                                                                                                                                                                                                                                        |
| Geretourneerde order    | Gebruik dit type wanneer een klant een artikel terugstuurt. Er wordt automatisch een retourartikelnummer (RMA-nummer) toegewezen.                                                                                                                                                                                            |
| Artikelbehoeften | Dit type wordt automatisch gemaakt wanneer u een artikelverkoop via een project maakt.                                                                                                                                                                                                                       |

### <a name="sales-agreements"></a>Verkoopovereenkomsten

Een verkoopovereenkomst is een contract waarmee een klant toezegt een specifieke hoeveelheid van een product te kopen of het product gedurende een specifieke periode te kopen in ruil voor speciale prijzen en kortingen. De prijzen en kortingen van de verkoopovereenkomst vervangen alle prijzen en kortingen die worden genoemd in eventuele bestaande handelsovereenkomsten. Een verkoopovereenkomst is gedurende een gedefinieerde periode geldig. De gewenste verzenddatum die is opgegeven voor een verkoop op de pagina **Verkooporder** moet zich in de geldige periode bevinden. Een verkoopovereenkomst is standaard in wachtstand. U kunt alleen een order plaatsen vanuit een verkoopovereenkomst wanneer deze is ingesteld op **Effectief**.

### <a name="backorders"></a>Naleveringen

Bij het invoeren en valideren van orders moet u mogelijk naleveringen en uitzonderingen beheren voordat de verkoop kan worden voltooid. Naleveringen zijn inkooporders die nog niet door de leverancier zijn geleverd of verkooporders die nog niet aan een klant zijn geleverd. Het is belangrijk dat naleveringen worden opgevolgd. Als producten bijvoorbeeld niet op tijd door een leverancier worden geleverd, zult u waarschijnlijk de leveringsdatum voor een klant moeten wijzigen en de klant hierover moeten informeren. U kunt naleveringen weergeven per artikel, klant of leverancier.

#### <a name="viewing-backorders-by-item"></a>Naleveringen weergeven per artikel

Als u de naleveringen per artikel bekijkt, kunt u opvolgen voor de verwachte stroom transacties voor een bepaald artikel. U kunt bijvoorbeeld de volgende gegevens controleren:

-   Het aantal verkooporders dat voor een artikel is geplaatst
-   Of nog leveringen van het artikel van leveranciers ontbreken
-   Of er meer artikelen moeten worden besteld, zodat u alle verkooporders op tijd kunt leveren

Door deze controle uit te voeren, kunt u reageren op aanvragen van klanten over het tijdstip van de artikellevering. Bovendien kunt u bepaalde naleveringen een hogere prioriteit geven en indien nodig de voorradige artikelen tussen de orders verdelen.

#### <a name="viewing-backorders-by-customer"></a>Naleveringen weergeven per klant

Met het overzicht van de naleveringen op klant kunt u de status van de resterende orders van de klant bekijken. Deze controle is handig wanneer u moet reageren op klanten die wachten op artikelen die vertraging hebben opgelopen.

#### <a name="viewing-backorders-by-vendor"></a>Naleveringen weergeven per leverancier

Wanneer u naleveringen op leverancier bekijkt, kunt u de ontbrekende leveringen en verwachte datums van levering opvolgen. Via deze controle kunt u prioriteiten toewijzen wanneer producten van de leveranciers binnenkomen en de verkooporders voor levering moeten worden verzameld.

### <a name="invoices"></a>Facturen

Tijdens het verkoopproces kunt u drie typen facturen maken:

-   Klantfactuur
-   Vrije-tekstfactuur
-   Pro-formafactuur

#### <a name="customer-invoice"></a>Klantfactuur

Een klantfactuur is een factuur die door een organisatie aan een klant wordt verstrekt in verband met een verkoop. U maakt een dergelijke klantfactuur op basis van een verkooporder die een koptekst en een of meer regels bevat voor artikelen of services. De klantfactuur voltooit de cyclus van verkooporder, pakbon en verkoopfactuur.  

U kunt een enkele klantfactuur boeken en afdrukken op basis van een verkooporder of de pakbon en de datum. U kunt ook meerdere klantfacturen boeken en samen afdrukken op basis van de pakbonnen en datums. Wanneer u een enkele klantfactuur boekt, door gebruik te maken van de verkooporder, wordt de hoeveelheid **Resterend gedeelte van factuur** voor elk artikel bijgewerkt met het totaal van de gefactureerde hoeveelheden van de geselecteerde verkooporder.  

Als zowel de hoeveelheid voor **Resterend gedeelte van factuur** als de hoeveelheid voor **Nog te leveren** voor alle artikelen op de verkooporder 0 (nul) is, wordt de status van de verkooporder gewijzigd in **Gefactureerd**. Als de hoeveelheid in een van beide velden niet 0 is, blijft de status van de verkooporder ongewijzigd en kunt u aanvullende facturen invoeren. Als u een of meer klantfacturen wilt boeken en afdrukken op basis van de pakbonnen, moet u ten minste één pakbon voor elke verkooporder al hebben geboekt. De klantfactuur is gebaseerd op de pakbonnen en hieruit worden de vermelde hoeveelheden overgenomen.  

U kunt een klantfactuur maken op basis van de artikelen op de pakbonregel die tot op heden zijn verzonden, ook als nog niet alle artikelen voor een bepaalde verkooporder zijn verzonden. U kunt dit bijvoorbeeld doen als uw rechtspersoon één factuur per klant per maand verzendt waarin alle leveringen in de desbetreffende maand zijn opgenomen. Met elke pakbon wordt een gedeeltelijke of gehele levering van de artikelen op de verkooporder aangeduid.  

Wanneer u de factuur maakt, wordt de hoeveelheid voor **Resterend gedeelte van factuur** voor elk artikel bijgewerkt met het totaal van de geleverde hoeveelheden via de geselecteerde pakbonnen. Als de hoeveelheid voor **Resterend gedeelte van factuur** en de hoeveelheid voor **Nog te leveren** voor alle artikelen op de verkooporder 0 (nul) zijn, wordt de status van de verkooporder gewijzigd in **Gefactureerd**. Als de hoeveelheid niet 0 is, blijft de status van de verkooporder ongewijzigd en kunt u aanvullende facturen invoeren. Voorraadtransacties worden bijgewerkt met het factuurnummer en de status op de verkooporderregel wordt gewijzigd in **Gefactureerd**.

#### <a name="free-text-invoice"></a>Vrije-tekstfactuur

Een vrije-tekstfactuur is een factuur die niet is gerelateerd aan een verkooporder. Deze factuur bevat orderregels met grootboekrekeningen, vrije-tekstomschrijvingen en een verkoopbedrag. U kunt een artikelnummer invoeren op dit type factuur en u moet de juiste btw-gegevens invoeren. Op elke factuurregel wordt een hoofdrekening voor de verkoop vermeld. Het klantsaldo wordt geboekt naar de totaalrekening van het boekingsprofiel dat gebruikt wordt voor de vrije-tekstfactuur.

#### <a name="pro-forma-invoice"></a>Pro-formafactuur

Een pro forma-factuur is een factuur die wordt gemaakt als raming van het werkelijke factuurbedrag voordat de factuur wordt geboekt. Een pro forma-factuur kunt u zowel voor een klantfactuur als voor een vrije-tekstfactuur afdrukken.

### <a name="additional-resources"></a>Aanvullende resources

#### <a name="blogs"></a>Weblogs

U kunt een overzicht van een verkoopproces vinden in de post [Hoe verkoop werkt in Dynamics 365 Finance and Operations](https://financefunction.tech/2018/05/15/how-sales-work-in-dynamics-365-for-finance-and-operations).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
