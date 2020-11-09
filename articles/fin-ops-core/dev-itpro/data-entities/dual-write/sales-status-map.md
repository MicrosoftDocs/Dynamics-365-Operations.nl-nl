---
title: De toewijzing voor de statusvelden van de verkooporder instellen
description: In dit onderwerp wordt uitgelegd hoe u de statusvelden voor verkooporders instelt voor twee keer wegschrijven.
author: dasani-madipalli
manager: tonyafehr
ms.date: 06/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: damadipa
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 5855581100606003c1faf6b88a0ab234ae378893
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997669"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-fields"></a>De toewijzing voor de statusvelden van de verkooporder instellen

[!include [banner](../../includes/banner.md)]

De velden die de status van de verkooporder aangeven, hebben verschillende opsommingswaarden in Microsoft Dynamics 365 Supply Chain Management en Dynamics 365 Sales. Aanvullende instellingen zijn vereist om deze velden te kunnen koppelen in twee keer wegschrijven.

## <a name="fields-in-supply-chain-management"></a>Velden in Supply Chain Management

In Supply Chain Management geven twee velden de status van de verkooporder weer. De velden die u moet toewijzen zijn **Status** en **Documentstatus**.

De opsommingswaarde **Status** geeft de algemene status van de order aan. Deze status wordt weergegeven in de orderkop.

De opsommingswaarde **Status** heeft de volgende waarden:

- Openstaande order
- Geleverd
- Gefactureerd
- Geannuleerd

De opsommingswaarde **Documentstatus** geeft het meest recente document aan dat voor de order is gegenereerd. Als de order bijvoorbeeld is bevestigd, is dit document een verkooporderbevestiging. Als een verkooporder gedeeltelijk is gefactureerd en de resterende regel is bevestigd, behoudt het document de status **Factuur** omdat de factuur later in het proces wordt gegenereerd.

De opsommingswaarde **Documentstatus** heeft de volgende waarden:

- Bevestiging
- Orderverzamellijst
- Pakbon
- Factuur

## <a name="fields-in-sales"></a>Velden in Verkoop

In Verkoop geven twee velden de status van de order weer. De velden die u moet toewijzen zijn **Status** en **Verwerkingsstatus**.

De opsommingswaarde **Status** geeft de algemene status van de order aan. Het heeft de volgende waarden:

- Actief
- Ingediend
- Afgehandeld
- Gefactureerd
- Geannuleerd

De opsommingswaarde **Verwerkingsstatus** is geïntroduceerd zodat de status nauwkeuriger kan worden toegewezen met Supply Chain Management.

In de volgende tabel wordt de toewijzing van **Verwerkingsstatus** in Supply Chain Management weergegeven.

| Verwerkingsstatus   | Status in Supply Chain Management | Documentstatus in Supply Chain Management |
|---------------------|-----------------------------------|--------------------------------------------|
| Actief              | Openstaande order                        | None                                       |
| Bevestigd           | Openstaande order                        | Bevestiging                               |
| Opgenomen              | Openstaande order                        | Orderverzamellijst                               |
| Gedeeltelijk geleverd | Openstaande order                        | Pakbon                               |
| Geleverd           | Geleverd                         | Pakbon                               |
| Gedeeltelijk gefactureerd  | Geleverd                         | Factuur                                    |
| Gefactureerd            | Gefactureerd                          | Factuur                                    |
| Geannuleerd           | Geannuleerd                         | Niet van toepassing                             |

In de volgende tabel wordt de toewijzing van **Verwerkingsstatus** tussen Verkoop en Supply Chain Management weergegeven.

| Verwerkingsstatus   | Status in Verkoop | Status in Supply Chain Management |
|---------------------|-----------------|-----------------------------------|
| Actief              | Actief          | Openstaande order                        |
| Bevestigd           | Ingediend       | Openstaande order                        |
| Opgenomen              | Ingediend       | Openstaande order                        |
| Gedeeltelijk geleverd | Actief          | Openstaande order                        |
| Gedeeltelijk gefactureerd  | Actief          | Openstaande order                        |
| Gedeeltelijk gefactureerd  | Afgehandeld       | Geleverd                         |
| Gefactureerd            | Gefactureerd        | Gefactureerd                          |
| Geannuleerd           | Geannuleerd       | Geannuleerd                         |

## <a name="setup"></a>Instelling

Om de toewijzing voor de statusvelden van verkooporders in te stellen, moet u de kenmerken **IsSOPIntegrationEnabled** en **isIntegrationUser** inschakelen.

Volg deze stappen als u het kenmerk **IsSOPIntegrationEnabled** wilt inschakelen.

1. Ga in een browser naar `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Vervang **\<test-name\>** door de koppeling van uw bedrijf met Verkoop.
2. Zoek **organizationid** op de pagina die is geopend en noteer de waarde.

    ![Organizationid zoeken](media/sales-map-orgid.png)

3. Open de browserconsole in Verkoop en voer het volgende script uit. Gebruik de waarde van **organizationid** uit stap 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on record update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-code in de browserconsole](media/sales-map-script.png)

4. Controleer of **IsSOPIntegrationEnabled** is ingesteld op **true**. Gebruik de URL uit stap 1 om de waarde te controleren.

    ![IsSOPIntegrationEnabled ingesteld op true](media/sales-map-integration-enabled.png)

Volg deze stappen als u het kenmerk **isIntegrationUser** wilt inschakelen.

1. Ga in Verkoop naar **Instelling \> Aanpassen \> Het systeem aanpassen**. Selecteer **Gebruikersentiteit** en open **Formulier \> Gebruiker**.

    ![Het gebruikersformulier openen](media/sales-map-user.png)

2. Zoek in Veldverkenner **Integratiegebruikersmodus** en dubbelklik erop om deze toe te voegen aan het formulier. Sla de wijziging op.

    ![Het veld Integratiegebruikersmodus toevoegen aan het formulier](media/sales-map-field-explorer.png)

3. Ga in Verkoop naar **Instelling \> Beveiliging \> Gebruikers** en wijzig de weergave van **Ingeschakelde gebruikers** in **Toepassingsgebruikers**.

    ![De weergave wijzigen van Ingeschakelde gebruikers in Toepassingsgebruikers](media/sales-map-enabled-users.png)

4. Selecteer de twee items voor **DualWrite IntegrationUser**.

    ![Lijst met toepassingsgebruikers](media/sales-map-user-mode.png)

5. Wijzig de waarde van het veld **Integratiegebruikersmodus** in **Ja**.

    ![De waarde van het veld Integratiegebruikersmodus wijzigen in Ja](media/sales-map-user-mode-yes.png)

Uw verkooporders zijn nu toegewezen.
