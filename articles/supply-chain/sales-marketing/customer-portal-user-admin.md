---
title: Gebruikers van klantportal maken en beheren (bevat video)
description: In dit artikel wordt uitgelegd hoe u gebruikersaccounts voor de klantportal maakt en machtigingen hiervoor instelt.
author: Henrikan
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-04-22
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: ec4f20daac39e1728ab46db159059e51a0cae0a6
ms.sourcegitcommit: 12b3dbee905f8b2eb2e6c383c822a0fc9fccf063
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/01/2022
ms.locfileid: "9103765"
---
# <a name="create-and-manage-customer-portal-users"></a>Gebruikers van klantportal maken en beheren

[!include [banner](../includes/banner.md)]


In de standaardimplementatie kunnen gebruikers zichzelf niet zelf registreren voor websites die zijn gemaakt met de klantportal. Om zich aan te melden en een website te gebruiken moeten gebruikers door de beheerder worden uitgenodigd. Microsoft heeft de mogelijkheid voor gebruikers om zichzelf te registreren, opzettelijk geblokkeerd.

Voordat een gebruiker een website kan gebruiken, moet voor die gebruiker een contactpersoonrecord worden gemaakt. Deze record geeft aan bij welke klantaccount en rechtspersoon de gebruiker behoort. Deze informatie is essentieel om ervoor te zorgen dat de gebruiker verkooporders kan maken en weergeven.

Wanneer gebruikers zichzelf registreren, worden er automatisch contactpersoonrecords gemaakt. U kunt dus niet garanderen dat een gebruiker het juiste klantaccount en de juiste rechtspersoon selecteert. De uitnodigingsprocedure zorgt er daarentegen voor dat een beheerder het juiste klantaccount en de juiste rechtspersoon aan de contactpersoonrecord toewijst voordat er een uitnodiging wordt verzonden. Als u de oplossing wilt aanpassen zodat gebruikers zichzelf kunnen registreren, moet u rekening houden met de mogelijke gevolgen.

## <a name="video"></a>Video
> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4ADkI]

De video [Klanten uitnodigen om uw klantenportal te registreren en te gebruiken](https://youtu.be/drGUYHX9QIQ) (zie hierboven) is opgenomen in de [afspeellijst voor Finance + Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) die beschikbaar is op YouTube.

## <a name="prerequisite-setup"></a>Instellingsvereisten

Contactpersonen in Power Apps-portals worden als records opgeslagen in de tabel **Contactpersonen** in Microsoft Dataverse. Met twee wegschrijven worden deze records vervolgens gesynchroniseerd in Microsoft Dynamics 365 Supply Chain Management, als dat nodig is.

![Systeemdiagram voor contactpersonen van klantportal.](media/customer-portal-contacts.png "Systeemdiagram voor contactpersonen van klantportal")

Voordat u nieuwe klanten gaat uitnodigen, moet u controleren of u de tabeltoewijzing **Contactpersoon** hebt ingeschakeld bij Twee keer wegschrijven.

## <a name="the-invitation-process"></a>Het uitnodigingsproces

Als u een bestaande contactpersoon wilt uitnodigen voor de klantportal, volgt u de stappen in [Contactpersonen uitnodigen voor uw portals](/powerapps/maker/portals/configure/invite-contacts) in de documentatie voor Power Apps-portals.

Voordat u een klant kunt uitnodigen voor deelname aan de klantportal, controleert u of de [contactpersoonrecord van de klant](/powerapps/maker/portals/configure/configure-contacts) beschikbaar is en op de volgende manier is ingesteld:

1. Stel het veld **Bedrijf** in op de rechtspersoon in Supply Chain Management waaraan u de klant wilt toewijzen.
2. Stel het veld **Accountnummer** in op het nummer van het klantaccount in Supply Chain Management waaraan u de klant wilt toewijzen.

Nadat een contactpersoon is gemaakt, kunt u deze bekijken in Supply Chain Management.

Zie [Een contactpersoon configureren voor gebruik in een portal](/powerapps/maker/portals/configure/configure-contacts) in de documentatie van Power Apps-portals voor meer informatie.

## <a name="out-of-box-web-roles-and-table-permissions"></a>Standaard webrollen en tabelmachtigingen

Gebruikersrollen in Power Apps-portals worden gedefinieerd door [webrollen](/powerapps/maker/portals/configure/create-web-roles) en [tabelmachtigingen](/powerapps/maker/portals/configure/assign-entity-permissions). Een paar rollen zijn standaard gedefinieerd voor de klantportal. U kunt nieuwe rollen maken en bestaande rollen wijzigen of verwijderen.

### <a name="out-of-box-web-roles"></a>Standaard webrollen

In deze sectie worden de webrollen beschreven die bij de klantportal worden meegeleverd.

Zie [Webrollen voor portals maken](/powerapps/maker/portals/configure/create-web-roles) en [Op records gebaseerde beveiliging toevoegen met behulp van tabelmachtigingen voor portals](/powerapps/maker/portals/configure/assign-entity-permissions) in de documentatie van Power Apps-portals voor meer informatie over het wijzigen van de standaard gebruikersrollen.

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
| Besteller klant&nbsp;X:&nbsp;Jane | Ja | Ja | Ja | Nee | Nee |
| Besteller klant&nbsp;X:&nbsp;Sam | Ja | Ja | Nee | Ja | Nee |
| Besteller&nbsp;klant Y:&nbsp;May | Ja | Nee | Nee | Nee | Nee |

> [!NOTE]
> Hoewel zowel Sam als Rob contactpersonen zijn voor klant X, kunnen ze alleen de orders zien die ze zelf hebben geplaatst en niets anders. Hoewel May een order heeft geplaatst, kan ze die order niet zien in de klantportal omdat ze een niet-geautoriseerde gebruiker is. (Ze moet de order bovendien hebben geplaatst via een ander kanaal dan de klantportal.)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
