---
title: Human Resources inrichten
description: In dit onderwerp wordt u door het proces van het inrichten van een nieuwe productieomgeving voor Dynamics 365 Human Resources geleid.
author: andreabichsel
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 2632616834e405d31facdcf3853baaf96066e9aa
ms.sourcegitcommit: e6437d994c3be0c5bb4a9263af3aa8351020d83a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/14/2021
ms.locfileid: "6248816"
---
# <a name="provision-human-resources"></a>Human Resources inrichten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

In dit onderwerp wordt u door het proces van het inrichten van een nieuwe productieomgeving voor Dynamics 365 Human Resources geleid. In dit onderwerp wordt ervan uitgegaan dat u Human Resources hebt aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). Als u een bestaande Microsoft Dynamics 365-licentie hebt waarin het Human Resources-serviceabonnement al is opgenomen en u de stappen in dit artikel niet kunt voltooien, neemt u contact op met de ondersteuning.

Om te beginnen, moet de globale beheerder zich aanmelden bij [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) en een nieuw Human Resources-project maken. Tenzij u vanwege een licentieprobleem Human Resources niet kunt inrichten, hebt u geen ondersteuning van vertegenwoordigers van de ondersteuning of DSE (Dynamics Service Engineering) nodig.

## <a name="provision-a-human-resources-trial-environment"></a>Een Human Resources-proefomgeving inrichten

Voordat u uw eerste sandbox- of productieomgeving inricht, kunt u een [Human Resources-proefomgeving](https://go.microsoft.com/fwlink/p/?LinkId=2115962) inrichten om de Human Resources-functionaliteit te valideren. Proefomgevingen bevatten fictieve gegevens die kunnen worden gebruikt om het programma op een veilige manier te verkennen. Hoewel een proefomgeving eigendom is van de gebruiker die hierom heeft verzocht, kunnen andere gebruikers worden uitgenodigd via de systeembeheerervaring voor Human Resources. 

Proefomgevingen zijn niet bedoeld als productieomgevingen. Proefomgevingen zijn beperkt tot een periode van 60 dagen. Wanneer een proefperiode verloopt, worden de omgeving en alle gegevens erin permanent verwijderd. De omgeving kan niet worden geconverteerd naar een sandbox of een productieomgeving. Nadat de bestaande omgeving is verlopen, kunt u zich aanmelden voor een nieuwe proefomgeving.

## <a name="plan-human-resources-environments"></a>Human Resources-omgevingen plannen

Voordat u uw eerste Human Resources-omgeving maakt, moet u de omgevingsbehoeften voor uw project zorgvuldig plannen. Een basisabonnement op Human Resources omvat twee omgevingen: een productieomgeving en een werkomgeving. Afhankelijk van de complexiteit van uw project moet u mogelijk extra omgevingen voor uw bedrijf aanschaffen ter ondersteuning van projectactiviteiten. 

Voor extra omgevingen is onder andere het volgende van belang:

- **Gegevensmigratie**: mogelijk moet u rekening houden met een extra omgeving voor gegevensmigratieactiviteiten, zodat uw omgeving kan worden gebruikt voor testdoeleinden tijdens het project. Als u een extra omgeving hebt, kunnen activiteiten voor gegevensmigratie worden voortgezet terwijl de test- en configuratieactiviteiten gelijktijdig plaatsvinden in een andere omgeving.
- **Integratie**: mogelijk moet u rekening houden met een extra omgeving voor het configureren en testen van integraties. Dit kan native integraties omvatten, zoals de Ceridian Dayforce LinkedIn Talent Hub-integraties, of aangepaste integraties, zoals die voor salarisadministratie, volgsystemen voor sollicitanten of vergoedingssystemen en leveranciers.
- **Training**: u hebt mogelijk een afzonderlijke omgeving nodig die is geconfigureerd met een set trainingsgegevens om uw werknemers te trainen het nieuwe systeem te gebruiken. 
- **Project met meerdere fasen**: u hebt mogelijk een extra omgeving nodig voor configuratie, gegevensmigratie, testen of andere activiteiten in een projectfase die is gepland na de eerste keer live gaan van het project.

 > [!IMPORTANT]
 > Het is raadzaam uw productieomgeving in uw gehele project te gebruiken als uw GOLD-configuratieomgeving. Dit is belangrijk, omdat u een sandbox-omgeving niet naar een productieomgeving kunt kopiëren. Wanneer u live gaat, is uw GOLD-omgeving uw productieomgeving en zult u uw wijzigingsactiviteiten in deze omgeving voltooien.</br></br>
 > We raden u aan uw werkomgeving of een andere omgeving te gebruiken voor het uitvoeren van een simulatie-cutover voordat u live gaat. U kunt dit doen door de productieomgeving te vernieuwen met uw GOLD-configuratie in uw sandbox-werkomgeving.</br></br>
 > Het is raadzaam een gedetailleerde cutover-controlelijst bij te houden, inclusief alle gegevenspakketten die nodig zijn om de definitieve gegevens naar de productieomgeving te migreren tijdens de go-live cutover.</br></br>
 > Het is ook raadzaam uw sandbox-omgeving in uw gehele project te gebruiken als uw TEST-omgeving. Als u extra omgevingen nodig hebt, kan uw organisatie ze voor bijkomende kosten inkopen.</br></br>

## <a name="create-an-lcs-project"></a>Een LCS-project maken

Als u LCS wilt gebruiken om Human Resources-omgevingen te beheren, moet u eerst een LCS-project maken.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index) met de account waarmee u zich hebt geabonneerd op Human Resources.

   > [!NOTE]
   > Om te zorgen voor een goede inrichting, moet de account waarmee u de Human Resources-omgeving inricht zijn toegewezen aan de rol **Systeembeheerder** of **Systeemaanpasser** in de Power Apps-omgeving die is gekoppeld aan de Human Resources-omgeving. Meer informatie over het toewijzen van beveiligingsrollen aan gebruikers in Power Platform vindt u in [Beveiliging van gebruikers configureren voor bronnen](/power-platform/admin/database-security).

2. Selecteer het plusteken (**+**) om een project te maken.

3. Selecteer **Microsoft Dynamics 365 Human Resources** als de productnaam en -versie.

4. Selecteer de **Dynamics 365 Human Resources**-methodologie.

5. Selecteer **Maken**.

Zie de **Human Resources**-methodologie die u hebt gemaakt in het nieuwe project voor informatie over hoe u aan de slag gaat met Human Resources. Wanneer u het project hebt gemaakt, voert u de volgende procedure uit om uw Human Resources-omgeving in te richten.

## <a name="provision-a-human-resources-project"></a>Een Human Resources-project inrichten

Nadat u een LCS-project hebt gemaakt, kunt u Human Resources inrichten in een omgeving.

1. Selecteer in uw LCS-project de tegel **Beheer Human Resources-app**.

2. Geef aan of deze omgeving een sandbox- of productie-exemplaar van Human Resources is. Vroege previewfuncties kunnen beschikbaar zijn in sandbox-exemplaren om in een vroeg stadium feedback te krijgen en tests uit te voeren.
   
    > [!NOTE]
    > Het exemplaartype voor Human Resources kan niet meer dan één keer worden gewijzigd. Controleer of het juiste exemplaartype is geselecteerd voordat u doorgaat.</br></br>
    > Het Human Resources-exemplaar type staat los van het exemplaartype van de Microsoft Power Apps-omgeving dat u instelt in het Power Apps-beheercentrum.
    
3. Selecteer de optie **Demogegevens opnemen** als u wilt dat in uw omgeving dezelfde demogegevensset wordt opgenomen die is gebruikt in de Human Resources-testdrive. Demogegevens zijn nuttig voor de langetermijndemo of -trainingsomgevingen en mogen nooit worden gebruikt voor productieomgevingen. U moet deze optie bij de aanvankelijke implementatie kiezen. U kunt een bestaande implementatie niet later bijwerken.

4. Human Resources wordt altijd ingericht in een Microsoft Power Apps-omgeving om de Power Apps-integratie en -uitbreidbaarheid mogelijk te maken. Lees de sectie 'Een Power Apps-omgeving selecteren' van dit artikel voor u doorgaat. Als u nog geen Power Apps-omgeving hebt, selecteert u Omgevingen beheren in LCS of gaat u naar het Power Apps-beheercentrum. Volg daarna de stappen voor [Een Power Apps-omgeving maken](/powerapps/administrator/create-environment).

5. Selecteer de omgeving waarin Human Resources moet worden ingericht.

6. Selecteer **Ja** om akkoord te gaan met de voorwaarden en te beginnen met implementeren.

   Uw nieuwe omgeving wordt weergegeven in de lijst met omgevingen in het navigatievenster aan de linkerkant. U kunt de omgeving echter pas gebruiken als de implementatiestatus is bijgewerkt naar **Geïmplementeerd**. Dit proces duurt meestal een paar minuten. Als het inrichtingsproces mislukt, moet u contact opnemen met de ondersteuning.

7. Selecteer **Aanmelden bij Human Resources** om uw nieuwe omgeving te gebruiken.

    > [!NOTE]
    > Als u de definitieve vereisten nog niet hebt goedgekeurd, kunt u een testexemplaar van Human Resources in het project implementeren. Vervolgens kunt u deze instantie gebruiken om uw oplossing te testen tot u uw goedkeuring geeft. Als u uw nieuwe omgeving voor tests gebruikt, moet u deze procedure herhalen om een productieomgeving te maken.

## <a name="select-a-power-apps-environment"></a>Een Power Apps-omgeving selecteren

U kunt het gebruik van Human Resources-gegevens integreren en uitbreiden met Power Apps-hulpmiddelen. Zie voor meer informatie over Power Apps-omgevingen, inclusief het omgevingsbereik, omgevingstoegang en het maken en kiezen van een omgeving [Aankondiging van Power Apps-omgevingen](https://powerapps.microsoft.com/blog/powerapps-environments/). 

Gebruik de volgende richtlijnen bij het bepalen in welke Power Apps-omgeving u Human Resources wilt implementeren: 

1. Selecteer **Omgevingen beheren** in LCS. U kunt ook rechtstreeks naar het Power Apps-beheercentrum gaan waar u bestaande omgevingen kunt weergeven en nieuwe omgevingen kunt maken.

2. Eén Human Resources-omgeving wordt toegewezen aan één Power Apps-omgeving.

3. Een Power Apps-omgeving bevat de toepassing Human Resources samen met de bijbehorende Power Apps-, Power Automate- en Dataverse-toepassingen. Als de Power Apps-omgeving wordt verwijderd, worden ook de toepassingen erin gewist. Tijdens het inrichten van een Human Resources-omgeving kunt u een omgeving **Proef** of **Productie** inrichten. Kies het type omgeving op basis van hoe de omgeving wordt gebruikt. 

4. Gegevensintegratie en teststrategieën moeten worden overwogen, zoals Sandbox, UAT of Productie. Het is raadzaam dat u rekening houdt met de verschillende gevolgen voor uw implementatie, aangezien de toewijzing van een Human Resources-omgeving aan een Power Apps-omgeving later niet eenvoudig te wijzigen is.

5. U kunt de volgende Power Apps-omgevingen niet gebruiken voor Human Resources. Ze worden gefilterd op basis van de selectielijst in LCS:
 
    - **Standaard Power Apps-omgevingen**: hoewel elke tenant automatisch wordt ingericht met een standaard Power Apps-omgeving, is het niet raadzaam deze te gebruiken met Human Resources. Alle tenantgebruikers hebben toegang tot de Power Apps-omgeving en kunnen onbedoeld productiegegevens beschadigen tijdens het testen en verkennen van Power Apps- of Power Automate-integraties.
   
    - **Proefomgevingen**: deze omgevingen worden met een vervaldatum gemaakt. Na de vervaldatum worden uw omgeving en eventuele exemplaren van Human Resources die zich in de omgeving bevinden, automatisch verwijderd.
   
    - **Niet-ondersteunde regio's**: De omgeving moet zich in een ondersteunde geografie bevinden. Meer informatie over dit onderwerp vindt u in [Ondersteunde geografieën](hr-admin-setup-provision.md#supported-geographies).

6. Nadat u hebt vastgesteld welke omgeving de juiste is om te gebruiken, kunt u doorgaan met het inrichtingsproces. 

### <a name="supported-geographies"></a>Ondersteunde geografieën

Op dit moment ondersteunt Human Resources de volgende geografieën:

- Verenigde Staten
- Europa
- Verenigd Koninkrijk
- Australië
- Canada
- Azië 

Wanneer u een Human Resources-omgeving maakt, selecteert u een Power Apps-omgeving die u aan de Human Resources-omgeving koppelt. De Human Resources-omgeving wordt vervolgens ingericht in dezelfde Azure-geografie als de geselecteerde Power Apps-omgeving. U kunt selecteren waar de Human Resources-omgeving en database fysiek aanwezig zijn, door de geografische regio te selecteren wanneer u de Power Apps-omgeving maakt die u aan de Human Resources-omgeving koppelt.

U kunt de Azure-*geografie* selecteren waarin de omgeving wordt ingericht, maar u kunt niet de specifieke Azure-*regio* selecteren. Door middel van automatisering wordt de specifieke regio binnen de geografie bepaald waarin de omgeving wordt gemaakt, om de taakverdeling en prestaties te optimaliseren. Informatie over Azure-geografieën en regio's vindt u in de documentatie over [Azure-geografieën](https://azure.microsoft.com/global-infrastructure/geographies).

De gegevens voor de Human Resources-omgeving worden altijd opgenomen in de Azure-geografie waarin deze worden gemaakt. De omgeving wordt echter niet altijd in dezelfde Azure-regio opgenomen. Ten behoeve van herstel na noodgevallen worden de gegevens gerepliceerd in zowel de primare Azure-regio als ook in een tweede failover-regio binnen dezelfde geografie.

 > [!NOTE]
 > Het migreren van een Human Resources-omgeving van de ene Azure-regio naar een andere wordt niet ondersteund.

## <a name="grant-access-to-the-environment"></a>Toegang verlenen tot de omgeving

Standaard heeft de globale beheerder die de omgeving heeft gemaakt toegang tot deze omgeving. Aan alle overige gebruikers van de toepassing moet u uitdrukkelijk toestemming verlenen. U moet gebruikers toevoegen en de juiste rollen aan deze gebruikers toewijzen in de Human Resources-omgeving. De globale beheerder die Human Resources heeft geïmplementeerd, moet ook Attract en Onboard starten om de initialisatie te voltooien en toegang in te schakelen voor andere tenantgebruikers. Totdat dit gebeurt, kunnen andere gebruikers geen toegang krijgen tot Attract en Onboard en krijgen ze toegangsovertredingsfouten. Zie voor meer informatie [Nieuwe gebruikers maken](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) en [Gebruikers toewijzen aan beveiligingsrollen](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
