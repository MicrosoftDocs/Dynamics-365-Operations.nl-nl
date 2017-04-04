---
title: Schrappingsregels
description: Dit onderwerp biedt informatie over schrappingregels en de verschillende opties voor rapportage over schrappingen.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: db4b05bc55d735513d7580ca5908a1e84eb760c6
ms.openlocfilehash: 152b63fdfc78b3c4e79b93340d18c5cf69257024
ms.lasthandoff: 03/31/2017


---

# <a name="elimination-rules"></a>Schrappingsregels

Dit onderwerp biedt informatie over schrappingregels en de verschillende opties voor rapportage over schrappingen.

Schrappingtransacties zijn vereist wanneer de bovenliggende rechtspersoon zaken doet met een of meerdere dochtermaatschappijen en gebruik maakt van geconsolideerde financiële rapportage. Geconsolideerde financiële overzichten moeten alleen transacties bevatten die tussen de geconsolideerde organisatie en andere entiteiten buiten die organisaties plaatsvinden. Daarom moeten transacties tussen rechtspersonen die deel uitmaken van dezelfde organisatie worden verwijderd of geëlimineerd, uit het grootboek, zodat deze niet worden weergegeven in financiële rapporten. Er zijn meerdere manieren om over schrappingen te rapporteren:

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
Wanneer u schrappingregels in Dynamics 365 voor bewerkingen instelt, wordt u aangeraden dat u een financiële dimensie die speciaal voor schrapping doeleinden maken. De meeste klanten naam Partner handel of iets dergelijks. Als u besluit het gebruik van een financiële dimensie, moet u ervoor dat u hebt de hoofdrekeningen die specifiek zijn voor intercompany-transacties alleen. 

De instellingen voor schrappingen wordt gevonden in het gedeelte instellen van de module consolidaties. Nadat u een omschrijving voor de regel invoert, moet u het bedrijf dat het schrappingjournaal wordt geboekt naar kiezen. Dit moet een bedrijf dat **gebruiken voor financiële schrappingproces** geselecteerd in de instellingen van de rechtspersoon. 

U kunt een datum instellen waarop de schrappingregel wordt van kracht en is verlopen, indien nodig. Stelt u **actieve** naar **Ja** als u wilt dat in het voorstel schrapping beschikbaar wilt stellen. Selecteer een journaalnaam met het type van **schrapping**.

Nadat u de basisprincipes hebt gedefinieerd, kunt u de werkelijke verwerkingsregels definiëren door te klikken op **regels**. Er zijn twee opties voor schrappingen, het bedrag van de netto wijziging verwijderen of het definiëren van een vast bedrag. 

Selecteer de bronrekening. U kunt een sterretje (\*) als jokerteken. Bijvoorbeeld 1\* selecteert alle rekeningen die met een 1 als een gegevensbron voor de toewijzing beginnen. 

Nadat u uw bronrekeningen hebt geselecteerd de **specificatie rekening** bepaalt de rekening van het doelbedrijf die wordt gebruikt. Selecteer **bron** als u gebruiken de dezelfde hoofdrekening die is gedefinieerd wilt in de **bron** rekening. Als u **door gebruiker gedefinieerde**, dan moet u een doelrekening opgeven. 

De Dimensiespecificatie fungeert op dezelfde manier. Als u **bron**, dezelfde dimensies wordt gebruikt in het doelbedrijf als het bronbedrijf. Als u **door gebruiker gedefinieerde**, moet u de dimensies opgeven in het doelbedrijf door te klikken op de **doeldimensies** menu-item. 

Afmetingen bron en de financiële dimensies en waarden die worden gebruikt als een bron van de schrapping selecteren.

## <a name="process-elimination-transactions"></a>Schrappingstransacties verwerken
Er zijn twee manieren om schrappingtransacties te verwerken, tijdens het samenvoegen online of door een schrappingjournaal maken en uitvoeren van het voorstelproces schrapping. Deze sectie is gericht op het journaal maken en uitvoeren van het schrappingproces. 

Selecteer in een bedrijf dat is opgegeven als eliminatiebedrijf, **schrappingjournaal** in de module consolidaties. Nadat u de journaalnaam hebt geselecteerd, klikt u op **regels**. U kunt het voorstel uitvoeren door het selecteren van de **voorstellen** menu's en vervolgens te klikken op **Schrappingvoorstel**.

Selecteer het bedrijf dat de bron van de samengevoegde gegevens en kies vervolgens de regel die u wilt verwerken. Voer een begindatum naar het begin van de zoekopdracht voor schrappingsbedragen en een einddatum instellen voor het beëindigen van de zoekdatum voor schrappingsbedragen. De **GB-boekingsdatum** veld is de datum die wordt gebruikt om het journaal naar het grootboek te boeken. Nadat u op **OK**, u kunt de bedragen bekijken en het journaal boekt.


