---
title: Talent inrichten
description: In dit onderwerp wordt u door het proces van het inrichten van een nieuwe omgeving voor Dynamics 365 Talent geleid.
author: andreabichsel
manager: AnnBe
ms.date: 02/18/2020
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
ms.openlocfilehash: 5bcdb50475fb341a538211cb122eb7c13067d86a
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527213"
---
# <a name="provision-talent"></a>Talent inrichten

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp wordt u door het proces van het inrichten van een nieuwe productieomgeving voor Dynamics 365 Talent geleid. In dit onderwerp wordt ervan uitgegaan dat u Talent hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). Als u een bestaande Microsoft Dynamics 365-licentie hebt waarin het Talent-serviceabonnement al is opgenomen en u de stappen in dit onderwerp niet kunt voltooien, neemt u contact op met de ondersteuning.

Om te beginnen, moet de globale beheerder zich aanmelden bij [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) en een nieuw Talent-project maken. Tenzij u vanwege een licentieprobleem Talent niet kunt inrichten, hebt u geen ondersteuning van vertegenwoordigers van de ondersteuning of DSE (Dynamics Service Engineering) nodig.

## <a name="create-an-lcs-project"></a>Een LCS-project maken
Als u LCS wilt gebruiken om Talent-omgevingen te beheren, moet u eerst een LCS-project maken.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index) met de account waarmee u zich hebt geabonneerd op Talent.

2. Selecteer het plusteken (**+**) om een project te maken.

3. Selecteer **Microsoft Dynamics 365 Talent** als de productnaam en -versie.

4. Selecteer de **Dynamics 365 Talent**-methodologie.

5. Selecteer **Maken**. 

Zie de methodologie **Talent** die u hebt gemaakt in het nieuwe project voor informatie over hoe u aan de slag gaat met Talent. Wanneer u het project hebt gemaakt, voert u de volgende procedure uit om uw Talent-omgeving in te richten.

## <a name="provision-a-talent-project"></a>Een Talent-project inrichten

Nadat u een LCS-project hebt gemaakt, kunt u Talent inrichten in een omgeving.

1. Selecteer in uw LCS-project de tegel **Beheer Talent-app**.

2. Geef aan of dit een sandbox- of productie-exemplaar van Talent is. Vroege previewfuncties kunnen beschikbaar zijn in sandbox-exemplaren om in een vroeg stadium feedback te krijgen en tests uit te voeren. 

    > [!NOTE]
    > Het exemplaartype voor Talent kan niet meer dan één keer worden gewijzigd. Controleer of het juiste exemplaartype is geselecteerd voordat u doorgaat.

    > [!NOTE]
    > Het type Talent-exemplaar staat los van het exemplaartype van de Microsoft Power Apps-omgeving die u instelt in het Power Apps-beheercentrum.

3. Selecteer de optie **Demonstratiegegevens opnemen** als u wilt dat in uw omgeving dezelfde demogegevensset wordt opgenomen die is gebruikt in de ervaring Talent-testdrive. Dit is nuttig voor de langetermijndemo of -trainingsomgevingen en mag nooit worden gebruikt voor productieomgevingen.  Houd er rekening mee dat u deze optie bij de aanvankelijke implementatie moet kiezen. U kunt een bestaande implementatie niet later bijwerken.

4. Talent wordt altijd ingericht in een Microsoft Power Apps-omgeving om de Power Apps-integratie en -uitbreidbaarheid mogelijk te maken. Lees de sectie “Een Power Apps-omgeving selecteren“ in dit onderwerp voordat u doorgaat. Als u nog geen Power Apps-omgeving hebt, selecteert u Omgevingen beheren in LCS of gaat u naar het Power Apps-beheercentrum. Volg daarna de stappen voor [Een Power Apps-omgeving maken](https://docs.microsoft.com/powerapps/administrator/create-environment).

5. Selecteer de omgeving waarin Talent moet worden ingericht.

6. Selecteer **Ja** om akkoord te gaan met de voorwaarden en te beginnen met implementeren.

    Uw nieuwe omgeving wordt weergegeven in de lijst met omgevingen in het navigatievenster aan de linkerkant. U kunt de omgeving echter pas gebruiken als de implementatiestatus is bijgewerkt naar **Geïmplementeerd**. Dit proces duurt meestal een paar minuten. Als het inrichtingsproces mislukt, moet u contact opnemen met de ondersteuning.

7. Selecteer **Aanmelden bij Talent** om uw nieuwe omgeving te gebruiken.

    > [!NOTE]
    > Als u de definitieve vereisten nog niet hebt goedgekeurd, kunt u een testexemplaar van Talent in het project implementeren. Vervolgens kunt u deze instantie gebruiken om uw oplossing te testen tot u uw goedkeuring geeft. Als u uw nieuwe omgeving voor tests gebruikt, moet u deze procedure herhalen om een productieomgeving te maken.

    > Omdat er slechts twee LCS-omgevingen zijn toegestaan als onderdeel van het Talent-abonnement, kunt u ook overwegen gebruik te maken van gratis 60 dagen [Talent-proefomgeving](https://dynamics.microsoft.com/talent/overview/). Hoewel een proefomgeving eigendom is van de gebruiker die hierom heeft verzocht, kunnen andere gebruikers worden uitgenodigd via de systeembeheerervaring voor Human Resources. Proefomgevingen bevatten fictieve gegevens die kunnen worden gebruikt om het programma op een veilige manier te verkennen. Ze zijn niet bedoeld als productieomgevingen. Wanneer een proefomgeving na 60 dagen verloopt, worden alle gegevens erin permanent verwijderd. Nadat de bestaande omgeving is verlopen, kunt u zich aanmelden voor een nieuwe proefomgeving.

## <a name="select-a-power-apps-environment"></a>Een Power Apps-omgeving selecteren

Dankzij de integratie tussen Talent en de Power Apps-omgevingen kunt u Talent-gegevens integreren en het gebruik ervan uitbreiden met Power Apps-tools. Informatie over dat het doel van Power Apps-omgevingen helpt niet alleen bij het maken van toepassingen om Talent uit te breiden, maar ook bij het selecteren van de juiste omgeving voor Talent. Zie voor meer informatie over Power Apps-omgevingen, inclusief het omgevingsbereik, omgevingstoegang en het maken en kiezen van een omgeving [Aankondiging van Power Apps-omgevingen](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Gebruik de volgende richtlijnen bij het bepalen in welke Power Apps-omgeving u Talent wilt implementeren: 

1. Selecteer in LCS **Omgevingen beheren** of ga rechtstreeks naar het Power Apps-beheercentrum waar u bestaande omgevingen weergeeft en nieuwe omgevingen maakt.

2. Eén Talent-omgeving wordt toegewezen aan één Power Apps-omgeving.

3. Een Power Apps-omgeving bevat de toepassing Talent samen met de bijbehorende Power Apps-, Power Automate- en Common Data Service-toepassingen. Als de Power Apps-omgeving wordt verwijderd, worden ook de toepassingen erin gewist. Tijdens het inrichten van een Talent-omgeving kunt u een omgeving **Proef** of **Productie** inrichten. Kies het type omgeving op basis van hoe de omgeving wordt gebruikt. 

4. Gegevensintegratie en teststrategieën moeten worden overwogen, zoals Sandbox, UAT of Productie. Het is raadzaam dat u rekening houdt met de verschillende gevolgen voor uw implementatie, aangezien de toewijzing van een Talent-omgeving aan een Power Apps-omgeving later niet eenvoudig te wijzigen is.

5. De volgende Power Apps-omgevingen kunnen niet worden gebruikt voor Talent en worden gefilterd in de selectielijst binnen LCS:
 
    - **Standaard Power Apps-omgevingen**: hoewel elke tenant automatisch een standaard Power Apps-omgeving heeft, wordt gebruik niet aanbevolen met Talent omdat alle tenantgebruikers toegang hebben tot de Power Apps-omgeving. Ze kunnen bij het testen en verkennen van de Power Apps- of Power Automate-integraties per ongeluk productiegegevens beschadigen.
   
    - **Proefomgevingen**: deze omgevingen worden gemaakt met een vervaldatum en verlopen na die tijd, waardoor uw omgeving en alle Talent-exemplaren in de omgeving automatisch worden verwijderd.
   
    - **Niet-ondersteunde regio's**: momenteel wordt Talent alleen ondersteund in de volgende gebieden: Verenigde Staten, Europa, Verenigd Koninkrijk, Australië, Canada en Azië.
  
6. Nadat u hebt vastgesteld welke omgeving de juiste is om te gebruiken, kunt u doorgaan met het inrichtingsproces. 
 
## <a name="grant-access-to-the-environment"></a>Toegang verlenen tot de omgeving

Standaard heeft de globale beheerder die de omgeving heeft gemaakt toegang tot deze omgeving. Aan alle overige gebruikers van de toepassing moet echter uitdrukkelijk toestemming worden verleend. Om toegang te verlenen moet u gebruikers toevoegen en de juiste rollen aan deze gebruikers toewijzen in de Human Resources-omgeving. De globale beheerder die Talent heeft geïmplementeerd, moet ook Attract en Onboard starten om de initialisatie te voltooien en toegang in te schakelen voor andere tenantgebruikers.  Totdat dit gebeurt, kunnen andere gebruikers geen toegang krijgen tot Attract en Onboard en krijgen ze toegangsovertredingsfouten. Zie voor meer informatie [Nieuwe gebruikers maken](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) en [Gebruikers toewijzen aan beveiligingsrollen](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]