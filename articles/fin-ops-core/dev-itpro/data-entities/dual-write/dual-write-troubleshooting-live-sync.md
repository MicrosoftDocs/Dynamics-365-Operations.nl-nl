---
title: Problemen met live synchronisatie oplossen
description: Dit onderwerp bevat informatie over het oplossen van problemen met live synchronisatie.
author: RamaKrishnamoorthy
ms.date: 08/19/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 73a226d10c951179fd9f3bc2aed4a70efcc7f020
ms.sourcegitcommit: 98061a5d096ff4b9078d1849e2ce6dd7116408d1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/01/2021
ms.locfileid: "7466239"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Problemen met live synchronisatie oplossen

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp bevat informatie voor het oplossen van problemen voor de integratie van twee keer wegschrijven tussen Finance and Operations-apps en Microsoft Dataverse. Dit onderwerp bevat specifieke informatie over het oplossen van problemen met live synchronisatie.

> [!IMPORTANT]
> Bij sommige problemen die in dit onderwerp worden beschreven, is mogelijk de rol van systeembeheerder vereist of de inloggegevens van de tenantbeheerder van de Microsoft Azure Active Directory (Azure AD). In elk gedeelte wordt uitgelegd of een specifieke rol of specifieke inloggegevens vereist zijn.

## <a name="live-synchronization-shows-an-error-when-you-create-a-row"></a>Bij live synchronisatie wordt een fout weergegeven wanneer u een rij aanmaakt

Mogelijk wordt het volgende foutbericht weergegeven wanneer u een rij in een Finance and Operations-app maakt:

*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"De gebruiker is geen lid van de organisatie.\\"}}\], De externe server heeft een fout geretourneerd: (403) verboden."}}".*

Volg de stappen in [Systeemvereisten en vereisten vooraf](requirements-and-prerequisites.md) om het probleem op te lossen. Om deze stappen te voltooien, moeten gebruikers van de toepassing voor twee keer wegschrijven die in Dataverse zijn aangemaakt, beschikken over de rol systeembeheerder. Het standaardteam van eigenaar moet ook de rol systeembeheerder hebben.

## <a name="live-synchronization-shows-an-error-when-you-try-to-save-table-data"></a>Bij live synchronisatie wordt een fout weergegeven wanneer u tabelgegevens probeert op te slaan

**Vereiste rol om de fout op te lossen:** systeembeheerder

Mogelijk wordt het volgende foutbericht weergegeven wanneer u probeert tabelgegevens op te slaan in een Finance and Operations-app:

*De wijzigingen in de database kunnen niet worden opgeslagen. Werkeenheid kan transactie niet doorvoeren. Kan geen gegevens schrijven in maateenheid van entiteit. Schrijven naar UnitOfMeasureEntity is mislukt met foutbericht Kan niet synchroniseren met maateenheden van entiteit.*

Om het probleem op te lossen, moet u ervoor zorgen dat de vooraf vereiste verwijzingsgegevens aanwezig zijn in zowel de app Finance and Operations als Dataverse. Als een klantrecord bijvoorbeeld deel uitmaakt van een specifieke klantengroep, zorg er dan voor dat het record van de klantengroep bestaat in Dataverse.

Voer de volgende stappen uit als er op beide plekken gegevens voorkomen en is bevestigd dat het probleem niet samenhangt met gegevens.

1. Open de entiteit **DualWriteProjectConfigurationEntity** met de Excel-invoegtoepassing. Als u de invoegtoepassing wilt gebruiken, moet u de ontwerpmodus in de Excel-invoegtoepassing van Finance and Operations inschakelen en de **DualWriteprojectConfigurationEntity** aan een werkblad toevoegen. Zie [Entiteitsgegevens weergeven en bijwerken met Excel](../../office-integration/use-excel-add-in.md) voor meer informatie.
2. Selecteer en verwijder de records waarmee problemen zijn in de toewijzing voor twee keer wegschrijven en het project. Er zullen twee records bestaan voor elke toewijzing voor twee keer wegschrijven.
3. Publiceer de wijzigingen met de Excel-invoegtoepassing. Deze stap is belangrijk omdat hiermee de records uit de entiteit en onderliggende tabellen worden verwijderd.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Fouten met lees- of schrijfbevoegdheid oplossen wanneer u gegevens maakt in een Finance and Operations-app

Mogelijk wordt het foutbericht 'Ongeldige aanvraag' weergegeven wanneer u gegevens in een Finance and Operations-app aanmaakt.

![Voorbeeld van foutbericht Ongeldige aanvraag.](media/error_record_id_source.png)

Dit probleem is op te lossen door de juiste beveiligingsrol toe te wijzen aan het team van de toegewezen Dynamics 365 Sales- of Dynamics 365 Customer Service-bedrijfseenheden om de ontbrekende bevoegdheid in te schakelen.

1. Zoek in de Finance and Operations-app de bedrijfseenheid die is toegewezen in de verbindingsset Gegevensintegratie.

    ![Organisatietoewijzing.](media/mapped_business_unit.png)

2. Meld u aan bij de omgeving in de app voor klantbetrokkenheid, navigeer naar **Instelling \> Beveiliging** en zoek het team van de toegewezen bedrijfseenheid.

    ![Team van de toegewezen bedrijfseenheid.](media/setting_security_page.png)

3. Open de pagina voor het team om deze te bewerken en selecteer **Rollen beheren**.

    ![De knop Rollen beheren.](media/manage_team_roles.png)

4. Wijs in het dialoogvenster **Teamrollen beheren** de rol toe die de lees-/schrijf bevoegdheid voor de relevante tabellen heeft en selecteer vervolgens **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Synchronisatie problemen oplossen in een omgeving met een recent gewijzigde Dataverse-omgeving

**Vereiste rol om de fout op te lossen:** systeembeheerder

Mogelijk wordt het volgende foutbericht weergegeven wanneer u gegevens in een Finance and Operations-app maakt:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Kan geen nettolading genereren voor entiteit CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Het maken van de nettolading is mislukt met fout Ongeldige URI: de URI is leeg."}\],"isErrorCountUpdated":true}*

Het foutbericht ziet er als volgt uit in de app voor klantbetrokkenheid:

> Er is een onverwachte fout opgetreden vanuit de ISV-code. (Fouttype = ClientError) Onverwachte uitzondering vanuit invoegtoepassing (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: verwerken van entiteitsaccount mislukt - (een verbindingspoging is mislukt omdat de verbonden partij niet correct reageert na een bepaalde tijd of de tot stand gebrachte verbinding is mislukt omdat de verbonden host niet heeft gereageerd.

Deze fout treedt op als de Dataverse-omgeving onjuist opnieuw wordt ingesteld wanneer u probeert gegevens aan te maken in de Finance and Operations-app.

> [!IMPORTANT]
> Als u de omgevingen opnieuw hebt gekoppeld, moet u alle entiteitstoewijzingen stoppen voordat u verder gaat met de te ondernemen beperkende stappen.

Om het probleem op te lossen, moet u stappen in zowel de Dataverse-app als in de Finance and Operations-app voltooien.

1. Volg in de Finance and Operations-app deze stappen:

    1. Open de entiteit **DualWriteProjectConfigurationEntity** met de Excel-invoegtoepassing. Als u de invoegtoepassing wilt gebruiken, moet u de ontwerpmodus in de Excel-invoegtoepassing van Finance and Operations inschakelen en de **DualWriteprojectConfigurationEntity** aan een werkblad toevoegen. Zie [Entiteitsgegevens weergeven en bijwerken met Excel](../../office-integration/use-excel-add-in.md) voor meer informatie.
    2. Selecteer en verwijder de records waarmee problemen zijn in de toewijzing voor twee keer wegschrijven en het project. Er zullen twee records bestaan voor elke toewijzing voor twee keer wegschrijven.
    3. Publiceer de wijzigingen met de Excel-invoegtoepassing. Deze stap is belangrijk omdat hiermee de records uit de entiteit en onderliggende tabellen worden verwijderd.
    4. Om fouten te voorkomen wanneer u de Finance and Operations- of Dataverse-omgevingen opnieuw met elkaar koppelt, moet u ervoor zorgen dat er geen configuraties met twee keer wegschrijven overblijven.

2. Volg in Dataverse deze stappen:

    1. Meld u aan bij uw Dataverse-omgeving (bijvoorbeeld `https://*****.crm.dynamics.com/`).
    2. Ga naar **Geavanceerde instellingen** \> **Geavanceerd zoeken**.
    3. Selecteer **DualWrite Runtime Configuration**.
    4. Selecteer de kolom die u wilt weergeven.
    5. Selecteer **Resultaten** om de configuraties weer te geven.
    6. Alle exemplaren verwijderen.

3. Volg in de Finance and Operations-app deze stappen:

    1. Open de entiteit **DualWriteProjectConfigurationEntity** met de Excel-invoegtoepassing. Als u de invoegtoepassing wilt gebruiken, moet u de ontwerpmodus in de Excel-invoegtoepassing van Finance and Operations inschakelen en de **DualWriteprojectConfigurationEntity** aan een werkblad toevoegen. Zie [Entiteitsgegevens weergeven en bijwerken met Excel](../../office-integration/use-excel-add-in.md) voor meer informatie.
    2. Selecteer en verwijder de records waarmee problemen zijn in de toewijzing voor twee keer wegschrijven en het project. Er zullen twee records bestaan voor elke toewijzing voor twee keer wegschrijven.
    3. Publiceer de wijzigingen met de Excel-invoegtoepassing. Deze stap is belangrijk omdat hiermee de records uit de entiteit en onderliggende tabellen worden verwijderd.
    4. Om fouten te voorkomen wanneer u de Finance and Operations- of Dataverse-omgevingen opnieuw met elkaar koppelt, moet u ervoor zorgen dat er geen configuraties met twee keer wegschrijven overblijven.

## <a name="live-synchronization-error-after-you-do-a-full-database-copy"></a>Fout in live synchronisatie nadat u een volledige kopie van de database hebt gemaakt

Het kan zijn dat u het volgende foutbericht ontvangt nadat u een volledige kopie van de database hebt uitgevoerd van een systeem naar een ander systeem en vervolgens hebt geprobeerd een databasebewerking uit te voeren:

*SecureConfig Organization (???) komt niet overeen met werkelijke CRM-organisatie (???).*

Het foutbericht wordt weergegeven via de invoegtoepassing twee keer wegschrijven-runtime om te garanderen dat de configuratie voor twee keer wegschrijven die in het ene systeem is ingesteld, niet in een ander systeem kan worden gebruikt.

Als u het probleem wilt oplossen, verwijdert u alle records in de tabel **msdyn_dualwriteruntimeconfig** nadat u de database hebt hersteld. Raadpleeg [Omgevingen voor twee keer wegschrijven loskoppelen en opnieuw koppelen](relink-environments.md) voor meer informatie.

## <a name="live-synchronization-issues-that-are-caused-by-incorrect-query-filter-syntax-on-the-dual-write-maps"></a>Problemen met live synchronisatie die worden veroorzaakt door een onjuiste syntax van het queryfilter op de toewijzingen voor twee keer wegschrijven

Hoewel de query-expressie voor een filter met toewijzing voor twee keer wegschrijven syntactisch correct is, werkt deze mogelijk niet zoals verwacht. De filterexpressie is op een entiteit en niet op een afzonderlijke gegevensbron van een queryobject. De SQL-query die wordt gegenereerd, retourneert daarom niet de verwachte resultaten.

Hier volgt een voorbeeld.

```dos
Query entity = PROJECTENTITY
Query expression = (ParentProject == "")
```

U zou kunnen verwachten dat projecten zonder bovenliggende gegevens worden uitgefilterd. Het filter werkt echter niet omdat het is vertaald naar een query die op het volgende voorbeeld lijkt.

```sql
SELECT T1.RECID,T1.MODIFIEDDATETIME,T1.RECVERSION,T1.RECID,T1.DIMENSION,
T1.LOCATION,T1.PROJECTCONTROLLER,T1.PROJECTID,T1.PROJECTMANAGER,T1.REFERENCE,
T1.SALESMANAGER,T1.SCHEDULED,T1.RECVERSION#8,T1.RECVERSION#7,
T1.RECVERSION#6,T1.RECVERSION#5,T1.RECVERSION#4,T1.RECVERSION#3,
T1.RECVERSION#2,T1.RECID#8,T1.RECID#7,T1.RECID#6,T1.RECID#5,
T1.RECID#4,T1.RECID#3,T1.RECID#2,T1.PARTITION FROM PROJECTENTITY T1 
WHERE(((((((((((PARTITION=5637144576) AND (DATAAREAID=N'usmf')) AND 
((PARTITION#2=5637144576) OR (PARTITION#2 IS NULL))) AND 
((PARTITION#3=5637144576) OR (PARTITION#3 IS NULL))) AND 
((PARTITION#4=5637144576) OR (PARTITION#4 IS NULL))) AND 
((PARTITION#5=5637144576) OR (PARTITION#5 IS NULL))) AND 
((PARTITION#6=5637144576) OR (PARTITION#6 IS NULL))) AND 
((PARTITION#7=5637144576) OR (PARTITION#7 IS NULL))) AND 
((PARTITION#8=5637144576) OR (PARTITION#8 IS NULL))) AND 
((DATAAREAID#8=N'usmf') OR (DATAAREAID#8 IS NULL))) AND 
(PARENTPROJECT='')) 
ORDER BY T1.PROJECTID
```

Het werkelijke resultaat is dat het veld `parentProject` wordt geëvalueerd naar `null`. Deze `null` is echter niet gelijk aan de lege tekenreeks. Vanwege deze mismatch retourneert het queryfilter geen geldige resultaten.

Volg deze stappen om het probleem op te lossen.

1. Voeg een berekende kolom toe die kan worden toegevoegd aan een uitbreidingsmodel en die wordt onderschreven door logica die `null` converteert naar de lege tekenreeks.

    ```dos
    SysComputedColumn::if(SysComputedColumn::isNullExpression(ParentProject), SysComputedColumn::returnLiteral(""), fieldName);
    ```

2. Gebruik het filter op de nieuwe berekende kolom in plaats van de standaardkolom.

Om het filter te beoordelen in een ontwikkelomgeving kunt u de volgende X++-code gebruiken om de resultaten te valideren. Voer deze code uit als zelfstandig programma. U kunt deze gebruiken om verschillende soorten filters te beoordelen die van toepassing zijn op een entiteit voordat u die filters gebruikt op toewijzingen voor twee keer wegschrijven. De query kan worden uitgevoerd op de database om afwijkingen te beoordelen.

```xpp
var entityName = "PROJECTENTITY";
var filterExpression = '(ParentProject == "")';
Query query = new Query();
query.literals(NoYes::Yes); 
QueryBuildDataSource qbd = query.addDataSource(tablename2id(entityName));
qbd.addRange(fieldname2id(qbd.table(),identifierStr(RecVersion))).value(filterExpression);
qbd.addSelectionField(fieldname2id(qbd.table(),identifierStr(RecId)));
QueryRun qRun = new QueryRun(query);
// This provides the actual sql statement to execute
var actualSqlStatement = query.getSQLStatement();
while(qRun.next())
{
    var rec = qRun.get(tableName2Id(entityName));
}
```

## <a name="data-from-finance-and-operations-apps-isnt-synced-to-dataverse"></a>Gegevens van Finance and Operations-apps worden niet gesynchroniseerd naar Dataverse

Tijdens live synchronisatie kan er een probleem optreden waarbij slechts een gedeelte van de gegevens wordt gesynchroniseerd tussen Finance and Operations-apps en Dataverse-apps of waarbij gegevens niet worden gesynchroniseerd.

> [!NOTE]
> Dit probleem moet in de ontwikkelfase worden verholpen.

Controleer de volgende vereisten voordat u het probleem gaat oplossen:

+ Zorg ervoor dat uw aangepaste wijzigingen in één transactiebereik worden geschreven.
+ Zakelijke gebeurtenissen en het framewerk voor twee keer wegschrijven verwerken `doinsert()`-, `doUpdate()`- en `recordset()`-bewerkingen of records waar `skipBusinessEvents(true)` is gemarkeerd, niet. Als uw code binnen deze functies valt, wordt het twee keer wegschrijven niet geactiveerd.
+ Zakelijke gebeurtenissen moeten worden geregistreerd voor de gegevensbron die is toegewezen. Sommige gegevensbronnen maken mogelijk gebruik van een outer join en kunnen gemarkeerd zijn als alleen-lezen in Finance and Operations-apps. Deze gegevensbronnen worden niet bijgehouden.
+ Wijzigingen worden alleen geactiveerd als de wijzigingen in de toegewezen velden staan. Wijzigingen aan niet-toegewezen velden zullen twee keer wegschrijven niet activeren.
+ Zorg ervoor dat filterevaluaties een geldig resultaat opleveren.

### <a name="troubleshooting-steps"></a>Stappen om problemen op te lossen

1. Veldtoewijzingen controleren op de beheerpagina voor twee keer afschrijven. Als een veld niet is toegewezen vanuit Finance and Operations-apps naar Dataverse, wordt het niet bijgehouden. In de volgende afbeelding wordt het veld **Omschrijving** bijvoorbeeld wel bijgehouden vanuit Dataverse, maar niet vanuit Finance and Operations-apps. Wijzigingen in dat veld in Finance and Operations-apps worden niet bijgehouden.

    ![Bijgehouden veld.](media/live-sync-troubleshooting-1.png)

2. Bepaal of de gegevensbron wordt bijgehouden in de definitie van zakelijke gebeurtenissen. In de volgende afbeelding wordt bijvoorbeeld geen veld uit de tabel **DefaultDimensionDAVs** en de onderliggende tabellen bijgehouden voor wijzigingen. Gegevensbronnen die een outer join gebruiken en die zijn gemarkeerd als alleen-lezen, worden niet bijgehouden.

    ![Veld dat niet wordt bijgehouden.](media/live-sync-troubleshooting-2.png)

3. Bepaal of de toegewezen tabelvelden verschijnen in de tabel **BUSINESSEVENTSDEFINITION**, zoals weergegeven in de volgende afbeelding. Als u het veld dat u zoekt niet in het queryresultaat vindt, wordt het niet geactiveerd door twee keer wegschrijven.

    ![Bijgehouden veld in de tabel.](media/live-sync-troubleshooting-3.png)

### <a name="sample-scenario"></a>Voorbeeldscenario

In Finance and Operations-apps wordt het adres van een contactpersoonrecord bijgewerkt, maar de adreswijziging wordt niet gesynchroniseerd naar Dataverse. Dit scenario treedt op omdat geen enkel record in de tabel **BusinessEventsDefinition** de combinatie van de betreffende tabel en de entiteit heeft. Met name de tabel **LogisticsPostalAddress** is niet de directe gegevensbron voor de entiteit **smmContactpersonCDSV2Entity**. De entiteit **smmContactpersonCDSV2Entity** heeft **smmContactPersonV2Entity** als de gegevensbron en **smmContactPersonV2Entity** heeft op zijn beurt **LogisticsPostalAddressBaseEntity** als gegevensbron. De tabel **LogisticsPostalAddress** is de gegevensbron voor **LogisticsPostalAddressBaseEntity**.

Een vergelijkbare situatie kan optreden in sommige niet-standaardpatronen, zoals gevallen waarin de tabel die wordt gewijzigd in Finance and Operations-apps niet duidelijk aan de entiteit is gekoppeld die de tabel bevat. De primaire adresgegevens worden bijvoorbeeld berekend in de entiteit **smmContactPersonCDSV2Entity**. Het framewerk voor twee keer schrijven probeert te bepalen hoe een wijziging in een onderliggende tabel weer wordt toegewezen aan entiteiten. Meestal is deze benadering voldoende. In sommige gevallen is de koppeling echter zo complex dat u specifiek moet zijn. U moet ervoor zorgen dat de **RecId** van de gerelateerde tabel rechtstreeks beschikbaar is voor de entiteit. Voeg vervolgens een statische methode toe om de tabel op wijzigingen te controleren.

Bekijk voor een voorbeeld de methode **smmContactPersonCDSV2Entity::getEntityDataSourceToFieldMapping()**. **CustCustomerV3entity** en **VendVendorV2Entity** zijn aangepast om deze situatie te verwerken.

Volg deze stappen om het probleem op te lossen.

1. Voeg een veld **PrimaryPostalAddressRecId** toe aan de entiteit **entiteit smmContactPersonV2Entity**. Maak het intern.

    ![Veld toegevoegd aan de entiteit smmContactPersonV2Entity.](media/Troubleshoot_live_sync_issue_1.png)

2. Veld toegevoegd aan de entiteit **smmContactPersonV2Entity**.

    ![Veld toegevoegd aan de entiteit smmContactPersonCDSV2Entity.](media/Troubleshoot_live_sync_issue_2.png)

3. Voeg de volgende methode toe aan de klasse **smmContactPersonCDSV2Entity**.

    ```xpp
    public static container getEntityDataSourceToFieldMapping(container mapping)
    {
        mapping += [[tablestr(smmContactPersonCDSV2Entity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)]];
        return mapping;
    }
    ```

4. Synchroniseer de database en maak een build van het programma.
5. Stop alle toewijzingen voor twee keer wegschrijven die zijn aangemaakt voor de entiteit **smmContactPersonCDSV2Entity**.
6. Start de toewijzing. U moet de nieuwe tabel (in dit voorbeeld **LogisticsPostalAddress**) bekijken die u bent begonnen bij te houden met behulp van de kolom **RefTableName** voor de rij waarin de waarde voor **refentityname** gelijk is aan **smmContactPersonCDSV2Entity** in de tabel **BusinessEventsDefinition**.

## <a name="error-when-you-create-a-record-where-multiple-records-are-sent-from-a-finance-and-operations-app-to-dataverse-in-the-same-batch"></a>Fout bij het aanmaken van een record waar meerdere records vanuit een Finance and Operations-app naar Dataverse worden verzonden in dezelfde batch

Voor elke transactie worden gegevens door een Finance and Operations-app aangemaakt in een batch, en die batch wordt naar Dataverse verzonden. Als er twee records worden aangemaakt als onderdeel van dezelfde transactie die naar elkaar verwijzen, wordt er mogelijk een foutbericht weergegeven dat op het volgende voorbeeld in de Finance and Operations-app lijkt:

*Kan geen gegevens naar de entiteit aaa_fundingsources schrijven. Kan geen ebecsfs_contracts opzoeken met de waarden {PC00...}. Kan geen aaa_fundingsources opzoeken met waarden {PC00...}. Schrijfopdrachten naar aaa_fundingsources mislukt met foutbericht Uitzonderingsbericht: De externe server heeft een foutmelding geretourneerd: (400) Ongeldige aanvraag*.

Om dit probleem op te lossen, maakt u relaties tussen entiteiten aan in de Finance and Operations-app om aan te geven dat de twee entiteiten aan elkaar gerelateerd zijn en dat de gerelateerde records in dezelfde transactie worden afgehandeld.

## <a name="enable-verbose-logging-of-error-messages"></a>Uitgebreide logboekregistratie van foutberichten inschakelen

In een Finance and Operations-app kunnen fouten optreden die gerelateerd zijn aan de Dataverse-omgeving. Het foutbericht bevat mogelijk niet de volledige tekst van het bericht of andere relevante gegevens. Als u meer informatie wilt, kunt u uitgebreide logboekregistratie inschakelen door de vlag **IsDebugMode** in te stellen die beschikbaar is voor de entiteit **DualWriteprojectConfigurationEntity** in alle projectconfiguraties in Finance and Operations-apps.

1. Open de entiteit **DualWriteProjectConfigurationEntity** met de Excel-invoegtoepassing. Als u de invoegtoepassing wilt gebruiken, moet u de ontwerpmodus in de Excel-invoegtoepassing van Finance and Operations inschakelen en de **DualWriteprojectConfigurationEntity** aan een werkblad toevoegen. Zie [Entiteitsgegevens weergeven en bijwerken met Excel](../../office-integration/use-excel-add-in.md) voor meer informatie.
2. Stel de vlag **IsDebugMode** in op **Ja** in het project.
3. Voer het scenario uit.
4. De uitgebreide logboeken zijn beschikbaar in de tabel **DualWriteErrorLog**. Als u gegevens wilt opzoeken met de tabelbrowser, gebruikt u de volgende URL: `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`.
5. Als u meer logboeken in wilt vastleggen in foutopsporingsmodus, installeer dan de update in [KB 4595434 (Oplossing voor lege waarden die worden doorgegeven in live synchronisatie voor twee keer wegschrijven)](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=c29ce15a80e6b3b4c01a722d9bdae1d7e71aa3662a044cfd0b765f736cfa98e9).

## <a name="error-when-you-add-an-address-for-a-customer-or-contact"></a>Foutmelding wanneer u een adres voor een klant of contactpersoon toevoegt

Mogelijk wordt het volgende foutbericht weergegeven wanneer u een adres voor een klant of contactpersoon probeert toe te voegen in Finance and Operations-apps of in Dataverse:

*Kan geen gegevens naar entiteit msdyn_partypostaladdresses schrijven. Schrijfopdrachten naar DirPartyPostalAddressLocationCDSEntity mislukt met foutbericht Aanvraag mislukt met statuscode BadRequest en CDS-foutcode: 0x80040265 antwoordbericht: Er is een fout opgetreden in de invoegroepassing. Er bestaat al een record met de kenmerkwaarden Locatie-ID. Voor de sleutel van de locatie-ID en die van de entiteit moet deze set kenmerken unieke waarden bevatten. Selecteer unieke waarden en probeer het opnieuw.*

Om het probleem op te lossen, installeert u de versie van het pakket voor indeling met twee keer wegschrijven versie (2.2.2.60), zodat de sleutels in de tabel **Adres** worden gedefinieerd zoals getoond in de volgende tabel.

| Eigenschap | Waarde |
|---|---|
| Weergavenaam | **Locatiesleutel** |
| Naam | **msdyn_locationkey** |
| Velden | **msdyn_locationid**, **parentid** |
| Status | **Actief** |
| Systeemtaak | Leeg |

## <a name="error-when-you-add-a-customer-in-dataverse"></a>Fout wanneer u een klant toevoegt in Dataverse

Mogelijk wordt het volgende foutbericht weergegeven wanneer u probeert een klant toe te voegen in Dataverse:

*'RecordError0': 'Schrijven mislukt voor entiteit Klanten V3 met onbekende uitzondering - Partijrecord niet gevonden voor partijtype 'Organisatie'}'.*

Wanneer er een klant wordt aangemaakt in Dataverse, wordt er een nieuw partijnummer gegenereerd. Het foutbericht wordt getoond wanneer de klantrecord samen met de partij wordt gesynchroniseerd naar Finance and Operations-apps, maar er al een klantrecord bestaat met een ander partijnummer.

Om het probleem op te lossen, kan de klant worden opgezocht via een zoekactie op partij. Als de klant niet bestaat, maak dan een nieuwe klantrecord aan. Als de klant wel bestaat, gebruik dan de bestaande partij om de nieuwe klantrecord aan te maken.

## <a name="error-when-you-create-a-new-customer-vendor-or-contact-in-dataverse"></a>Foutmelding wanneer u een nieuwe klant, leverancier of contactpersoon aanmaakt in Dataverse

Mogelijk wordt het volgende foutbericht weergegeven wanneer u een nieuwe klant, leverancier of contactpersoon probeert aan te maken in Dataverse

*Kan het type van een partij niet bijwerken van 'DirOrganization' naar 'DirPerson'; in plaats daarvan moet de bestaande partij worden verwijderd, gevolgd door het uitvoeren van een invoegactie met het nieuwe type.*

In Dataverse is er een nummerreeks op de tabel **msdyn_party**. Wanneer er een account wordt aangemaakt in Dataverse, wordt er een nieuwe partij aangemaakt (bijvoorbeeld **Partij-001** van het type **Organisatie**). Deze gegevens worden naar de Finance and Operations-app verzonden. Als de Dataverse-omgeving opnieuw wordt ingesteld of de Finance and Operations-omgeving aan een andere Dataverse-omgeving wordt gekoppeld en er vervolgens een nieuwe contactpersoonrecord wordt aangemaakt in Dataverse, wordt er een nieuwe partijwaarde gemaakt die begint met **Partij-001**. Dit keer is de partijrecord die wordt aangemaakt **Partij-001** van het type **Persoon**. Wanneer deze gegevens worden gesynchroniseerd, tonen Finance and Operations-apps het voorgaande foutbericht, omdat partijrecord **Partij-001** van het type **Organisatie** al bestaat.

Om het probleem op te lossen, wijzigt u de automatische nummerreeks voor het veld **msdyn_partynumber** van de tabel **msdyn_party** in Dataverse naar een andere automatische nummerreeks.

## <a name="performance-issue-with-customer-or-contact-mappings"></a>Prestatieprobleem bij toewijzingen klant of contactpersoon

Mogelijk kunt u de prestaties van live synchronisatie voor klanten en contactpersonen marginaal verbeteren door de methode **getEntityDataSourceToFieldMapping** (in de entiteit **CustCustomerV3Entity**) en de methode **getEntityDataSourceToFieldMapping** (in de entiteit **smmContactPersonCDSV2Entity**) aan te passen. Door deze aanpassingen wordt het aantal records in de tabel **BusinessEventsDefinition** beperkt. Door deze afname van het aantal records neemt het aantal gebeurtenissen dat wordt gegenereerd ook af.

De methode **getEntityDataSourceToFieldMapping** in de entiteit **CustCustomerV3Entity** zorgt ervoor dat een update van het elektronische adres of postadres van de klant zakelijke gebeurtenissen activeert, zodat de bijgewerkte gegevens naar Dataverse worden verzonden. Als u niet alle velden gebruikt en de informatie bij twee keer wegschrijven niet nodig hebt, maakt u van de betreffende regels in de methode een commentaar. Elk(e) bij te houden veld en tabel die wordt toegevoegd in deze methode, voegt een record toe in de tabel **BusinessEventsDefinition** voor de combinatie van de bijgehouden tabel en de bijgehouden entiteit.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, AddressRecordId)],
        [identifierstr(DirPartyBaseEntity), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactURLRecordId)],
        [identifierstr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactPhoneRecordId)],
        [identifierstr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactEmailRecordId)],
        [identifierstr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(CustCustomerV3Entity, PrimaryContactFaxRecordId)],
        [identifierstr(DirPartyBaseEntity4), tablenum(DirPartyLocation), fieldstr(CustCustomerV3Entity, DirPartyLocationRecordId)],
        [identifierstr(DirPartyBaseEntity5), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, InvoiceAddressRecordId)],
        [identifierstr(DirPartyBaseEntity6), tablenum(LogisticsPostalAddress), fieldstr(CustCustomerV3Entity, DeliveryAddressRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(DirPartyTable), fieldstr(CustCustomerV3Entity, PartyRecordId)]];
    return mapping;
}
```

Op vergelijkbare wijze zorgt de methode **getEntityDataSourceToFieldMapping** in de entiteit **smmContactPersonCDSV2Entity** ervoor dat elke update van het elektronische adres of postadres van de contactpersoon zakelijke gebeurtenissen activeert, zodat de bijgewerkte gegevens naar Dataverse worden verzonden. In de methode kunt u alle regels voor velden die u niet gebruikt, omzetten naar commentaar.

```xpp
public static container getEntityDataSourceToFieldMapping(container mapping)
{
    mapping += [
        [tablestr(DirPartyBaseEntity), tablenum(LogisticsPostalAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryPostalAddressRecId)],
        [identifierStr(DirPartyBaseEntity), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PrimaryAddressLocation)],
        [identifierStr(DirPartyBaseEntity1), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactEmailRecordId)],
        [identifierStr(DirPartyBaseEntity2), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFaxRecordId)],
        [identifierStr(DirPartyBaseEntity3), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactPhoneRecordId)],
        [identifierStr(DirPartyBaseEntity4), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactFacebookRecordId)],
        [identifierStr(DirPartyBaseEntity5), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTwitterRecordId)],
        [identifierStr(DirPartyBaseEntity6), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactURLRecordId)],
        [identifierStr(DirPartyBaseEntity7), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactLinkedInRecordId)],
        [identifierStr(DirPartyBaseEntity8), tablenum(LogisticsElectronicAddress), fieldstr(smmContactPersonCDSV2Entity, PrimaryContactTelexRecordId)],
        [identifierStr(DirPartyBaseEntity9), tablenum(DirPartyTable), fieldstr(smmContactPersonCDSV2Entity, PartyRecordId)]];
    return mapping;
}
```

Volg deze stappen nadat u de methoden hebt bijgewerkt.

1. Synchroniseer de database en maak een build van het programma.
2. Stop alle toewijzingen voor twee keer wegschrijven die zijn aangemaakt voor de entiteiten **smmContactPersonCDSV2Entity** en **CustCustomerV3Entity**.
3. Start de toewijzingen. U hoort minder records te zien in de entiteiten **smmContactPersonCDSV2Entity** en **CustCustomerV3Entity** en de tabel **BusinessEventsDefinition** en de prestaties kunnen marginaal verbeteren.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
