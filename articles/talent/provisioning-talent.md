---
title: Talent inrichten
description: In dit onderwerp wordt u door het proces van het inrichten van een nieuwe omgeving voor Dynamics 365 for Talent geleid.
author: andreabichsel
manager: AnnBe
ms.date: 00/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: 17271
ms.assetid: ba1ad49d-8232-400e-b11f-525423506a3f
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-11-20
ms.dyn365.ops.version: Talent July 2017 update
ms.openlocfilehash: 98f60e466b8b97215fdba0f48ca53ca57157283b
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517715"
---
# <a name="provision-talent"></a>Talent inrichten

[!include [banner](includes/banner.md)]

In dit onderwerp wordt u door het proces van het inrichten van een nieuwe productieomgeving voor Dynamics 365 for Talent geleid. In dit onderwerp wordt ervan uitgegaan dat u Talent hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). Als u een bestaande Microsoft Dynamics 365-licentie hebt waarin het Talent-serviceabonnement al is opgenomen en u de stappen in dit onderwerp niet kunt voltooien, neemt u contact op met de ondersteuning.

Om te beginnen, moet de globale beheerder zich aanmelden bij [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) en een nieuw Talent-project maken. Tenzij u vanwege een licentieprobleem Talent niet kunt inrichten, hebt u geen ondersteuning van vertegenwoordigers van de ondersteuning of DSE (Dynamics Service Engineering) nodig.

## <a name="create-an-lcs-project"></a>Een LCS-project maken
Als u LCS wilt gebruiken om Talent-omgevingen te beheren, moet u eerst een LCS-project maken.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index) met de account waarmee u zich hebt geabonneerd op Talent.
2. Selecteer het plusteken (**+**) om een project te maken.
3. Selecteer **Microsoft Dynamics 365 for Talent** als de productnaam en -versie.
4. Selecteer de **Dynamics 365 for Talent**-methodologie.
5. Selecteer **Maken**.

Zie de methodologie **Talent** die u hebt gemaakt in het nieuwe project voor informatie over hoe u aan de slag gaat met Talent. Wanneer u het project hebt gemaakt, voert u de volgende procedure uit om uw Talent-omgeving in te richten.

## <a name="provision-a-talent-project"></a>Een Talent-project inrichten
Nadat u een LCS-project hebt gemaakt, kunt u Talent inrichten in een omgeving.

1. Selecteer in uw LCS-project de tegel **Beheer Talent-app**.
2. Talent wordt altijd ingericht in een Microsoft PowerApps-omgeving om de PowerApps-integratie en -uitbreidbaarheid mogelijk te maken. Lees de sectie “Een PowerApps-omgeving selecteren“ in dit onderwerp voordat u doorgaat. Als u nog geen PowerApps-omgeving hebt, selecteert u Omgevingen beheren in LCS of gaat u naar het PowerApps-beheercentrum. Volg daarna de stappen voor het [Maken van een PowerApps-omgeving](https://docs.microsoft.com/en-us/powerapps/administrator/create-environment).

    > [!NOTE]
    > Om bestaande omgevingen weer te geven of nieuwe omgevingen te maken, moet de tenantbeheerder die Talent inricht, worden toegewezen aan de PowerApps P2-licentie. Als uw organisatie geen PowerApps P2-licentie heeft, kunt u er een krijgen van uw provider van cloudoplossingen of downloaden via de [pagina met PowerApps-prijzen](https://powerapps.microsoft.com/en-us/pricing/).

4. Selecteer **Toevoegen** en selecteer de omgeving waarin Talent moet worden ingericht.
5. Selecteer de optie **Demonstratiegegevens opnemen** als u wilt dat in uw omgeving dezelfde demogegevensset wordt opgenomen die is gebruikt in de ervaring Talent-testdrive. Dit is nuttig voor de langetermijndemo of -trainingsomgevingen en mag nooit worden gebruikt voor productieomgevingen.  Houd er rekening mee dat u deze optie bij de aanvankelijke implementatie moet kiezen. U kunt een bestaande implementatie niet later bijwerken.
6. Selecteer **Ja** om akkoord te gaan met de voorwaarden en te beginnen met implementeren.

    Uw nieuwe omgeving wordt weergegeven in de lijst met omgevingen in het navigatievenster aan de linkerkant. U kunt de omgeving echter pas gebruiken als de implementatiestatus is bijgewerkt naar **Geïmplementeerd**. Dit proces duurt meestal een paar minuten. Als het inrichtingsproces mislukt, moet u contact opnemen met de ondersteuning.

7. Selecteer **Aanmelden bij Talent** om uw nieuwe omgeving te gebruiken.

    > [!NOTE]
    > Als u de definitieve vereisten nog niet hebt goedgekeurd, kunt u een testexemplaar van Talent in het project implementeren. Vervolgens kunt u deze instantie gebruiken om uw oplossing te testen tot u uw goedkeuring geeft. Als u uw nieuwe omgeving voor tests gebruikt, moet u deze procedure herhalen om een productieomgeving te maken.

    > Omdat er slechts twee LCS-omgevingen zijn toegestaan als onderdeel van het Talent-abonnement, kunt u ook overwegen gebruik te maken van gratis 60 dagen [Talent-proefomgeving](https://dynamics.microsoft.com/en-us/talent/overview/). Hoewel een proefomgeving eigendom is van de gebruiker die hierom heeft verzocht, kunnen andere gebruikers worden uitgenodigd via de systeembeheerervaring voor HR Core. Proefomgevingen bevatten fictieve gegevens die kunnen worden gebruikt om het programma op een veilige manier te verkennen. Ze zijn niet bedoeld als productieomgevingen. Wanneer een proefomgeving na 60 dagen verloopt, worden alle gegevens erin permanent verwijderd. Nadat de bestaande omgeving is verlopen, kunt u zich aanmelden voor een nieuwe proefomgeving.

## <a name="select-a-powerapps-environment"></a>Een PowerApps-omgeving selecteren

Dankzij de integratie tussen Talent en de PowerApps-omgevingen kunt u Talent-gegevens integreren en het gebruik ervan uitbreiden met PowerApps-tools. Informatie over dat het doel van PowerApps-omgevingen helpt niet alleen bij het maken van toepassingen om Talent uit te breiden, maar ook bij het selecteren van de juiste omgeving voor Talent. Zie voor meer informatie over PowerApps-omgevingen, inclusief het omgevingsbereik, omgevingstoegang en het maken en kiezen van een omgeving [Aankondiging van PowerApps-omgevingen](https://powerapps.microsoft.com/en-us/blog/powerapps-environments/). 

Gebruik de volgende richtlijnen bij het bepalen in welke PowerApps-omgeving u Talent wilt implementeren: 

1. Selecteer in LCS **Omgevingen beheren** of ga rechtstreeks naar het PowerApps-beheercentrum waar u bestaande omgevingen weergeeft en nieuwe omgevingen maakt.
2. Eén Talent-omgeving wordt toegewezen aan één PowerApps-omgeving.
3. Een PowerApps-omgeving ´bevat´ de toepassing Talent samen met de bijbehorende PowerApps-, Flow- en Common Data Service-toepassingen. Als de PowerApps-omgeving wordt verwijderd, worden ook de toepassingen erin gewist. Tijdens het inrichten van een Talent-omgeving kan 'Proef' of 'Productie' worden ingericht. Kies het type omgeving op basis van hoe de omgeving wordt gebruikt. 
4. Gegevensintegratie en teststrategieën moeten worden overwogen, zoals Sandbox, UAT of Productie. Het is raadzaam dat u rekening houdt met de verschillende gevolgen voor uw implementatie, aangezien de toewijzing van een Talent-omgeving aan een PowerApps-omgeving later niet eenvoudig te wijzigen is.
5. De volgende PowerApps-omgevingen kunnen niet worden gebruikt voor Talent en worden gefilterd in de selectielijst binnen LCS:
 
    - **Standaard PowerApps-omgevingen**: hoewel elke tenant automatisch een standaard PowerApps-omgeving heeft, wordt gebruik niet aanbevolen met Talent omdat alle tenantgebruikers toegang hebben tot de PowerApps-omgeving. Ze kunnen bij het testen en verkennen van de PowerApps- of Flow-integraties per ongeluk productiegegevens beschadigen.
   
    - **Proefomgevingen**: deze omgevingen worden gemaakt met een vervaldatum en verlopen na die tijd, waardoor uw omgeving en alle Talent-exemplaren in de omgeving automatisch worden verwijderd.
   
    - **Niet-ondersteunde regio's**: momenteel wordt Talent alleen ondersteund in de volgende gebieden: Verenigde Staten, Europa, Verenigd Koninkrijk en Australië.
  
6. Nadat u hebt vastgesteld welke omgeving de juiste is om te gebruiken, kunt u doorgaan met het inrichtingsproces. 
 
## <a name="grant-access-to-the-environment"></a>Toegang verlenen tot de omgeving
Standaard heeft de globale beheerder die de omgeving heeft gemaakt toegang tot deze omgeving. Aan alle overige gebruikers van de toepassing moet echter uitdrukkelijk toestemming worden verleend. Om toegang te verlenen moet u gebruikers toevoegen en de juiste rollen aan deze gebruikers toewijzen in de Core HR-omgeving. De globale beheerder die Talent heeft geïmplementeerd, moet ook de toepassingen Attract en Onboard starten om de initialisatie te voltooien en toegang in te schakelen voor andere tenantgebruikers.  Totdat dit gebeurt, kunnen andere gebruikers geen toegang krijgen tot de toepassingen Attract en Onboard en krijgen ze toegangsovertredingsfouten. Zie voor meer informatie [Nieuwe gebruikers maken](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) en [Gebruikers toewijzen aan beveiligingsrollen](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 
