---
title: Grootschalige implementatie van verzegelde Commerce-selfservicecomponenten
description: In dit artikel wordt uitgelegd hoe u het framework voor installatieprogramma's voor selfservicecomponenten kunt gebruiken om implementaties op de achtergrond te installeren en te onderhouden.
author: jashanno
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: jashanno
ms.search.validFrom: 2021-04-30
ms.openlocfilehash: 426473c14cdf9e171810aafd97dbb1afd5988b2f
ms.sourcegitcommit: 24673493d14f2045a08fe7240689bee34e099cb5
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2022
ms.locfileid: "9589084"
---
# <a name="mass-deployment-of-sealed-commerce-self-service-components"></a>Grootschalige implementatie van verzegelde Commerce-selfservicecomponenten

[!include [banner](../includes/banner.md)]

Dit artikel is van toepassing op de installatieprogramma's voor componenten van het verzegelde framework die elke maand worden uitgebracht, vanaf release 10.0.18, en beschikbaar worden gemaakt in de bibliotheek voor deze gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS). De eerste versies van deze nieuwe installatieprogramma's worden aangeduid als **(preview)**. Deze aanduiding is echter alleen bedoeld om onderscheid te maken tussen de nieuwe installatieprogramma's terwijl Microsoft bepaalt of er extra functionele vereisten zijn om deze te gebruiken. Dit betekent niet dat de installatieprogramma's niet geldig zijn voor productie. Op basis van de release van deze nieuwe installatieprogramma's is Microsoft van plan om de oude (verouderde) installatieprogramma's in of rond oktober 2023 af te schaffen. 

In dit artikel wordt uitgelegd hoe u de nieuwe installatieprogramma's kunt gebruiken om via opdrachtregelargumenten installatie- en onderhoudsupdates uit te voeren op de achtergrond. Met deze argumenten kunt u massale implementaties op verschillende manieren uitvoeren.

> [!NOTE]
> De nieuwe verzegelde selfservice installatieprogramma's worden niet beschikbaar gemaakt in Headquarters en kunnen alleen worden gedownload via LCS.

## <a name="delimiters-for-mass-deployment"></a>Scheidingstekens voor massale implementaties

De volgende tabel toont de scheidingstekens die bij de uitvoering van de opdrachtregel kunnen worden gebruikt.


| Scheidingsteken                 | Description |
|---------------------------|-------------|
| -AadTokenIssuerPrefix | Het voorvoegsel voor de uitgever van de Microsoft Azure Active Directory-token (Azure AD). |
| -AsyncClientAadClientId | De Azure AD-client-id die Async Cient moet gebruiken tijdens de communicatie met Headquarters. |
| -AsyncClientAppInsightsInstrumentationKey | De AppInsights-instrumentatiesleutel van Async Client. |
| -AsyncClientCertFullPath | Het volledig ingedeelde URN-pad dat de vingerafdruk gebruikt als de zoekmetriek van de locatie van het Async Client-identiteitscertificaat dat moet worden gebruikt voor verificatie met Azure AD voor communicatie met Headquarters. `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` is bijvoorbeeld een correct ingedeelde URN. De waarde **\<MyThumbprint\>** wordt vervangen door de vingerafdruk van het certificaat dat moet worden gebruikt. Gebruik deze parameter niet samen met de parameter **-AsyncClientCertThumbprint**. |
| -AsyncClientCertThumbprint | De vingerafdruk van het Async Client-identiteitscertificaat dat moet worden gebruikt voor verificatie met Azure AD voor de communicatie met Headquarters. Deze vingerafdruk wordt gebruikt om te zoeken in de locatie en naam **LocalMachine/My store** om het juiste certificaat te zoeken dat moet worden gebruikt. Gebruik deze parameter niet samen met de parameter **-AsyncClientCertFullPath**. |
| -ClientAppInsightsInstrumentationKey | De AppInsights-instrumentatiesleutel van Client. |
| -CloudPosAppInsightsInstrumentationKey | De AppInsights-instrumentatiesleutel van Cloud POS. |
| -Config | Het configuratiebestand dat tijdens de installatie moet worden gebruikt. Een voorbeeld van een bestandsnaam is **Contoso.CommerceScaleUnit.xml**. |
| -CposAadClientId | De Azure AD-client-id die Cloud POS moet gebruiken tijdens het activeren van het apparaat. Deze parameter is niet vereist voor on-premises implementaties. |
| -Device | De apparaat-id, zoals weergegeven op de pagina **Apparaten** in Headquarters. |
| -EnvironmentId | De omgevings-id. |
| -HardwareStationAppInsightsInstrumentationKey | De AppInsights-instrumentatiesleutel voor Hardware Station. |
| Installeren | Een parameter waarmee wordt opgegeven of het onderdeel dat door dit installatieprogramma wordt geleverd, moet worden geïnstalleerd. Deze parameter is vereist voor het uitvoeren van een installatie en heeft geen voorloopstreepje. |
| -InstallOffline | Voor Modern POS geeft deze parameter aan dat ook de offline database moet worden geïnstalleerd en geconfigureerd. Gebruik ook de parameter **-SQLServerName**. Anders probeert het installatieprogramma een standaardexemplaar te zoeken dat aan de vereisten voldoet. Wanneer u Azure Active Directory-verificatie (Azure AD) gebruikt, werkt POS offline niet. Er is namelijk altijd online connectiviteit vereist. |
| -Port | De poort die moet worden gekoppeld aan en gebruikt door de virtuele Retail Server-map. Als geen poort is ingesteld, wordt de standaardpoort 443 gebruikt. |
| -Register | De register-id, zoals weergegeven op de pagina **Registers** in Headquarters. |
| -RetailServerAadClientId | De Azure AD-client-id die Retail Server moet gebruiken tijdens de communicatie met Headquarters. |
| -RetailServerAadResourceId | De resource-id van de Azure AD-app voor Retail Server die tijdens het activeren van het apparaat moet worden gebruikt. Deze parameter is niet vereist voor on-premises implementaties. |
| -RetailServerCertFullPath | Het volledig ingedeelde URN-pad dat de vingerafdruk gebruikt als de zoekmetriek van het Retail Server-identiteitscertificaat dat moet worden gebruikt voor verificatie met Azure AD voor communicatie met Headquarters. `store://My/LocalMachine?FindByThumbprint=<MyThumbprint>` is bijvoorbeeld een correct ingedeelde URN waarbij de waarde **\<MyThumbprint\>** wordt vervangen door de vingerafdruk van het certificaat die moet worden gebruikt. Gebruik deze parameter niet samen met de parameter **-RetailServerCertThumbprint**. |
| -RetailServerCertThumbprint | De vingerafdruk van het Retail Server-identiteitscertificaat dat moet worden gebruikt voor verificatie met Azure AD voor de communicatie met Headquarters. Deze vingerafdruk wordt gebruikt om te zoeken in de winkellocatie en -naam **LocalMachine/My** om het juiste certificaat te zoeken dat moet worden gebruikt. Gebruik deze parameter niet samen met de parameter **-RetailServerCertFullPath**. |
| -RetailServerURL | De Retail Server-URL die door het installatieprogramma moet worden gebruikt. (Deze URL wordt ook wel de \[CSU-URL\] (Commerce Scale Unit) genoemd.) In Modern POS wordt deze waarde gebruikt tijdens het activeren van het apparaat. |
| -SkipAadCredentialsCheck| Een schakeloptie die aangeeft of de controles van de vereiste voor Azure AD-referenties moeten worden overgeslagen. De standaardwaarde is **onwaar**. |
| -SkipCertCheck | Een schakeloptie die aangeeft of de controles van de certificaatvereiste moeten worden overgeslagen. De standaardwaarde is **onwaar**. |
| -SkipIisCheck | Een schakeloptie die aangeeft of de controles van de IIS-vereiste (Internet Information Services) moeten worden overgeslagen. De standaardwaarde is **onwaar**. |
| -SkipNetFrameworkCheck | Een schakeloptie die aangeeft of de controles van de .NET Framework-vereiste moeten worden overgeslagen. De standaardwaarde is **onwaar**. |
| -SkipScaleUnitHealthcheck | Een schakeloptie die aangeeft of de statuscontrole voor geïnstalleerde onderdelen moet worden overgeslagen. De standaardwaarde is **onwaar**. |
| -SkipSChannelCheck | Een schakeloptie die aangeeft of de controles van de vereiste voor veilige kanalen moeten worden overgeslagen. De standaardwaarde is **onwaar**. |
| -SkipSqlFullTextCheck | Een schakelknop die aangeeft of de validatie van de SQL Server-vereiste die Zoeken in volledige tekst vereist, moet worden overgeslagen. De standaardwaarde is **onwaar**. |
| -SkipSqlServerCheck | Een schakeloptie die aangeeft of de controles van de SQL Server-vereiste moeten worden overgeslagen. De standaardwaarde is **onwaar**. |
| -SqlServerName | De SQL Server-naam. Als de naam niet wordt opgegeven, probeert het installatieprogramma het standaardexemplaar te vinden. |
| -SslcertFullPath | Het volledig ingedeelde URN-pad dat de vingerafdruk gebruikt als de zoekmetriek van de certificaatlocatie die moet worden gebruikt om HTTP-verkeer na de schaaleenheid te versleutelen. `store:\/\/My\/LocalMachine\?FindByThumbprint\=\<MyThumbprint\>` is bijvoorbeeld een correct ingedeelde URN waarbij de waarde **\<MyThumbprint\>** wordt vervangen door de de vingerafdruk van het certificaat die moet worden gebruikt. Gebruik deze parameter niet samen met de parameter **-SslCertThumbprint**. |
| -SslCertThumbprint | De vingerafdruk van het certificaat dat moet worden gebruikt voor het versleutelen van HTTP-verkeer naar de schaaleenheid. Deze vingerafdruk wordt gebruikt om te zoeken in de locatie en naam **LocalMachine/My store** om het juiste certificaat te zoeken dat moet worden gebruikt. Gebruik deze parameter niet samen met de parameter **-SslCertFullPath**. |
| -StoreSystemAosUrl | De URL van Headquarters (AOS). |
| -StoreSystemChannelDatabaseId | De afzetkanaaldatabase-id (naam). |
| -TenantId | De id van de Azure AD-tenant. |
| -TransactionServiceAzureAuthority | De Azure AD-autoriteit voor Transaction Service. |
| -TransactionServiceAzureResource | De Azure AD-resource voor Transaction Service. |
| -TrustSqlServerCertificate | Een schakeloptie die aangeeft of het Server-certificaat moet worden vertrouwd terwijl er een verbinding met SQL Server tot stand wordt gebracht. Om beveiligingsrisico's te voorkomen, moeten productie-implementaties hier nooit de waarde **true** leveren. De standaardwaarde is **onwaar**. |
| -Verbosity | Het logboekregistratieniveau dat tijdens de installatie wordt aangevraagd. Normaal gesproken moet deze waarde niet worden gebruikt. |
| -WindowsPhoneAppInsightsInstrumentationKey | De AppInsights-instrumentatiesleutel voor Hardware Station. |

## <a name="general-overview"></a>Algemeen overzicht

Het nieuwe raamwerk voor installatieprogramma's voor selfservice bevat diverse functies en verbeteringen. Het nieuwe raamwerk genereert momenteel uitsluitend installatieprogramma's voor Modern POS, Hardware Station en CSU (zelfgehost). Het is belangrijk om inzicht te krijgen in het basisgebruik van de opdrachtregel voor de verzegelde installatieprogramma's. Deze moet er ongeveer zo uitzien als in het volgende voorbeeld. 
 
```Console
<Component Installer Name>.exe install -<Parameter Name> "<Parameter Information>"
```

Het installatieprogramma vereist de parameter **install** (of **uninstall** om de installatie te verwijderen) en de parameters die specifiek zijn voor die installatie. **Parameternaam** moet alle benodigde parameters bevatten, zoals de kassa-, CSU-URL- of certificaatgegevens. **Parameterinformatie** moet eventuele extra informatie over de parameters bevatten.

Het verzegelde raamwerk is gemaakt om de volgende wijzigingen mogelijk te maken:
- **Verzegeld**: het nieuwe raamwerk voor installatieprogramma's scheidt door Microsoft gedistribueerde installatieprogramma's voor basisonderdelen van de op uitbreidbaarheid gebaseerde aanpassingen. De aanpassingen worden daarna geïnstalleerd, maar zijn vervolgens ongebonden ten aanzien van updates (zodat updates alleen voor het Microsoft-basisonderdeel zijn toegestaan, alleen voor de aanpassingen of voor beide).
- **Zonder GUI** : er is geen gebruikersinterface meer. In plaats daarvan is er voor elk installatieprogramma voor onderdelen een volledig opdrachtregelgestuurd uitvoerbaar bestand. Deze wijziging is een van de belangrijkste wijzigingen of functies die worden gebruikt om het nieuwe raamwerk voor installatieprogramma's te gebruiken voor massale implementaties.
- **Uitgebreide logboekregistratie**: verbeterde logboeken voor installatieprogramma's zorgen voor een betere validatie van de voltooiing of mislukking van de installatie, de uitgevoerde stappen en eventuele waarschuwingen of fouten die zijn gegenereerd.
- **Opschonen**: in het nieuwe raamwerk werken de installatieprogramma's voor onderdelen harder om de installatiemappen opgeruimd te houden, door de volledige inhoud van de onderdeelmap leeg te maken voordat de nieuwere onderdelen worden geïnstalleerd. Door deze opschoningen blijven er geen restbestanden over die problemen kunnen veroorzaken en installaties kunnen voorkomen.

Drie onderdelen zijn niet naar het nieuwe raamwerk gemigreerd: de virtuele randapparatuursimulator, Async Server Connector Service (die wordt gebruikt voor ondersteuning voor Dynamics AX 2012 R3) en de realtime servicevervanging (die wordt gebruikt voor ondersteuning van Dynamics AX 2012 R3).

> [!NOTE]
> Installatieprogramma's worden lokaal opgeslagen en bewaard.  Het is belangrijk om na verloop van tijd de behouden installatieprogramma's te beheren of te verwijderen om geen schijfruimte te verspillen. Het wordt aangeraden het huidige installatieprogramma voor de basisonderdelen en de installatieprogramma's voor uitbreidingen voor de laatste versies te behouden met het oog op herstel vanuit extreme situaties.

## <a name="migration"></a>Migratie

Voor de migratie van het oude framewerk voor installatieprogramma's voor selfservicecomponenten naar het nieuwe framework moeten de oude onderdelen eerst worden verwijderd.

- **Modern POS**: door het nieuwe framework voor installatieprogramma's heeft de toepassing een nieuwe toepassingshandtekening-id ontvangen. Oude onderdelen moeten daarom volledig worden verwijderd voordat het Modern POS-onderdeel van het nieuwe framework wordt geïnstalleerd. Omdat volledige verwijdering vereist is, moet het apparaat opnieuw worden geactiveerd. (Deze apparaatheractivering is een eenmalige vereiste, mits de installatie niet opnieuw wordt verwijderd.)
- **Hardware Station**: als een IIS-website vereist het nieuwe framework voor installatieprogramma's dat de basismapstructuur wordt bijgewerkt. Oude onderdelen moeten daarom volledig worden verwijderd voordat het onderdeel Hardware Station van het nieuwe framework wordt geïnstalleerd.
- **Commerce Scale Unit (CSU, zelfgehost)** – Als een reeks IIS-websites vereist het nieuwe framework voor installatieprogramma's dat de basismapstructuur wordt bijgewerkt.  Oude onderdelen moeten daarom volledig worden verwijderd voordat het CSU-onderdeel (zelfgehost) van het nieuwe framework wordt geïnstalleerd.

## <a name="modern-pos"></a>Modern POS

### <a name="before-you-begin"></a>Voordat u begint

Het is van groot belang dat u het oude, selfservice Modern POS-onderdeel verwijdert. Zie de migratiestappen eerder in dit artikel voor meer informatie.

> [!NOTE]
> Op een systeem met één computer, zoals een ontwikkelaarstopologie of een demonstratieomgeving, of wanneer Commerce Scale Unit en Modern POS op dezelfde computer zijn geïnstalleerd, kan Store Commerce mogelijk niet de activering van het apparaat voltooien. Dit probleem treedt op omdat Store Commerce geen netwerkoproepen kan uitvoeren op dezelfde computer (dat wil zeggen oproepen naar zichzelf). Hoewel dit nooit een scenario moet zijn in een productie-opstelling, kan het probleem worden beperkt door een uitzondering in een AppContainer loopback-uitzondering in te schakelen, zodat communicatie op dezelfde computer kan plaatsvinden. Verschillende toepassingen zijn openbaar beschikbaar om deze loopback mogelijk te maken. Zie [Loopback inschakelen en netwerkisolatieproblemen oplossen](/previous-versions/windows/apps/hh780593(v=win.10)) voor meer informatie over loopback. Het is belangrijk te begrijpen dat een loopback een veiligheidsrisico kan inhouden, dus het is niet aan te raden een loopback te gebruiken, tenzij het absoluut noodzakelijk is.

### <a name="examples-of-silent-deployment"></a>Voorbeelden van installatie op de achtergrond

In deze sectie worden voorbeelden gegeven van opdrachten die worden gebruikt om Modern POS te installeren.

#### <a name="silently-install-modern-pos"></a>Modern POS op de achtergrond installeren

Met de volgende opdracht wordt Modern POS op de achtergrond geïnstalleerd (of bijgewerkt). De opdracht heeft de standaardopdrachtstructuur die wordt gebruikt voor het op de achtergrond uitvoeren van onderhoud voor onderdelen die momenteel zijn geïnstalleerd. De structuur gebruikt de basiswaarden van **&lt;InstallerName.exe&gt;**.

Met de volgende basisopdracht worden de beschikbare opties weergegeven als om een installatie wordt gevraagd. Het wordt sterk aangeraden deze opdracht te gebruiken wanneer u het installatieprogramma voor het eerst test of gebruikt.

```Console
CommerceModernPOS.exe -help install
```

> [!NOTE]
> Een configuratiebestand is niet vereist voor Modern POS. Het installatieprogramma heeft nu parameters (eerder in dit artikel weergegeven) voor de verschillende waarden die tijdens het activeren van het apparaat worden gebruikt.

Met de volgende opdracht worden alle parameters opgegeven die moeten worden gebruikt tijdens het activeren van apparaten nadat de toepassing Modern POS is geïnstalleerd. In dit voorbeeld wordt gebruikgemaakt van het register **Houston-3**, dat veel wordt gebruikt in Dynamics 365 Commerce-demonstratiegegevens.

```Console
CommerceModernPOS.exe install -Register "Houston-3" -Device "Houston-3" -RetailServerURL "https://MyDynamics365CommerceURL.dynamics.com/Commerce"
```

Met de volgende opdracht geeft u de parameters op die moeten worden gebruikt om de offline database te installeren en te configureren. De SQL Server wordt samen met het configuratiebestand opgegeven dat moet worden gebruikt.

```Console
CommerceModernPOS.exe install -InstallOffline -SQLServerName "SQLExpress" -Config "ModernPOS.Houston-3.xml"
```

U kunt deze concepten combineren om de gewenste installatieresultaten te bereiken.

## <a name="hardware-station"></a>Hardwarestation

### <a name="before-you-begin"></a>Voordat u begint

Het is van groot belang dat u het oude, selfservice onderdeel Hardware Station verwijdert. Zie de migratiestappen eerder in dit artikel voor meer informatie. Er is geen hulpmiddel voor verkopersrekeninggegevens meer. In plaats daarvan worden de verkopersrekeninggegevens geïnstalleerd wanneer een POS-terminal aan Hardware Station wordt gekoppeld. Het wordt sterk aangeraden de volgende opdracht te gebruiken wanneer u dit installatieprogramma voor het eerst test:

```Console
CommerceHardwareStation.exe -help install
```

### <a name="examples-of-silent-deployment"></a>Voorbeelden van installatie op de achtergrond

In deze sectie worden voorbeelden gegeven van opdrachten die worden gebruikt om Hardware Station te installeren.

#### <a name="silently-install-hardware-station"></a>Hardware Station op de achtergrond installeren

Met de volgende opdracht wordt Hardware Station op de achtergrond geïnstalleerd (of bijgewerkt). De opdracht heeft de standaardopdrachtstructuur die wordt gebruikt voor het uitvoeren van onderhoud voor onderdelen die momenteel zijn geïnstalleerd. De structuur gebruikt de basiswaarden van **&lt;InstallerName.exe&gt;**.

Met de volgende basisopdracht wordt het installatieprogramma voor de uitvoerbare bestanden uitgevoerd.

```Console
HardwareStation.exe install -Port 443 -StoreSystemAOSURL "https://MyDynamics365CommerceURL.dynamics.com/" -StoreSystemChannelDatabaseID "Houston" -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers"
```

> [!NOTE]
> Een configuratiebestand is niet vereist voor Hardware Station. Het installatieprogramma heeft nu parameters (eerder in dit artikel weergegeven) voor de verschillende waarden die vereist zijn.

Met de volgende opdracht worden alle parameters opgegeven die nodig zijn om de vereiste controles tijdens een standaardinstallatie over te slaan. 

> [!NOTE]
> Het is niet raadzaam om controles over te slaan zonder deze van te voren grondig of in ontwikkelsituaties te testen.

```Console
HardwareStation.exe install -SkipFirewallUpdate -SkipOPOSCheck -SkipVersionCheck -SkipURLCheck -Config "HardwareStation.Houston.xml"
```

Zoals gewoonlijk kunt u deze concepten combineren om de gewenste installatieresultaten te bereiken.

## <a name="commerce-scale-unit-self-hosted"></a>Commerce Scale Unit (zelfgehost)

Het wordt sterk aangeraden de volgende opdracht te gebruiken wanneer u dit installatieprogramma voor het eerst test:

```Console
CommerceStoreScaleUnitSetup.exe -help install
```

### <a name="before-you-begin"></a>Voordat u begint

Het is van groot belang dat u het oude, selfservice onderdeel CSU (zelfgehost) verwijdert. Zie de migratiestappen eerder in dit artikel voor meer informatie.

### <a name="examples-of-silent-deployment"></a>Voorbeelden van installatie op de achtergrond

In deze sectie worden voorbeelden gegeven van opdrachten die worden gebruikt om CSU (zelfgehost) te installeren.

#### <a name="silently-install-csu-self-hosted"></a>CSU (zelfgehost) op de achtergrond installeren

Met de volgende opdracht wordt CSU (zelfgehost) op de achtergrond geïnstalleerd (of bijgewerkt). De opdracht heeft de standaardopdrachtstructuur die wordt gebruikt voor het op de achtergrond uitvoeren van onderhoud voor onderdelen die momenteel zijn geïnstalleerd. De structuur gebruikt de basiswaarden van **&lt;InstallerName.exe&gt;**.

Vergeleken met de andere selfservice installatieprogramma's is CSU (Commerce Scale Unit) ingewikkelder en moet u vrij veel extra gegevens opgeven. De volgende opdracht is de minimumopdracht (met parameters) die nodig is om het installatieprogramma voor uitvoerbare bestanden uit te voeren als geen configuratiebestand aanwezig is.

```Console
CommerceScaleUnit.exe install -port 446 -SSLCertThumbprint "MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Config "Contoso.StoreSystemSetup.xml"
```

> [!NOTE]
> Voor CSU (zelfgehost) is nog steeds een configuratiebestand vereist.

De volgende opdracht is een grondigere opdracht waarmee het installatieprogramma voor uitvoerbare bestanden met enkele alternatieve parameters wordt uitgevoerd.

```Console
CommerceScaleUnit.exe install -Port 446 -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate -Verbosity 0 -Config "Contoso.StoreSystemSetup.xml"
```

Met de volgende opdracht worden parameters opgegeven die nodig zijn om de vereiste controles tijdens een standaardinstallatie over te slaan. 

> [!NOTE]
> Het is niet raadzaam om controles over te slaan zonder deze van te voren grondig of in ontwikkelsituaties te testen.


```Console
CommerceScaleUnit.exe installer -skipscaleunithealthcheck -skipcertcheck -skipaadcredentialscheck -skipschannelcheck -skipiischeck -skipnetcorebundlecheck -skipsqlservercheck -skipnetframeworkcheck -skipversioncheck -skipurlcheck -Config "Contoso.StoreSystemSetup.xml" -SSLCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -AsyncClientCertFullPath "store://My/LocalMachine?FindByThumbprint=MySSLCertificateThumbprintOftenHasNumbers" -RetailServerCertFullPath "store://My/LocalMachine?FindByThumbprint=MyCertificateThumbprintUsedByRetailServer" -AsyncClientAADClientID "MyAAD-Client-IDFor-AsyncClient" -RetailServerAADClientID "MyAAD-Client-IDFor-RetailServer" -CPOSAADClientID "MyAAD-Client-IDFor-CloudPOS" -RetailServerAADResourceID "https://retailstorescaleunit.retailserver.com" -TrustSqlServerCertificate
```

U kunt deze concepten combineren om de gewenste installatieresultaten te bereiken.

<!--## Mass deployment examples using InTune

This section will be added in a future update.

## Mass deployment examples using System Center Configuration Manager (SCCM)

This section will be added in a future update.-->

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
