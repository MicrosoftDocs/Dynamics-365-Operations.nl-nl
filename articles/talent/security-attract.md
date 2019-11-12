---
title: Beveiliging en rollenbeheer in Attract
description: Dit onderwerp biedt informatie over rolbeveiliging in Microsoft Dynamics 365 Talent - Attract.
author: andreabichsel
manager: AnnBe
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 7db2ac241db121f07eb3524c7c5c9a8f64e78537
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/03/2019
ms.locfileid: "2551421"
---
# <a name="security-and-role-management-in-attract"></a>Beveiliging en rollenbeheer in Attract

[!include[banner](../includes/banner.md)]

In Microsoft Dynamics 365 Talent: Attract wordt op rollen gebaseerde beveiliging gebruikt. Toegang wordt met andere woorden niet verleend aan afzonderlijke gebruikers, maar aan de beveiligingsrollen waaraan de gebruikers zijn toegewezen. Een gebruiker aan wie een beveiligingsrol is toegewezen, heeft toegang tot de set bevoegdheden die aan die rol zijn gekoppeld.

Attract bevat vijf basisgebruikersrollen:

- Beheerder
- Aanstellend manager
- Werver
- Interviewer
- Alleen-lezen

De rol beheerder is de enige rol die gemachtigd is voor het toevoegen van andere gebruikers en om hun bevoegdheden te wijzigen.

- **Toevoegen**: selecteer in het beheercentrum op het tabblad **Gebruikersmachtigingen** **Rollen toewijzen**, zoek de gebruiker om toe te voegen en wijs vervolgens bevoegdheden aan die gebruiker toe.
- **Bewerken**: zoek de gebruiker of zoek de gebruiker in de lijst en selecteer **Bewerken** om zijn of haar bevoegdheden te wijzigen.
- **Verwijderen**: als u bevoegdheden van een gebruiker verwijdert, verwijdert u de gebruiker niet uit het systeem. U beperkt echter de toegang en de bevoegdheden van de gebruiker in Attract. Bijvoorbeeld Hilda is toegewezen aan de rol Aanstellend manager en zij wordt aan een functie toegevoegd als aanstellend manager. Als Hilda later wordt verwijderd uit de rol Aanstellend manager, blijft ze een aanstellend manager in de taak en heeft ze nog steeds toegang tot die taak. Zij kan echter geen andere taken maken.

De volgende secties bieden een beschrijving op hoog niveau van elke rol. De tabellen verderop in het onderwerp geven meer gedetailleerde informatie.

> [!NOTE]
> Sommige functies zijn alleen beschikbaar met de Uitgebreide invoegtoepassing voor aanstellingen voor Attract.

## <a name="administrator"></a>Beheerder

Gebruikers die zijn toegewezen aan de rol Beheerder, kunnen alle gegevens in Attract openen en wijzigen. Beheerders kunnen gegevens maken, lezen, bijwerken en verwijderen. Ze hebben ook toegang tot het beheercentrum, waar ze de Attract-toepassing kunnen configureren en gebruikersgegevens kunnen instellen. Het wordt aangeraden dat ten minste één persoon wordt toegewezen aan de beheerdersrol. Standaard wordt de omgevingsbeheerder in Microsoft PowerApps ingesteld als beheerder in Attract. Als u zich hebt aangemeld voor de evaluatieversie van Attract, wordt automatisch de rol beheerder aan u toegewezen. Op dit moment moeten gebruikers die de rol Beheerder hebben, voor het maken van taken ook de rol Werver of de rol Aanstellend manager hebben.

## <a name="hiring-manager"></a>Aanstellend manager

Gebruikers die zijn toegewezen aan de rol Aanstellend manager, kunnen taken maken en bijwerken van taken die ze eerder hebt gemaakt. Aanstellend managers kunnen slechts een beperkt aantal acties uitvoeren op een taak en de toepassingen die gekoppeld aan die taak zijn. Alleen gebruikers die zijn toegewezen aan de rol Aanstellend manager kunnen worden toegevoegd aan een aanstellend team als aanstellend managers.

## <a name="recruiter-role"></a>Rol Werver

Gebruikers die zijn toegewezen aan de rol Werver hebben volledige lees-, maak-, bijwerk- en verwijderbevoegdheden voor de taken die ze hebben gemaakt. Ze ook hebben volledige maak-, lees-, bijwerk- en verwijderbevoegdheden voor de toepassingen die zijn gekoppeld aan taken waarvan ze eigenaar zijn. Alleen gebruikers die zijn toegewezen aan de rol Werver, kunnen als wervers worden toegevoegd aan een aanstellend team.

## <a name="interviewer"></a>Afnemer van sollicitatiegesprek

Alle gebruikers met een Microsoft Azure Active Directory (Azure AD)-account in de organisatie kunnen worden toegevoegd aan een aanstellingsteam als interviewer. Gebruikers die zijn toegewezen aan de rol Interviewer, kunnen de taakdetails en sollicitantgegevens weergeven voor taken waarvoor ze in het aanstellend team zitten. Voor deze taken kunnen interviewers ook aanstellingsaanbevelingen doen en feedback over kandidaten geven. Ze kunnen echter niet de taakdetails of sollicitantgegevens bijwerken.

## <a name="read-only"></a>Alleen-lezen

Gebruikers die zijn toegewezen aan de rol Alleen-lezen, hebben alleen-lezen toegang tot alle gegevens in de Attract-omgeving. Ze kunnen echter geen gegevens maken of bewerken.

## <a name="find-out-which-roles-you-have"></a>Uitzoeken welke rollen u hebt

1.  Klik in Attract op het vraagteken (**?**) in de rechterbovenhoek van de pagina.

2.  Klik op **Info**.

    U ziet welke functies u hebt voor Attract in het venster dat verschijnt:

    ![Uw Attract-licentietype weergeven](media/attract-license-types.png)
    
## <a name="delegated-roles"></a>Gedelegeerde rollen

Voor elke taak waarvoor ze in het aanstellend team zitten, kunnen wervers en aanstellend managers een of meer gemachtigden voor henzelf aanwijzen. Zij kunnen echter geen gemachtigden aanwijzen voor andere mensen in het aanstellend team.

Gemachtigden hebben dezelfde bevoegdheden als de persoon die ze heeft aangewezen. Bijvoorbeeld: als een aanstellend manager een gedelegeerde voor zichzelf voor een taak aanwijst, heeft de gemachtigde dezelfde bevoegdheden als die aanstellend manager voor die taak. Gemachtigden kunnen andere gemachtigden niet verwijderen uit het aanstellend team. Ze kunnen ook niet de mensen verwijderen die hen hebben aangewezen als gemachtigden.

## <a name="job-details-and-actions"></a>Taakdetails en acties

Gebruikers met de rol Werver of Aanstellend manager kunnen taken maken. De volgende bevoegdheden gelden voor de taakdetails en de acties die op taken kunnen worden uitgevoerd.

| Gegevens of actie    | Werver | Aanstellend manager | Interviewer |
|-------------------|-----------|----------------|-------------|
| Functiedetails       | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Alleen-lezen |
| Wervingsteam       | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Alleen-lezen |
| Personeelsadvertentie       | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Alleen-lezen | Alleen-lezen |
| Proces           | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Alleen-lezen |
| Sollicitanten toevoegen    | Sollicitanten toevoegen voor taken waarvoor de gebruiker in het aanstellend team zit | Sollicitanten toevoegen voor taken waarvoor de gebruiker in het aanstellend team zit | Niet toegestaan |
| Kandidaten toevoegen     | Kandidaten toevoegen voor taken waarvoor de gebruiker in het aanstellend team zit | Een configuratieoptie in de [instelling van kandidaatactiviteit](./activities-attract.md#prospect-activity) bepaalt of interviewers kandidaten kunnen toevoegen en weergeven. | Niet toegestaan |
| Taak activeren      | Taken activeren waarvoor de gebruiker in het aanstellend team zit | Taken activeren waarvoor de gebruiker in het aanstellend team zit | Niet toegestaan |
| Functie sluiten         | Taken sluiten waarvoor de gebruiker in het aanstellend team zit | Niet toegestaan | Niet toegestaan |
| Functie verwijderen        | Taken verwijderen waarvoor de gebruiker in het aanstellend team zit | Alleen als er geen sollicitanten zijn toegevoegd aan de taak | Niet toegestaan |
| Sollicitanten verwijderen | Sollicitanten verwijderen als de gebruiker in het aanstellend team zit | Niet toegestaan | Niet toegestaan |

## <a name="application-details-and-actions"></a>Sollicitatiedetails en -acties

De volgende bevoegdheden gelden voor de taakspecifieke gegevens voor sollicitanten en de acties die op sollicitaties kunnen worden uitgevoerd.

| Gegevens of actie          | Werver | Aanstellend manager | Interviewer |
|-------------------------|-----------|----------------|-------------|
| Sollicitatiedocumenten   | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Alleen-lezen |
| Sollicitatienotities       | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Maken, lezen, bijwerken en verwijderen voor taken waarvoor de gebruiker in het aanstellend team zit | Alleen-lezen|
| Sollicitatieactiviteit    | Weergeven als de gebruiker in het aanstellend team zit | Weergeven als de gebruiker in het aanstellend team zit | Alleen-lezen |
| Sollicitatiefeedback    | Alle feedback toevoegen en weergeven als de gebruiker in het aanstellend team zit | Alle feedback toevoegen en weergeven als de gebruiker in het aanstellend team zit | Kan feedback toevoegen\*\* |
| Sollicitatie afwijzen      | Kan afwijzen als de gebruiker in het aanstellend team zit | Niet toegestaan | Niet toegestaan |
| Fase verder           | Kan afwijzen als de gebruiker in het aanstellend team zit | Kan vervolgen als de gebruiker in het aanstellend team zit | Niet toegestaan |
| Aanbiedingsbeheer starten | Kan aanbiedingsbeheer starten | Er is een configuratieoptie in de aanbiedingsactiviteit. | Niet toegestaan |


\*\* Een configuratieoptie in de [instelling van de feedbackactiviteit](./activities-attract.md) bepaalt of interviewers elkaars feedback kunnen zien.


## <a name="process-templates"></a>Processjablonen

De volgende bevoegdheden gelden voor aanstellingssjablonen. Het vermogen van teamleden om sjablonen te maken en bewerken wordt geconfigureerd in **Sjabloonbeheer** in het beheercentrum. Als sjabloonbeheer is ingeschakeld, kunnen wervers en aanstellend managers hun eigen processjablonen maken en bewerken. Als sjabloonbeheer is uitgeschakeld, kunnen alleen beheerders processjablonen maken en bewerken. In de volgende tabel wordt ervan uitgegaan dat sjabloonbeheer is ingeschakeld.

| Gegevens              | Werver                                           | Aanstellend manager                                      | Interviewer |
|-------------------|-----------------------------------------------------|-----------------------------------------------------|-------------|
| Processjablonen | Volledige bevoegdheden voor sjablonen die de gebruiker maakt | Volledige bevoegdheden voor sjablonen die de gebruiker maakt | Geen toegang   |

## <a name="email-and-email-templates"></a>E-mail en e-mailsjablonen

De volgende bevoegdheden gelden voor e-mailsjablonen en de acties die op e-mails kunnen worden uitgevoerd. Alleen beheerders kunnen e-mailsjablonen maken en bewerken.

| Gegevens of actie     | Werver          | Aanstellend manager     | Interviewer |
|--------------------|--------------------|--------------------|-------------|
| E-mailsjablonen    | Alleen-lezen toegang   | Alleen-lezen toegang   | Geen toegang   |
| E-mail verzenden         | Verzenden per activiteit  | Verzenden per activiteit  | Geen toegang   |
| E-mailinhoud | E-mailinhoud | E-mailinhoud | Geen toegang   |

## <a name="talent-pools"></a>Talentenpools

De volgende bevoegdheden zijn van toepassing op talentenpools. Talentenpools zijn alleen zichtbaar voor de persoon die ze heeft gemaakt, tenzij die persoon ze wil delen. Kandidaatzoekopdrachten kunnen worden gebruikt voor kandidaten die niet zijn toegevoegd aan een benoemde pool.

| Gegevens of actie   | Werver                                       | Aanstellend manager                                  | Interviewer |
|------------------|-------------------------------------------------|-------------------------------------------------|-------------|
| Benoemde pool       | Volledige bevoegdheden voor pools die de gebruiker maakt | Volledige bevoegdheden voor pools die de gebruiker maakt | Geen toegang   |
| Pool delen       | Alleen pools die de gebruiker maakt                | Alleen pools die de gebruiker maakt                | Geen toegang   |
| Kandidaat zoeken | Volledige zoekmogelijkheden                        | Volledige zoekmogelijkheden                        | Geen toegang   |

## <a name="candidates"></a>Kandidaten

Kandidaten zijn personen die zijn toegevoegd aan een talentenpool, maar die niet zijn gekoppeld aan een taak.

| Gegevens                        | Werver                        | Aanstellend manager                   | Interviewer |
|-----------------------------|----------------------------------|----------------------------------|-------------|
| Profiel: kandidaatdetails | Maken, lezen, bijwerken en verwijderen | Maken, lezen, bijwerken en verwijderen | Geen toegang   |
| Documenten                   | Maken, lezen, bijwerken en verwijderen | Maken, lezen, bijwerken en verwijderen | Geen toegang   |
