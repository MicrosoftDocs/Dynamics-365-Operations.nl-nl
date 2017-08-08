---
title: On-premises omgevingen instellen en implementeren
description: Dit onderwerp bevat informatie over het plannen, instellen en implementeren van een on-premises omgeving.
author: kfend
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3e9a2e33d9579769f6808b598f865d75f072c450
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>On-premises omgevingen instellen en implementeren

In dit document wordt beschreven hoe uw implementatie plant, de infrastructuur instelt en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) implementeert.

## <a name="finance-and-operations-components"></a>Componenten Finance and Operations

De toepassing Finance and Operations bestaat uit drie hoofdonderdelen:

- AOS (Application Object Server)
- Business Intelligence (BI)
- Financiële rapportage/Management Reporter

Deze onderdelen zijn afhankelijk van de volgende systeemsoftware:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1, dat de volgende functies omvat:

    - Zoeken in volledige-tekstindex is ingeschakeld.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > De toepassing wordt niet uitgevoerd als Zoekopdracht in volledige tekst niet is ingeschakeld.

- SQL Server Management Studio
- Standalone Microsoft Azure Service Fabric
- Windows PowerShell 5.0 of hoger
- Active Directory Federation Services (AD FS) op Windows Server 2016

  De domeincontroller moet Windows Server 2012 R2 of hoger zijn met een domeinfunctionaliteitsniveau van 2012 R2 of hoger

  Voor meer informatie over niveaus voor domeinfunctionaliteit zie: 
  - [Wat zijn functionele niveaus in Active Directory](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Inzicht in functionele niveaus voor Active Directory Domain Services](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

De onderdelen voor Finance and Operations worden gedistribueerd via Microsoft Dynamics Lifecycle Services (LCS). Voordat u deze kunt implementeren, moet u licentiesleutels aanschaffen via het kanaal voor [Enterprise-overeenkomsten](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx) en een on-premises project in LCS instellen. Implementaties kunnen alleen via LCS worden gestart. Zie voor meer informatie over het instellen van on-premises projecten in LCS [Een on-premises project maken in Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Authenticatie

De on-premises toepassing werkt met AD FS. Voor interactie met LCS moet u ook Azure Active Directory (Azure AD) configureren.

## <a name="standalone-service-fabric"></a>Standalone Service Fabric

Finance and Operations gebruikt Standalone Service Fabric. Raadpleeg de documentatie bij [Service Fabric voor meer informatie](/azure/service-fabric/).

## <a name="infrastructure"></a>Infrastructuur

Finance and Operations is ontworpen om te werken met een hyper-geconvergeerde architectuur. De hardwareconfiguratie bevat de volgende onderdelen:

- Standalone Service Fabric-cluster die is gebaseerd op Windows Server 2016-virtuele machines (VM's)
- SQL Server (zowel Clustered SQL en Always-On worden ondersteund)
- AD FS voor verificatie
- Server Message Block (SMB) versie 3 bestandsshare voor opslag
- Optioneel: Microsoft Office Server 2017

Zie voor meer informatie [Systeemvereisten](../get-started/system-requirements.md) en richtlijnen voor licentieomvang.

### <a name="hardware-layout"></a>Hardware-indeling

Plan uw infrastructuur en het Service Fabric-cluster, op basis van het aanbevolen formaat in [Grootte van de hardware voor on-premises omgevingen vaststellen](../get-started/hardware-sizing-on-premises-environments.md). Zie voor meer informatie over het plannen van het Service Fabric-cluster [Implementatie van Service Fabric-cluster plannen en voorbereiden](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

De tabel hieronder geeft een voorbeeld van de hardware-indeling. Dit voorbeeld wordt steeds gebruikt in dit onderwerp ter illustratie van de instellingen.

> [!NOTE]
> Het primaire knooppunt van het Service Fabric-cluster moet ten minste drie knooppunten hebben. In dit voorbeeld wordt **OrchestratorType** aangewezen als het primaire knooppunttype.

| Doel van de machine                                 | Machinenaam    | IP-adres    |
|-------------------------------------------------|-----------------|---------------|
| Domeincontroller                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Bestandsserver                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On-cluster                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Klant                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric-cluster/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric-cluster/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric-cluster/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric-cluster/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric-cluster/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric-cluster/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric-cluster/Management Reporter-knooppunt | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric-cluster/SSRS-knooppunt                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Instelling

### <a name="prerequisites"></a>Vereisten

Voordat u begint met het instellen, moet aan de volgende vereisten zijn voldaan. Het instellen van deze vereisten valt buiten het bereik voor dit document.

- Active Directory Domain Services (AD DS) is geïnstalleerd en geconfigureerd in uw netwerk.
- AD FS is geïmplementeerd.
- SQL Server, SSRS en Management Studio zijn geïnstalleerd.

### <a name="overview"></a>Overzicht

De volgende stappen moeten worden uitgevoerd om de infrastructuur voor Finance and Operations in te stellen.

1. Uw domeinnaam en DNS-zones plannen
2. Uw certificaten plannen en verkrijgen
3. Uw gebruikers- en serviceaccounts plannen
4. DNS-zones maken en A-records toevoegen
5. VM's toevoegen aan het domein
6. Vereiste software installeren op VM's
7. Setupscripts downloaden vanuit LCS
8. Uw configuratie beschrijven
9. Certificaten installeren
10. Een standalone Service Fabric-cluster instellen
11. LCS-connectiviteit voor de tenant configureren
12. Bestandsopslag instellen
13. SQL Server instellen
14. De databases configureren
15. Referenties coderen
16. SSRS instellen
17. AD FS configureren

### <a name="plan-your-domain-name-and-dns-zones"></a>Uw domeinnaam en DNS-zones plannen

Wij raden aan om een openbaar geregistreerde domeinnaam voor de productie-installatie van AOS te gebruiken. Op die manier kan deze worden geopend buiten het netwerk als externe toegang vereist is.

Als het domein van uw bedrijf bijvoorbeeld contoso.com is, is de zone voor Finance and Operations (on-premises) mogelijk d365ffo.onprem.contoso.com met de volgende hostnamen:

- ax.d365ffo.onprem.contoso.com voor AOS-computers
- sf.d365ffo.onprem.contoso.com voor het Service Fabric-cluster

### <a name="plan-and-acquire-your-certificates"></a>Uw certificaten plannen en verkrijgen

Er zijn Secure Sockets Layer (SSL)-certificaten vereist voor de beveiliging van een Service Fabric-cluster en alle toepassingen die zijn geïmplementeerd. Voor uw productie en de sandbox-werkbelasting is het raadzaam dat u de certificaten verkrijgt bij een certificeringsinstantie (CA) zoals [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) of [GlobalSign](https://www.globalsign.com/en/ssl/). Als uw domein is ingesteld met [Active Directory Certificate Services](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), kunt u de certificaten maken via AD CS. Elk certificaat moet een persoonlijke sleutel bevatten die is gemaakt voor het uitwisselen van sleutels en moet worden geëxporteerd naar een Personal Information Exchange-bestand (.pfx).

Zelfondertekende certificaten kunnen alleen worden gebruikt voor testdoeleinden. De installatiescripts bevatten voor het gemak scripts voor het genereren en exporteren van zelfondertekende certificaten. Zoals gezegd, kunnen deze certificaten alleen voor testdoeleinden worden gebruikt.

| Doel                                      | Uitleg | Extra vereisten |
|----------------------------------------------|-------------|-------------------------|
| SSL-certificaat voor SQL Server                   | Dit certificaat wordt gebruikt voor het coderen van gegevens die worden verzonden via een netwerk tussen een exemplaar van SQL Server en een clienttoepassing. | <p>De domeinnaam van het certificaat moet overeenkomen met de volledig gekwalificeerde domeinnaam (FQDN) van het SQL Server-exemplaar of listener.</p><p>Als de SQL-listener bijvoorbeeld wordt gehost op de computer DAX7SQLAOSQLA, is de DNS-naam van het certificaat DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Certificaat voor Service Fabric-server            | Dit certificaat wordt gebruikt voor de beveiliging van de communicatie tussen de knooppunten van de Service Fabric. Dit certificaat wordt ook gebruikt als het servercertificaat dat wordt aangeboden aan de client die verbinding met het cluster maakt. | <p>De domeinnaam van het certificaat moet overeenkomen met de DNS-zone waar AOS en Service Fabric worden gehost.</p><p>De domeinnaam van het certificaat is bijvoorbeeld \*. onprem.contoso.com of \*. contoso.com.</p><p>Als u een certificaat met jokertekens gebruikt, is het jokerteken van toepassing op slechts één niveau. Een subdomein met een Subject Alternative Name (SAN) moet worden toegepast op het certificaat, als er meerdere niveaus zijn, zoals \*. contoso.com in het vorige voorbeeld.</p> |
| Certificaat voor Service Fabric-client            | Dit certificaat wordt gebruikt door clients voor het weergeven en beheren van het Service Fabric-cluster. | |
| Coderingscertificaat                     | Dit certificaat wordt gebruikt voor het versleutelen van gevoelige gegevens zoals het wachtwoord voor SQL Server en de wachtwoorden voor gebruikersaccounts. | <p>Het gebruik van de certificaatsleutel moet Data Encipherment (10) omvatten en niet serververificatie of clientverificatie.</p><p>Zie voor meer informatie [Geheimen beheren in Service Fabric-toepassingen](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL-certificaat                          | <p>Dit certificaat wordt gebruikt als het servercertificaat dat wordt aangeboden aan de client voor de AOS-website. Het wordt ook gebruikt voor het inschakelen van de certificaten voor Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP).</p><p>Het Service Fabric-servercertificaat kan hier worden gebruikt als het een certificaat met een jokerteken is.</p> | <p>De domeinnaam van het certificaat moet overeenkomen met de DNS-zone waar AOS en Service Fabric worden gehost.</p><p>De domeinnaam van het certificaat is bijvoorbeeld \*.d365ffo.onprem.contoso.com, \*.onprem.contoso.com of \*.contoso.com.</p><p>Als u een certificaat met jokertekens gebruikt, is het jokerteken van toepassing op slechts één niveau. Een SAN-subdomein moet worden toegepast op het certificaat, als er meerdere niveaus zijn, zoals \*. contoso.com in het vorige voorbeeld.</p> |
| Certificaat voor sessieverificatie           | Dit certificaat wordt gebruikt door AOS voor het beveiligen van de sessie-informatie van een gebruiker. | Dit is ook het certificaat voor de **bestandsshare** die wordt gebruikt bij de implementatie vanuit LCS. |
| Certificaat voor gegevens coderen en ondertekenen | Deze certificaten worden gebruikt door AOS voor het versleutelen van gevoelige gegevens. | |
| Clientcertificaat voor financiële rapportage       | Dit certificaat wordt gebruikt voor de beveiliging van de communicatie tussen de financiële rapportageservices en AOS. | |
| Rapportagecertificaat                        | Dit certificaat wordt gebruikt voor de beveiliging van de communicatie tussen SSRS en AOS. | |
| On-premise certificaat voor lokale agent           | <p>Dit certificaat wordt gebruikt voor de beveiliging van de communicatie tussen een lokale agent die on-premise en door LCS wordt gehost.</p><p>Met dit certificaat kan de lokale agent handelen namens de Azure AD-tenant en communiceren met LCS om implementaties te organiseren en controleren.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Uw gebruikers- en serviceaccounts plannen

U moet verschillende gebruikers of serviceaccounts maken voor Finance and Operations (on-premises). U moet een combinatie maken met groepsbeheerde serviceaccounts (gMSAs), domeinaccounts en SQL-accounts. In de volgende tabel ziet u de gebruikersaccounts, hun doel en voorbeelden van namen die worden gebruikt in dit onderwerp.

| Gebruikersaccount                                            | Type           | Doel | Gebruikersnaam |
|---------------------------------------------------------|----------------|---------|-----------|
| Serviceaccount voor toepassing Financiële rapportage         | gMSA           |         | Contoso\\svc-FRAS$ |
| Serviceaccount voor proces Financiële rapportage             | gMSA           |         | Contoso\\svc-FRPS$ |
| Serviceaccount voor Click Once Designer Financiële rapportage | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS-serviceaccount                                     | gMSA           | Deze gebruiker moet worden gemaakt voor testen in de toekomst. Het is de bedoeling dat AOS in toekomstige versies met gMSA kan werken. Als u deze gebruiker tijdens het instellen maakt, is dit handig voor een naadloze overgang naar gMSA. | Contoso\\svc-AXSF$ |
| AOS-serviceaccount                                     | Domeinaccount | AOS gebruikt deze gebruiker in de GA-versie. | Contoso\\AXServiceUser |
| Beheerdergebruiker AOS SQL DB                                   | SQL-gebruiker       | Deze gebruiker wordt in Finance and Operations gebruikt voor verificatie in SQL\*. Deze gebruiker wordt in toekomstige versies ook vervangen door de gMSA-gebruiker. | AXDBAdmin |
| Serviceaccount lokale implementatie-agent                  | gMSA           | Dit account wordt door de lokale agent gebruikt om de implementatie op verschillende knooppunten te organiseren. | Contoso\\Svc-LocalAgent$ |

\* De SQL-gebruikersnaam en het wachtwoord voor SQL-verificatie zijn beveiligd, omdat ze in de bestandsshare worden gecodeerd en opgeslagen.

### <a name="create-dns-zones-and-add-a-records"></a>DNS-zones maken en A-records toevoegen

DNS is geïntegreerd met AD DS zodat u resources in een netwerk kunt indelen, beheren en zoeken. Maak een DNS-zone voor forward lookup en A-records voor de AOS-hostnaam en het Service Fabric-cluster. In dit voorbeeld is d365ffo.onprem.contoso.com de naam van de DNS-zone en zijn de A-records/hostnamen als volgt:

- **ax**.d365ffo.onprem.contoso.com voor AOS-computers
- **sf**.d365ffo.onprem.contoso.com voor het Service Fabric-cluster

#### <a name="add-a-dns-zone"></a>Een DNS-zone toevoegen

Voer de volgende procedure uit om een DNS-zone toe te voegen.

1. Meld u aan bij de computer van de domeincontroller, klik op **Start** en typ **dnsmgmt.msc** om DNS Manager te starten.
2. Klik met de rechtermuisknop op de naam van de domeincontroller en klik op **Nieuwe zone** \> **Volgende**.
3. Selecteer **Primaire zone**.
4. Laat het selectievakje **Zone opslaan in Active Directory (alleen beschikbaar als de DNS-Server een beschrijfbare domeincontroller is)** ingeschakeld en klik op **Volgende**.
5. Selecteer **Naar alle DNS-Servers die worden uitgevoerd op domeincontrollers in dit domein: Contoso.com**, en klik op **Volgende**.
6. Selecteer **Zones voor forward lookup** en klik op **Volgende**.
7. Voer de zonenaam voor uw instellingen in en klik op **Volgende**. Typ bijvoorbeeld **d365ffo.onprem.contoso.com**.
8. Selecteer **Geen dynamische updates toestaan** en klik op **Volgende**.

#### <a name="set-up-an-a-record-for-aos"></a>Een A-record voor AOS instellen

Maak in de nieuwe DNS-zone een A-record met de naam **ax.d365ffo.onprem.contoso.com** voor **elk** Service Fabric-clusterknooppunt van het type **AOSNodeType**. Maak geen A-records voor de andere knooppunttypen.

1. Klik met de rechtermuisknop op de nieuwe zone en klik vervolgens op **Nieuwe host**.
2. Voer de naam en het IP-adres van het Service Fabric-clusterknooppunt in (bijvoorbeeld 10.179.108.12) en klik vervolgens op **Host toevoegen**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Een A-record instellen voor de orchestrator

Maak in de nieuwe DNS-zone een A-record met de naam **sf.d365ffo.onprem.contoso.com** voor **elk** Service Fabric-clusterknooppunt van het type **OrchestratorType**. Maak geen A-records voor de andere knooppunttypen.

1. Klik met de rechtermuisknop op de nieuwe zone en klik vervolgens op **Nieuwe host**.
2. Voer de naam en het IP-adres van het Service Fabric-clusterknooppunt in (bijvoorbeeld 10.179.108.15) en klik vervolgens op **Host toevoegen**.

#### <a name="join-vms-to-the-domain"></a>VM's toevoegen aan het domein

Voeg elke VM toe aan het domein door de stappen uit te voeren in [Windows Server 2016 toevoegen aan een Active Directory-domein](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html). Of gebruik het Windows PowerShell-script.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Nadat de VM's zijn toegevoegd aan het domein, voegt u de AOS-serviceaccounts (Contoso\svc AXSF$, Contoso\svc AXSF$) toe aan de lokale beheerdersgroep. In het artikel [Een lid toevoegen aan een lokale groep](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx) vindt u de procedure hiervoor.

#### <a name="disable-user-access-control"></a>Toegangsbeheer voor gebruikers uitschakelen 

Voer het volgende script uit om het toegangsbeheer voor gebruikers op **elk** Service Fabric-knooppunt uit te schakelen.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> U moet het knooppunt opnieuw opstarten nadat het script is voltooid.

#### <a name="add-prerequisite-software-to-vms"></a>Vereiste software installeren op VM's

In de volgende tabel wordt de vereiste software vermeld die moet worden toegepast op de computers van elk knooppunttype.

> [!NOTE]
> U moet de computer opnieuw opstarten nadat u de onderdelen hebt geïnstalleerd.

| Knooppunttype | component | Opdracht |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC-stuurprogramma | Zie [Microsoft ODBC-stuurprogramma 13.1 voor SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Framework versie 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework versie 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | Internet Information Services (IIS) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ distributiepakketten voor Microsoft Visual Studio 2013 | Zie [Microsoft Visual C++ distributiepakketten voor Microsoft Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Distributiepakket van Microsoft Access Database Engine 2010 | Zie [Distributiepakket van Microsoft Access Database Engine 2010](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework versie 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework versie 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 in **Native** modus | |
| MR        | .NET Framework versie 2.0–3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework versie 4.0–4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Microsoft Visual C++ distributiepakketten voor Microsoft Visual Studio 2013 | Zie [Microsoft Visual C++ distributiepakketten voor Microsoft Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Setupscripts downloaden vanuit LCS

Er zijn verschillende scripts beschikbaar voor een verbeterde ervaring bij het instellen. Volg deze stappen om de setupscripts van LCS te downloaden.

1. Meld u aan bij LCS (<https://lcs.dynamics.com/v2>).
2. Klik in het dashboard op de tegel voor de **bibliotheek voor gedeelde activa**.
3. Klik op het tabblad **Model**.
4. Selecteer in het raster de rij **Dynamics 365 for Operations - On-premises implementatiescripts**.
5. Klik op **Versies** en download de meest recente versie van de scripts.

### <a name="describe-your-configuration"></a>Uw configuratie beschrijven

Deze sectie bevat informatie over de scripts die moet worden uitgevoerd. De scripts worden besproken in de volgorde waarin ze moeten worden uitgevoerd. Als u de scripts wilt uitvoeren, vult u het sjabloonbestand in op $(downloadPath)\\ConfigTemplate.xml. Het bestand ConfigTemplate.xml beschrijft de Service Fabric-clusters, de certificaten die worden gebruikt voor het configureren en de accounts die toegang moeten krijgen tot de relevante certificaten. In het meegeleverde voorbeeld worden de waarden ingevuld voor de voorbeeldinfrastructuur die in dit onderwerp wordt beschreven. Het sjabloonbestand wordt gebruikt in het volgende gedeelte.

#### <a name="create-the-domain-account-for-a-service-user"></a>Het domeinaccount voor een servicegebruiker maken

Voer de volgende opdracht uit om het domeingebruikersaccount contoso\\AXServiceUser te maken.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>GMSAs maken

1. Activeer de map **$(DownloadPath)** en voer de volgende Windows PowerShell-opdracht uit.

    > [!NOTE]
    > Met dit script worden niet de gebruikers gemaakt. In plaats daarvan worden de opdrachten afgedrukt die handmatig moeten worden uitgevoerd op de computer van de domeincontroller.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Kopieer de uitvoer van de opdracht naar een Windows PowerShell-venster. Zorg ervoor dat de regeleinden worden verwijderd en voer de regels uit op de computer met de Active Directory-domeincontroller met verhoogde bevoegdheden (klik met de rechtermuisknop en vervolgens op **Als Administrator uitvoeren**).
3. Voer het volgende script uit op de computer met de Active Directory-domeincontroller om te valideren dat de accounts zijn gemaakt. Zorg ervoor dat u het script uitvoert nadat u het patroon dat overeenkomt met de naamgevingsconventie van de serviceaccounts, hebt vervangen.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Voer het script Export-AddGMSAsONVMScript.ps1 uit op de clientcomputer. Met dit script worden scripts gegenereerd die worden uitgevoerd op elke Service Fabric VM en toegevoegd aan een map die met de naam van elke VM overeenkomt.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>IIS Stoppen

Maak verbinding met elke Service Fabric VM via Remote Desktop Protocol (RDP) en voer de handmatige stappen uit in [De webserver (IIS 7) starten of stoppen](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx). Of gebruik het volgende Windows PowerShell-script door via RDP verbinding te maken met elke Service Fabric VM.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_De IIS-functie moet worden geïnstalleerd maar uitgeschakeld omdat er bepaalde afhankelijkheden zijn met de IIS-dll's in het product._

### <a name="install-certificates"></a>Certificaten installeren

1. Als u de eerder vermelde certificaten hebt aangeschaft bij een geldige certificeringsinstantie, vult u de .pfx-bestandsnaam en de vingerafdruk voor de certificaten in het bestand ConfigTemplate.xml in. Stel het kenmerk **generateSelfSignedCert** in op **False** en het **exporteerbare** kenmerk op **False**. Kopieer de .pfx-bestanden naar de map $(DownloadPath)\\InfrastructureScripts\\Certs.
2. Als u zelfondertekende certificaten gebruikt (alleen voor testdoeleinden), voert u het volgende script uit. Als u zelfondertekende certificaten wilt maken in het bestand ConfigTemplate.xml, controleert u of **generateSelfSignedCert** is ingesteld op **True** en **exporteerbaar** is ingesteld op **True**. Het script werkt de XML bij met de vingerafdruk voor de certificaten.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Exporteer de nieuwe certificaten met de persoonlijke sleutel (het .pfx-bestand). Gebruik het volgende script om de opdrachten voor het exporteren te genereren en uit te voeren in Windows PowerShell. De .pfx-bestanden worden in de map Certs geplaatst.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > De certificaten moeten zijn geïnstalleerd en aanwezig zijn in het certificaat:\\CurrentUser\\Mijn. De certificaten moeten ook exporteerbaar zijn.

    Als u zelfondertekende certificaten gebruikt, gaat u naar de volgende sectie. U hoeft deze procedure niet te voltooien.

4. Nadat u de .pfx-bestanden hebt geëxporteerd of gekopieerd naar de map $(DownloadPath)\\InfrastructureScripts\\Certs, voert u de volgende opdrachten uit voor het genereren van scripts die in de mappen worden geplaatst die met de VM's overeenkomen.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Kopieer de scripts in elke map voor de VM's die met de naam van de map overeenkomen.
6. Voer op elke VM de volgende scripts uit in de volgorde waarin ze worden vermeld.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Een standalone Service Fabric-cluster instellen

1. Voer de volgende opdracht uit om het bestand ClusterConfig.json te genereren.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Zie voor meer informatie [Stap 1B: Een cluster met meerdere computers maken](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Een zelfstandig cluster op Windows beveiligen met x.509-certificaten](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) en [Een zelfstandig cluster maken op Windows Server](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Download het [zelfstandige installatiepakket voor Service Fabric](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) naar een van de Service Fabric-knooppunten. Nadat het zipbestand is gedownload, heft u de blokkering op door met de rechtermuisknop op het zipbestand en vervolgens op **Eigenschappen** te klikken. Schakel in het dialoogvenster het selectievakje **Deblokkeren** in in de rechterbenedenhoek.
3. Kopieer het zipbestand naar een van de knooppunten in het Service Fabric-cluster en pak het bestand uit.
4. Voer de volgende opdrachten uit om een binnenkomende firewallregel te maken op poort 443 en 445 in alle knooppunten.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Voer de volgende opdrachten uit om een binnenkomende firewallregel te maken op poort 80, alleen voor het SSRS-knooppunt.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Kopieer het bestand ClusterConfig.json naar uw uitgepakte installatielocatie van de zelfstandige Service Fabric.
7. Ga naar de uitgepakte installatielocatie in Windows PowerShell met behulp van verhoogde bevoegdheden en voer de volgende opdracht uit om de clusterconfiguratie te testen.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Als de test slaagt, voert u de volgende opdracht om het cluster te implementeren.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Nadat het cluster is gemaakt, opent u de Service Fabric-verkenner op elke clientcomputer voor het valideren van de installatie:

    1. Installeer het clientcertificaat van de Service Fabric in CurrentUser\\Mijn als dit nog niet is gebeurd.
    2. Ga naar **IE-instellingen** \> **Compatibiliteitsmodus** en schakel het selectievakje **Intranetsites weergeven in compatibiliteitsmodus** uit.
    3. Ga naar `https://sf.d365ffo.onprem.contoso.com:19080`, waar sf.d365ffo.onprem.contoso.com de hostnaam is van het Service fabric-cluster dat is opgegeven in de zone. Als DNS-naamomzetting niet is geconfigureerd, gebruikt u het IP-adres van de computer.
    4. Selecteer het clientcertificaat. De pagina met de **Service Fabric-verkenner** wordt weergegeven.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>LCS-connectiviteit voor de tenant configureren

Implementatie en onderhoud van Finance and Operations worden geregeld via LCS met behulp van een on-premises lokale agent. Voor het opzetten van de connectiviteit vanuit LCS naar de Finance and Operations-tenant, moet u een certificaat configureren waarmee de lokale agent kan handelen namens uw Azure AD-tenant (bijvoorbeeld Contoso.Onmicrosoft.com).

Gebruik het on-premises agentcertificaat dat u hebt aangeschaft bij een certificeringsinstantie of het zelfondertekende certificaat dat u hebt gegenereerd met behulp van scripts.

Alleen gebruikersaccounts met de rol Globale beheerder voor de map kunnen certificaten voor het autoriseren van LCS toevoegen. Standaard is de persoon die zich voor Microsoft Office 365 voor uw organisatie aanmeldt, de globale beheerder voor de map.

> [!NOTE]
> U moet het certificaat precies één keer per tenant configureren. Alle on-premises omgevingen kunnen hetzelfde certificaat gebruiken om verbinding te maken met LCS.

1. Download en installeer de meest recente versie van Azure PowerShell op een clientcomputer. Zie voor meer informatie [Azure PowerShell installeren en configureren](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Meld u aan bij de [Azure-portal van de klant](https://portal.azure.com) om te controleren of u de rol Globale beheerder voor de map hebt.
3. Voer het volgende script uit via $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Bestandsopslag instellen

U moet maximaal twee beschikbare SMB 3.0-bestandsshares instellen. Zie [SMB-beveiligingsverbeteringen](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1) voor informatie over het inschakelen van SMB 3.0.
Beveiligde dialectonderhandeling kan downgrades van SMB 2.0 of 3.0 naar SMB 1.0 niet detecteren of voorkomen. Om deze reden en om te profiteren van de volledige mogelijkheden van SMB-codering, wordt aangeraden de SMB 1.0-server uit te schakelen.

> [!NOTE]
> Om te garanderen dat uw gegevens beveiligd zijn in uw omgeving is, moet de BitLocker-stationsversleuteling zijn ingeschakeld op elke computer. Zie voor informatie over het inschakelen van BitLocker [BitLocker: implementeren in Windows Server 2012 en hoger](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Een bestandsshare voor het opslaan van gebruikersdocumenten die worden geüpload naar AOS (bijvoorbeeld \\\\DAX7SQLAOFILE1\\aos-opslag).
- Een bestandsshare voor het opslaan van de laatste build en configuratiebestanden voor het organiseren van de implementatie (bijvoorbeeld \\\\DAX7SQLAOFILE1\\agent)

    > [!NOTE]
    > Houd dit bestandssharepad zo kort mogelijk om te voorkomen dat de maximale padlengte wordt overschreden voor de bestanden die worden opgeslagen in de share.

1. Voer de volgende opdracht uit op de computer met de bestandsshare.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>De bestandsshare \\\\DAX7SQLAOFILE1\\aos-opslag instellen

2. Selecteer in Serverbeheer **Bestands- en opslagservices** \> **Shares**.
3. Klik op **Taken** \> **Nieuwe Share** om een nieuwe share te maken met de naam **aos-opslag**.
4. Wijs machtigingen voor **Wijzigen** toe voor elke computer in de het Service Fabric-cluster behalve **OrchestratorNodeType**.
5. Wijs machtigingen voor **Wijzigen** toe voor de AOS-domeingebruiker (contoso\\AXServiceUser) en de gMSA-gebruiker (contoso\\svc-AXSF).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>De bestandsshare \\\\DAX7SQLAOFILE1\\agent instellen

6. Ga terug naar Serverbeheer, selecteer **Bestands- en opslagservices** \> **Shares**.
7. Klik op **Taken** \> **Nieuwe Share** om een nieuwe share te maken met de naam **agent**.
8. Wijs machtigingen voor **Volledige controle** toe aan de gMSA-gebruiker voor de lokale implementatie-agent (contoso\\svc LocalAgent$).

### <a name="set-up-sql-server"></a>SQL Server instellen

1. Installeer SQL Server 2016 SP1 met hoge beschikbaarheid, als SQL-clusters met een Storage Area Network (SAN) of in een Always On-configuratie.  Controleer of **Database Engine, Reporting Services, Zoekopdracht in volledige tekst** en **Beheerhulpprogramma's** al zijn geïnstalleerd.
> [!NOTE]
> Zorg ervoor dat de SQL Always On is ingesteld op [Initiële gegevenssynchronisatiepagina selecteren (Wizards Always On beschikbaarheidsgroep)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards) en volg [Secundaire databases handmatig voorbereiden](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Voer de SQL-service uit als een domeingebruiker.
3. Haal een SSL-certificaat op bij een certificeringsinstantie voor het configureren van Finance and Operations. Voor testomgevingen kunt u ook een zelfondertekend certificaat maken en gebruiken.

**Zelfondertekend certificaat voor geclusterd SQL-exemplaar**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Zelfondertekend certificaat voor Always-On SQL-exemplaar**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Met behulp van het certificaat voert u de stappen uit in [SSL-codering inschakelen voor een exemplaar van SQL Server met Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) voor het configureren van SSL op SQL Server.
5. Volg deze stappen voor elk knooppunt van het cluster. Zorg ervoor dat u de wijzigingen aanbrengt in het niet-actieve knooppunt en voer failover uit nadat wijzigingen zijn aangebracht.

    1. Importeer het certificaat in LocalMachine\\Mijn.
    2. Verleen certificaatmachtigingen aan het serviceaccount dat wordt gebruikt voor het uitvoeren van SQL-service. Klik in Microsoft Management Console (MMC) met de rechtermuisknop op het certificaat (certlm.msc) en klik vervolgens op **Taken** \> **Persoonlijke sleutels beheren**.
    3. Voeg de vingerafdruk van het certificaat toe aan HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib kunnen\\certificaat.
    4. Stel in Microsoft SQL Server Configuration Manager **ForceEncryption** in op **Ja**.

6. Exporteer de openbare sleutel van het certificaat (het cer-bestand) en installeer het in de vertrouwde hoofdmap van elk Service Fabric-knooppunt.

### <a name="configure-the-orchestratordata-database"></a>De OrchestratorData-database configureren

1.  Maak een lege database maken en geef deze de naam **OrchestratorData**. Deze database wordt gebruikt door de on-premises agent voor het regelen van de implementaties.
2.  Verleen de lokale agent gMSA (svc LocalAgent$) machtigingen als **db\_eigenaar** voor de database:

    1. Vouw in de structuur de servernaam uit, vouw **Beveiliging** \> **Aanmeldingen** uit, klik met de rechtermuisknop en klik op **Nieuwe aanmelding**.

        ![Opdracht Nieuwe aanmelding](./media/OPSetup_01_NewLogin.png)


    2. Zoek het serviceaccount **svc-LocalAgent$**. Klik op **locaties**, selecteer **Hele map** en klik vervolgens op **Objecttypen** en selecteer **-Serviceaccount**.

        ![Selecteer het dialoogvenster Gebruiker, Serviceaccount of Groep](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Stel **Serverrol toewijzen** in op **Openbaar**.
    4. Wijs de rolmachtiging voor **db\_eigenaar** database toe aan de OrchestratorData-database.

### <a name="configure-the-finance-and-operations-database"></a>Finance and Operations-database configureren

1. Meld u aan bij LCS (<https://lcs.dynamics.com/v2>).
2. Klik in het dashboard op de tegel voor de **bibliotheek voor gedeelde activa**.
3. Klik op het tabblad **Model** 
4. Klik in het raster op de rij **Dynamics 365 for Operations on-premises, Enterprise edition - demonstratiegegevens** voor het downloaden van het zipbestand.
5. Het zipbestand bevat lege .bak-bestanden en demogegevens. Kies op basis van uw behoeften het juiste .bak-bestand. Als u bijvoorbeeld demogegevens nodig hebt, zet u het bestand AxBootstrapDB_Demodata.bak terug. 
6. Zet de AxBootstrapDB_DemoData.bak-database terug.
7. Wijzig de naam van de database in **AXDBRAIN**.
8. Voer de volgende query's uit op de teruggezette database.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Werk de databasebestanden bij:

    1. Klik met de rechtermuisknop op de database en vervolgens op **Eigenschappen**.
    2. Klik op **Bestanden** om de eigenschappen van de database te wijzigen.
    3. Voer in het veld **Oorspronkelijke grootte (MB)** een waarde in die groter is dan 5.120.

        ![Dialoogvenster Database-eigenschappen](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. Stel voor **AXDBBuild\_-gegevens** het veld **Toename/maximaliseren** in op **200** megabyte (MB).
    5. Stel voor **AXDBBuild\_-logbestand** het veld **Toename/maximaliseren** in op **500** MB.

        ![Het dialoogvenster Toename wijzigen](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Maak een nieuwe gebruiker waarvoor SQL-verificatie is ingeschakeld (axdbadmin).
6. Gebruik de informatie in de volgende tabel om de gebruikers en databaserollen toe te wijzen.

    | Gebruiker             | Type    | Databaserol |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_eigenaar     |
    | svc-LocalAgent$  | gMSA    | db\_eigenaar     |
    | svc-FRPS$        | gMSA    | db\_eigenaar     |
    | svc-FRAS$        | gMSA    | db\_eigenaar     |
    | axdbadmin        | SqlUser | db\_eigenaar     |

7. Geef de gebruiker svc AXSF$ en de SQL-gebruiker axdbadmin toegang tot de volgende rollen in de database tempdb:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. Voer de volgende Transact-SQL-opdrachten (T-SQL) uit in Management Studio:

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Voer de volgende opdracht uit:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>De financiële rapportage-database configureren

1.  Maak een lege database en geef deze de naam **FinancialReporting**.
2.  Gebruik de informatie in de volgende tabel om de gebruikers en databaserollen toe te wijzen.

    | Gebruiker             | Type | Databaserol |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_eigenaar     |
    | svc-FRPS$        | gMSA | db\_eigenaar     |
    | svc-FRAS$        | gMSA | db\_eigenaar     |

### <a name="encrypt-credentials"></a>Referenties coderen

1. Installeer op elke clientcomputer het coderingscertificaat in het certificaatarchief LocalMachine\\Mijn.
2. Verleen aan de huidige gebruiker leestoegang tot de persoonlijke sleutel van dit certificaat.
3. Maak het bestand Credentials.json zoals hier wordt weergegeven.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** is het wachtwoord van de gebruiker voor het gecodeerde domein voor de AOS-domeingebruiker (contoso\\axserviceuser).
    - **SqlUser** is de gecodeerde SQL-gebruiker (axdbadmin) die toegang tot de Finance and Operations-database (AXDBRAIN) en **SqlPassword** is het gecodeerde SQL-wachtwoord.

4. Kopieer het bestand .json naar de SMB-bestandsshare, \\\\AX7SQLAOFILE1\\agent\\Referenties\\Credentials.json.
5. Werk het bestand Credentials.json bij met gecodeerde waarden.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. Vervang in Credentials.json **\<encryptedDomainUserPassword\>** door het gecodeerde domeinwachtwoord.
    2. Vervang **\<encryptedSqlUser\>** door de gecodeerde SQL-gebruiker voor Finance and Operations.
    3. Vervang **\<encryptedSqlPassword\>** door het gecodeerde SQL-wachtwoord voor Finance and Operations.
    
### <a name="set-up-ssrs"></a>SSRS instellen

1.  Voordat u begint, controleert u of de vereiste onderdelen die aan het begin van dit onderwerp worden vermeld, zijn geïnstalleerd.
2.  Volg de stappen naar [SQL Server Reporting Services configureren voor een on-premises implementatie](../analytics/configure-ssrs-on-premises.md).

### <a name="configure-ad-fs"></a>AD FS configureren

Voordat u deze procedure kunt voltooien, moet AD FS worden geïmplementeerd op Windows Server 2016. Zie voor informatie over het implementeren van AD FS [Implementatiehandleiding Windows Server 2016 en 2012 R2 AD FS Implementatiehandleiding](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Voor Finance and Operations is een extra configuratie naast de standaardconfiguratie van AD FS. Voor de volgende stappen wordt Windows PowerShell uitgevoerd op een computer met de service van AD FS-rol geïnstalleerd. Het gebruikersaccount moet beschikken over voldoende machtigingen voor het beheer van AD FS. De gebruiker moet bijvoorbeeld een domeinbeheerdersaccount hebben.

1. Configureer de AD FS-id zo dat deze overeenkomt met de uitgever van het AD FS-token.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Tenzij u AD FS voor gemengde omgevingen hebt geconfigureerd, moet u Windows Integrated Authentication (WIA) voor verbindingen voor intranetverificatie uitschakelen. Zie voor meer informatie over het configureren van WIA, zodat dit kan worden gebruikt met AD FS [Browsers configureren voor het gebruik van Windows Integrated Authentication (WIA) met AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. Als u zich wilt aanmelden met het e-mailadres van de gebruiker, moet dit een acceptabele verificatie-invoer vormen.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

Voordat AD FS Finance and Operations vertrouwt voor de uitwisseling van verificatie, moeten verschillende topassingsgegevens worden geregistreerd in AD FS onder een AD FS-toepassingsgroep. Om het instelproces te versnellen en het aantal fouten te verminderen, kunt u het volgende script gebruiken voor registratie. Kopieer het script Publish-ADFSApplicationGroup.ps1 en de map D365FO-OP naar een computer waarop de AD FS-functieservice is geïnstalleerd. Voer vervolgens het script uit met behulp van een gebruikersaccount, zoals een beheerdersaccount dat beschikt over voldoende machtigingen voor het beheren van AD FS. Zie de documentatie die wordt vermeld in het script voor meer informatie over het gebruik van het script. Maak een notitie van de client-id's die zijn opgegeven in de uitvoer, omdat u in een volgende stap in LCS wordt gevraagd naar deze gegevens.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

De AD FS-managementconsole moet lijken op de volgende illustratie. Als u Serverbeheer wilt openen, klikt u op **extra** \> **AD FS Management** en vervolgens onderaan in de structuurweergave aan de linkerkant op **Toepassingsgroepen**. Dubbelklik op de toepassingsgroep om meer details weer te geven.

![Eigenschappen van toepassingsgroep](./media/OPSetup_05_ApplicatioGroupProperties.png)

Tot slot controleert u of u toegang hebt tot de AD FS OpenID-configuratie-URL op een Service Fabric-knooppunt van het type **AOSNodeType**, door naar `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` te gaan in een webbrowser. Als u een bericht ontvangt waarin wordt gemeld dat de site niet veilig is, hebt u uw AD FS SSL-certificaat niet toegevoegd aan het Trusted Root Certification Authorities-archief. Deze stap wordt beschreven in de Implementatiehandleiding voor AD FS. Als u toegang hebt tot de URL, wordt een JSON-bestand (JavaScript Object Notation) geretourneerd dat de AD FS-configuratie bevat en ziet u dat de URL van uw AD FS wordt vertrouwd.

Daarmee is de instelling van de infrastructuur voltooid. In de volgende secties wordt beschreven hoe u naar [LCS](https://lcs.dynamics.com) navigeert om uw connector in te stellen en uw Dynamics 365 for Finance and Operations-omgeving te implementeren.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Connector configureren en on-premises lokale agent installeren

1. Meld u aan bij [LCS](https://lcs.dynamics.com/) en open het on-premises implementatieproject.
2. Klik in het menu hamburger op **Projectinstellingen**.

    ![Opdracht Projectinstellingen](./media/OPSetup_06_ProjectSettings.png)

3. Klik op **On-premises connectors**.
4. Klik op **Toevoegen** om een nieuwe connector te maken.
5. Download in het tabblad **Hostinfrastructuur instellen** en het installatieprogramma voor de agent.

    ![Knop Installatieprogramma agent downloaden in het tabblad Hostinfrastructuur instellen](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Controleer of het zipbestand niet is vergrendeld. Klik met de rechtermuisknop op het bestand, klik op **Eigenschappen** en selecteer **Deblokkeren**.
7. Pak het installatieprogramma van de agent uit op een Service Fabric-knooppunt van het type **OrchestratorType**.
8. Voer op het tabblad **Agent configureren** de configuratie-instellingen in.
9. Sla de configuratie op en klik vervolgens op **Configuraties downloaden** voor het downloaden van het configuratiebestand localagent-config.json.

    ![Knop Configuraties downloaden op het tabblad Agent configureren](./media/OPSetup_08_DownloadConfigurations.png)

10. Kopieer het bestand localagent-config.json naar de computer waarop het agentinstallatiepakket zich bevindt.
11. Voer in een opdrachtpromptvenster de volgende opdracht uit door te navigeren naar de map die het agentinstallatieprogramma bevat.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > De gebruiker die deze opdracht uitvoert, moet beschikken over de machtigingen **db\_eigenaar** voor de OrchestratorData-database.
    
12. Nadat de lokale agent is geïnstalleerd, gaat u terug naar de on-premises connector in LCS.
13. Klik op het tabblad **Instellingen valideren** op de knop **Bericht agent**. Hierdoor wordt de LCS-verbinding met uw lokale agent getest. Wanneer de verbinding tot stand is gebracht, ziet de pagina eruit als de onderstaande afbeelding.

     ![Agent valideren](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Implementatie van uw Dynamics 365 for Finance and Operations (on-premises)-omgeving

1. Ga naar het on-premises project in LCS, ga naar **Omgeving**, **Sandbox** en klik op **Configureren**
2. Selecteer uw **Omgevingstopologie** en volg de wizard om de implementatie te starten.
3. De lokale agent haalt het implementatieverzoek op, start de implementatie en stuurt een bericht naar LCS als deze klaar is.

