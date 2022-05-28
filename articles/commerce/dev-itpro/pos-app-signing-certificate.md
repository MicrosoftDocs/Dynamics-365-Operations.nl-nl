---
title: MPOS ondertekenen met een certificaat voor ondertekening van programmacode
description: In dit onderwerp wordt uitgelegd hoe u MPOS kunt ondertekenen met een certificaat voor ondertekening van programmacode.
author: mugunthanm
ms.date: 05/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: tfehr
ms.custom: 28021
ms.search.region: Global
ms.author: mumani
ms.search.validFrom: 2019-09-2019
ms.openlocfilehash: e45961cf1ddb385d914b700d03bc95d07de47b68
ms.sourcegitcommit: d70f66a98eff0a2836e3033351b482466bd9c290
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/11/2022
ms.locfileid: "8741540"
---
# <a name="sign-mpos-appx-with-a-code-signing-certificate"></a>APPX-bestand voor MPOS ondertekenen met een certificaat voor ondertekening van programmacode

[!include [banner](../includes/banner.md)]

Als u Modern POS (MPOS) wilt installeren, moet u de MPOS-app ondertekenen met een certificaat voor code-ondertekening van een betrouwbare provider en hetzelfde certificaat installeren op alle computers waarop MPOS is geïnstalleerd onder de vertrouwde hoofdmap voor de huidige gebruiker.

Als u de MPOS-app wilt ondertekenen met een certificaat, gebruikt u een van deze opties in het bestand **Retail SDK\\Build tool\\Customization.settings**:

- Voeg het taakonderdeel Veilig bestand van de Azure DevOps-bouwstappen toe en upload het certificaat om de bestandstaak te beveiligen. Gebruik de variabele voor het uitvoerpad van de bestandstaak als parameter in het bestand Customization.settings.

    > [!NOTE]
    > De taak Veilig bestand ondersteunt niet een met wachtwoord beveiligd certificaat. U moet het wachtwoord verwijderen voordat u deze taak uploadt. Aangezien het certificaat wordt geüpload naar de systeemtaak voor beveiligde bestanden in Azure, kunt u het wachtwoord alleen voor deze stap verwijderen. Overleg het verwijderen van het wachtwoord echter met uw beveiligingsexperts om te bepalen of dit de juiste actie voor uw project is. Verwijder het certificaatwachtwoord niet voor andere scenario's.
- Gebruik een certificaat dat in het bestandssysteem bestaat. Hiervoor downloadt of genereert u een certificaat en plaatst u dit in het bestandssysteem waar de build wordt uitgevoerd. De door Microsoft gehoste agent of buildgebruiker moet toegang hebben tot dit pad en bestand.
- Gebruik een vingerafdruk om het certificaat in de opslag op te zoeken en u aan te melden met dat certificaat.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Een beveiligde bestandstaak gebruiken voor het ondertekenen van de Universal Windows Platform-app

> [!NOTE]
> U kunt ook de Azure Key Vault gebruiken om het certificaat op te slaan en de Azure-ondertekeningsfunctie gebruiken voor het ondertekenen van het bestand Modern POS .appx en installatieprogramma's voor selfservice. Zie voor voorbeelden van pijplijnscripts en aanvullende informatie [Een build-pipeline instellen in Azure DevOps om selfservicepakketten voor Retail te genereren](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Het gebruik van een beveiligde bestandstaak is de aanbevolen methode voor het ondertekenen van de UWP-app (Universal Windows Platform). Zie [Het ondertekenen van pakketten configureren](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing) voor meer informatie over het ondertekenen van pakketten. Dit proces wordt weergegeven in de volgende afbeelding.

![Ondertekeningsstroom voor de MPOS-app.](media/POSSigningFlow.png)

> [!NOTE]
> Op dit moment wordt door de OOB-pakketten alleen het ondertekenen van het appx-bestand ondersteund. De verschillende selfserviceprogramma's, zoals MPOIS, RSSU en HWS, worden niet ondertekend door dit proces. U moet deze handmatig ondertekenen met SignTool of andere ondertekeningstools. Het certificaat dat wordt gebruikt voor het ondertekenen van het appx-bestand, moet worden geïnstalleerd op de computer waarop Modern POS is geïnstalleerd.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Stappen voor het configureren van het certificaat voor ondertekenen in Azure Pipelines

### <a name="certificate-in-the-file-systemsecure-location"></a>Certificaat dat in het bestandssysteem/veilige locatie

Download de [taak DownloadFile](/visualstudio/msbuild/downloadfile-task) en voeg deze toe als eerste stap in het buildproces. Het voordeel van het gebruik van de taak Veilig bestand is dat het bestand wordt gecodeerd en op de schijf wordt geplaatst tijdens de build, ongeacht of de build-pipeline slaagt, mislukt of wordt geannuleerd. Het bestand wordt verwijderd van de downloadlocatie nadat het buildproces is voltooid.

1. Download de taak Veilig bestand en voeg deze toe als eerste stap in de Azure build-pipeline. U kunt de taak Veilig bestand downloaden via [DownloadFile](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
2. Upload het certificaat naar de taak Veilig bestand en stel de verwijzingsnaam in onder Uitvoervariabelen, zoals in de volgende afbeelding wordt weergegeven.
    > [!div class="mx-imgBorder"]
    > ![Taak Veilig bestand](media/SecureFile.png)
3. Maak een nieuwe variabele in Azure Pipelines door **Nieuwe variabele** te selecteren op het tabblad **Variabelen**.
4. Geef in het waardeveld een naam voor de variabele op, bijvoorbeeld **MySigningCert**.
5. Sla de variabele op.
6. Open het bestand **Customization.settings** vanuit **RetailSDK\\BuildTools** en werk **ModernPOSPackageCertificateKeyFile** bij met de variabelenaam die is gemaakt in de pijplijn (stap 3). Bijvoorbeeld:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Deze stap is vereist als het certificaat niet is beveiligd met een wachtwoord. Als het certificaat is beveiligd met een wachtwoord, gaat u verder met de volgende stappen.
 
7. Voeg een nieuwe beveiligde-tekstvariabele toe op het tabblad **Variabelen** van de pijplijn. Stel de naam in op **MySigningCert.tokens** en stel de waarde in van het wachtwoord voor het certificaat. Selecteer het vergrendelingspictogram om de variabele te beveiligen.
8. Voeg een taak **Powershell Script** aan de pijplijn toe (na Veilig bestand downloaden en vóór de stap Build). Geef de **weergavenaam** op en stel het type in als **Inline**. Kopieer en plak het volgende in de scriptsectie.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

9. Open het bestand **Customization.settings** vanuit **RetailSDK\\BuildTools** en werk **ModernPOSPackageCertificateThumbprint** bij met de waarde van de certificaatvingerafdruk.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Zie [Vingerafdruk voor certificaat ophalen](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint) voor meer informatie over het ophalen van de vingerafdruk van een certificaat. 

 
## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Een certificaat downloaden of genereren om de MPOS-app handmatig te ondertekenen met msbuild in SDK

Als een gedownload of gegenereerd certificaat wordt gebruikt om de MPOS-app te ondertekenen, dan wordt het knooppunt **ModernPOSPackageCertificateKeyFile** in het bestand **BuildTools\\Customization.settings** bijgewerkt om te verwijzen naar de locatie van het pfx-bestand (**$(SdkReferencesPath)\\appxsignkey.pfx**). Bijvoorbeeld:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

In dit geval is de bestandsnaam van het certificaat **appxsignkey.pfx**, dat zich bevindt in de map **Retail SDK\\Reference**.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>De MPOS-app ondertekenen met vingerafdruk

Als u vingerafdrukken gebruikt om de MPOS-app te ondertekenen, installeert u het certificaat lokaal. Werk de vingerafdrukwaarde bij in het knooppunt **ModernPOSPackageCertificateThumbprint** bij in het bestand **BuildTools\\Customization.settings**.

Deze optie werkt als de buildgebruiker een lokale gebruiker is. Als u echter de Azure DevOps-agents gebruikt om de build te genereren, heeft de agent mogelijk geen toegang tot de certificaatopslag om het certificaat te gebruiken voor het ondertekenen of is het certificaat niet geïnstalleerd op de buildcomputer. In dit geval is de oplossing om de buildgebruiker te wijzigen in de lokale gebruiker en het certificaat in het vak te installeren. Deze optie werkt echter niet als u geen beheertoegang tot het vak hebt.

> [!NOTE]
> Als het .pfx-bestand of de taakoptie Veilig bestand wordt gebruikt om de app te ondertekenen, laat u het knooppunt **ModernPOSPackageCertificateThumbprint** in **Customization.settings** leeg. Als de vingerafdrukoptie wordt gebruikt, laat u **ModernPOSPackageCertificateKeyFile** leeg. Als beide waarden worden bijgewerkt, mislukt de build.

### <a name="certification-renewal"></a>Certificering verlengen

### <a name="renew-a-certificate-from-trusted-ca"></a>Een certificaat van betrouwbare CA verlengen

Neem contact op met uw certificerende instantie (CA) voor het certificaatverlengingsproces. Voor een vertrouwd certificaat hoeft er van MPOS-zijde geen actie te worden ondernomen.

### <a name="renew-a-self-signed-certificate"></a>Een zelfondertekend certificaat certificaat vernieuwen

Gebruik niet het voorbeeldcertificaat dat beschikbaar is in de Retail SDK voor productie. Het kan alleen worden gebruikt voor ontwikkelingsdoeleinden. Het voorbeeld Contoso-certificaat kan niet worden verlengd en het voorbeeldcertificaat in Retail SDK versie 10.0.16 of eerder vervalt op 31 december 2020. Als dit certificaat, of een zelfondertekend certificaat, is gebruikt om een aangepast Modern POS te ondertekenen, is het zeer goed mogelijk dat het Modern POS na deze datum niet goed werkt.
 
### <a name="impact"></a>Impact
 
Als het bovenstaande voor u geldt, zal het installatieprogramma niet meer kunnen worden uitgevoerd na 31 december 2020. Afhankelijk van het gebruikte IT-beleid van uw bedrijf is het mogelijk dat Modern POS niet kan functioneren. Het is van cruciaal belang dat u dit test door de datum tijdelijk naar een toekomstige datum te wijzigen om de invloed op uw organisatie te bepalen.
 
### <a name="steps-to-determine-the-issue"></a>Stappen om het probleem te bepalen
 
1.  Gebruik Windows-instellingen om de computerklok te wijzigen in een datum en tijd in het jaar 2021.
2.  Controleer of Modern POS kan worden geopend, of aanmelden kan plaatsvinden en een transactie kan worden voltooid.
3.  Controleer of het installatieprogramma voor de Modern POS-selfservice kan worden uitgevoerd, en zo ja, of de installatie is voltooid.
4.  Zet de Windows-klokinstellingen terug op de juiste datum en tijd.
 
Als u al deze stappen zonder problemen kunt voltooien, kunt u het huidige certificaat gebruiken na 31 december 2020.  
 
### <a name="steps-going-forward"></a>Verdere stappen 

Het wordt aangeraden het eerder gebruikte certificaat te vernieuwen. Het wordt aangeraden een nieuw certificaat te verkrijgen. Hiervoor voert u een van de volgende acties uit:
 
- **Voorkeur**: een certificaat voor code-ondertekening aanvragen bij een betrouwbare certificeringsinstantie.

- **Geen voorkeur**: een zelfondertekend certificaat voor ondertekening genereren. Dit wordt meestal alleen gebruikt voor ontwikkelingsdoeleinden binnen een domein en wordt niet aanbevolen voor productie. 

- **Beschikbaar als tijdelijke oplossing**: gebruik het vernieuwd Contoso-certificaat voor code-ondertekening. Dit wordt meestal gebruikt voor testdoeleinden, dus het wordt afgeraden om dit te gebruiken in de productie.
 
Genereer vervolgens een nieuw, aangepast Modern POS-pakket dat wordt ondertekend met dit certificaat dat wordt verkregen uit een van de bovenstaande acties. Afhankelijk van het certificaat moet een van de volgende stappen worden uitgevoerd:
 
- Als u een nieuw, vertrouwd certificaat (of een nieuw zelfondertekend certificaat) gebruikt, moet u een nieuw certificaat op elk apparaat installeren. Daarna moet u het zojuist gemaakte Modern POS-pakket (installatieprogramma) verwijderen, de bestaande toepassing ongedaan maken en vervolgens het nieuwe Modern POS-pakket opnieuw installeren. U moet op elk apparaat een activering van het Modern POS uitvoeren.

- Als u het vernieuwde Contoso-certificaat gebruikt, moet u het nieuwe certificaat op elk apparaat installeren en het Modern POS-pakket (installatieprogramma) installeren. U moet de installatie niet ongedaan maken, maar u moet het apparaat opnieuw installeren. Houd er rekening mee dat activering van een apparaat van het Modern POS niet is vereist. Deze optie is een tijdelijke oplossing. Gebruik deze optie alleen om heractivering te voorkomen en het probleem op te lossen voordat u een nieuw, vertrouwd certificaat krijgt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
