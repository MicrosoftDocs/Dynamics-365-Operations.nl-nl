---
title: Niet-gekoppelde restituties verwerken met Dynamics 365 Commerce Payment Connector voor Adyen
description: In dit onderwerp wordt beschreven hoe niet-gekoppelde restituties werken wanneer Microsoft Dynamics 365 Payment Connector voor Adyen wordt gebruikt.
author: BrianShook
ms.date: 10/07/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.author: BrShoo
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: c137dcf7d35031a293c88d8c4f5dc1e5f3d9e2f9
ms.sourcegitcommit: a21a664cd35b95c8600c5af0aac588a64e892902
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/11/2021
ms.locfileid: "7623916"
---
# <a name="process-unlinked-refunds-with-the-dynamics-365-commerce-payment-connector-for-adyen"></a>Niet-gekoppelde restituties verwerken met Dynamics 365 Commerce Payment Connector voor Adyen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe niet-gekoppelde restituties werken wanneer [Microsoft Dynamics 365 Payment Connector voor Adyen](adyen-connector.md) wordt gebruikt. Daarnaast wordt gekeken naar de mogelijkheid om een restitutie te verwerken met een nieuwe betalingsmethode in een POS of callcenter.

Met Dynamics 365 Payment Connector voor Adyen kunt u restituties verwerken met een andere betalingsmethode dan is gebruikt voor de oorspronkelijke transactie. Hoewel het raadzaam is om [gekoppelde restituties](linked-refunds.md) te gebruiken om een restitutie te verwerken ten opzichte van de oorspronkelijke betalingsmethode die is opgegeven, zijn restituties op een andere betalingsmethode in sommige scenario's vereist. De kaart die voor de oorspronkelijke betaling is gebruikt, kan bijvoorbeeld nu zijn verlopen of verloren of kan zijn geannuleerd door de gebruiker.

## <a name="prerequisites"></a>Vereisten

Aan de volgende vereisten moet worden gedaan voordat niet-gekoppelde restituties kunnen worden verwerkt in Dynamics 365 Payment Connector voor Adyen:

- Stel [betalingsmethoden](../payment-methods.md) in.
- Stel [betalingen voor meerdere kanalen](../omni-channel-payments.md) in.

## <a name="additional-configuration"></a>Aanvullende configuratie

Dynamics 365 Payment Connector voor Adyen biedt een standaardimplementatie voor elk ondersteund restitutiescenario dat in de volgende sectie wordt beschreven. Klanten die de standaardimplementatie van Dynamics 365 Payment Connector voor Adyen niet gebruiken, moeten de connector instellen die tokenisatie van creditcards ondersteunt.

## <a name="supported-refund-scenarios"></a>Ondersteunde restitutiescenario's

Dynamics 365 Commerce ondersteunt restituties van van eerder goedgekeurde en bevestigde transacties. Restituties kunnen bestaan uit een volledige of gedeeltelijke restitutie van de transactie. Restituties kunnen niet het volledige bedrag van de oorspronkelijke betalingsautorisatie overschrijden. Niet-gekoppelde restituties worden alleen in het POS en callcenter ondersteund.

## <a name="enable-unlinked-refunds-functionality"></a>Functionaliteit voor niet-gekoppelde restituties inschakelen

Voer de volgende stappen uit om de functionaliteit voor niet-gekoppelde restituties in te schakelen in Commerce Headquarters.

1. Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde Commerce-parameters**.
1. Stel op het tabblad **Betalingen voor meerdere kanalen** de optie **Betalingen voor meerdere kanalen gebruiken** in op **Ja**.

### <a name="supported-payment-method-variants"></a>Ondersteunde betalingswijzevarianten

De volgende betalingsmethodevarianten ondersteunen niet-gekoppelde restituties standaard:

- Kaarten
- Portemonnee

Niet alle betalingsmethodevarianten ondersteunen niet-gekoppelde restituties. De volgende tabel bevat een lijst met gangbare betalingsmethoden en toont de ondersteuningsmogelijkheden van elke betalingsmethode voor gekoppelde en niet-gekoppelde restituties.

| Betaalwijze        | Gekoppelde restitutie | Niet-gekoppelde restitutie |
|-----------------------|:-------------:|:---------------:|
| amexcommercial        | Ja           | Ja             |
| amexconsumer          | Ja           | Ja             |
| amexcorporate         | Ja           | Ja             |
| amexdebit             | Ja           | Ja             |
| amexprepaid           | Ja           | Ja             |
| amexprepaidreloadable | Ja           | Ja             |
| amexsmallbusiness     | Ja           | Ja             |
| discover              | Ja           | Ja             |
| maestro               | Ja           | Ja             |
| maestrouk             | Ja           | Ja             |
| mc                    | Ja           | Ja             |
| mcalphabankbonus      | Ja           | Ja             |
| mcprepaidanonymous    | Ja           | Ja             |
| visa                  | Ja           | Ja             |
| visaalphabankbonus    | Ja           | Ja             |
| visacheckout          | Ja           | Ja             |
| visadankort           | Ja           | Ja             |
| visahipotecario       | Ja           | Ja             |
| visasaraivacard       | Ja           | Ja             |
| vpay                  | Ja           | Ja             |
| givex                 | **Nee**        | Ja             |
| svs                   | **Nee**        | Ja             |
| cup                   | Ja           | Ja             |
| diners                | Ja           | Ja             |
| interac               | **Nee**        | Ja             |
| jcb                   | Ja           | Ja             |
| jcb_applepay          | Ja           | Ja             |
| unionpay              | Ja           | Ja             |

### <a name="process-an-unlinked-refund-in-pos"></a>Een niet-gekoppelde restitutie in POS verwerken

Een klant retourneert een artikel aan een POS-kassamedewerker binnen de toegestane periode voor retouren en heeft een geldig ontvangstbewijs. Tijdens de verwerking van de retour bevat het dialoogvenster **Betaling retourneren** een optie **Een betalingsmethode kiezen**. De kassamedewerker kan vervolgens een betalingsmethode kiezen uit de ondersteunde betalingsmethoden voor restituties (kaarten en creditcards).

### <a name="process-an-unlinked-refund-in-call-center"></a>Een niet-gekoppelde restitutie in een callcenter verwerken

Wanneer een niet-gekoppelde restitutie wordt verwerkt voor een order in een callcenter, selecteert een medewerker van het callcenter een betalingsmethode die afwijkt van de oorspronkelijke methode. De werknemer wordt vervolgens gevraagd een pincode voor het overschrijven van een beheerder aan te vragen. De pincode is nodig voordat de andere betalingsmethode voor de restitutie kan worden verwerkt.

#### <a name="set-up-an-administrator-override-pin-for-call-center"></a>Een pincode voor het overschrijven van de beheerder instellen voor een callcenter

Als u voor een callcenter een pincode voor het overschrijven van de beheerder wilt instellen in Commerce Headquarters, gaat u als volgt te werk.

1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Instellingen van callcenter** of zoekt u naar Overschrijvingsmachtigingen.
1. Selecteer de rol om de niet-gekoppelde machtigingen voor restitutieverwerking toe te staan.
1. Stel op het sneltabblad **Retouren** de optie **Alternatieve betaling toestaan** in op **Ja**.

## <a name="additional-resources"></a>Aanvullende bronnen

[Dynamics 365 Payment Connector voor Adyen](adyen-connector.md)

[Gekoppelde restituties van eerder goedgekeurde en bevestigde transacties](linked-refunds.md)
