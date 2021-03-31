---
title: De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites
description: In dit onderwerp wordt beschreven hoe u de betalingsmethode voor klantrekeningen configureert voor B2B-e-commercesites (business-to-business).
author: josaw1
manager: AnnBe
ms.date: 01/20/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailOperations
audience: Application User, IT Pro
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: josaw
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 82dfd6ac7e97d838ef442fd6ded4a4f165fc795b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5211196"
---
# <a name="configure-the-customer-account-payment-method-for-b2b-e-commerce-sites"></a>De betalingsmethode voor de klantrekening configureren voor B2B-e-commercesites

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u de betalingsmethode voor klantrekeningen configureert voor B2B-e-commercesites (business-to-business).

Detailhandelaren kunnen verschillende typen betalingen accepteren voor de producten en diensten die ze verkopen in een e-commercekanaal. Elk betalingstype dat een detailhandelaar accepteert, moet worden geconfigureerd in Microsoft Dynamics 365 Commerce wanneer het systeem wordt ingesteld. De betalingsmethode voor de klantrekening (of 'a conto') moet worden ondersteund op B2B-e-commercesites. 

## <a name="prerequisites"></a>Vereisten

1. Voeg de betalingsmethode voor klantrekeningen toe in Commerce Headquarters.
2. Koppel de betalingsmethode voor de klantrekening aan het e-commercekanaal.
3. Zorg ervoor dat **Op rekening toestaan** is ingeschakeld voor de klant bij **Retail en commerce \> Klanten \> Alle klanten \> Standaardwaarden betalingen** in Commerce Headquarters. Zorg er ook voor dat de parameters voor **Kredietlimiet** goed zijn ingesteld voor de klant bij **Retail en commerce \> Klanten \> Alle klnanten \> Crediteringen en aanmaningen** in Commerce Headquarters. 

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

## <a name="additional-resources"></a>Aanvullende bronnen

[Een B2B-e-commercesite instellen](set-up-b2b-site.md)

[Hiërarchieën voor organisatiemodellering voor B2B-organisaties maken](org-model.md)

[Gebruikers van zakenpartners op B2B-sites voor e-commerce beheren](manage-b2b-users.md)

[De limieten voor de producthoeveelheid instellen voor B2B-e-commercesites](quantity-limits.md)

[Updates voor SDK's en modulebibliotheken](../e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]