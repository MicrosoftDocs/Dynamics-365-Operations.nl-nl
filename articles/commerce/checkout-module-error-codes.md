---
title: Foutverwijzingscodes voor betalingsmodule
description: Dit artikel beschrijft de foutverwijzingscodes van de betalingsmodule die worden weergegeven in foutberichten voor de gebruiker in Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 10/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2022-09-20
ms.openlocfilehash: 952cb932522b4e0bb91be985e4f8974cb6cd8bc0
ms.sourcegitcommit: 435e69160dbd7f9c61b37ac4440285a5df144622
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/28/2022
ms.locfileid: "9728240"
---
# <a name="checkout-module-error-reference-codes"></a>Foutverwijzingscodes voor betalingsmodule

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dit artikel beschrijft de foutcodes van de betalingsmodule die worden weergegeven in foutberichten voor de gebruiker in Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce heeft gestandaardiseerde foutverwijzingen ingevoerd die kunnen worden opgenomen in betalingsfouten van online kanalen die worden getoond aan online klanten. In Commerce versie 10.0.31 en hoger bevatten foutberichten in de betalingsmodule foutcodes en wordt geen onnodige informatie weergegeven aan de online klant. De foutcodes verwijzen naar fouten die gedetailleerd worden beschreven in dit artikel.

Afhankelijk van de fout die is opgetreden, bevat de tabel in dit artikel de volgende details:

- Een omschrijving van de voorwaarde die de fout heeft veroorzaakt, of aanvullende details
- Informatie ter overweging bij de configuraties van de omgeving of betalingsconnector
- Informatie waarnaar in een ondersteuningsaanvraag kan worden verwezen als aanvullende assistentie is vereist

## <a name="prerequisites"></a>Vereisten

Als u de onderstaande foutverwijzingscodes voor de uitcheckmodule wilt inschakelen, gaat u in Site Builder voor uw site naar **Site-instellingen \> Extensies** en selecteert u in de sectie **Winkelwagen en uitchecken** de optie **Betere berichtgeving over foutmeldingen in het online kanaal inschakelen**. 

## <a name="checkout-module-error-reference-codes"></a>Foutverwijzingscodes voor betalingsmodule

Gebruik de volgende tabel voor meer details over verwijzingen naar foutcodes die worden geleverd door klanten of worden ervaren in de online winkel. Schuif naar rechts om de kolom **Foutbeschrijving** weer te geven.

| Foutcode | Met Dynamics samenhangende foutcode | Foutomschrijving |
| ---------- | ------------------------------ | ----------------- |
| CCR001     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardTypeMissingOrNotSupported | De betaling kan niet worden geautoriseerd. Kaarttype-id in **TokenizedPaymentCard** ontbreekt of opgegeven kaarttype-id wordt niet ondersteund. |
| CCR002     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePayment | Geweigerd. De betaling kan niet worden geautoriseerd. |
| CCR003     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToAuthorizePaymentCardAdditionalContextRequired | De betaling kan niet worden geautoriseerd. Aanvullende informatie vereist van de klant. |
| CCR004     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToRetrieveCardPaymentAcceptResult | Sorry, er is een fout opgetreden. Het resultaat van de acceptatie van de kaartbetaling kan niet worden verkregen. Probeer het opnieuw of neem contact op met uw systeembeheerder. |
| CCR005     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentRequiresMerchantProperties | Kan geen betaling doen vanwege ontbrekende betalingseigenschappen van winkel. Neem contact op met uw systeembeheerder. |
| CCR006     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidPaymentRequest | Kan de betalingsservice voor de bewerking niet ophalen. Controleer uw betalingsmethode-instellingen voor de betalingsmethode die is geselecteerd. |
| CCR007     | Microsoft\_Dynamics\_Commerce\_Runtime\_MultipleCustomerAccountPaymentsNotAllowed | Er is al een betaling met de klantrekening toegepast. Slechts één betaling per transactie is toegestaan. |
| CCR008     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountLimitSignDifferentFromAmountDue | De klantrekeninglimiet verschilt van het verschuldigde bedrag. Probeer een andere betalingsmethode of neem contact op met de klantondersteuning voor assistentie. |
| CCR009     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsTotalAmountForCarryOutAndReturnItems | De klantrekeningbetaling is hoger dan de totale verschuldigde hoeveelheid voor de vermelde artikelen. Probeer het later opnieuw of neem contact op met de klantenondersteuning voor assistentie. |
| CCR010     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentUsingUnauthorizedAccount | Voor de klantrekeningbetaling is een eigen rekening vereist of een vereffeningsfactuurrekening op een betalingsmethoderegel. |
| CCR011     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentExceedsCustomerAccountFloorLimit | Kan een betaling van een klantrekening op dit moment niet verwerken: de ondergrens is overschreden. |
| CCR012     | Microsoft\_Dynamics\_Commerce\_Runtime\_CustomerAccountPaymentForCustomerWithoutAllowOnAccount | Deze klant mag niet betalen op rekening. |
| CCR013     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToCancelPayment | Sorry, er is een fout opgetreden. De betaling kan niet worden geannuleerd. Probeer het opnieuw. |
| CCR014     | Microsoft\_Dynamics\_Commerce\_Runtime\_UnableToReadCardTokenInfo | Er is een fout opgetreden bij het verwerken van de betaling. Probeer het later opnieuw. |
| CCR015     | Microsoft\_Dynamics\_Commerce\_Runtime\_NotEnoughRewardPoints | Het loyaliteitsbetalingsbedrag overschrijdt hetgeen is toegestaan voor de gebruikte loyaliteitskaart in deze transactie. |
| CCR016     | Microsoft\_Dynamics\_Commerce\_Runtime\_RefundAmountMoreThanAllowed | Het loyaliteitsrestitutiebedrag overschrijdt hetgeen is toegestaan voor de gebruikte loyaliteitskaart in deze transactie. |
| CCR017     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidLoyaltyCardNumber | Het loyaliteitskaartnummer is niet gevonden. Activeer het loyaliteitskaartnummer of voer een ander kaartnummer in en probeer het opnieuw. |
| CCR018     | Microsoft\_Dynamics\_Commerce\_Runtime\_BlockedLoyaltyCard | Het loyaliteitskaartnummer is niet beschikbaar. Voer een ander kaartnummer in en probeer het opnieuw. |
| CCR019     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoTenderLoyaltyCard | Deze loyaliteitskaart is niet gerechtigd om loyaliteitspunten in te wisselen voor deze transactie. |
| CCR020     | Microsoft\_Dynamics\_Commerce\_Runtime\_GiftCardCurrencyMismatch | Er is een fout opgetreden bij het nummer van de geschenkbon. Probeer een andere geschenkbon of neem contact op met de klantondersteuning voor assistentie. |
| CCR021     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAmountExceedsGiftBalance | Het bedrag overschrijdt het saldo op de geschenkbon. Voer een ander bedrag in en probeer het opnieuw. |
| CCR022     | Microsoft\_Dynamics\_Commerce\_Runtime\_NoMoreThanOneLoyaltyTender | De transactie kan niet meer dan een loyaliteitsbetalingsregel bevatten. |
| CCR023     | Microsoft\_Dynamics\_Commerce\_Runtime\_PaymentAlreadyVoided | Gegevens in de betalingsgegevens ontbreken of zijn onjuist. Controleer de betalingsgegevens en probeer het opnieuw. |
| CCR024     | Microsoft\_Dynamics\_Commerce\_Runtime\_FraudRisk | De order kan momenteel niet worden verwerkt. Probeer het later opnieuw. |
| CCR025     | Time-out bij front-end voor betalings-API | Time-out opgetreden bij front-endbewerking. Bevestig dat de order is verwerkt in Dynamics 365 Commerce headquarters. |
| CCR026     | Oorspronkelijk geautoriseerd bedrag gewijzigd | Het orderbedrag is anders dan het oorspronkelijke autorisatiebedrag dat met de betalingsgateway is verwerkt. Dit kan het gevolg zijn van het vervallen van een coupon, promotie of verkoop. |
| CCR027     | Microsoft\_Dynamics\_Commerce\_Runtime\_InvalidCartVersion | Er is een fout opgetreden bij het verwerken van een betaling. De verwijzing die wordt geleverd aan de winkelwagen-API heeft een andere verwijzing dan verwacht (mogelijke inconsistenties tijdens het uitcheckproces). |
| CCR028     | Microsoft\_Dynamics\_Commerce\_Runtime\_MissingRequiredCartTenderLines | Er is een fout opgetreden bij de geprobeerde betalingsmethode. Neem contact op met ondersteuning om uw rekeninginstellingen te bekijken of probeer het opnieuw met een andere betalingsmethode. |

## <a name="additional-resources"></a>Aanvullende bronnen

[Veelgestelde vragen over betalingen](dev-itpro/payments-retail.md)

[Betalingsmodule](add-checkout-module.md)

[Betalingsmodule](payment-module.md)
