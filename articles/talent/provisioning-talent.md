---
title: Talent inrichten
description: In dit onderwerp wordt u door het proces van het inrichten van een nieuwe omgeving voor Microsoft Dynamics 365 for Talent geleid.
author: rschloma
manager: AnnBe
ms.date: 11/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: 2fc4119f3b33aa583274f4d823e296752cdde41d
ms.contentlocale: nl-nl
ms.lasthandoff: 08/08/2018

---
# <a name="provision-talent"></a>Talent inrichten

[!include [banner](includes/banner.md)]

In dit onderwerp wordt u door het proces van het inrichten van een nieuwe productieomgeving voor Microsoft Dynamics 365 for Talent geleid. In dit onderwerp wordt ervan uitgegaan dat u Talent hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). Als u een bestaande Microsoft Dynamics 365-licentie hebt waarin het Talent-serviceabonnement al is opgenomen en u de stappen in dit onderwerp niet kunt voltooien, neemt u contact op met de ondersteuning.

Om te beginnen, moet de globale beheerder zich aanmelden bij [Microsoft Dynamics Lifecycle Services](http://lcs.dynamics.com) (LCS) en een nieuw Talent-project maken. Tenzij u vanwege een licentieprobleem Talent niet kunt inrichten, hebt u geen ondersteuning van vertegenwoordigers van de ondersteuning of DSE (Dynamics Service Engineering) nodig.

## <a name="create-an-lcs-project"></a>Een LCS-project maken
Als u LCS wilt gebruiken om Talent-omgevingen te beheren, moet u eerst een LCS-project maken.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index) met de account waarmee u zich hebt geabonneerd op Talent.
2. Selecteer het plusteken (**+**) om een project te maken.
3. Selecteer **Microsoft Dynamics 365 for Talent** als de productnaam en -versie.
4. Selecteer de methodologie **Dynamics 365 for Talent**.
5. Selecteer **Maken**.

Zie de methodologie **Talent** die u hebt gemaakt in het nieuwe project voor informatie over hoe u aan de slag gaat met Talent. Wanneer u het project hebt gemaakt, voert u de volgende procedure uit om uw Talent-omgeving in te richten.

## <a name="provision-a-talent-project"></a>Een Talent-project inrichten
Nadat u een LCS-project hebt gemaakt, kunt u Talent inrichten in een omgeving.

1. Selecteer in uw LCS-project de tegel **Beheer Talent-app**.
2. Talent wordt altijd ingericht in een Microsoft PowerApps-omgeving om de PowerApps-integratie en -uitbreidbaarheid mogelijk te maken. Lees de sectie “Een PowerApps-omgeving selecteren“ in dit onderwerp voordat u doorgaat. 
3. Als u nog geen PowerApps-omgeving hebt, volgt u de stappen in de sectie Een nieuwe PowerApps-omgeving maken (indien vereist) van dit onderwerp voordat u doorgaat.

    > [!NOTE]
    > Om bestaande omgevingen weer te geven of nieuwe omgevingen te maken, moet de tenantbeheerder die Talent inricht, worden toegewezen aan de PowerApps P2-licentie. Als uw organisatie geen PowerApps P2-licentie heeft, kunt u er een krijgen van uw provider van cloudoplossingen of downloaden via de [pagina met PowerApps-prijzen](https://powerapps.microsoft.com/en-us/pricing/).

4. Selecteer **Toevoegen** en selecteer de omgeving waarin Talent moet worden ingericht.
5. Selecteer de optie 'Demonstratiegegevens opnemen' als u wilt dat in uw omgeving dezelfde Demogegevensset wordt opgenomen die is gebruikt in de ervaring Talent-testdrive.  Dit is nuttig voor de langetermijndemo of -trainingsomgevingen en mag nooit worden gebruikt voor productieomgevingen.  Houd er rekening mee dat u deze optie moet kiezen bij de aanvankelijke implementatie en niet later een bestaande installatie kunt bijwerken.
6. Selecteer **Ja** om akkoord te gaan met de voorwaarden en te beginnen met implementeren.

    Uw nieuwe omgeving wordt weergegeven in de lijst met omgevingen in het navigatievenster aan de linkerkant. U kunt de omgeving echter pas gebruiken als de implementatiestatus is bijgewerkt naar **Geïmplementeerd**. Dit proces duurt meestal een paar minuten. Als het inrichtingsproces mislukt, moet u contact opnemen met de ondersteuning.

7. Selecteer **Aanmelden bij Talent** om uw nieuwe omgeving te gebruiken.

> [!NOTE]
> Als u de definitieve vereisten nog niet hebt goedgekeurd, kunt u een testexemplaar van Talent in het project implementeren. Vervolgens kunt u deze instantie gebruiken om uw oplossing te testen tot u uw goedkeuring geeft. Als u uw nieuwe omgeving voor tests gebruikt, moet u deze procedure herhalen om een productieomgeving te maken.

> [!NOTE]
> Omdat er slechts twee LCS-omgevingen zijn toegestaan als onderdeel van het Talent-abonnement, kunt u ook overwegen gebruik te maken van gratis 60 dagen [Talent- proefomgeving](https://dynamics.microsoft.com/en-us/talent/overview/). Hoewel een proefomgeving eigendom is van de gebruiker die hierom heeft verzocht, kunnen andere gebruikers worden uitgenodigd via de systeembeheerervaring voor HR Core. Proefomgevingen bevatten fictieve gegevens die kunnen worden gebruikt om het programma op een veilige manier te verkennen. Ze zijn niet bedoeld als productieomgevingen. Wanneer een proefomgeving na 60 dagen verloopt, worden alle gegevens erin permanent verwijderd. Nadat de bestaande omgeving is verlopen, kunt u zich aanmelden voor een nieuwe proefomgeving.

## <a name="select-a-powerapps-environment"></a>Een PowerApps-omgeving selecteren

Dankzij de integratie tussen Talent en de PowerApps-omgevingen kunt u Talent-gegevens integreren en het gebruik ervan uitbreiden met PowerApps-tools. Informatie over dat het doel van PowerApps-omgevingen helpt niet alleen bij het maken van toepassingen om Talent uit te breiden, maar ook bij het selecteren van de juiste omgeving voor Talent. Zie voor meer informatie over PowerApps-omgevingen, inclusief het omgevingsbereik, omgevingstoegang en het maken en kiezen van een omgeving [Aankondiging van PowerApps-omgevingen](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Gebruik de volgende richtlijnen bij het bepalen in welke PowerApps-omgeving u Talent wilt implementeren: 
1. Selecteer in LCS Omgevingen beheren of navigeer rechtstreeks naar het PowerApps-beheercentrum waar u bestaande omgevingen weergeeft en nieuwe omgevingen maakt.
2. Eén Talent-omgeving wordt toegewezen aan één PowerApps-omgeving.
3. Een PowerApps-omgeving bevat de toepassing Talent samen met de bijbehorende PowerApps-, Flow- en CDS-toepassingen. Als de PowerApps-omgeving wordt verwijderd, worden ook de toepassingen erin gewist.
4. Gegevensintegratie en teststrategieën moeten worden overwogen. Bijvoorbeeld: sandbox, UAT, productie. Daarom is het raadzaam dat u rekening houdt met de verschillende gevolgen voor uw implementatie, aangezien de toewijzing van een Talent-omgeving aan een PowerApps-omgeving later niet eenvoudig te wijzigen is.
5. De volgende PowerApps-omgevingen kunnen niet worden gebruikt voor Talent en worden gefilterd in de selectielijst binnen LCS:
 
    **CDS 2.0-omgevingen** CDS 2.0 is beschikbaar vanaf 21 maart 2018. Maar Talent ondersteunt CDS 2.0 nog niet. Hoewel u CDS 2.0-databases wel kunt bekijken en maken in het PowerApps-beheercentrum, kunnen ze niet meer worden gebruikt in Talent. De optie om CDS 2.0-omgevingen te gebruiken in Talent-implementaties, zal op een later tijdstip beschikbaar zijn.
   
   > [!Note]
   > Als u het verschil wilt zien tussen CDS 1.0- en 2.0-omgevingen in de beheerportal, selecteert u een omgeving en kijkt u naar **Details**. Voor CDS 2.0-omgevingen geldt 'U kunt deze instellingen beheren in het Dynamics 365-beheercentrum', dat ze verwijzen naar een instantieversie en geen tabblad Database hebben. 
 
   **Standaard PowerApps-omgevingen** Hoewel elke tenant automatisch een standaard PowerApps-omgeving heeft, wordt gebruik niet aanbevolen met Talent omdat alle tenantgebruikers toegang hebben tot de PowerApps-omgeving. Ze kunnen bij het testen en verkennen van de PowerApps- of Flow-integraties per ongeluk productiegegevens beschadigen.
   
   <strong>TestDrive-omgevingen</strong> Omgevingen met een naam als 'TestDrive: alias@domain' worden gemaakt met een vervalperiode van 60 dagen en verlopen na die tijd, waardoor de omgeving automatisch wordt verwijderd.
   
   **Niet-ondersteunde regio's** Momenteel wordt Talent alleen ondersteund in de volgende gebieden: Verenigde Staten, Europa en Australië.
  
6. Er is geen specifieke actie als u de juiste omgeving voor gebruik hebt vastgesteld. Ga door met het inrichtingsproces. 
 
## <a name="create-a-new-powerapps-environment-if-required"></a>Een nieuwe PowerApps-omgeving maken (indien vereist)

Voer een PowerShell-script uit voor het maken van een nieuwe PowerApps-omgeving voor Talent als de tenantbeheerder de licentie PowerApps Plan 2 heeft. Het script automatiseert de volgende stappen:


 + Een PowerApps-omgeving maken
 + Een CDS 1.0-database maken
 + Alle voorbeeldgegevens in de CDS 1.0-database wissen


Voer de volgende instructies uit voor het script:

1. Download het bestand ProvisionCDSEnvironment.zip van de volgende locatie: [ProvisionCDSEnvironment scripts](https://go.microsoft.com/fwlink/?linkid=870436)  

2. Klik vanuit de downloadmap met de rechtermuisknop op het bestand ProvisionCDSEnvironment.zip dat zojuist is gedownload en selecteer **Eigenschappen**.  Als er een beveiligingsopmerking onderaan in het dialoogvenster staat met de tekst 'Dit bestand is afkomstig van een andere computer en wordt mogelijk geblokkeerd om deze computer te beveiligen', schakelt u het selectievakje in op **Deblokkeren** en klikt u vervolgens op **Toepassen** en dan op **OK**.

3. Pak de volledige inhoud van het bestand ProvisionCDSEnviroinment.zip uit in een andere map dan uw basismap.

4. Voer het programma Windows PowerShell of Windows PowerShell ISE uit als beheerder.

   Ga naar het onderwerp [Uitvoeringsbeleid instellen](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/set-executionpolicy?view=powershell-6) voor meer informatie over het instellen van het uitvoeringsbeleid zodat scripts kunnen worden uitgevoerd. Het is raadzaam de volgende ' Set-uitvoeringsbeleid -uitvoeringsbeleid onbeperkt - bereikproces' te gebruiken, maar zorg ervoor het beveiligingsbeleid van uw bedrijf te volgen en het venster PowerShell te sluiten na voltooiing. 
  
5. Ga in PowerShell naar de map waarin u het bestand hebt uitgepakt en voer de volgende opdracht uit waarbij u de waarden vervangt zoals hieronder wordt aangegeven:
 
   ```.\ProvisionCDSEnvironment -EnvironmentName MyNewEnvironment -Location YourLocation```

    
   **MyNewEnvironment** moet worden vervangen door de naam van uw omgeving. Deze naam wordt weergegeven in LCS en is zichtbaar als gebruikers selecteren welke Talent-omgeving ze willen gebruiken. 

   **YourLocation** moet worden vervangen door een van de ondersteunde regio's voor Talent: Verenigde staten, Europa, australië. 

   **-Uitgebreid** is optioneel en biedt gedetailleerde informatie voor support als er problemen optreden.

6. Ga door met het inrichtingsproces.
 

## <a name="grant-access-to-the-environment"></a>Toegang verlenen tot de omgeving
Standaard heeft de globale beheerder die de omgeving heeft gemaakt toegang tot deze omgeving. Aan alle overige gebruikers van de toepassing moet echter uitdrukkelijk toestemming worden verleend. U kunt toegang verlenen door [gebruikers toe te voegen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) en [de juiste rollen aan deze gebruikers toe te wijzen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles) in de Core HR-omgeving. De globale beheerder die Talent heeft geïmplementeerd, moet ook de toepassingen Attract en Onboard starten om de initialisatie te voltooien en toegang in te schakelen voor andere tenantgebruikers.  Totdat dit gebeurt, kunnen andere gebruikers geen toegang krijgen tot de toepassingen Attract en Onboard en krijgen ze toegangsovertredingsfouten.


