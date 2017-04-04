---
title: Gebruikers van leverancierssamenwerking beheren
description: In dit onderwerp wordt beschreven hoe u de inrichting van nieuwe gebruikers van de leverancierssamenwerking kunt aanvragen en hoe u nieuwe contactpersonen van de nieuwe leverancierssamenwerking kunt toevoegen.
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: smmContactPerson, VendVendorContactPerson, VendVendorPortalUser
audience: Application User, IT Pro
ms.search.scope: Operations, Core
ms.custom: 220744
ms.assetid: edc19ad0-3565-4d47-98ac-dda6098f63ac
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: f77012e7b64b7f153103e9bbe91e8ded202b509a
ms.openlocfilehash: 380f1bcdf7109dc12fd898199033eac7710d863c
ms.lasthandoff: 03/31/2017


---

# <a name="manage-vendor-collaboration-users"></a>Gebruikers van leverancierssamenwerking beheren

In dit onderwerp wordt beschreven hoe u de inrichting van nieuwe gebruikers van de leverancierssamenwerking kunt aanvragen en hoe u nieuwe contactpersonen van de nieuwe leverancierssamenwerking kunt toevoegen. 

De interface voor leverancierssamenwerking in Microsoft Dynamics 365 for Operations bevat informatie over inkooporders, facturen en consignatievoorraad voor externe leveranciers. U kunt nieuwe contactpersonen voor leverancierssamenwerking maken en vragen of nieuwe gebruikers worden ingericht als u als externe leverancier met de beveiligingsrol **Leveranciersbeheerder (extern)** of vergelijkbare machtigingen werkt. U kunt deze taken ook uitvoeren als u als inkoopmedewerker werkt. In dit onderwerp verwijst deze rol naar een inkoopmedewerker die in het bedrijf werkt dat het exemplaar van Dynamics 365 for Operations bezit. Zie voor meer informatie over het gebruik van leverancier samenwerking als u een externe leverancier [leverancier met klanten](vendor-collaboration-work-customers-dynamics-365-operations.md).  

Zie voor meer informatie over het gebruik van leverancier samenwerking als u een aanbesteding professionele [leverancier samenwerking aan met externe leveranciers,](vendor-collaboration-work-external-vendors.md).

## <a name="add-new-vendor-collaboration-contacts"></a>Nieuwe contactpersonen voor leverancierssamenwerking toevoegen
Als u iemand toegang tot leverancierssamenwerking wilt geven, moet deze persoon eerst als contactpersoon voor leverancierssamenwerking worden toegevoegd. U kunt ook contactpersonen voor werknemers in uw bedrijf toevoegen die geen leverancierssamenwerking gebruiken. Zij kunnen bijvoorbeeld fungeren als contactpunt voor andere typen aanschaffingsinformatie. Nieuwe contactpersonen worden toegevoegd op de **alle contactpersonen** pagina, dat toegankelijk is vanuit de **leverancier samenwerking**&gt;**contactpersonen** menu. Een nieuwe contactpersoon toevoegen:

1.  Klik op **Nieuw**.
2.  Voer de gegevens van de contactpersoon in.
3.  Kies welke rechtspersoon ze in uw bedrijf vertegenwoordigen en met welke rechtspersoon ze werken in het bedrijf waarmee ze zullen samenwerken. U hiertoe een **rechtspersoon in mijn bedrijf**/**rechtspersoon in het bedrijf van klant** paar.
4.  Klik op **Maken**.

Als u een contactpersoon wilt verwijderen, kunt u alleen de contactpersonen verwijderen die u hebt gemaakt.

## <a name="vendor-collaboration-user-requests"></a>Gebruikersaanvragen voor leverancierssamenwerking
Gebruikersaanvragen voor leverancierssamenwerking kunnen worden ingediend door een inkoopmedewerker of een beheerder van een externe leverancier.

-   Als u een externe leverancier bent, u indienen aanvragen van de **alle contactpersonen** pagina binnen de **leverancier samenwerking** module.
-   Als u een inkoopmedewerker bent, verzendt u aanvragen vanaf de pagina **Contactpersonen weergeven**. Hiertoe op de registratie van de leverancier in de **Setup** sectie in het actievenster de optie **contactpersonen**&gt;**contactpersonen weergeven**.

U kunt een aanvraag indienen om een gebruiker in te richten, een gebruiker te deactiveren of beveiligingsrollen te wijzigen. Als u een beheerder van een externe leverancier bent, moet u als contactpersoon zijn geregistreerd voor de leveranciersrekeningen waarvoor u gebruikersaanvragen wilt maken en u moet toegang tot de interface voor leverancierssamenwerking hebben voor deze leveranciersrekeningen.  

Wanneer een aanvraag wordt ingediend, wordt deze toegevoegd aan de lijst **Gebruikersaanvragen voor leverancierssamenwerking** in de module **Leverancierssamenwerking** en de lijst **Gebruikersaanvraag voor leverancierssamenwerking** in de module **Inkoopbeheer** (deze module is niet toegankelijk voor externe gebruikers).

### <a name="provision-a-user"></a>Een gebruiker inrichten

Voordat u een aanvraag voor de inrichting van een nieuwe gebruiker kunt indienen, moet die persoon zijn ingesteld als contactpersoon voor een of meer leveranciersrekeningen. Een aanvraag voor een nieuwe gebruiker voor leverancierssamenwerking maken:

1.  Op de **alle contactpersonen** pagina, klikt u op **voorziening leveranciersgebruiker**.
2.  Voer een e-mailadres voor de gebruiker in. Dit adres wordt door de gebruiker gebruikt om zich aan te melden bij Dynamics 365 for Operations. Als het e-mailadres bij een domein hoort dat als tenant bij Microsoft Azure is geregistreerd, moet het e-mailadres voor een correcte inrichting een bestaand AAD-account (Azure Active Directory) zijn. Als het e-mailadres niet bij een domein hoort dat bij Microsoft Azure is geregistreerd, wordt een AAD-account gemaakt als onderdeel van het inrichtingsproces en ontvangt de nieuwe gebruiker per e-mail een uitnodiging. E-mailadres consument adressen met domeinen, zoals @hotmail.com, @gmail.com, of @comcast.netkan niet worden gebruikt voor het registreren van een Dynamics 365 voor bewerkingen gebruiker.
3.  Stel de optie **Toegang tot leverancierssamenwerking toegestaan** in op **Ja** voor alle rechtspersonen waartoe de gebruiker toegang nodig heeft.
4.  Schakel in het gedeelte **Gebruikersrollen toewijzen** het selectievakje **Toewijzen** in voor de beveiligingsrollen die de nieuwe gebruiker moet hebben.
5.  Klik op **Aanbieden**.

Wanneer de gebruikersaanvraag leverancier wordt ingediend, de **leverancier samenwerking toegang toegestaan** veld is ingesteld op **Ja** voor de geselecteerde leveranciersrekening en de gebruiker vragen werkstroom is gestart. Als onderdeel van de werkstroom wordt een nieuwe gebruiker gemaakt in Dynamics 365 for Operations en worden er beveiligingsrollen toegewezen. Daarnaast wordt een Azure B2B-service geactiveerd die interactie met de Azure-portal initieert en een nieuw of bestaand AAD-account koppelt aan het Dynamics 365 for Operations-gebruikersaccount.

### <a name="inactivate-a-user"></a>Een gebruiker inactief maken

Er zijn twee manieren om toegang tot leverancierssamenwerking voor een gebruiker te verwijderen:

-   Op de pagina **Contactpersonen** voor de leverancier stelt u de optie **Toegang tot leverancierssamenwerking toegestaan** in op **Nee** voor de contactpersoon. Dit kan worden gedaan per rechtspersoon waarvoor de persoon een contactpersoon is. Deze optie kan alleen worden gebruikt door inkoopmedewerkers.
-   Maak de volledige gebruikersaccount inactief door de aanvraag **Leveranciersgebruiker inactief maken** te verzenden.

Om aan te vragen dat een gebruiker is uitgeschakeld:

1.  Op de **alle contactpersonen** pagina, klikt u op **uit****leveranciersgebruiker**.
2.  Schrijf een opmerking in het veld **Zakelijke reden**.
3.  Klik op **Aanbieden**.

### <a name="modify-security-roles"></a>Beveiligingsrollen wijzigen

De **leverancier gebruikersrollen beheren** pagina gelijk is aan de **voorziening leveranciersgebruiker** pagina, behalve dat de lijst met beveiligingsrollen kan worden bewerkt.  

Om aan te vragen dat de beveiligingsrollen voor een gebruiker worden gewijzigd:

1.  Op de **alle contactpersonen** pagina, klikt u op **onderhouden****gebruikersrollen leverancier**.
2.  Schrijf een opmerking in het veld **Zakelijke reden**.
3.  Selecteer in het gedeelte **Gebruikersrollen onderhouden** de beveiligingsrollen die u wilt toewijzen of deselecteer de rollen die u wilt verwijderen.
4.  Click **Submit**.



