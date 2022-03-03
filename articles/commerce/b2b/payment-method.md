---
title: De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites
description: In dit onderwerp wordt beschreven hoe u de betalingsmethode voor de klantrekening configureert in Microsoft Dynamics 365 Commerce. Hierin wordt ook beschreven hoe kredietlimieten van invloed zijn op het vastleggen van a conto-betalingen op e-commercesites voor B2B (business-to-business).
author: josaw1
ms.date: 02/16/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0366f7b51ac138cc7305f98d5607c554440e6d34
ms.sourcegitcommit: 68114cc54af88be9a3a1a368d5964876e68e8c60
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/17/2022
ms.locfileid: "8323350"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de betalingsmethode voor de klantrekening configureert in Microsoft Dynamics 365 Commerce. Hierin wordt ook beschreven hoe kredietlimieten van invloed zijn op het vastleggen van a conto-betalingen op e-commercesites voor B2B (business-to-business).

Detailhandelaren kunnen verschillende typen betalingen accepteren voor de producten en diensten die ze verkopen in een e-commercekanaal. Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd in Dynamics 365 Commerce wanneer het systeem wordt ingesteld. De betalingsmethode voor de klantrekening (of 'a conto') moet worden ondersteund op B2B-e-commercesites. 

## <a name="prerequisites"></a>Vereisten

1. Voeg de betalingsmethode voor klantrekeningen toe in Commerce Headquarters.
2. Koppel de betalingsmethode voor de klantrekening aan het e-commercekanaal.
3. Zorg ervoor dat de eigenschap **Op rekening toestaan** is ingeschakeld voor de klant bij **Retail en commerce \> Klanten \> Alle klanten \> Standaardwaarden betalingen** in Commerce Headquarters.

    > [!NOTE]
    > Als alle klanten de a conto-betalingsmethode moeten kunnen inschakelen, kunt u de eigenschap **Op rekening toestaan** instellen op **Ja** voor de standaardklant van het kanaal dat aan de B2B-site is gekoppeld. 

## <a name="enable-the-customer-account-payment-method-in-commerce-site-builder"></a>De betalingsmethode voor de klantrekening inschakelen in Commerce-site builder 

Volg deze stappen om de betalingsmethode voor de klantrekening in te schakelen in Commerce-site builder.

1. Ga naar **Site-instellingen \> Extensies**.
1. Stel de eigenschap **Betalingen van klantrekeningen inschakelen** in op **Ingeschakeld voor B2B-klanten**. 
1. Selecteer **Opslaan en publiceren**.

> [!NOTE]
> De nieuwe site-instellingen worden pas van kracht nadat het bestand app.settings.json is bijgewerkt. Zie [Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md) voor meer informatie.

## <a name="enable-the-customer-account-payment-method-on-the-checkout-page-for-the-b2b-e-commerce-site"></a>De betalingsmethode voor de klantrekening inschakelen op de uitcheckpagina voor de B2B-e-commercesite

Volg deze stappen om de betalingsmethode voor de klantrekening in te schakelen op de uitcheckpagina voor de B2B-e-commercesite.

1. In de Commerce-site builder kunt u de uitcheckpagina of het fragment bekijken en bewerken met de uitcheckmodule voor de B2B-e-commercesite.
1. Selecteer in het vak **Container van uitchecksectie** de optie **Module toevoegen** en voeg vervolgens een module **Betaling van klantrekening** toe.
1. Plaats de module **Betalingen van klantrekening** door de ellipen (**...**) te selecteren en vervolgens **Omhoog** of **Omlaag** te selecteren.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

## <a name="confirm-that-the-customer-account-payment-method-has-been-enabled-and-published"></a>Controleren of de betalingsmethode voor de klantrekening is ingeschakeld en gepubliceerd

Volg deze stappen om te controleren of de betalingsmethode voor de klantrekening is ingeschakeld

1. Meld u aan bij de e-commercesite.
1. Voeg een product aan de winkelwagen toe.
1. Ga naar de uitcheckpagina. U ziet nu de nieuwe betalingsmethode voor de **Klantrekening**.

## <a name="work-with-credit-limits"></a>Werken met kredietlimieten

Wanneer de mogelijkheden voor klantrekeningbetalingen zijn ingeschakeld op de B2B-site, willen organisaties doorgaans informatie over kredietlimieten en kredietlimietsaldi tonen tijdens het ordervastleggingsproces. De kredietlimiet voor een klant wordt gedefinieerd door de eigenschap **Kredietlimiet** op het sneltabblad **Crediteringen en aanmaningen** van de klantrecord in Commerce Headquarters. In B2B-scenario's moet een order die een klant vaak plaatst ook worden gefactureerd aan de rekening van de organisatie waar de klant bij hoort. Daarom moet u de eigenschap **Te factureren rekening** op het sneltabblad **Factuur en levering** van de klantrecord instellen op de klantrekening-id van de organisatie. Wanneer de klant vervolgens een order plaatst op de B2B-site, wordt de order aan de organisatie gefactureerd. De B2B-site gebruikt ook de kredietlimiet van de organisatie in plaats van de kredietlimiet die in de klantrecord is gedefinieerd.

De berekening en het saldo van kredietlimieten die worden weergegeven op de B2B-website zijn afhankelijk van de instelling van de eigenschap **Type kredietlimiet** in Commerce Headquarters. De locatie van deze eigenschap varieert, afhankelijk van de functie **Kredietbeheer** is ingeschakeld in de werkruimte **Functiebeheer**:

- Als de functie **Kredietbeheer** is ingeschakeld, bevindt de eigenschap zich op het sneltabblad **Kredietlimieten** in **Crediteringen en aanmaningen \> Instellen \> Parameters voor crediteringen en aanmaningen \> Krediet**. 
- Als de functie **Creditbeheer** is uitgeschakeld, bevindt de eigenschap zich onder **Kredietbeoordeling** in **Klanten \> Instellen \> Parameters van module Klanten \> Kredietbeoordeling**.

De waarden die door de eigenschap **Kredietlimiettype** worden ondersteund, zijn **Geen**, **Saldo**, **Saldo + pakbon of productontvangstbon** en **Saldo + Alle**. Zie [Kredietlimiettypewaarden](/dynamics365/supply-chain/sales-marketing/credit-limits-customers) voor meer informatie over deze waarden.

> [!NOTE]
> We raden u aan om de eigenschap **Kredietlimiettype** in te stellen op **Saldo + verpakkingsbon of productbon**, zodat openstaande verkooporders niet bijdragen aan de saldoberekening. Als uw klanten toekomstige orders plaatsen, hoeven ze niet te vrezen dat deze orders invloed hebben op hun huidige saldo.

Een andere eigenschap die invloed heeft op a conto-orders is de eigenschap **Verplichte kredietlimiet**. Deze bevindt zich op het sneltabblad **Crediteringen en aanmaningen** van de klantrecord. Door deze eigenschap in te stellen op **Ja** voor specifieke klanten, kunt u het systeem dwingen om hun kredietlimiet te controleren, zelfs als de eigenschap **Kredietlimiettype** is ingesteld op **Geen** om op te geven dat de kredietlimiet niet moet worden gecontroleerd voor een klant.

Op dit moment hebben B2B-locaties waarvoor de eigenschap **Verplichte kredietlimiet** is ingeschakeld extra functionaliteit. Als de eigenschap is ingeschakeld voor een klantrecord en de klant een order plaatst, verhindert de B2B-site dat de a conto-betalingswijze wordt gebruikt om meer te betalen dan het resterende creditsaldo. Als het resterende creditsaldo van de klant $ 1000 is en de order een waarde van $ 1200 heeft, kan de klant maar $ 1000 betalen via de a conto-methode. In dat geval moet de klant een andere betalingswijze gebruiken om het saldo te betalen. Als de eigenschap **Verplichte kredietlimiet** is uitgeschakeld voor een klantrecord, kan de klant elk bedrag betalen met de a conto-betalingswijze. Hoewel een klant wel orders kan plaatsen, staat het systeem niet toe dat deze orders worden afgehandeld als ze de kredietlimiet overschrijden. Als u de kredietlimiet moet controleren voor alle klanten die in aanmerking komen voor a conto-betalingen, raden we u aan om de eigenschap **Kredietlimiettype** op **Saldo + verpakkingsbon of productbon** en **Verplichte kredietlimiet** op **Nee** in te stellen.

De module **Crediteringen en aanmaningen** biedt nieuwe mogelijkheden voor kredietbeheer. Als u deze mogelijkheden wilt inschakelen, moet u de functie **Kredietbeheer** in de werkruimte **Functiebeheer** inschakelen. Met een van de nieuwe mogelijkheden kunnen verkooporders in de wachtstand worden gezet op basis van blokkeringsregels. De persona kredietbeheerder kan de orders vervolgens na een nadere analyse vrijgeven of afwijzen. De mogelijkheid om verkooporders in de wachtstand te plaatsen is echter niet van toepassing op Commerce-orders, omdat verkooporders vaak een vooruitbetaling hebben en de functie **Creditbeheer** vooruitbetalingsscenario's niet volledig ondersteunt. 

Als een klantsaldo de kredietlimiet overschrijdt tijdens de afhandeling van de order, worden de verkooporders niet in de wacht gezet, ongeacht of de functie **Kredietbeheer** is ingeschakeld. In plaats daarvan wordt in Commerce een waarschuwingsbericht of een foutbericht gegenereerd, afhankelijk van de waarde van het veld **Bericht bij overschrijding van de kredietlimiet** op het sneltabblad **Kredietlimiet**.

De eigenschap **Uitsluiten van kredietbeheer** waardoor Commerce-verkooporders niet in de wacht kunnen worden gezet, bevindt zich in de koptekst van de verkooporder (**Retail en commerce \> Klanten \> Alle verkooporders**). Als deze eigenschap is ingesteld op **Ja** (de standaardwaarde) voor Commerce-verkooporders, worden de orders uitgesloten van de wachtwerkstroom voor kredietbeheer. Hoewel de eigenschap de naam **Uitsluiten van kredietbeheer** heeft, wordt de gedefinieerde kredietlimiet nog wel gebruikt tijdens orderafhandeling. De orders worden niet meer in de wachtstand gezet.

De mogelijkheid om Commerce-verkooporders in de wacht zetten op basis van blokkeringsregels wordt gepland voor toekomstige Commerce-releases. Tot deze functie wordt ondersteund, kunt u de volgende XML-bestanden in uw Visual Studio-oplossing aanpassen als u Commerce-verkooporders moet dwingen om door de nieuwe kredietbeheerstromen te gaan. Pas in de bestanden de logica aan zodat de markering **CredManExcludeSalesOrder** op **Nee** wordt ingesteld. Op deze manier wordt de eigenschap **Uitsluiten van creditbeheer** standaard ingesteld op **Geen** voor Commerce-verkooporders.

- RetailCreateCustomerOrderExtensions_CredMan_Extension.xml
- RetailCallCenterOrderExtensions_CredMan_Extension.xml

Als de markering **CredManExcludeSalesOrder** wordt ingesteld op **Nee** en een B2B-klant bij winkels kan inkopen via de POS-toepassing, kan het boeken van contante transacties mislukken. Er is bijvoorbeeld een blokkeringsregel voor het type contantbetaling en de B2B-klant koopt bepaalde artikelen contact in de winkel. In dit geval kan de resulterende verkooporder niet worden gefactureerd omdat deze in de wachtstand wordt gezet. Daarom mislukt de boeking. Daarom is het raadzaam om end-to-end tests uit te voeren nadat u deze aanpassing hebt geïmplementeerd.

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2B-e-commercesite instellen](set-up-b2b-site.md)

[B2B-zakenpartners beheren met behulp van klanthiërarchieën](partners-customer-hierarchies.md)

[Gebruikers van zakelijke partners beheren op e-commercesites voor B2B](manage-b2b-users.md)

[De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites](quantity-limits.md)

[Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
