---
title: Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten inrichten
description: In dit artikel wordt het proces beschreven van de inrichting van een nieuwe productieomgeving voor Microsoft Dynamics 365 Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten.
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
ms.openlocfilehash: 2fd8176d16178ecc4ba667e5937f2cec2e0af2c3
ms.sourcegitcommit: bd3b55e1af28e592c97b540de1e87cd8ba9c35a8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/03/2022
ms.locfileid: "9221587"
---
# <a name="provision-human-resources-in-the-finance-and-operations-infrastructure"></a>Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten inrichten

_**Is van toepassing op:** Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten_ 

> [!NOTE]
> Vanaf juli 2022 kunnen er geen nieuwe Human Resources-omgevingen worden ingericht in de zelfstandige Human Resources-infrastructuur en er kunnen geen nieuwe Microsoft Dynamics LCS-projecten (Lifecycle Services) in worden gemaakt. Klanten kunnen Human Resources-omgevingen implementeren in de infrastructuur voor financiën en bedrijfsactiviteiten.

In dit artikel wordt het proces beschreven van de inrichting van een nieuwe productieomgeving voor Microsoft Dynamics 365 Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten.

## <a name="prerequisites"></a>Vereisten

Voordat u begint met de inrichting van een nieuwe omgeving, moet aan de volgende voorwaarden zijn voldaan:

- U hebt Human Resources aangeschaft via een provider van cloudoplossingen of een EA-overeenkomst (Enterprise Architecture). Als u een bestaande Dynamics 365-licentie hebt waarin het Human Resources-serviceabonnement al is opgenomen en u de stappen in dit artikel niet kunt voltooien, neemt u contact op met de ondersteuning.
- De globale beheerder heeft zich aangemeld bij [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com) en heeft een nieuw project voor financiën en bedrijfsactiviteiten gemaakt.

## <a name="provision-a-human-resources-trial-environment"></a>Een Human Resources-proefomgeving inrichten

> [!NOTE]
> Vanaf april 2022 zijn de Human Resources-testomgevingen niet meer beschikbaar in de zelfstandige toepassing. Potentiële klanten die geïnteresseerd zijn in het evalueren van de HR-mogelijkheden in apps voor financiën en bedrijfsactiviteiten, kunnen de gratis proefversie van 30 dagen samen met de demonstratiegegevens gebruiken. Dynamics 365 Finance omvat de HR-mogelijkheden van de Finance-infrastructuur dankzij de samenvoeging van de zelfstandige toepassing. Zie [Samenvoeging van HR-aanbod combineert mogelijkheden voor klanten](https://cloudblogs.microsoft.com/dynamics365/it/2021/09/15/merging-of-hr-offerings-brings-capabilities-together-for-customers) voor meer informatie . Raadpleeg de [stapsgewijze handleiding](../fin-ops-core/fin-ops/get-started/before-you-buy.md) voor meer informatie over Dynamics 365 Finance-proefversies.

## <a name="plan-human-resources-environments"></a>Human Resources-omgevingen plannen

Voordat u uw eerste Human Resources-omgeving maakt, moet u de omgevingsbehoeften voor uw project zorgvuldig plannen. Een basisabonnement op Human Resources omvat twee omgevingen: een productieomgeving en een standaardacceptatietest (Sandbox-omgeving). Afhankelijk van de complexiteit van uw project kunt u extra omgevingen voor uw bedrijf aanschaffen ter ondersteuning van projectactiviteiten.

Hier volgen enkele overwegingen voor extra optionele omgevingen:

- **Gegevensmigratie**: met gegevensmigratieactiviteiten kan uw sandbox-omgeving worden gebruikt voor testdoeleinden tijdens het project. Als u een extra omgeving hebt, kunnen activiteiten voor gegevensmigratie worden voortgezet terwijl de test- en configuratieactiviteiten gelijktijdig plaatsvinden in een andere omgeving.
- **Integratie**: configureer en test integraties die native integraties of aangepaste integraties kunnen omvatten, zoals die voor salarisadministratie, volgsystemen voor sollicitanten of vergoedingssystemen en providers.
- **Training**: u hebt mogelijk een afzonderlijke omgeving nodig die is geconfigureerd met een set trainingsgegevens zodat u uw werknemers kunt trainen in het gebruik van het nieuwe systeem. 
- **Project met meerdere fasen**: u hebt mogelijk een extra omgeving nodig voor configuratie, gegevensmigratie, testen of andere activiteiten in een projectfase die is gepland nadat het project voor de eerste keer live is gegaan.
- **Ontwikkeling**: in de infrastructuur voor financiën en bedrijfsactiviteiten kunt u de oplossing nu uitbreiden en uw eigen aanpassingen ontwikkelen. Elke ontwikkelaar moet zijn/haar eigen ontwikkelomgeving gebruiken. Zie [Ontwikkelomgevingen implementeren en openen](../fin-ops-core/dev-itpro/dev-tools/access-instances.md) voor meer informatie.
- **GOLD**: voor nieuwe implementaties wordt vaak een afzonderlijke GOLD-omgeving gebruikt die oorspronkelijk wordt behouden voor configuratie en gegevensmigratie. Deze omgeving kan in de gehele implementatie worden gebruikt om andere omgevingen te vernieuwen. Deze wordt gebruikt om de nieuwe productieomgeving te maken die de basisconfiguratie en gegevensmigratie heeft. U kunt een productieomgeving pas implementeren in infrastructuur voor financiën en bedrijfsactiviteiten als u het gereedheidsproces voor go-live hebt voltooid. Zie [Voorbereiden voor go-live](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) voor meer informatie.

<!--NOTE: Need to come back and verify Tier-1 can be used and if a customer cannot purchase tier 3-5 need specific documentation about this.-->

> [!IMPORTANT]
> Wanneer u uw omgevingen in ogenschouw neemt, raden we de volgende aanpak aan:
>
> - Gebruik de omgeving van uw standaardacceptatietest (voorheen Sandbox) of een andere omgeving om een simulatiecutover te doen vóór uw go-live.
> - Houd een gedetailleerde cutover-controlelijst bij die elk gegevenspakket bevat dat nodig is om de definitieve gegevens naar de productieomgeving te migreren tijdens de go-live cutover. Deze aanbeveling is vooral belangrijk als u geen afzonderlijke GOLD-omgeving hebt voor het opslaan van uw configuraties.
> - Gebruik uw omgeving van standaardacceptatietest (voorheen Sandbox) of een andere tier-2 of hogere omgeving als uw TEST-omgeving tijdens uw project. Als u extra omgevingen nodig hebt, kan uw organisatie deze tegen extra betaling aanschaffen.

## <a name="create-an-lcs-project"></a>Een LCS-project maken

Als u LCS wilt gebruiken om Human Resources-omgevingen te beheren, moet u eerst een LCS-project maken. Als u uw Human Resources-omgeving migreert naar de infrastructuur voor financiën en bedrijfsactiviteiten, moet u een nieuw LCS-project maken voor apps voor financiën en bedrijfsactiviteiten. Als u al een LCS-project hebt voor andere apps voor financiën en bedrijfsactiviteiten, kunt u de Human Resources-functies inschakelen in het werkgebied **Functiebeheer**. Zie [Overzicht van functiebeheer](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.

Wanneer een nieuwe klant zich bij Human Resources registreert, bevat het abonnement een implementatieprojectwerkgebied. Nadat de klant de service heeft geactiveerd, moet de tenantbeheerder zich aanmelden bij <https://lcs.dynamics.com> via het tenantaccount. Het projectwerkgebied wordt automatisch voor de organisatie gemaakt. Zie [Lifecycle Services (LCS) voor klanten van apps voor financiën en bedrijfsactiviteiten](../fin-ops-core/dev-itpro/lifecycle-services/lcs-works-lcs.md) voor meer informatie.

> [!NOTE]
> Om een succesvolle inrichting te waarborgen, moet het account waarmee u de Human Resources-omgeving inricht zijn toegewezen aan de rol **Systeembeheerder** of de rol **Systeemaanpasser** in de Power Apps-omgeving die is gekoppeld aan de Human Resources-omgeving. Raadpleeg voor meer informatie over het toewijzen van beveiligingsrollen aan gebruikers in het Microsoft Power Platform [Beveiliging van gebruikers configureren voor resources](/power-platform/admin/database-security).

U moet het proces van LCS-projectonboarding voltooien voordat u omgevingen kunt gaan implementeren. Zie [Projectonboarding](../fin-ops-core/dev-itpro/lifecycle-services/project-onboarding.md) voor meer informatie. Zie de [Gebruikershandleiding voor Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md) voor meer informatie over het gebruik van LCS.

## <a name="deploy-human-resources-environments"></a>Human Resources-omgevingen implementeren

Voor de implementatie van apps voor financiën en bedrijfsactiviteiten zoals Human Resources in de cloud, moet u inzicht hebben in de omgeving en het abonnement waarvoor u de implementatie uitvoert, wie welke taken kan uitvoeren en welke gegevens en aanpassingen u moet beheren. U wordt aangeraden een serviceaccount te gebruiken in plaats van een benoemde gebruiker wanneer u nieuwe omgevingen implementeert. Zie [Overzicht van cloudimplementaties](/fin-ops-core/dev-itpro/deployment/cloud-deployment-overview) voor meer informatie over de implementaties van omgevingen in de infrastructuur voor financiën en bedrijfsactiviteiten.

Als u een productieomgeving wilt implementeren voor Human Resources in de infrastructuur voor financiën en bedrijfsactiviteiten, moet u het gereedheidsproces voor go-live voltooien. Zie [Voorbereiden voor go-live](../fin-ops-core/fin-ops/imp-lifecycle/prepare-go-live.md) voor meer informatie. Dit proces omvat de abonnementsschatting in LCS. Zie [Abonnementsschatting](../fin-ops-core/dev-itpro/lifecycle-services/subscription-estimator.md) voor meer informatie.

## <a name="integrate-microsoft-power-platform-with-human-resources"></a>Microsoft Power Platform integreren met Human Resources

Microsoft Power Platform biedt een reeks mogelijkheden voor Dynamics 365-toepassingen via het Power Platform-beheercentrum. U kunt het gebruik van Human Resources-gegevens integreren en uitbreiden met Microsoft Power Platform. Zie [Integratie van Microsoft Power Platform met apps voor financiën en bedrijfsactiviteiten](../fin-ops-core/dev-itpro/power-platform/overview.md) voor informatie over het integreren van Human Resources met Microsoft Power Platform.

## <a name="supported-geographies"></a>Ondersteunde geografieën

Zie [Wereldwijd gebruik: informatie over ondersteunde regio´s en talen](https://dynamics.microsoft.com/availability-reports/) voor informatie over de talen en regio´s die worden ondersteund voor Human Resources.

## <a name="grant-access-to-the-environment"></a>Toegang verlenen tot de omgeving

Standaard heeft de globale beheerder die de omgeving heeft gemaakt toegang tot deze omgeving. Aan alle overige gebruikers van de toepassing moet u uitdrukkelijk toestemming verlenen. U moet gebruikers toevoegen en de juiste rollen aan deze gebruikers toewijzen in de Human Resources-omgeving. Zie voor meer informatie [Nieuwe gebruikers maken](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) en [Gebruikers toewijzen aan beveiligingsrollen](/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).

## <a name="additional-resources"></a>Aanvullende bronnen
Meer informatie over het gebruiken en beheren van projecten in LCS in de infrastructuur van de apps voor financiën en bedrijfsactiviteiten vindt u met behulp van de volgende resources:

- [Lifecycle Services-resources](../fin-ops-core/dev-itpro/lifecycle-services/lcs.md)
- [Gebruikershandleiding Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-user-guide.md)
- [Overzicht van Selfservice-implementatie](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md)
- [Startpagina Bewerkingen databaseverplaatsingen](../fin-ops-core/dev-itpro/database/dbmovement-operations.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
