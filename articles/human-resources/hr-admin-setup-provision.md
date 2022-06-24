---
title: Human Resources inrichten
description: In dit artikel wordt het proces van het inrichten van een nieuwe productieomgeving voor Microsoft Dynamics 365 Human Resources uitgelegd.
author: twheeloc
ms.date: 01/07/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 341b14d493c85a1e94666fa7e07b80704645e5f1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858238"
---
# <a name="provision-human-resources"></a>Human Resources inrichten

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



In dit artikel wordt het proces van het inrichten van een nieuwe productieomgeving voor Microsoft Dynamics 365 Human Resources uitgelegd. 

## <a name="prerequisites"></a>Vereisten

Voordat u een nieuwe productieomgeving inricht, moet aan de volgende voorwaarden zijn voldaan:

- U hebt Human Resources aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). Als u een bestaande Microsoft Dynamics 365-licentie hebt waarin het Human Resources-serviceabonnement al is opgenomen en u de stappen in dit artikel niet kunt voltooien, neemt u contact op met de ondersteuning.

- De globale beheerder heeft zich aangemeld bij [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) en een nieuw Human Resources-project gemaakt. 

## <a name="provision-a-human-resources-trial-environment"></a>Een Human Resources-proefomgeving inrichten

>[!NOTE]
> Vanaf april 2022 zijn de Human Resources-testomgevingen niet meer beschikbaar in de zelfstandige toepassing. Potentiële klanten die geïnteresseerd zijn in het evalueren van de HR-mogelijkheden in apps voor financiën en bedrijfsactiviteiten, kunnen dit doen met behulp van de gratis proefversie van 30 dagen en de demonstratiegegevens. Dynamics 365 Finance omvat de HR-mogelijkheden van de Finance-infrastructuur dankzij de samenvoeging van de zelfstandige toepassing. Raadpleeg [Merging of HR offerings brings capabilities together for customers](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers) voor meer informatie. Raadpleeg de stapsgewijze [handleiding](../fin-ops-core/fin-ops/get-started/before-you-buy.md) voor meer informatie over Dynamics 365 Finance-proefversies. 


Voordat u uw eerste sandbox- of productieomgeving inricht, kunt u een [Human Resources-proefomgeving](https://go.microsoft.com/fwlink/p/?LinkId=2115962) inrichten om de Human Resources-functionaliteit te valideren. Proefomgevingen bevatten fictieve gegevens die kunnen worden gebruikt om het programma op een veilige manier te verkennen. Hoewel een proefomgeving eigendom is van de gebruiker die hierom heeft verzocht, kunnen andere gebruikers worden uitgenodigd via de systeembeheerervaring voor Human Resources. 

Testomgevingen bieden de mogelijkheid om de functionaliteit Human Resources te beoordelen voor personen die nog geen toegang hebben tot een Human Resources-omgeving. Als u een proefomgeving inricht en de geverifieerde gebruiker al toegang heeft tot een of meer bestaande Human Resources-omgevingen, wordt de gebruiker omgeleid naar de bestaande omgeving of een lijst met omgevingen.

Proefomgevingen zijn niet bedoeld als productieomgevingen. Proefomgevingen zijn beperkt tot een periode van 30 dagen. Wanneer een proefperiode verloopt, worden de omgeving en alle gegevens erin permanent verwijderd. De omgeving kan niet worden geconverteerd naar een sandbox of een productieomgeving. Nadat de bestaande omgeving is verlopen, kunt u zich aanmelden voor een nieuwe proefomgeving.

Bij het aanmaken van een testomgeving voor Human Resources wordt ook een testomgeving aangemaakt voor Power Apps voor de tenant, die wordt gekoppeld aan de Human Resources-omgeving. De Power Apps-omgeving, met de naam TestDrive, heeft dezelfde testperiode als de Human Resources-omgeving.

> [!NOTE]
> Het inrichten van een testomgeving voor Human Resources mislukt als de geverifieerde gebruiker niet over machtigingen voor het aanmaken van testomgevingen voor Power Apps beschikt. De gebruiker moet zijn opgenomen in de gebruikersgroep die testomgevingen kan aanmaken in het Power Platform-beheercentrum. Raadpleeg [Beheren wie omgevingen in het Power Platform-beheercentrum kan aanmaken](/power-platform/admin/control-environment-creation) voor meer informatie.

## <a name="plan-human-resources-environments"></a>Human Resources-omgevingen plannen

Voordat u uw eerste Human Resources-omgeving maakt, moet u de omgevingsbehoeften voor uw project zorgvuldig plannen. Een basisabonnement op Human Resources omvat twee omgevingen: een productieomgeving en een werkomgeving. Afhankelijk van de complexiteit van uw project moet u mogelijk extra omgevingen voor uw bedrijf aanschaffen ter ondersteuning van projectactiviteiten. 

Overwegingen voor extra omgevingen:

- **Gegevensmigratie**: mogelijk moet u rekening houden met een extra omgeving voor gegevensmigratieactiviteiten, zodat uw omgeving kan worden gebruikt voor testdoeleinden tijdens het project. Als u een extra omgeving hebt, kunnen activiteiten voor gegevensmigratie worden voortgezet terwijl de test- en configuratieactiviteiten gelijktijdig plaatsvinden in een andere omgeving.
- **Integratie**: mogelijk moet u rekening houden met een extra omgeving voor het configureren en testen van integraties. Dit kan native integraties omvatten, zoals de Ceridian Dayforce- of LinkedIn Talent Hub-integraties, of aangepaste integraties, zoals die voor salarisadministratie, volgsystemen voor sollicitanten of vergoedingssystemen en leveranciers.
- **Training**: u hebt mogelijk een afzonderlijke omgeving nodig die is geconfigureerd met een set trainingsgegevens om uw werknemers te trainen het nieuwe systeem te gebruiken. 
- **Project met meerdere fasen**: u hebt mogelijk een extra omgeving nodig voor configuratie, gegevensmigratie, testen of andere activiteiten in een projectfase die is gepland na de eerste keer live gaan van het project.

 > [!IMPORTANT]
 > We raden het volgende aan om voor uw omgeving te overwegen:
 > - Gebruik uw productieomgeving in uw gehele project als uw GOLD-configuratieomgeving. Dit is belangrijk, omdat u een sandbox-omgeving niet naar een productieomgeving kunt kopiëren. Wanneer u live gaat, is uw GOLD-omgeving uw productieomgeving en zult u uw wijzigingsactiviteiten in deze omgeving voltooien.</br></br>
 > - Gebruik uw werkomgeving of een andere omgeving voor het uitvoeren van een simulatie-cutover voordat u live gaat. U kunt dit doen door de productieomgeving te vernieuwen met uw GOLD-configuratie in uw sandbox-werkomgeving.</br></br>
 > - Houd een gedetailleerde cutover-controlelijst bij, inclusief alle gegevenspakketten die nodig zijn om de definitieve gegevens naar de productieomgeving te migreren tijdens de go-live cutover.</br></br>
 > - Gebruik uw sandboxomgeving in uw gehele project als uw TEST-configuratieomgeving. Als u extra omgevingen nodig hebt, kan uw organisatie ze voor bijkomende kosten inkopen.</br></br>

## <a name="create-an-lcs-project"></a>Een LCS-project maken

Als u LCS wilt gebruiken om Human Resources-omgevingen te beheren, moet u eerst een LCS-project maken.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index) met de account waarmee u zich hebt geabonneerd op Human Resources.

   > [!NOTE]
   > Om te zorgen voor een goede inrichting, moet de account waarmee u de Human Resources-omgeving inricht zijn toegewezen aan de rol **Systeembeheerder** of **Systeemaanpasser** in de Power Apps-omgeving die is gekoppeld aan de Human Resources-omgeving. Raadpleeg voor meer informatie over het toewijzen van beveiligingsrollen aan gebruikers in het Power Platform [Beveiliging van gebruikers configureren voor bronnen](/power-platform/admin/database-security).

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
    
3. Selecteer de optie **Demogegevens opnemen** als u wilt dat in uw omgeving dezelfde demogegevensset wordt opgenomen die is gebruikt in de Human Resources-testomgeving. Demogegevens zijn nuttig voor de langetermijndemo of -trainingsomgevingen en mogen nooit worden gebruikt voor productieomgevingen. U moet deze optie bij de aanvankelijke implementatie kiezen. U kunt een bestaande implementatie niet later bijwerken.

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

5. De volgende Power Apps-omgevingen kunt u niet gebruiken voor Human Resources. Ze worden gefilterd op basis van de selectielijst in LCS:
 
    - **Standaard Power Apps-omgevingen**: hoewel elke tenant automatisch wordt ingericht met een standaard Power Apps-omgeving, is het niet raadzaam deze te gebruiken met Human Resources. Alle tenantgebruikers hebben toegang tot de Power Apps-omgeving en kunnen onbedoeld productiegegevens beschadigen tijdens het testen en verkennen van Power Apps- of Power Automate-integraties.
   
    - **Proefomgevingen**: deze omgevingen worden met een vervaldatum gemaakt. Na de vervaldatum worden uw omgeving en eventuele exemplaren van Human Resources die zich in de omgeving bevinden, automatisch verwijderd.
   
    - **Niet-ondersteunde regio's**: De omgeving moet zich in een ondersteunde geografie bevinden. Meer informatie over dit onderwerp vindt u in [Ondersteunde geografieën](hr-admin-setup-provision.md#supported-geographies).

6. Functionaliteit voor twee keer wegschrijven voor het integreren van Human Resources-data met de Power Apps-omgeving kan alleen worden gebruikt als de optie **Dynamics 365-apps inschakelen** is ingeschakeld voor de omgeving. Zie de [startpagina van Twee keer wegschrijven](../fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page.md) voor meer informatie over twee keer wegschrijven.

    > [!NOTE]
    > De optie **Dynamics 365-apps inschakelen** moet worden geselecteerd op het moment dat de Power Apps-omgeving wordt gemaakt. Als de optie niet wordt geselecteerd tijdens de inrichting, kunt u geen twee keer wegschrijven gebruiken om data te integreren tussen Dynamics 365 Human Resources en de Power Apps-omgeving of kunt u geen Dynamics 365-apps installeren in de omgeving zoals Dynamics 365 Sales en Field Service. Deze optie is niet omkeerbaar. Voor meer informatie zie [Enkele belangrijke overwegingen bij het maken van een nieuwe omgeving](/power-platform/admin/create-environment#some-important-considerations-when-creating-a-new-environment) op de documentatiesite van Power Platform.

7. Nadat u hebt vastgesteld welke omgeving de juiste is om te gebruiken, kunt u doorgaan met het inrichtingsproces. 

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

Standaard heeft de globale beheerder die de omgeving heeft gemaakt toegang tot deze omgeving. Aan alle overige gebruikers van de toepassing moet u uitdrukkelijk toestemming verlenen. U moet gebruikers toevoegen en de juiste rollen aan deze gebruikers toewijzen in de Human Resources-omgeving. Zie voor meer informatie [Nieuwe gebruikers maken](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) en [Gebruikers toewijzen aan beveiligingsrollen](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles). 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
