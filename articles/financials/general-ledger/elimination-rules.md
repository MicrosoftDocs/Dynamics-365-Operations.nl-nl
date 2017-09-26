---
title: Schrappingsregels
description: Dit onderwerp bevat informatie over schrappingsregels en de verschillende opties voor het rapporteren van schrappingen.
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 76af350f37109260a757ccc0b93908637d0579dc
ms.contentlocale: nl-nl
ms.lasthandoff: 06/13/2017

---

# <a name="elimination-rules"></a>Schrappingsregels

[!include[banner](../includes/banner.md)]


Dit onderwerp bevat informatie over schrappingsregels en de verschillende opties voor het rapporteren van schrappingen.

Schrappingtransacties zijn vereist wanneer de bovenliggende rechtspersoon zaken doet met een of meerdere dochtermaatschappijen en gebruik maakt van geconsolideerde financiële rapportage. Geconsolideerde financiële overzichten moeten alleen transacties bevatten die tussen de geconsolideerde organisatie en andere entiteiten buiten die organisaties plaatsvinden. Daarom moeten transacties tussen rechtspersonen die deel uitmaken van dezelfde organisatie worden verwijderd of geëlimineerd uit het grootboek, zodat ze niet in financiële rapporten worden weergegeven. Er zijn meerdere manieren om over schrappingen te rapporteren:

-   Een schrappingsregel kan in een consolidatie- of eliminatiebedrijf worden gemaakt en verwerkt.
-   Financiële rapportage kan worden gebruikt om de schrappingsrekeningen en -dimensies in een specifieke rij of kolom weer te geven.
-   Een afzonderlijke rechtspersoon kan worden gebruikt om handmatige transactievermeldingen te boeken om schrappingen bij te houden.

Dit onderwerp is gericht op schrappingsregels die in een consolidatie- of eliminatiebedrijf worden verwerkt. U kunt schrappingregels opstellen om schrappingtransacties te maken in een rechtspersoon die is opgegeven als de doelrechtspersoon voor schrappingen. Deze doelrechtspersoon wordt de eliminatierechtspersoon genoemd. Schrappingjournalen kunnen tijdens het consolidatieproces of met behulp van een schrappingsjournaalvoorstel worden gegenereerd. Voordat u schrappingregels opstelt, moet u vertrouwd zijn met de volgende definities:

-   **Bronrechtspersoon** – De rechtspersoon waarop de bedragen die geschrapt worden, geboekt zijn.
-   **Doelrechtspersoon** - De rechtspersoon waarop schrappingsregels worden geboekt.
-   **Schrappingsrechtspersoon** - De rechtspersoon die is opgegeven als de doelrechtspersoon voor schrappingen.
-   **Geconsolideerde rechtspersoon** – De rechtspersoon die gemaakt wordt voor het rapporteren van financiële resultaten voor een groep rechtspersonen. De financiële gegevens van de rechtspersonen worden naar deze rechtspersoon samengevoegd en vervolgens wordt een financieel verslag gemaakt met behulp van de gecombineerde gegevens.

De volgende tabel geeft de soorten transacties weer die mogelijk moeten worden geëlimineerd.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Transactietype</th>
<th>Voorbeeld:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Invoer en facturering van verkooporders (gecentraliseerde verwerking)</td>
<td>U verkoopt een product aan een klant namens een andere rechtspersoon in uw organisatie.</td>
</tr>
<tr class="even">
<td>Invoer (intercompany/intracompany) en facturering van verkooporders</td>
<td>U verkoopt producten tussen rechtspersonen in uw organisatie.</td>
</tr>
<tr class="odd">
<td>Inkooporders (gecentraliseerde verwerking)</td>
<td>U schaft voorraad, diensten, vaste activa en andere producten van een leverancier aan namens een andere rechtspersoon in uw organisatie.</td>
</tr>
<tr class="even">
<td>Voorraadbeheer (intercompany/intracompany)</td>
<td><ul>
<li>U brengt de voorraad van één rechtspersoon over naar de vaste activa van een andere rechtspersoon in uw organisatie.</li>
<li>U brengt de voorraad van één rechtspersoon over naar de voorraad van een andere rechtspersoon in uw organisatie.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tracering van transitvoorraad</td>
<td>U brengt artikelen over van het ene naar het andere magazijn in dezelfde rechtspersoon, maar naar verschillende geografische locaties.</td>
</tr>
<tr class="even">
<td>Gecentraliseerde verwerking van leveranciersfacturen</td>
<td>U registreert een factuur namens een andere rechtspersoon in uw organisatie.</td>
</tr>
<tr class="odd">
<td>Gecentraliseerde verwerking van leverancierbetalingen</td>
<td>U betaalt een factuur namens een andere rechtspersoon in uw organisatie.</td>
</tr>
<tr class="even">
<td>Kasbeheer en schatkist (gecentraliseerde verwerking)</td>
<td><ul>
<li>U verwerkt belastingbetalingen, belastingrestituties, rentelasten, leningen, voorschotten, dividendbetalingen en vooruitbetaalde royalties of provisies.</li>
<li>U betaalt onkosten namens een andere rechtspersoon in uw organisatie. De factuur wordt ingevoerd in de boeken van de bestemmingsrechtspersoon en u moet tussen rechtspersonen vereffenen. Één rechtspersoon betaalt bijvoorbeeld de onkostendeclaratie van een werknemer in een andere rechtspersoon. In dit geval bevat de onkostendeclaratie van de werknemer onkosten die gerelateerd zijn aan een andere rechtspersoon.</li>
<li>U brengt contant geld over van de ene rechtspersoon in uw organisatie naar de andere.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Klanten (gecentraliseerde verwerking)</td>
<td>U ontvang contant geld voor de klantfactuur van een andere rechtspersoon en u stort de cheque bij de bankrekening van die rechtspersoon.</td>
</tr>
<tr class="even">
<td>Salaris (gecentraliseerde verwerking, intercompany/intracompany)</td>
<td><ul>
<li>U betaalt de salarissen van een andere rechtspersoon. Een rechtspersoon betaalt bijvoorbeeld de salarissen van haar eigen werknemers, maar brengt werk in rekening dat een werknemer tijdens die salariscyclus voor een andere rechtspersoon heeft gedaan. Of een werknemer werkte bijvoorbeeld parttime voor rechtspersoon A en parttime voor rechtspersoon B, waarbij de vergoedingen van toepassing zijn op het volledige salaris. In deze gevallen bevat het salaris van de werknemer betalingen uit beide rechtspersonen. Niet alleen de salarissen worden geboekt, maar ook belastingen, vergoedingen, inhoudingen en transitorische posten voor salarissen.</li>
<li>U brengt arbeid over van de ene afdeling of divisie naar de andere.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Vaste activa (intercompany/intracompany)</td>
<td>U verplaatst vaste activa naar de vaste activa of voorraad van een andere rechtspersoon.</td>
</tr>
<tr class="even">
<td>Toewijzingen (intercompany/intracompany)</td>
<td>U verwerkt bedrijfstoewijzingen. Toewijzingen zijn activiteiten naar een willekeurige toegewezen rekening, ongeacht de bronmodule.</td>
</tr>
</tbody>
</table>

## <a name="example"></a>Voorbeeld:
Uw rechstpersoon, rechtspersoon A, verkoopt widgets aan een andere rechtspersoon in uw organisatie, rechtspersoon B. In het volgende voorbeeld ziet u hoe de transacties die tussen de twee rechtspersonen plaatsvinden mogelijk moeten worden geëlimineerd:

-   Rechtspersoon A verkoopt een widget die 10,00 kost aan rechtspersoon B voor 10,00.
-   Rechtspersoon A verkoopt een widget die 10,00 kost aan rechtspersoon B voor 10,00, plus 2,00 voor daadwerkelijke verzendkosten.
-   Rechtspersoon A verkoopt een widget die 10,00 kost aan rechtspersoon B voor 15,00 en hanteert een marge op de verkoop.
-   Rechtspersoon A verkoopt een widget die 10,00 kost aan rechtspersoon B voor 15,00 en hanteert de helft van de marge op de verkoop. Rechtspersoon B hanteert de andere helft van de marge op de verkoop. Daarom wordt de opbrengst gesplitst. Gedeelde opbrengsten bieden een stimulans om bij een andere rechtspersoon in de organisatie te bestellen in plaats van bij een externe organisatie.

Al deze transacties resulteren in intercompany-transacties die worden geboekt naar rekeningen voor betalen aan en betalen van. Bovendien bevatten deze transacties mogelijk prijsverhogings- en prijsverlagingsbedragen wanneer het bedrag van de intercompanyverkoop niet overeenkomt met de kosten van de verkochte goederen.

## <a name="set-up-elimination-rules"></a>Schrappingregels instellen
Wanneer u schrappingsregels in Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition instelt, wordt u aangeraden een financiële dimensie te maken die speciaal geldt voor schrappingsdoeleinden. De meeste klanten noemen dit Handelspartner of iets dergelijks. Als u besluit geen financiële dimensie te gebruiken, moet u ervoor zorgen dat u hoofdrekeningen hebt die specifiek en uitsluitend voor intercompany-transacties gelden. 

De instellingen voor schrappingen vindt u in het gedeelte Instellen van de module Consolidaties. Nadat u een omschrijving voor de regel hebt ingevoerd, moet u het bedrijf selecteren waarnaar het schrappingsjournaal wordt geboekt. Dit moet een bedrijf zijn waarvoor **Gebruiken voor proces voor financiële schrapping** is ingeschakeld in de instellingen van de rechtspersoon. 

U kunt een datum instellen waarop de schrappingsregel van kracht wordt en, indien nodig, wanneer deze is verlopen. U moet **Actief** instellen op **Ja** als u wilt dat de regel beschikbaar is in het schrappingsvoorstelproces. Selecteer een journaalnaam met het type **Schrapping**.

Nadat u de basisprincipes hebt gedefinieerd, kunt u de werkelijke verwerkingsregels definiëren door te klikken op **Regels**. Er zijn twee opties voor schrappingen: het bedrag van de nettowijziging verwijderen of een vast bedrag definiëren. 

Selecteer uw bronrekening. U kunt als jokerteken een sterretje (\*) gebruiken. In het voorbeeld worden met 1\* alle rekeningen geselecteerd die beginnen met 1 als een gegevensbron voor de toewijzing. 

Nadat u uw bronrekeningen hebt geselecteerd, wordt met de **Rekeningspecificatie** de rekening bepaald van het doelbedrijf dat wordt gebruikt. Selecteer **Bron** als u dezelfde hoofdrekening wilt gebruiken die is gedefinieerd in de rekening **Bron**. Als u **Door gebruiker gedefinieerd** selecteert, moet u een doelrekening opgeven. 

De dimensiespecificatie werkt op dezelfde manier. Als u **Bron** selecteert, worden dezelfde dimensies in het doelbedrijf gebruikt als het bronbedrijf. Als u **Door gebruiker gedefinieerd** selecteert, moet u de dimensies opgeven in het doelbedrijf door te klikken op de menuoptie **Doeldimensies**. 

Selecteer brondimensies en de financiële dimensies en waarden die worden gebruikt als een bron van de schrapping.

## <a name="process-elimination-transactions"></a>Schrappingstransacties verwerken
Er zijn twee manieren om schrappingstransacties te verwerken, tijdens het online consolidatieproces of door een schrappingsjournaal te maken en het schrappingsvoorstelproces uit te voeren. Dit gedeelte is gericht op het maken van het journaal en het uitvoeren van het schrappingsproces. 

Selecteer in een bedrijf dat is gedefinieerd als een eliminatiebedrijf **Schrappingsjournaal** in de module consolidaties. Klik op **Regels** als u de journaalnaam hebt geselecteerd. U kunt het voorstel uitvoeren door het menu **Voorstellen** en vervolgens **Schrappingsvoorstel** te selecteren.

Selecteer het bedrijf dat de bron is van de geconsolideerde gegevens en kies vervolgens de regel die u wilt verwerken. Voer een begindatum in waarop de zoekopdracht naar schrappingsbedragen moet beginnen, en een einddatum voor het beëindigen van de zoekdatum voor schrappingsbedragen. Voer in het veld **Boekingsdatum GB** de datum in waarop het journaal naar het grootboek moet worden geboekt. Nadat u op **OK** hebt geklikt, kunt u de bedragen bekijken en het journaal boeken.




