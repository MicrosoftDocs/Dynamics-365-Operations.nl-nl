---
title: Een SharePoint-verbinding configureren
description: In dit artikel wordt uitgelegd hoe u een verbinding configureert zodat elektronische facturering toegang krijgt tot een Microsoft-site SharePoint.
author: gionoder
ms.date: 12/15/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: gionoder
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.form: ''
ms.openlocfilehash: a2762178686d1f29c457b6de2a9b052fd048484b
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283982"
---
# <a name="configure-a-sharepoint-connection"></a>Een SharePoint-verbinding configureren

[!include [banner](../includes/banner.md)]

Via de elektronische factureringsservice kunnen bestanden worden gelezen vanuit Microsoft SharePoint-mappen en kunnen bestanden worden geüpload naar SharePoint. Als u ervoor wilt zorgen dat Elektronische facturering toegang heeft tot een specifieke SharePoint-site, moet u de referenties van de site bij de elektronische factureringsservice opgeven. Geef de referenties bovendien niet rechtstreeks op om ze veilig op te slaan. Sla ze op in een Azure Key Vault en geef een Azure Key Vault-geheim op.

## <a name="grant-access-to-a-sharepoint-folder"></a>Toegang tot een SharePoint-map verlenen

1. Maak een appregistratie in de tenant waar Regulatory Configuration Service (RCS) is geïnstalleerd.

    1. Meld u aan bij de [Azure-portal](https://portal.azure.com/).
    2. Ga naar **App-registraties**.
    3. Selecteer **Nieuwe registratie**.
    4. Voer een naam in, zoals **SharePoint-app voor elektronische facturering**, en voer de registratie uit
    5. Selecteer de nieuwe app-registratie.
    6. Schakel op het tabblad **Verificatie** de optie **Openbare clientstromen toestaan** in.
    4. Selecteer op het tabblad **Certificaten en geheimen** de optie **Nieuw clientgeheim** om een clientgeheim te maken.
    5. Kopieer de waarde van het gemaakte geheim.

    Volg deze richtlijnen:

    - Gebruik niet dezelfde appregistratie voor verschillende services.
    - Volg de [aanbevelingen voor wachtwoordbeleid](/microsoft-365/admin/misc/password-policy-recommendations?view=o365-worldwide).
    - Stel een rotatie van wachtwoorden in. Maak tijdens de rotatie een nieuw clientgeheim voor de app-registratie, werk de sleutelkluis bij en verwijder het oude clientgeheim.

2. Sla de waarden voor **Geheim app-registratie** en de **Toepassings-id (client)** op als twee nieuwe geheimen in de sleutelkluis in de instellingenen van de elektronische factureringsomgeving.
3. Voeg de gemaakte geheimen toe aan de Key Vault-parameters in de instellingen voor de elektronische factureringsomgeving in RCS.
4. Verleen in de Azure-portal toegang tot SharePoint. Deze stap moet worden voltooid door de tenantbeheerder.

    1. Selecteer de app-registratie die u hebt gemaakt.
    2. Selecteer **Een machtiging toevoegen** op het tabblad **API-machtigingen**.
    3. Selecteer **Microsoft graph (toepassingstoestemmingen)** \> **Sites.Selected**.
    4. Selecteer **Beheerderstoestemming verlenen voor \<user&nbsp;name\>**.
    5. Controleer het veld **Status** om na te gaan of er toestemmingen zijn verleend.

        ![Machtigingen die zijn verleend op het tabblad API-machtigingen.](media/configured-permissions.jpg)

    6. Open [Grafiekverkenner - Microsoft Graph](https://developer.microsoft.com/graph/graph-explorer) en meld u aan.
    7. Selecteer onder **SharePoint-sites** in het linkerdeelvenster op het tabblad **Voorbeeldquery's** de optie **SharePoint-site ophalen op basis van het relatieve pad van de site**.
    8. Vul de parameters voor **\{host-name\}** en **\{server-relative-path\}** in. Vul bijvoorbeeld `<domain>.sharepoint.com` in voor **\{host-name\}** en `sites/<siteName>`**\{server-relative-path\}**.

        > [!NOTE]
        > Laat de parameter **\{server-relative-path\}** leeg voor de standaardwebsite.

    9. Selecteer **Query uitvoeren** en sla het resultaat op.
    10. Configureer de volgende query.

        `POST https://graph.microsoft.com/v1.0/sites/{site-id}/permissions`

        In deze query is **\{site-id\}** de waarde van het **id-knooppunt** van het vorige antwoord op de query.

        Hier is de aanvraagbody.

        ```json
        {
            "roles": [
                "read",
                "write"
            ],
            "grantedToIdentities": [
                {
                    "application": {
                        "id": "{app-id}",
                        "displayName": "{app-name}"
                    }
                }
            ]
        }
        ```

        In deze aanvraagbody is **\{app-id\}** de waarde van **Toepassings-id (client)** en **\{app-name\}** de waarde van **Toepassingsnaam**.

        ![POST-query.](media/app-id-query.jpg)

    11. Selecteer op het tabblad **Machtigingen wijzigen** **Venster met machtigingen openen** en selecteer vervolgens **Sites** \> **Sites.FullControl.All** \> **Toestemming**.
    12. Selecteer **Query uitvoeren**.

De elektronische factureringsservice heeft nu toegang tot uw SharePoint-site.
