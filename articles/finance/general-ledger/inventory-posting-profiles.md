---
title: Voorraadboekingsprofielen
description: Dit onderwerp bevat een overzicht van voorraadboekingsprofielen.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28e3a3051978f921e01a929496e96909e6c32429
ms.sourcegitcommit: 00b39900d3cbdbc9ca1ab3145265007f5dc98a3f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/25/2022
ms.locfileid: "8806369"
---
# <a name="inventory-posting-profiles"></a>Voorraadboekingsprofielen

[!include [banner](../includes/banner.md)]

Met voorraadboekingsprofielen wordt de boeking van transacties van het voorraadsubgrootboek naar het grootboek beheerd. Transacties van het voorraadsubgrootboek kunnen vanuit een groot aantal modules worden gegenereerd, waaronder **Verkoop en marketing**, **Inkoopbeheer**, **Productiebeheer** en meer. Transacties van het subgrootboek kunnen op elk moment worden geboekt als een artikel in een verkoop- of inkooporder wordt gebruikt. 

Extra transacties van het voorraadsubgrootboek kunnen worden geboekt:
- Telkens wanneer een document wordt bijgewerkt.
- Wanneer een pakbon van een verkooporder of een factuur wordt geboekt.
- Wanneer een productontvangstbon of factuur van een inkooporder wordt gegenereerd.

Ga naar Transacties van voorraadgrootboek voor meer informatie.

## <a name="inventory-transaction-overview"></a>Overzicht voorraadtransacties

Elke transactie van het voorraadsubgrootboek bevat het volgende:
 - Quantity 
 - Prijs 
 - Site 
 - Magazijn 
 - Locatie 

Met voorraadsubgrootboektransacties worden twee boekingen in het grootboek gemaakt via de fysieke boeking en de financiële boeking. Ga voor meer informatie naar [Fysieke en financiële updates](/supply-chain/cost-management/physical-financial-updates.md).
Het volgende voorbeeld is een inkooporder met drie regels. Voor dit voorbeeld gaan we ervanuit dat de gehele order voor één locatie en magazijn is. Elke inkooporderregel heeft één gerelateerde InventTrans-record (ook bekend als een voorraadtransactie) en elke regel is bestemd voor een hoeveelheid van 10. In het volgende diagram wordt de relatie tussen één inkooporderkoptekst en drie inkooporderregels weergegeven, elk met één InventTrans-record.

![Relatiediagram voor een inkooporder met drie regels, elk met één InventTrans-record.](./media/InventTransRelationship.PNG)

Een hoeveelheid van 5 wordt ontvangen op de eerste inkooporderregel. De volledige hoeveelheid voor de tweede regel en geen ontvangen hoeveelheid op de derde regel van de inkooporder. Er is nu een tweede voorraadtransactie aan de eerste inkooporderregel gerelateerd. De transactie voor de tweede inkooporderregel wordt bijgewerkt naar **Ontvangen** en de derde transactie blijft hetzelfde. In het volgende diagram wordt de relatie met de extra InventTrans-record voor inkooporderregel 1 weergegeven.

![Relatiediagram voor een inkooporder met drie regels. Eén regel is gedeeltelijk ontvangen en bevat twee InventTrans-records.](./media/InventTransRelationshipPartialReceipt.PNG)

In dit voorbeeld wordt een boekstuk geboekt naar het grootboek. Dit is het fysieke boekstuk. De artikelmodelgroep is geconfigureerd voor boeking van fysieke voorraad en voor alle artikelen wordt dezelfde artikelmodelgroep gebruikt. Het voorraadboekingsprofiel gebruikt één set hoofdrekeningen. Er wordt één boekstuk gemaakt en de InventTrans-record koppelt zowel InventTrans 1 als InventTrans 2 aan hetzelfde boekstuk.

Vervolgens wordt een factuur ontvangen voor de hoeveelheid die is ontvangen op regel 1 en 2. In het grootboek wordt nog een boekstuk gemaakt. Dit is het financiële boekstuk. De artikelmodelgroep is geconfigureerd voor boeking van financiële voorraad. Het nieuwe tweede boekstuk wordt gerelateerd aan InventTrans 1 en InventTrans 2.

Afhankelijk van het kostenmodel kan er een derde grootboekboeking bestaan voor uw voorraadsubgrootboektransacties met betrekking tot de afsluiting en vereffening van de voorraad. Ga voor meer informatie naar [Voorraad sluiten](/supply-chain/cost-management/inventory-close.md). U kunt de details van alle voorraadtransacties weergeven door naar **Voorraadbeheer** > **Query´s en rapporten** > **Transacties** te gaan.

>[!Important]
> De voorraadtransacties worden opgesplitst voor elke unieke combinatie van voorraaddimensie en voor elke gedeeltelijke update. Dit werd in het voorgaande voorbeeld voor gedeeltelijke updates weergegeven.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Voorraad splitsen op basis van voorraaddimensievoorbeeld

De inkooporderregel 3 in het voorbeeld is een geserialiseerd artikel. Er worden tien serienummers geregistreerd voor de inkooporder tijdens het ontvangstproces. De voorraadtransactie wordt opgesplitst in 10 voorraadtransacties. In het volgende diagram worden de relatie en extra voorraadtransacties weergegeven, elk met een eigen serienummer dat is gerelateerd aan inkooporderregel 3.

![Relatiediagram voor een inkooporder met drie regels. Eén regel is geserialiseerd en bevat extra InventTrans-records](./media/InventTransRelationshipSerialNumber.PNG)

Als in het bovenstaande voorbeeld elk serienummer wordt ontvangen op één productontvangstbon, wordt er één extra boekstuk gemaakt. Het veld Fysiek boekstuk wordt aan elk serienummer gekoppeld. Hetzelfde geldt voor de financiële update wanneer u de inkooporder factureert.

## <a name="inventory-transactions"></a>Voorraadtransacties

U kunt voorraadtransacties weergeven op de pagina **Voorraadtransacties** onder **Voorraad- en magazijnbeheer** of **Kostenbeheer**. U kunt ook voorraadtransacties weergeven die zijn gerelateerd aan een specifieke brondocumentregel, zoals een inkooporderregel of verkooporderregel, door **Voorraad** en vervolgens **Transacties** te selecteren. 

De pagina **Voorraadtransacties** bevat de volgende velden.

| Veld            | Description                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Artikelnummer      | Het artikelnummer dat aan de transactie is gerelateerd.                                                                  |
| Fysieke datum    | De datum waarop de voorraad in het magazijn binnenkomt, het magazijn verlaat, waarop de voorraad wordt verbruikt in de productie of wordt geproduceerd. Bijvoorbeeld de boekingsdatum op
de boeking van de pakbon voor een verkooporder of de boeking van de productontvangstbon voor een inkooporder.                             |
| Fin. datum   | De datum waarop de voorraadtransactie wordt gesloten en de kosten worden vastgelegd in het grootboek. Bijvoorbeeld de boekingsdatum bij het genereren van de factuur 
voor een verkooporder of inkooporder. Updates van het verwijzingsdocument zijn niet toegestaan nadat de financiële datum is ingevuld. |
| Verwijzing        | Geeft de bron van de transactie aan en het type document dat wordt weergegeven in het veld **Nummer**. Bijvoorbeeld verkooporder, inkooporder of ontvangst van transferorder.                                                 |
| Nummer           | Geeft de verwijzings-id voor een transactie aan. Als het veld **Verwijzing** bijvoorbeeld verkooporder aangeeft, geeft het veld **Nummer** het verkoopordernummer aan.                                                       |
| Ontvangst (status) | Voor voorraadtransacties die ontvangsten zijn, geeft dit veld de status van de ontvangst aan. Een inkooporder is bijvoorbeeld een ontvangst en de status kan **Besteld** of **Ingekocht** zijn.                                                            |
| Uitgifte (status)   | Voor voorraadtransacties die uitgiften zijn, geeft dit veld de status van de uitgifte aan. Een verkooporder is bijvoorbeeld een uitgifte en de status kan **In bestelling** of **Verkocht** zijn.                         |
| Quantity         | De hoeveelheid van de voorraadtransactie. Positieve getallen worden gebruikt voor ontvangsten in de voorraad en negatieve getallen voor uitgiften uit de voorraad.                                                                                                                          |
| Eenheid             | De maateenheid waarin de hoeveelheid wordt uitgedrukt.                                                                                   |
| Hoeveelheid variabel gewicht      | De hoeveelheid catch weight voor de transactie. Ga voor meer informatie naar [Over catch weight-artikelen](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Eenheid variabel gewicht          | De catch weight-maateenheid waarin de hoeveelheid catch weight wordt uitgedrukt.                                                         |
| Kosten      | De uiteindelijke kosten van de voorraadtransactie. Dit veld wordt gevuld wanneer een transactie financieel wordt bijgewerkt. Afhankelijk van de methode voor kostprijsberekening kan dit veld worden bijgewerkt door het voorraadsluitings- en correctieproces.                            |

## <a name="inventory-status"></a>Voorraadstatus

Elke voorraadtransactie heeft een status die wordt weergegeven in het veld **Ontvangst** of **Uitgifte**. Het veld dat wordt gebruikt, is afhankelijk van het type voorraadtransactie. Ontvangsten zijn transacties waardoor de voorraad toeneemt. Bijvoorbeeld een inkooporder met een positieve hoeveelheid of een verkooporderretour met een negatieve hoeveelheid. Uitgiften zijn voorraadtransacties die de voorraad doen afnemen. Bijvoorbeeld een verkooporder met een positieve hoeveelheid of een inkooporderretour met een negatieve hoeveelheid.

### <a name="receipt-status"></a>Ontvangststatus

In de volgende tabel wordt de status van **Ontvangst** beschreven.

| **Ontvangststatus** | **Beschrijving**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Besteld            | De beginstatus van een voorraadtransactie die een ontvangst vertegenwoordigt. Dit zijn onder andere inkooporders met een positieve hoeveelheid, productieorders of verkooporderretouren met een negatieve hoeveelheid.                                                   |
| Geregistreerd         | Deze status wordt gebruikt wanneer er een ontvangstproces met twee stappen bestaat of wanneer de artikelontvangst wordt gebruikt om aan te geven dat het product is gearriveerd. De status wordt gebruikt wanneer batch- of serienummers worden 'toegewezen' aan of geregistreerd voor de order. Ga voor meer informatie over artikelontvangst naar [Overzicht van ontvangst](/supply-chain/inventory/arrival-overview.md). |
| Ontvangen           | Deze status wordt gebruikt wanneer de transactie fysiek wordt bijgewerkt. Voor een inkooporder is dat wanneer de productontvangstbon wordt geboekt. Voor een verkooporderretour is dat wanneer de pakbon wordt geboekt.                                                                            |
| Ingekocht          | Deze status wordt gebruikt wanneer de transactie financieel wordt bijgewerkt. Voor een inkooporder of verkooporderretour is dat wanneer de factuur wordt gegenereerd.                                                                                             |

### <a name="issue-status"></a>Uitgiftestatus

In de volgende tabel wordt de status van **Uitgifte** beschreven.

| **Uitgiftestatus**  | **Beschrijving**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| In bestelling          | De beginstatus van een voorraadtransactie die een uitgifte vertegenwoordigt. Dit zijn onder andere verkooporders met een positieve hoeveelheid, stuklijst- of formuleregels van productieorders of inkooporderretouren met een negatieve hoeveelheid.                                             |
| Besteld en gereserveerd  | Met deze voorraadstatus wordt aangegeven dat voorraad is gereserveerd voor een order die is gemaakt, maar nog niet fysiek in de voorraad is ontvangen. Wanneer de voorraad wordt ontvangen, wordt de status automatisch bijgewerkt naar **Fysiek gereserveerd**. Ga naar [Voorraadhoeveelheden reserveren](/supply-chain/inventory/reserve-inventory-quantities.md) voor meer informatie over reserveringen. |
| Fysiek gereserveerd | Deze status geeft aan dat de voorraad is toegewezen aan of gereserveerd voor een specifieke order. Als voorraad wordt gereserveerd, zijn is deze niet fysiek beschikbaar voor andere orders.                                 |
| Verzameld         | Hiermee wordt aangegeven dat de voorraad is opgehaald in het magazijn. De voorraad is nog steeds fysiek in het magazijn aanwezig, is niet verwijderd, maar is niet beschikbaar voor andere orders.  |
| Ingehouden          | Deze status wordt gebruikt wanneer de transactie fysiek wordt bijgewerkt. Voor een verkooporder is dit het moment waarop de pakbon wordt geboekt. Voor een inkooporderretour is dit wanneer de productontvangstbon wordt geboekt.                                                                      |
| Verkocht              | Dit is de status die wordt gebruikt wanneer de transactie financieel wordt bijgewerkt. Voor een inkooporder of verkooporder is dat wanneer de factuur wordt gegenereerd.|

Ga voor meer informatie over de voorraadtransacties naar [Details van voorraadtransacties](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Een voorraadboekingsprofiel configureren

Voer de volgende stappen uit om een voorraadboekingsprofiel te configureren:

1.  Open **Voorraadbeheer** > **Instellen** > **Boeken** > **Boeken**.
2.  Selecteer het tabblad voor het transactietype. Selecteer bijvoorbeeld **Inkooporder**.
3.  Selecteer het keuzerondje voor het boekingstype. Selecteer bijvoorbeeld **Inkoopuitgaven voor onkosten**.
4.  Selecteer **Nieuw**.
5.  Selecteer in het veld **Artikelcode** een optie voor **Tabel**, **Groep**, **Alle** of **Categorie**. Als u bijvoorbeeld een boekingsprofiel wilt configureren voor een specifieke artikelgroep, selecteert u **Groep**.
     - Als u **Tabel** hebt geselecteerd in stap 5, selecteert u het specifieke artikelnummer voor het boekingsprofiel in het veld **Artikelrelatie**.
     - Als u **Groep** hebt geselecteerd in stap 5, selecteert u **Artikelgroep** voor het boekingsprofiel in het veld **Artikelrelatie**.
     - Als u **Alle** hebt geselecteerd in stap 5, blijft het veld **Artikelrelatie** leeg.
     - Als u **Categorie** hebt geselecteerd in stap 5, blijft het veld **Artikelrelatie** leeg. Gebruik het veld **Categorierelatie** om de categorie te selecteren waarop het boekingsprofiel van toepassing is.

6.  Selecteer in het veld **Rekeningcode** een optie voor **Tabel**, **Groep** of **Alle**. Selecteer **Alle** als u bijvoorbeeld het boekingsprofiel wilt toepassen op alle leveranciers.
     - Als u **Tabel** hebt geselecteerd in stap 5, selecteert u het specifieke leveranciersnummer voor het boekingsprofiel in het veld **Rekeningrelatie**.
     - Als u **Groep** hebt geselecteerd in stap 5, selecteert u de leveranciersgroep voor het boekingsprofiel in het veld **Rekeningrelatie**.
     - Als u **Alle** hebt geselecteerd in stap 5, blijft het veld **Rekeningrelatie** leeg.

7.  Als u een bepaalde btw-groep met het geselecteerde boekingstype wilt koppelen, selecteert u een **btw-groep**. Als dit veld leeg, is het boekingstype van toepassing op alle bestaande belastinggroepen. Boeking die is opgegeven voor belastinggroepen, is alleen van toepassing op verkoop- en inkooptransacties.
8.  Geef in het veld **Hoofdrekening** het rekeningnummer op waarnaar u het rekeningtype wilt boeken. Als er geen rekeningnummer is gemaakt om te gebruiken als boekhoudtype, kunt u een nieuwe rekening maken. U maakt een nieuwe rekening op de pagina **Grootboekrekeninggegevens** in het grootboek.

## <a name="additional-resources"></a>Aanvullende bronnen

Elk tabblad op de pagina **Voorraadboekingsprofiel** heeft betrekking op een subgrootboek in Dynamics 365 Supply Chain Management. Ga voor meer informatie naar:
-   [Verkooporders boeken](sales-order-posting.md)
-   [Boeking van inkooporders](purchase-order-posting.md)
-   [Voorraadboeking](inventory-posting.md)
-   [Boeking voor Productiebeheer](production-posting.md)
-   [Boeking voor standaardkostenafwijking](standard-cost-variance-posting.md)
