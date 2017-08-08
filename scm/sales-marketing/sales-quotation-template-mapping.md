---
title: Kopteksten en regels van verkoopofferte synchroniseren tussen Sales en Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopoffertes tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: nl-nl
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Kopteksten en regels van verkoopofferte synchroniseren tussen Sales en Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Voordat u de oplossing Prospect naar contant geld kunt gebruiken, moet u vertrouwd zijn met de functie [Dynamics 365 Gegevensintegratie](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

In dit onderwerp komen de sjablonen en onderliggende taken aan de orde voor het synchroniseren van kopteksten en regels van verkoopoffertes tussen Microsoft Dynamics 365 for Sales en Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. 

## <a name="template-and-tasks"></a>Sjabloon en taken

De volgende sjablonen en onderliggende taken worden gebruikt voor het synchroniseren van de kopteksten en regels van verkoopoffertes tussen Sales en Finance and Operations:

- **Naam van de sjabloon:** Verkoopoffertes (Sales naar Fin and Ops)
- **Namen van de taken in het project:**

    - QuoteHeader
    - QuoteLine

De volgende synchronisatietaken zijn vereist voordat de synchronisatie van de kopteksten en regels van verkoopoffertes kan plaatsvinden:

- Producten
- Rekeningen (indien van toepassing)
- Contactpersonen (indien van toepassing)

## <a name="entity-set"></a>Entiteitset

| Verkoop        | CDS           | Finance en Operations    |
|--------------|---------------|---------------------------|
| Citaten       | Offerte     | Kopteksten van verkoopoffertes   |
| QuoteDetails | QuotationLine | Regels van CDS-verkoopofferte |

## <a name="entity-flow"></a>Entiteitstroom

Verkoopoffertes worden gemaakt in Sales en gesynchroniseerd met Finance and Operations.

Verkoopoffertes uit Sales worden alleen gesynchroniseerd als aan de volgende voorwaarden is voldaan:

- Alle producten op de verkoopofferteregels worden extern beheerd.
- De verkoopofferte is actief of geactiveerd.

## <a name="prospect-to-cash-solution-for-sales"></a>Oplossing Prospect naar contant geld voor Sales

Het veld **Heeft alleen extern onderhouden producten** is toegevoegd aan de offerte-entiteit om consistent bij te houden of de verkoopofferte geheel bestaat uit extern beheerde producten. Als een verkoopofferte alleen extern beheerde producten heeft, worden de producten beheerd in Finance and Operations. Zo garandeert u dat u niet verkoopofferteregels probeert te synchroniseren voor producten die onbekend zijn in Finance and Operations.

Alle producten en regels op de offerte worden bijgewerkt met de informatie **Heeft alleen extern onderhouden producten** uit de offertekoptekst. Deze informatie vindt u in het veld **Offerte heeft alleen extern onderhouden producten** op de offerteregelentiteit.

De velden **Korting**, **Toeslagen** en **Btw** worden bepaald door een complexe configuratie in Finance and Operations. Deze instellingen ondersteunen momenteel geen integratietoewijzing. In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** beheerd en verwerkt door Finance and Operations.

In Sales worden de volgende velden alleen-lezen gemaakt, omdat de waarden niet worden gesynchroniseerd met Finance and Operations:

- **Alleen-lezen velden in de koptekst van de verkoopofferte:** Kortingspercentage, Korting, Vrachtkosten
- **Alleen-lezen velden op de verkoopofferteregels:** Btw

## <a name="preconditions-and-mapping-setup"></a>Voorwaarden en instellingen voor toewijzing

- Voordat u verkoopoffertes in Sales synchroniseert, gaat u naar **Instellingen** &gt; **Beheer** &gt; **Systeeminstellingen** &gt; **Sales**, en zorgt u ervoor dat het veld **Berekeningsmethode korting** wordt ingesteld op **Per eenheid**. Deze instelling zorgt ervoor dat de regelitemkorting uit Sales overeenkomt met de instelling in Finance and Operations. Anders is de korting niet juist in Finance and Operations, omdat Finance and Operations de korting leest als korting per eenheid zelfs als dit een korting per regel is in Sales.
- Ga in Finance and Operations naar **Klanten** &gt; **Instellen** &gt; **Parameters klanten**. Selecteer op het tabblad **Nummerreeks** de nummerreeks voor verkoopoffertes en klik vervolgens op **Details weergeven**. Stel vervolgens onder **Algemene instelling** het veld **Handmatig** in op **Ja**.
- Ga in Finance and Operations naar **Klanten** &gt; **Instellen** &gt; **Parameters klanten**. Stel vervolgens op het tabblad **Zendingen** het veld **Controle leveringsdatum** in op **Geen**. Met deze instelling voorkomt u dat de synchronisatie voor verkoopoffertes mislukt.

### <a name="quoteheader"></a>QuoteHeader

- Het veld **Gevraagde leveringsdatum** is vereist in Finance and Operations en de synchronisatie mislukt als u het veld leeg laat. Om dit te voorkomen wordt een standaard datum opgehaald uit **Bron &gt; CDS** als het veld leeg is. De datum moet worden bijgewerkt met een voorkeurswaarde. Momenteel kunt u geen waarde invoeren als **Vandaag** om de datum van vandaag aan te geven. U moet een specifieke datum opgeven. De standaardwaarde van de sjabloon voor **Gevraagde leveringsdatum** is **1/1/2020**.
- Het veld **Land-regiocode adres** is vereist in Finance and Operations. Om synchronisatiefouten te voorkomen kunt u een standaardwaarde opgeven die wordt gebruikt als het veld is leeg in Sales. Deze standaardwaarde is ook handig, omdat u niet handmatig een waarde hoeft in te voeren in het veld **Land/regio** voor lokale adressen. Er is geen standaardwaarde in de sjabloon voor **DeliveryAddressCountryRegionISOCode**.
- Werk de toewijzing voor **CDS-organisatie-id** bij in **Bron &gt; CDS** zodat deze overeenkomt met **CDS-organisatie** in de Organisatie-eenheid:

    - De standaardwaarde van de sjabloon voor **Organization_OrganizationId** is **ORG001**.
    - De standaardwaarde van de sjabloon voor **Account_Organization_OrganizationId** is **ORG001**.
    - De standaardwaarde van de sjabloon voor **InvoiceAccount_OrganizationId** is **ORG001**.

### <a name="quoteline"></a>QuoteLine

- Werk de toewijzing voor **CDS-organisatie-id** bij in **Bron &gt; CDS** zodat deze overeenkomt met **CDS-organisatie** in de Organisatie-eenheid:

    - De standaardwaarde van de sjabloon voor **Organization_OrganizationId** is **ORG001**.
    - De standaardwaarde van de sjabloon voor **Product_Organization_Organization_OrganizationId** is **ORG001**.
    - De standaardwaarde van de sjabloon voor **Quotation_Organization_Organization_OrganizationId** is **ORG001**.

- Het veld **Gevraagde leveringsdatum** is vereist in Finance and Operations en de synchronisatie mislukt als u het veld leeg laat. Om dit te voorkomen wordt een standaard datum opgehaald uit **Bron &gt; CDS** als het veld leeg is. De datum moet worden bijgewerkt met een voorkeurswaarde. Momenteel kunt u geen waarde invoeren als **Vandaag** om de datum van vandaag aan te geven. U moet een specifieke datum opgeven. De standaardwaarde van de sjabloon voor **Gevraagde leveringsdatum** is **1/1/2020**.
- U kunt de volgende toewijzingen uit **CDS &gt; Bestemming** toevoegen om te garanderen dat offerteregels worden geïmporteerd in Finance and Operations als er geen standaardgegevens over de klant of het product zijn:

    - **SiteId**: een site is vereist voor het genereren van offertes en verkooporderregels in Finance and Operations. Er is geen standaardwaarde van de sjabloon voor **SiteId**.
    - **WarehouseId**: een magazijn is vereist voor het verwerken van offertes en verkooporderregels in Finance and Operations. Er is geen standaardwaarde van de sjabloon voor **WarehouseId**.

- Zorg ervoor dat de vereiste waardetoewijzing voor de verkoopmaateenheid in Finance and Operations bestaat in de toewijzing **CDS &gt; Bestemming** voor **Quantity_UOM** naar **SALESUNITSYMBOL**.

## <a name="template-mapping-in-data-integrator"></a>Sjabloontoewijzing in gegevensintegrator

> [!NOTE]
> - De velden **Korting**, **Toeslagen** en **Btw** worden bepaald door een complexe configuratie in Finance and Operations. Deze instellingen ondersteunen momenteel geen integratietoewijzing. In het huidige ontwerp worden de velden **Prijs**, **Korting**, **Toeslagen** en **Btw** verwerkt door Finance and Operations.
> - De velden **Betalingsvoorwaarden**, **Leveringscondities**, **Leveringsvoorwaarden**, **Verzendmethode** en **Leveringsmethode** maken geen deel uit van de standaardtoewijzingen. Als u deze velden wilt toewijzen, moet u een waardetoewijzing instellen die specifiek is voor de gegevens in de organisaties waartussen de entiteit wordt gesynchroniseerd.

In de volgende afbeeldingen ziet u een voorbeeld van de toewijzing van een sjabloon in gegevensintegrator.

### <a name="quoteheader"></a>QuoteHeader

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Sjabloontoewijzing in gegevensintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Verwante onderwerpen

[Producten uit Finance and Operations synchroniseren met producten in Sales](products-template-mapping.md)

[Rekeningen uit Sales synchroniseren met klanten in Finance and Operations](accounts-template-mapping.md)

[Contactpersonen synchroniseren tussen Sales met contactpersonen of klanten in Finance and Operations](contacts-template-mapping.md)



