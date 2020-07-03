---
title: Gebruikers van klantportal maken en beheren
description: In dit onderwerp wordt uitgelegd hoe u gebruikersaccounts voor de klantportal maakt en machtigingen hiervoor instelt.
author: dasani-madipalli
manager: tfehr
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: c56e41b8ea5039531205083b5b42aff05e05cf66
ms.sourcegitcommit: 713b5dfc76a6875d0ba6d86c5cbd585ea502cf9d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/01/2020
ms.locfileid: "3413951"
---
# <a name="create-and-manage-customer-portal-users"></a>Gebruikers van klantportal maken en beheren

In de standaardimplementatie kunnen gebruikers zichzelf niet zelf registreren voor websites die zijn gemaakt met de klantportal. Om zich aan te melden en een website te gebruiken moeten gebruikers door de beheerder worden uitgenodigd. Microsoft heeft de mogelijkheid voor gebruikers om zichzelf te registreren, opzettelijk geblokkeerd.

Voordat een gebruiker een website kan gebruiken, moet voor die gebruiker een contactpersoonrecord worden gemaakt. Deze record geeft aan bij welke klantaccount en rechtspersoon de gebruiker behoort. Deze informatie is essentieel om ervoor te zorgen dat de gebruiker verkooporders kan maken en weergeven.

Wanneer gebruikers zichzelf registreren, worden er automatisch contactpersoonrecords gemaakt. U kunt dus niet garanderen dat een gebruiker het juiste klantaccount en de juiste rechtspersoon selecteert. De uitnodigingsprocedure zorgt er daarentegen voor dat een beheerder het juiste klantaccount en de juiste rechtspersoon aan de contactpersoonrecord toewijst voordat er een uitnodiging wordt verzonden. Als u de oplossing wilt aanpassen zodat gebruikers zichzelf kunnen registreren, moet u rekening houden met de mogelijke gevolgen.

## <a name="prerequisite-setup"></a>Instellingsvereisten

Contactpersonen in Power Apps-portals worden als records opgeslagen in de entiteit **Contactpersonen** in Common Data Service. Met twee wegschrijven worden deze records vervolgens gesynchroniseerd in Microsoft Dynamics 365 Supply Chain Management, als dat nodig is.

![![Systeemdiagram voor contactpersonen van klantportal](media/customer-portal-contacts.png "Systeemdiagram voor contactpersonen van klantportal")](media/customer-portal-contacts.png "System diagram for Customer portal contacts")

Voordat u nieuwe klanten gaat uitnodigen, moet u controleren of u de entiteitstoewijzing **Contactpersoon** hebt ingeschakeld bij Twee keer wegschrijven.

## <a name="the-invitation-process"></a>Het uitnodigingsproces

Als u een bestaande contactpersoon wilt uitnodigen voor de klantportal, volgt u de stappen in [Contactpersonen uitnodigen voor uw portals](https://docs.microsoft.com/powerapps/maker/portals/configure/invite-contacts) in de documentatie voor Power Apps-portals.

Voordat u een klant kunt uitnodigen voor deelname aan de klantportal, controleert u of de [contactpersoonrecord van de klant](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) beschikbaar is en op de volgende manier is ingesteld:

1. Stel het veld **Bedrijf** in op de rechtspersoon in Supply Chain Management waaraan u de klant wilt toewijzen.
2. Stel het veld **Accountnummer** in op het nummer van het klantaccount in Supply Chain Management waaraan u de klant wilt toewijzen.

Nadat een contactpersoon is gemaakt, kunt u deze bekijken in Supply Chain Management.

Zie [Een contactpersoon configureren voor gebruik in een portal](https://docs.microsoft.com/powerapps/maker/portals/configure/configure-contacts) in de documentatie van Power Apps-portals voor meer informatie.

## <a name="out-of-box-web-roles-and-entity-permissions"></a>Standaard webrollen en entiteitsmachtigingen

Gebruikersrollen in Power Apps-portals worden gedefinieerd door [webrollen](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) en [entiteitsmachtigingen](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions). Een paar rollen zijn standaard gedefinieerd voor de klantportal. U kunt nieuwe rollen maken en bestaande rollen wijzigen of verwijderen.

### <a name="out-of-box-web-roles"></a>Standaard webrollen

In deze sectie worden de webrollen beschreven die bij de klantportal worden meegeleverd.

Zie [Webrollen voor portals maken](https://docs.microsoft.com/powerapps/maker/portals/configure/create-web-roles) en [Op records gebaseerde beveiliging toevoegen met behulp van entiteitsmachtigingen voor portals](https://docs.microsoft.com/powerapps/maker/portals/configure/assign-entity-permissions) in de documentatie van Power Apps-portals voor meer informatie over het wijzigen van de standaard gebruikersrollen.

#### <a name="administrator"></a>Beheerder

De beheerder houdt toezicht en onderhoudt de website. Deze persoon zal de klantportal opzetten en instellen. De beheerder onderhoudt de IT- en beveiligingsaspecten van de portal en zorgt ervoor dat alles probleemloos wordt uitgevoerd. De beheerder kan ook de portal aanpassen en/of wijzigen door nieuwe functies toe te voegen, nieuwe rollen te maken, enzovoort.

#### <a name="customer-representative"></a>Medewerker van klant

Een medewerker van de klant werkt voor een bedrijf en is verantwoordelijk voor het beheer van de orders die het bedrijf plaatst. Deze klantvertegenwoordiger kan alle orders zien die voor het bedrijf zijn geplaatst en de gebruikers die deze orders hebben geplaatst. Bovendien kan de medewerker van de klant informatie over het hele account bekijken en welke contactpersonen orders kunnen plaatsen namens dat account.

#### <a name="authorized-users"></a>Geautoriseerde gebruikers

Geautoriseerde gebruikers kunnen orders plaatsen en de status van de orders weergeven die ze hebben geplaatst. Ze kunnen echter niet de status weergeven van orders die andere gebruikers in hun bedrijf hebben geplaatst.

#### <a name="unauthorized-users"></a>Niet-geautoriseerde gebruikers

Niet-geautoriseerde gebruikers kunnen geen gegevens weergeven. Ze kunnen alleen openbare informatie zien, zoals voorwaarden en details over het bedrijf waarvoor de klantportal wordt uitgevoerd.

#### <a name="example"></a>Voorbeeld

In de volgende tabel ziet u welke verkooporders door de gebruikers van elke webrol in het systeem kunnen worden weergegeven.

| Verkooporder | Beheerder | Klantmedewerkers voor klant&nbsp;X | Geautoriseerde gebruiker: Jane | Geautoriseerde gebruiker: Sam | Niet-geautoriseerde gebruikers: May |
|---|---|---|---|---|---|
| Besteller klant&nbsp;X:&nbsp;Jane | Ja | Ja | Ja | No | No |
| Besteller klant&nbsp;X:&nbsp;Sam | Ja | Ja | No | Ja | No |
| Besteller&nbsp;klant Y:&nbsp;May | Ja | No | No | No | No |

> [!NOTE]
> Hoewel zowel Sam als Rob contactpersonen zijn voor klant X, kunnen ze alleen de orders zien die ze zelf hebben geplaatst en niets anders. Hoewel May een order heeft geplaatst, kan ze die order niet zien in de klantportal omdat ze een niet-geautoriseerde gebruiker is. (Ze moet de order bovendien hebben geplaatst via een ander kanaal dan de klantportal.)
