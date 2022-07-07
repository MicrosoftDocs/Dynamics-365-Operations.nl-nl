---
title: Samenwerking met leveranciers instellen en onderhouden
description: In dit artikel wordt uitgelegd hoe u leverancierssamenwerking instelt voor Dynamics 365 Supply Chain Management. Daarnaast wordt uitgelegd hoe u nieuwe gebruikers voor leverancierssamenwerking kunt inrichten en de beveiligingsrollen voor deze gebruikers kunt beheren.
author: GalynaFedorova
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 19fafb21e879d7436678bdb3c29d1a3d7e2330d7
ms.sourcegitcommit: bad64015da0c96a6b5d81e389708281406021d4f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/17/2022
ms.locfileid: "9023755"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Samenwerking met leveranciers instellen en onderhouden

[!include [banner](../includes/banner.md)]

De interface voor leverancierssamenwerking biedt gebruikers die externe leveranciers zijn, beperkte informatie over inkooporders, facturen en de consignatievoorraad. Via deze interface kan een leverancier ook antwoorden op offerteaanvragen en basisbedrijfsgegevens weergeven en bewerken.

In dit artikel wordt uitgelegd hoe u leverancierssamenwerking instelt voor Dynamics 365 Supply Chain Management. Daarnaast wordt uitgelegd hoe u een werkstroom kunt instellen om nieuwe gebruikers voor leverancierssamenwerking in te richten en hoe u de beveiligingsrollen voor deze gebruikers kunt beheren.

## <a name="set-up-vendor-collaboration-security-roles"></a>Beveiligingsrollen voor leverancierssamenwerking instellen

Een inkoopmedewerker of leverancier die over voldoende machtigingen beschikt, kan verzoeken dat een contactpersoon als een gebruiker wordt ingesteld door **Gebruiker van leverancier inrichten** voor de contactpersoonrecord in te schakelen. Tijdens het inrichtingsproces worden gebruikersmachtigingen geselecteerd voor de nieuwe externe gebruiker en wordt de nieuwe aanvraag voor een leveranciersgebruiker ingediend. Het is belangrijk dat u de gebruikersmachtigingen die beschikbaar zijn voor selectie, correct instelt in de leveranciersgebruikersaanvraag. Anders krijgen leveranciers mogelijk toegang tot informatie waar ze geen toegang tot moeten hebben in Supply Chain Management.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>De beveiligingsrollen instellen die beschikbaar zijn voor selectie wanneer een nieuwe gebruikersaanvraag wordt gebruikt voor een contactpersoon

1. Selecteer **Systeembeheer** &gt; **Beveiliging** &gt; **Externe rollen**.
2. Selecteer **Nieuw** en selecteer vervolgens een beveiligingsrol en de partijrol **Leverancier**.

Mogelijk wilt u de rollen **Leveranciersbeheerder (extern)** en **Leverancier (extern)** toevoegen die worden verstrekt in Supply Chain Management. U kunt ook beveiligingsrollen gebruiken die uw bedrijf heeft gemaakt.

U moet de rol **Leveranciersbeheerder (extern)** alleen beschikbaar maken als leveranciers nieuwe contacten moeten kunnen maken, als ze gebruikersaanvragen voor leverancierssamenwerking moeten kunnen indienen voor nieuwe gebruikers en wijzigingen in gebruikersgegevens en als ze deze aanvragen via een werkstroom moeten kunnen verwerken.

Als u van plan bent om handmatig leverancierscontacten en -gebruikers in te stellen, kunt u alleen de rol **Leverancier (extern)** beschikbaar maken. Deze rol wordt dan de enige rol die kan worden aangevraagd via een leveranciersgebruikersaanvraag.

> [!NOTE]
> De rol **SystemUser** wordt automatisch verleend als u handmatig een nieuw gebruikersaccount maakt. Daarom moet u die rol verwijderen en de rol **SystemExternalUser** toewijzen. Als er nieuwe gebruikersaccounts worden gemaakt via de werkstroom die is gestart door een leveranciersgebruikersaanvraag voor de inrichting van een nieuwe gebruiker, worden een of meer van de rollen die u hebt ingesteld voor leverancierssamenwerking en de rol **SystemExternalUser** toegewezen.

#### <a name="vendor-admin-external-security-role"></a>Beveiligingsrol Leveranciersbeheerder (extern)

De rol **Leveranciersbeheerder (extern)** kan worden gebruikt voor externe leveranciers die leverancierscontactgegevens onderhouden en aanvragen indienen voor de inrichting van nieuwe gebruikers van leverancierssamenwerking. Externe gebruikers met deze beveiligingsrol kunnen de volgende taken uitvoeren:

- Gegevens van contactpersonen weergeven en wijzigen, zoals de titel, het e-mailadres en het telefoonnummer van de persoon.
- Een nieuwe of bestaande contactpersoon toevoegen aan de leveranciersaccounts waarvoor ze contact zijn.
- Contactpersonen die ze hebben gemaakt, verwijderen.
- De koppeling tussen een contactpersoon en een leveranciersaccount activeren of deactiveren. Nadat de koppeling tussen een contactpersoon en een leveranciersaccount is gedeactiveerd, kan er niet meer naar de contactpersoon worden verwezen op nieuwe inkooporders of andere documenten.
- Een contactpersoon toestaan of het recht ontzeggen om documenten in de interface voor leverancierssamenwerking die specifiek zijn voor het leveranciersaccount, te openen. Nadat de koppeling tussen een contactpersoon en een leveranciersaccount is gedeactiveerd, wordt de contactpersoon de toegang geweigerd tot documenten die specifiek zijn voor het leveranciersaccount.
- Een nieuw gebruikersaccount aanvragen voor een contactpersoon met de actie **Gebruiker inrichten**.
- Erom verzoeken dat het gebruikersaccount van een contactpersoon wordt gedeactiveerd.
- Verzoeken om een wijziging van het gebruikersaccount van een contactpersoon die bestaat uit het toevoegen of verwijderen van beveiligingsrollen.
- Offerteaanvragen weergeven.

#### <a name="vendor-external-security-role"></a>Beveiligingsrol Leverancier (extern)

De rol **Leverancier (extern)** kan worden gebruikt voor externe leveranciers die met inkooporders werken. Externe gebruikers met deze beveiligingsrol kunnen de volgende taken uitvoeren:

- Reageren op inkooporders en informatie over deze inkooporders weergeven.
- Samenwerkingsfacturen van leveranciers onderhouden.
- De consignatievoorraad weergeven.
- Offerteaanvragen weergeven en erop reageren.
- Leveranciersgegevens weergeven.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Beveiligingsrollen instellen die worden gebruikt bij het onboarden van potentiële leveranciers

Als u leveranciers wilt onboarden waarvoor een aanvraag voor registratie van een potentiële leverancier is ingediend, moet u een externe beveiligingsrol instellen. Deze rol wordt aan nieuwe gebruikers toegewezen tijdens het inrichtingsproces dat wordt geregeld door de werkstroom van het type **Werkstroom gebruikersaanvragen (platform)**. Zie voor meer informatie de sectie [Werkstromen instellen voor het verwerken van gebruikersaanvragen voor leverancierssamenwerking](#set-up-workflows-to-process-vendor-collaboration-user-requests) verderop in dit artikel.

Zie [Leveranciers onboarden](vendor-onboarding.md) voor meer informatie over het onboarden van potentiële leveranciers.

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Een beveiligingsrol instellen die wordt gebruikt wanneer een nieuwe gebruikersaanvraag voor potentiële leveranciers wordt ingediend

1. Selecteer **Systeembeheer** > **Beveiliging** > **Externe rollen**.
2. Selecteer **Nieuw** en selecteer vervolgens een beveiligingsrol en de partijrol **Potentiële leverancier**.

U moet de rol **Potentiële leverancier (extern)** toevoegen die beschikbaar is in Supply Chain Management.

De beveiligingsrol verleent alleen toegang tot de nieuwe leveranciersregistratiewizard.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Werkstromen instellen voor het verwerken van gebruikersaanvragen voor leverancierssamenwerking

Om ervoor te zorgen dat alle relevante taken worden voltooid en dat de juiste goedkeuringen worden gegeven, moet u werkstromen instellen om gebruikersaanvragen voor leverancierssamenwerking af te handelen.

Gebruikersaanvragen voor leverancierssamenwerking worden ingediend door externe leveranciers met de beveiligingsrol **Leveranciersbeheerder (extern)** of vergelijkbare machtigingen, of door inkoopmedewerkers in uw bedrijf. Ze kunnen ook worden gegenereerd op basis van registratieaanvragen voor potentiële leveranciers tijdens het onboardingproces voor leveranciers.

Er zijn drie typen aanvragen:

- Aanvragen voor het inrichten van een nieuwe gebruiker
- Aanvragen voor het deactiveren van een bestaande gebruiker
- Aanvragen voor het wijzigen van de beveiligingsrollen van een bestaande gebruiker

Zie [Gebruikers van leverancierssamenwerking beheren](manage-vendor-collaboration-users.md) voor meer informatie over gebruikersaanvragen voor leverancierssamenwerking.

U moet twee of meer werkstromen maken om alle drie de typen gebruikersaanvragen voor leverancierssamenwerking te verwerken. Nieuwe werkstromen worden gemaakt op de pagina **Gebruikerswerkstromen**.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Voorbeeld van een werkstroom voor het inrichten van nieuwe gebruikers en het wijzigen van beveiligingsrollen

Voor het afhandelen van aanvragen van leveranciersgebruikers om nieuwe gebruikers te maken en beveiligingsrollen te wijzigen, kunt u een vertakkingsvoorwaarde aan het begin van de werkstroom plaatsen. Op deze manier kan er bij de aanvraag om een nieuwe gebruiker te maken een andere vertakking van de werkstroom worden gebruikt als bij de aanvraag om een bestaande gebruiker te wijzigen.

Als u deze vertakking wilt instellen, maakt u een nieuwe werkstroom van het type **Werkstroom gebruikersaanvragen (platform)**. De vertakkingen van deze werkstroom kunnen de volgende elementen bevatten.

#### <a name="branch-to-provision-new-users"></a>Vertakking voor het inrichten van nieuwe gebruikers

1. Wijs een goedkeuringstaak toe aan de persoon wiens verantwoordelijkheid het is om de toegangsverlening aan nieuwe gebruikers tot informatie over leverancierssamenwerking goed te keuren.
2. Wijs een taak toe aan de persoon die verantwoordelijk is voor het aanvragen van nieuwe Microsoft Azure Active Directory-gebruikersaccounts (Azure AD) in Azure Portal. Gebruik de vooraf gedefinieerde taak **Uitnodiging Azure AD B2B-gebruiker verzenden** voor deze stap. B2B-gebruikers kunnen automatisch worden geëxporteerd naar Azure AD. Gebruik de vooraf gedefinieerde taak **Azure AD B2B-gebruiker inrichten**. Zie [B2B-gebruikers exporteren naar Azure AD](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md) voor meer informatie.
3. Wijs een goedkeuringstaak toe aan de persoon die naar Azure uploadt. Als er geen account is gemaakt, wijst deze persoon de taak af en eindigt deze de werkstroom. Deze goedkeuringstaak kan worden overgeslagen als u de stap hebt opgenomen die automatisch nieuwe gebruikersaccounts naar Azure exporteert via de B2B-API (Application Programming Interface).
4. Voeg een geautomatiseerde taak toe waarmeer een nieuwe gebruiker wordt ingericht. Gebruik de vooraf gedefinieerde taak **Geautomatiseerde inrichting van gebruiker** voor deze stap.
5. Voeg een taak toe die de nieuwe gebruiker op de hoogte stelt. U kunt de nieuwe gebruikers bijvoorbeeld een welkomstmail sturen die een URL bevat voor Supply Chain Management. Dit e-mailbericht kan gebruikmaken van een sjabloon die u maakt op de pagina **E-mailberichten** en die u vervolgens selecteert op de pagina **Parameters gebruikerswerkstroom**. De sjabloon kan de tag **%portalURL%** bevatten. Wanneer de welkomstmail wordt gegenereerd, wordt deze tag vervangen door de URL van de Supply Chain Management-tenant.

    > [!NOTE]
    > Deze werkstroom kan worden gebruikt in meerdere scenario's voor het onboarden van gebruikers. Deze kan bijvoorbeeld worden gebruikt wanneer potentiële leveranciers of contactpersonen een leverancierssamenwerkingsaccount nodig hebben. Daarom moet u het e-mailbericht formuleren als een algemene mededeling die voor meerdere doeleinden kan worden gebruikt.

#### <a name="branch-to-modify-security-roles"></a>Vertakkingen gebruiken om beveiligingsrollen te wijzigen

1. Wijs een goedkeuringstaak toe aan de persoon die verantwoordelijk is voor het goedkeuren van wijzigingen in beveiligingsrollen.
2. Voeg een geautomatiseerde taak toe die de relevante beveiligingsrollen toevoegt of verwijdert. Gebruik de taak **Geautomatiseerde inrichting van gebruiker** voor deze stap.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Voorbeeld van een werkstroom voor het deactiveren van een gebruiker

Maak een werkstroom van het type **Werkstroom voor deactiveren gebruikersaanvragen (platform)** en voeg vervolgens de volgende taken toe.

1. Wijs een goedkeuringstaak toe aan de persoon die verantwoordelijk is voor het accepteren van aanvragen voor het deactiveren van gebruikers. U kunt voorwaarden toevoegen om deze goedkeuringsstap te automatiseren.
2. Voeg een geautomatiseerde taak toe die de gebruiker deactiveert. Gebruik de taak **Geautomatiseerde deactivering gebruiker** voor deze stap.
3. Voeg opschoontaken toe die vereist zijn. U kunt bijvoorbeeld een taak toevoegen die het account uit uw map in Azure Portal verwijdert.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Leverancierssamenwerking voor een specifieke leverancier inschakelen

Voordat u een gebruikersaccount maakt voor iemand die leverancierssamenwerking gaat gebruiken, moet u de leverancier zo instellen dat deze leverancierssamenwerking kan gebruiken. Meer informatie over hoe u dit doet, vindt u in [Leverancierssamenwerking met externe leveranciers](vendor-collaboration-work-external-vendors.md).

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Problemen oplossen met de inrichting van nieuwe gebruikers van leverancierssamenwerking

Nieuwe gebruikers van leverancierssamenwerking worden ingericht via de werkstroom die u instelt om gebruikersaanvragen voor leverancierssamenwerking van het type **Leveranciersgebruiker inrichten** te verwerken.

Als het e-mailadres van een nieuwe gebruiker van leverancierssamenwerking bij een domein hoort dat is geregistreerd bij Azure als tenant (dat wil zeggen als het een beheerd domeinaccount is), moet het e-mailadres een bestaand Azure AD-account zijn. Anders kan het inrichtingsproces niet worden voltooid.

Zie [Azure Active Directory B2B-samenwerking](/azure/active-directory/external-identities/what-is-b2b) voor meer informatie over het proces dat wordt gebruikt in de taak **Uitnodiging Azure AD B2B-gebruiker verzenden** in de werkstroom voor Azure AD-accountbeheer.

## <a name="additional-resources"></a>Aanvullende bronnen

[Leverancierssamenwerking met externe leveranciers](vendor-collaboration-work-external-vendors.md)

Bekijk een korte video over het onboardingproces voor leveranciers: [Een nieuwe leverancier onboarden](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
