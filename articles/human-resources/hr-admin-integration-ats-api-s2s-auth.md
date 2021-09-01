---
title: Server-naar-server-verificatie voor de API voor ATS-integratie
description: In dit onderwerp wordt beschreven hoe u server-naar-serververificatie kunt instellen voor integraties met de API voor ATS-integratie (Applicant Tracking System) van Dynamics 365 Human Resources.
author: jaredha
ms.date: 06/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-06-30
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: aabe2cd9fd962c8f1c5bbf7fe911e7c6ceeae082f61fc4359aaf7bf197531eff
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6778074"
---
# <a name="server-to-server-authentication-for-the-ats-integration-api"></a>Server-naar-server-verificatie voor de API voor ATS-integratie

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

In dit onderwerp wordt beschreven hoe u server-naar-serververificatie kunt instellen voor toepassingsintegraties met de API voor ATS-integratie (Applicant Tracking System) van Dynamics 365 Human Resources. Er zijn enkele beveiligingslagen die moeten worden beheerd voor de service-principal om toegang te krijgen tot de virtuele Microsoft Dataverse-tabel en bijbehorende gegevens. De gebruiker moet toegang krijgen tot de virtuele Dataverse-tabel in Microsoft Power Platform en tot de gegevens in Dynamics 365 Human Resources.

## <a name="enable-access-to-dataverse-virtual-tables-in-power-platform"></a>Toegang tot virtuele Dataverse-tabellen inschakelen in Power Platform

De eerste stap voor het verlenen van toegang tot de virtuele Dataverse-tabellen in Power Platform is het instellen van de toepassing in Power Platform voor verificatie op basis van virtuele Dataverse-tabeleindpunten. Stappen hiervoor worden beschreven in de [Microsoft Dataverse ontwikkelaarshandleiding](/powerapps/developer/data-platform).

  - Voor registraties in een app met een enkele tenant: [Server-naar-serververificatie gebruiken voor een enkele tenant](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication)
  - Voor appregistraties met meerdere tenants: [Server-naar-serververificatie gebruiken voor meerdere tenants](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication)

### <a name="creating-a-security-role-for-ats-integrations"></a>Een beveiligingsrol voor ATS-integraties maken

Een van de stappen na het maken van de toepassingsgebruiker is het toewijzen van de gebruiker aan een beveiligingsrol die de toegang definieert tot de eindpunten van de toepassing. Dit is stap 7 in [Een toepassingsgebruiker maken](/powerapps/developer/data-platform/use-single-tenant-server-server-authentication#application-user-creation) voor appregistraties voor een enkele app en [Een beveiligingsrol maken voor de toepassingsgebruiker](/powerapps/developer/data-platform/use-multi-tenant-server-server-authentication#create-a-security-role-for-the-application-user) voor registraties voor meerdere tenants. 

De rol waaraan u de toepassingsgebruiker toewijst, moet toegang hebben tot de gegevensentiteiten die voor uw ATS-integratie worden gebruikt. Deze is niet standaard beschikbaar, dus moet er een nieuwe beveiligingsrol worden gemaakt. De nieuwe rol kan worden gemaakt met de stappen die zijn beschreven in [Een beveiligingsrol maken](/power-platform/admin/create-edit-security-role#create-a-security-role).

Voor de nieuwe rol moet in elk geval de juiste toegang worden toegewezen aan de volgende entiteiten op het tabblad **Aangepaste entiteiten** van de nieuwe rol. U moet mogelijk extra entiteiten toevoegen als er uitgebreidere toepassingsgegevens worden gebruikt bij de integratie. Nadat de nieuwe rol is gemaakt, kan deze worden toegewezen aan de toepassingsgebruiker.

  - Basiswerker (mshr)
  - Kandidaat voor aanstelling (mshr)
  - Certificaatcompetentie (mshr)
  - Type certificaat (mshr)
  - Bedrijf
  - Compensatietaakfunctie (mshr)
  - Type compensatietaak (mshr)
  - Land/regio's (mshr)
  - Afdeling (mshr)
  - Opleidingscompetentie (mshr)
  - Diploma (mshr)
  - Opleidingsdisciplines (mshr)
  - Opleidingseisen (mshr)
  - Identificatie (mshr)
  - Identificatietype (mshr)
  - Instelling (mshr)
  - Uitgifte-instantie (mshr)
  - Taakcompensatie (mshr)
  - Taken (mshr)
  - Opleidingsniveau (mshr)
  - Contactpersonen van partij (mshr)
  - Personen (mshr)
  - Adressen van persoon (mshr)
  - Persoonscreening (mshr)
  - Positietype (mshr)
  - Posities V2 (mshr)
  - Competentie beroepservaring (mshr)
  - Beoordelingsniveau (mshr)
  - Beoordelingsmodellen (mshr)
  - Redencodes (mshr)
  - Wervingsaanvraag (mshr)
  - Locatie van wervingsaanvraag (mshr)
  - Positie van wervingsaanvraag (mshr)
  - Vaardigheden voor wervingsaanvraag (mshr)
  - Screeningtype (mshr)
  - Vaardigheidscompetentie (mshr)
  - Vaardigheden (mshr)
  - Titels (mshr)
  - Veteraanstatus (mshr)
  - Medewerker (mshr)

## <a name="granting-application-permissions-to-human-resources-data"></a>Toepassingsmachtigingen verlenen aan Human resources-gegevens

De tweede stap is ervoor zorgen dat de toepassing de juiste machtigingen krijgt voor de gegevens in Human resources door deze te koppelen aan een gebruiker in de Human resources-toepassing. Voor een toepassingsgebruiker worden de oproepen van server naar server via virtuele Dataverse-tabellen uitgevoerd in de context van de identiteit van de gebruiker (app) in Dataverse die de actie aanroept. De virtuele tabeladapterservice zoekt vervolgens de gekoppelde gebruiker in Human resources en voert de query uit in de context van die gebruiker. Dit betekent dat een gebruiker moet worden gemaakt in Human resources met de juiste rollen die zijn toegewezen, zodat deze toegang heeft tot de gegevens die de integratietoepassing nodig heeft.

Tevens moeten aan de Human resources-gebruiker de juiste machtigingen worden toegewezen voor de gegevens in Human resources. De rol **Wervingstoepassing** (HcmRecruitingIntegrator) is beschikbaar met bevoegdheden voor de primaire entiteiten die vereist zijn voor integratie met wervingsgegevens. Deze rol kan worden toegewezen aan de toepassingsgebruiker op de pagina **Gebruikers** om de juiste toegang tot de gegevens te verlenen. Zie [Beveiliging op basis van rollen](/fin-ops-core/dev-itpro/sysadmin/role-based-security) voor meer informatie over de beveiligingsrollen van Human resources.

### <a name="set-up-the-new-user-with-appropriate-permissions"></a>De nieuwe gebruiker instellen met de juiste machtigingen

Volg deze stappen om de nieuwe gebruiker in te stellen met de juiste machtigingen:

  1. Open de pagina **Gebruikers** in Human resources en selecteer vervolgens **Nieuw**.
  2. Voer een **gebruikers-id** en **gebruikersnaam** in voor de nieuwe toepassingsgebruiker. U kunt bijvoorbeeld "RecruitingIntegration" invoeren.

      > [!NOTE]
      > Als de app geen Microsoft Azure Active Directory-gebruikersaccount of e-mailadres (Azure AD) heeft, kunt u iets als "RecruitingApp" invoeren in de velden voor e-mailadres en provider voor de gebruiker.

  3. Selecteer op het sneltabblad **Rollen van gebruiker** de actie **Rollen toewijzen**.
  4. Selecteer **Wervingstoepassing** in het deelvenster **Rollen toewijzen aan gebruiker** en selecteer vervolgens **OK**.
  5. Sla de nieuwe gebruikersrecord op.

### <a name="link-the-new-human-resources-user-to-the-application"></a>De nieuwe Human resources-gebruiker koppelen aan de toepassing

Nadat de gebruiker is gemaakt, moet er een record worden gemaakt voor de toepassing in het formulier **Azure Active Directory-toepassingen** om de App te koppelen aan de Human resources-gebruiker.

  1. Open het formulier **Azure Active Directory-toepassingen** en selecteer **Nieuw**.
  2. Voer in het veld **Client-id** de client-id in van de toepassingsgebruiker die voor de toepassing is gemaakt.
  3. Voer in het veld **Naam** de naam in voor de integrerende toepassing.
  4. Selecteer in het veld **Gebruikers-id** de nieuwe Human resources-gebruiker die voor de wervingsintegratie is gemaakt.
  5. Sla de nieuwe record op.

Vervolgens heeft de toepassing toegang tot Human resources-gegevens, maar alleen tot de gegevens die vereist zijn voor het integreren van wervingsverzoeken.

## <a name="see-also"></a>Zie ook

[Kandidaten werven](hr-personnel-recruit.md)<br>
[Wat is Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[De Microsoft Dataverse web-API gebruiken](/powerapps/developer/data-platform/webapi/overview)<br>
[Optiesets maken en bijwerken met de web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
