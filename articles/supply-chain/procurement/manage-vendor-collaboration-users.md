---
title: Gebruikers van leverancierssamenwerking beheren
description: In dit onderwerp wordt beschreven hoe u de inrichting van nieuwe gebruikers van de leverancierssamenwerking kunt aanvragen en hoe u nieuwe contactpersonen van de nieuwe leverancierssamenwerking kunt toevoegen.
author: GalynaFedorova
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 515d995641f5bbe976643a38c26a46f7d8a115dd
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8678822"
---
# <a name="manage-vendor-collaboration-users"></a>Gebruikers van leverancierssamenwerking beheren

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de inrichting van nieuwe gebruikers van de leverancierssamenwerking kunt aanvragen en hoe u nieuwe contactpersonen van de nieuwe leverancierssamenwerking kunt toevoegen. 

De interface voor leverancierssamenwerking in Dynamics 365 Supply Chain Management bevat informatie over inkooporders, facturen en consignatievoorraad voor externe leveranciers. U kunt nieuwe contactpersonen voor leverancierssamenwerking maken en vragen of nieuwe gebruikers worden ingericht als u als externe leverancier met de beveiligingsrol **Leveranciersbeheerder (extern)** of vergelijkbare machtigingen werkt. U kunt deze taken ook uitvoeren als u als inkoopmedewerker werkt. In dit onderwerp verwijst deze rol naar een inkoopmedewerker die in het bedrijf werkt dat het exemplaar van Supply Chain Management bezit. Zie [Leverancierssamenwerking met klanten](vendor-collaboration-work-customers-dynamics-365-operations.md) voor meer informatie over het gebruik van leverancierssamenwerking als u een externe leverancier bent.  

Zie [Leverancierssamenwerking met externe leveranciers](vendor-collaboration-work-external-vendors.md) voor meer informatie over het gebruik van leverancierssamenwerking als u een inkoopmedewerker bent.

## <a name="add-new-vendor-collaboration-contacts"></a>Nieuwe contactpersonen voor leverancierssamenwerking toevoegen
Als u iemand toegang tot leverancierssamenwerking wilt geven, moet deze persoon eerst als contactpersoon voor leverancierssamenwerking worden toegevoegd. U kunt ook contactpersonen voor werknemers in uw bedrijf toevoegen die geen leverancierssamenwerking gebruiken. Zij kunnen bijvoorbeeld fungeren als contactpunt voor andere typen aanschaffingsinformatie. Nieuwe contactpersonen worden toegevoegd op de pagina **Alle contactpersonen**. Deze pagina kunt u openen via het menu **Leverancierssamenwerking** &gt; **Contactpersonen**. Een nieuwe contactpersoon toevoegen:

1.  Klik op **Nieuw**.
2.  Voer de gegevens van de contactpersoon in.
3.  Kies welke rechtspersoon ze in uw bedrijf vertegenwoordigen en met welke rechtspersoon ze werken in het bedrijf waarmee ze zullen samenwerken. U doet dit door een combinatie van **Rechtspersoon in mijn bedrijf**/**Rechtspersoon in klantbedrijf** te selecteren.
4.  Klik op **Maken**.

Als u een contactpersoon wilt verwijderen, kunt u alleen de contactpersonen verwijderen die u hebt gemaakt.

## <a name="vendor-collaboration-user-requests"></a>Gebruikersaanvragen voor leverancierssamenwerking
Gebruikersaanvragen voor leverancierssamenwerking kunnen worden ingediend door een inkoopmedewerker of een beheerder van een externe leverancier.

-   Als u een externe leverancier bent, verzendt u aanvragen vanaf de pagina **Alle contactpersonen** in de module **Leverancierssamenwerking**.
-   Als u een inkoopmedewerker bent, verzendt u aanvragen vanaf de pagina **Contactpersonen weergeven**. Hiervoor selecteert u in de leveranciersrecord in de sectie **Instellen** in het actievenster de optie **Contactpersonen** &gt; **Contactpersonen weergeven**.

U kunt een aanvraag indienen om een gebruiker in te richten, een gebruiker te deactiveren of beveiligingsrollen te wijzigen. Als u een beheerder van een externe leverancier bent, moet u als contactpersoon zijn geregistreerd voor de leveranciersrekeningen waarvoor u gebruikersaanvragen wilt maken en u moet toegang tot de interface voor leverancierssamenwerking hebben voor deze leveranciersrekeningen.  

Wanneer een aanvraag wordt ingediend, wordt deze toegevoegd aan de lijst **Gebruikersaanvragen voor leverancierssamenwerking** in de module **Leverancierssamenwerking** en de lijst **Gebruikersaanvraag voor leverancierssamenwerking** in de module **Inkoopbeheer** (deze module is niet toegankelijk voor externe gebruikers).

### <a name="provision-a-user"></a>Een gebruiker inrichten

Voordat u een aanvraag voor de inrichting van een nieuwe gebruiker kunt indienen, moet die persoon zijn ingesteld als contactpersoon voor een of meer leveranciersrekeningen. Een aanvraag voor een nieuwe gebruiker voor leverancierssamenwerking maken:

1. Klik op de pagina **Alle contactpersonen** op **Gebruiker van leverancier inrichten**.
2. Voer een e-mailadres voor de gebruiker in. Dit adres wordt gebruikt door de gebruiker om zich aan te melden bij Supply Chain Management. Als het e-mailadres bij een domein hoort dat als tenant bij Microsoft Azure is geregistreerd, moet het e-mailadres voor een correcte inrichting een bestaand AAD-account (Azure Active Directory) zijn. Als het e-mailadres niet bij een domein hoort dat bij Microsoft Azure is geregistreerd, wordt een AAD-account gemaakt als onderdeel van het inrichtingsproces en ontvangt de nieuwe gebruiker per e-mail een uitnodiging. E-mailadressen van consumenten met domeinen als @hotmail.com, @gmail.com en @comcast.net kunnen niet worden gebruikt om een gebruiker te registreren.
3. Stel de optie **Toegang tot leverancierssamenwerking toegestaan** in op **Ja** voor alle rechtspersonen waartoe de gebruiker toegang nodig heeft.
4. Schakel in het gedeelte **Gebruikersrollen toewijzen** het selectievakje **Toewijzen** in voor de beveiligingsrollen die de nieuwe gebruiker moet hebben.
5. Klik op **Aanbieden**.

Wanneer de leveranciersgebruikersaanvraag wordt ingediend, wordt het veld **Toegang tot leverancierssamenwerking toegestaan** ingesteld op **Ja** voor de geselecteerde leveranciersrekening en wordt er een gebruikersaanvraagworkflow gestart. Als onderdeel van de werkstroom wordt een nieuwe gebruiker gemaakt en worden er beveiligingsrollen toegewezen. Daarnaast wordt een Azure B2B-service geactiveerd die interactie met de Azure-portal initieert en een nieuwe of bestaande AAD-account koppelt aan de Supply Chain Management-gebruikersaccount. Zie voor meer informatie Wat is [Azure Azure AD B2B-samenwerking?](/azure/active-directory/active-directory-b2b-what-is-azure-ad-b2b).

### <a name="inactivate-a-user"></a>Een gebruiker inactief maken

Er zijn twee manieren om toegang tot leverancierssamenwerking voor een gebruiker te verwijderen:

-   Op de pagina **Contactpersonen** voor de leverancier stelt u de optie **Toegang tot leverancierssamenwerking toegestaan** in op **Nee** voor de contactpersoon. Dit kan worden gedaan per rechtspersoon waarvoor de persoon een contactpersoon is. Deze optie kan alleen worden gebruikt door inkoopmedewerkers.
-   Maak de volledige gebruikersaccount inactief door de aanvraag **Leveranciersgebruiker inactief maken** te verzenden.

Een aanvraag indienen om een gebruiker inactief te maken:

1.  Klik op de pagina **Alle contactpersonen** op **Leveranciersgebruiker** **inactief maken**.
2.  Schrijf een opmerking in het veld **Zakelijke reden**.
3.  Klik op **Aanbieden**.

### <a name="modify-security-roles"></a>Beveiligingsrollen wijzigen

Het enige verschil tussen de pagina's **Rollen van gebruiker van leverancier onderhouden** en **Gebruiker van leverancier inrichten** is dat de lijst met beveiligingsrollen op de eerstgenoemde pagina kan worden bewerkt.  

Een wijziging in de beveiligingsrollen van een gebruiker aanvragen:

1.  Klik op de pagina **Alle contactpersonen** op **Rollen van gebruiker** **van leverancier onderhouden**.
2.  Schrijf een opmerking in het veld **Zakelijke reden**.
3.  Selecteer in het gedeelte **Gebruikersrollen onderhouden** de beveiligingsrollen die u wilt toewijzen of deselecteer de rollen die u wilt verwijderen.
4.  Klik op **Aanbieden**.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]