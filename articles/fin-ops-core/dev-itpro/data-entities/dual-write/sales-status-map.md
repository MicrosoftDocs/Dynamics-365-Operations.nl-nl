---
title: De toewijzing instellen voor de verkooporderstatuskolommen
description: In dit onderwerp wordt uitgelegd hoe u de statuskolommen voor verkooporders instelt voor twee keer wegschrijven.
author: dasani-madipalli
ms.date: 06/25/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: damadipa
ms.search.validFrom: 2020-06-25
ms.openlocfilehash: 53d824ca2fb1eadf34e62bf9c08b837db3efaf42
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/10/2021
ms.locfileid: "7782279"
---
# <a name="set-up-the-mapping-for-the-sales-order-status-columns"></a>De toewijzing instellen voor de verkooporderstatuskolommen

[!include [banner](../../includes/banner.md)]

De kolommen die de status van de verkooporder aangeven, hebben verschillende opsommingswaarden in Microsoft Dynamics 365 Supply Chain Management en Dynamics 365 Sales. Aanvullende instellingen zijn vereist om deze kolommen te kunnen koppelen in twee keer wegschrijven.

## <a name="columns-in-supply-chain-management"></a>kolommen in Supply Chain Management

In Supply Chain Management geven twee kolommen de status van de verkooporder weer. De kolommen die u moet toewijzen zijn **Status** en **Documentstatus**.

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

## <a name="columns-in-sales"></a>kolommen in Sales

In Sales geven twee kolommen de status van de order weer. De kolommen die u moet toewijzen zijn **Status** en **Verwerkingsstatus**.

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

Om de toewijzing voor de statuskolommen van verkooporders in te stellen, moet u de kenmerken **IsSOPIntegrationEnabled** en **isIntegrationUser** inschakelen.

Volg deze stappen als u het kenmerk **IsSOPIntegrationEnabled** wilt inschakelen.

1. Ga in een browser naar `https://<test-name>.crm.dynamics.com/api/data/v9.0/organizations`. Vervang **\<test-name\>** door de koppeling van uw bedrijf met Verkoop.
2. Zoek **organizationid** op de pagina die is geopend en noteer de waarde.

    ![Organizationid zoeken.](media/sales-map-orgid.png)

3. Open de browserconsole in Verkoop en voer het volgende script uit. Gebruik de waarde van **organizationid** uit stap 2.

    ```javascript
    Xrm.WebApi.updateRecord("organization",
    "d9a7c5f7-acbf-4aa9-86e8-a891c43f748c", {"issopintegrationenabled" :
    true}).then(
        function success(result) {
            console.log("Account updated");
            // perform operations on row update
        },
        function (error) {
            console.log(error.message);
            // handle error conditions
        }
    );
    ```

    ![JavaScript-code in de browserconsole.](media/sales-map-script.png)

4. Controleer of **IsSOPIntegrationEnabled** is ingesteld op **true**. Gebruik de URL uit stap 1 om de waarde te controleren.

    ![IsSOPIntegrationEnabled ingesteld op true.](media/sales-map-integration-enabled.png)

Volg deze stappen als u het kenmerk **isIntegrationUser** wilt inschakelen.

1. Ga in Sales naar **Instelling \> Aanpassing \> Het systeem aanpassen**. Selecteer **Gebruikerstabel** en open **Formulier \> Gebruiker**.

    ![Het gebruikersformulier openen.](media/sales-map-user.png)

2. Zoek in Veldverkenner **Integratiegebruikersmodus** en dubbelklik erop om deze toe te voegen aan het formulier. Sla de wijziging op.

    ![De kolom Integratiegebruikersmodus toevoegen aan het formulier.](media/sales-map-field-explorer.png)

3. Ga in Verkoop naar **Instelling \> Beveiliging \> Gebruikers** en wijzig de weergave van **Ingeschakelde gebruikers** in **Toepassingsgebruikers**.

    ![De weergave wijzigen van Ingeschakelde gebruikers in Toepassingsgebruikers.](media/sales-map-enabled-users.png)

4. Selecteer de twee items voor **DualWrite IntegrationUser**.

    ![Lijst met toepassingsgebruikers.](media/sales-map-user-mode.png)

5. Wijzig de waarde van de kolom **Integratiegebruikersmodus** in **Ja**.

    ![De waarde van de kolom Integratiegebruikersmodus wijzigen in Ja.](media/sales-map-user-mode-yes.png)

Uw verkooporders zijn nu toegewezen.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]