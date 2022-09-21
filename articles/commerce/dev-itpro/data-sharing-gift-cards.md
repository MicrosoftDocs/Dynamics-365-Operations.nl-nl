---
title: Delen van gegevens tussen meerdere bedrijven voor geschenkbonnen
description: In dit artikel wordt beschreven hoe u Microsoft Dynamics 365 Commerce de functionaliteit voor het delen van gegevens in gegevensgebieden met Dynamics 365 Finance configureert om geschenkbongegevens te synchroniseren.
author: BrianShook
ms.date: 08/26/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-06-20
ms.openlocfilehash: bc0df6c4aac72907e8523069e3f1ae100780dc3c
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9473926"
---
# <a name="cross-company-data-sharing-for-gift-cards"></a>Delen van gegevens tussen meerdere bedrijven voor geschenkbonnen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u Microsoft Dynamics 365 Commerce configureert, zodat het de functionaliteit voor het delen van gegevens met Dynamics 365 Finance gebruikt om geschenkbongegevens te synchroniseren. De functionaliteit voor het delen van gegevensrecords kan dan worden gebruikt om gegevens tussen twee gegevensgebieden te delen met meerdere bedrijven. Op deze manier kan de interne cadeautabel van Commerce gegevens tussen twee bedrijfsentiteiten delen. Zie [Delen van gegevens tussen bedrijven](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing) voor meer informatie over Dynamics 365 Finance.

## <a name="key-terms"></a>Belangrijke termen

| Voorwaarde | Description |
|---|---|
| Bedrijf | De rechtspersoon in de Dynamics 365 Finance-omgeving. |
| Geschenkbon | Het interne geschenkbonproduct van Dynamics 365 Commerce. |

## <a name="prerequisites"></a>Vereisten

Gebruikers moeten hun omgeving configureren voor het delen van gegevens tussen bedrijven, zoals beschreven in [Delen van gegevens tussen bedrijven](/dynamics365/fin-ops-core/dev-itpro/sysadmin/cross-company-data-sharing).

Voor **RetailGiftCardTable** moet het veld **DataSharingType** ingesteld zijn op **Dubbel** om 'duplicate record sharing (DRS)' voor de geschenkbontabel mogelijk te maken. Zie [Delen van gegevens tussen bedrijven voor ontwikkelaars](/dynamics365/fin-ops-core/dev-itpro/sysadmin/drs-srs-dev) voor meer informatie.

## <a name="configure-cross-company-data-sharing-for-gift-cards"></a>Delen van gegevens tussen bedrijven voor geschenkbonnen configureren

Configureer het delen van gegevens tussen bedrijven voor geschenkbonnen volgens deze stappen.

1. Ga in Commerce headquarters naar **Systeembeheer \> Instellen \> Delen van gegevens tussen bedrijven configureren**.
1. Selecteer **Nieuw** in het actiedeelvenster om een record voor gegevens delen toe te voegen.
1. Voer in het veld **Naam** een naam in voor de gegevensdelingsrecord (bijvoorbeeld **Geschenkbonnen**).
1. Selecteer **Toevoegen** in de sectie **Te delen tabellen en velden**.
1. Voer in het dialoogvenster **Nieuwe tabel delen** in het veld **Tabelnaam** de tekst **RETAILGIFTCARDTABLE** (de tabel voor detailhandelgeschenkbonnen) in. Het veld **Tabellabel** wordt automatisch ingesteld op **Geschenkbontabel**.
1. Zorg ervoor dat de selectievakjes **Gegevens opslaan per bedrijf**, **Bevat unieke index** en **Nog niet gedeeld** allemaal zijn ingeschakeld. De selectie van deze selectievakjes activeert validaties die zijn gerelateerd aan de functionaliteit voor gegevensdeling.
1. Selecteer **Tabel toevoegen**. De record **Geschenkbontabel (RetailGiftCardTable)** moet nu worden weergegeven onder **Te delen tabellen en velden**. Selecteer het caretteken (^) om alle tabelvelden weer te geven die automatisch voor delen aan de tabel zijn gekoppeld.
1. In de sectie **Bedrijven die de records in deze tabellen delen** selecteert u **Toevoegen** om een bedrijf toe te voegen waarmee u gegevens wilt delen.
1. Selecteer in de rij onder **Bedrijf** een bedrijf in de vervolgkeuzelijst.
1. Voer in het veld **Naam** de bedrijfsnaam in.
1. Herhaal stap 8 en 10 als u nog meer bedrijfsrijen wilt toevoegen.
1. Wanneer u klaar bent met het toevoegen van bedrijfsrijen, selecteert u **Inschakelen** in het actiedeelvenster.
1. U ontvangt een waarschuwingsbericht met de tekst "U kunt deze actie beter alleen uitvoeren buiten bedrijfsuren. elijktijdige transactiebewerkingen kunnen niet worden uitgevoerd voor tabellen in het beleid. Wilt u doorgaan?" Selecteer **Ja** om te bevestigen.
1. U krijgt een waarschuwingsbericht met de tekst: "Wilt u alle bestaande gegevens nu naar alle gedeelde bedrijven kopiëren?¨ Selecteer **Ja** om te bevestigen.

Wanneer u beide berichten hebt bevestigd, beginnen tabellen met het kopiëren van gegevens in de geconfigureerde bedrijven. Tegoeden die op de geschenkbon van het ene bedrijf komen, zullen dan zichtbaar zijn voor het andere bedrijf.

## <a name="additional-resources"></a>Aanvullende bronnen

[Veelgestelde vragen over betalingen](payments-retail.md)

[Kassamodule](../add-checkout-module.md)

[Betalingsmodule](../payment-module.md)
