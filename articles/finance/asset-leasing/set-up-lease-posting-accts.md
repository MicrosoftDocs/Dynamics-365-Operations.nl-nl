---
title: Leaseboekingsrekeningen instellen
description: Dit onderwerp bevat een overzicht van de boekingsrekeningen die nodig zijn voor de transacties voor activaleases en legt uit hoe u boekingsrekeningen kunt definiëren op de pagina Leaseboekingsparameters.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: kfend
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 147d8cd93f9664039b2004b878dcaff96c8b6ce6
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726373"
---
# <a name="set-up-lease-posting-accounts"></a>Leaseboekingsrekeningen instellen

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat een overzicht van de boekingsrekeningen die nodig zijn voor de transacties voor activaleases en legt uit hoe u boekingsrekeningen kunt definiëren op de pagina **Leaseboekingsparameters**.

Om te voldoen aan Accounting Standards Codification Topic 842 (ASC 842) en International Financial Reporting Standard 16 (IFRS 16) moet u mogelijk rekeningen in uw rekeningschema maken. Rekeningen die u maakt om te voldoen aan de ASC- en IFRS-standaarden, zijn echter geen vaste-activarekeningen. Onder ASC 842 wordt een RoU-activum (met gebruiksrecht) geregistreerd voor zowel financiële als operationele leases. Deze leases staan los van de vaste activa. (U kunt nog steeds een RoU-activum onderhouden met behulp van vaste activa.)

Zie [Rekeningstructuren maken](../general-ledger/tasks/create-account-structures.md) voor meer informatie over het maken van rekeningstructuren. Zie [Een hoofdrekening maken](../general-ledger/tasks/create-main-account.md) voor meer informatie over het maken van een hoofdrekening.

De volgende tabel bevat voorbeelden van rekeningen die u voor transacties voor geleasde activa moet maken, als deze nog niet zijn gemaakt. Onder IFRS 16 worden de operationele leaserelaties nog steeds gebruikt voor leases met lage waarde en korte termijn.

| Nummer van grootboekrekening | Rekeningtype  | Rekeningnaam                                          |
|-----------------------|---------------|-------------------------------------------------------|
| 180150                | Activum         | Voertuig RoU-activum                                     |
| 180160                | Activum         | Gebouw RoU-activum                                    |
| 180250                | Activum         | Samengevoegde afschrijving - voertuigen                   |
| 180260                | Activum         | Samengevoegde afschrijving - gebouwen                  |
| 222300                | Aansprakelijkheid     | Kortlopende verplichting - financiële leases                |
| 222310                | Balans | Kortlopende verplichting - operationele leases              |
| 250200                | Aansprakelijkheid     | Te betalen nota's                                         |
| 250601                | Balans | Langlopende verplichting - financiële leases                 |
| 250602                | Balans | Langlopende verplichting - operationele leases               |
| 250606                | Balans | Uitgestelde gebruiksvergoeding                                         |
| 300160                | Balans | Ingehouden winst                                     |
| 604500                | Expense       | Leaseonkosten                                         |
| 604501                | Expense       | Onkosten voertuig operationele lease - rentetoerekening  |
| 604502                | Expense       | Onkosten voertuig operationele lease - afschrijving        |
| 605200                | Expense       | Onkosten gebouw operationele lease - rentetoerekening |
| 605201                | Expense       | Onkosten gebouw operationele lease - afschrijving       |
| 607101                | Expense       | Onkosten voertuig operationele lease                    |
| 607102                | Expense       | Onkosten gebouw operationele lease                   |
| 607103                | Expense       | Waardeverminderingskosten - financiële leases                   |
| 607104                | Expense       | Waardeverminderingskosten - operationele leases                 |
| 618910                | Expense       | Leaseonkosten - financiële leases                        |
| 618920                | Expense       | Variabele betalingen - financiële leases                    |
| 618930                | Expense       | Variabele betalingen - operationele leases                  |
| 800600                | Expense       | Rentelasten voertuiglease                        |
| 800601                | Expense       | Rentelasten gebouwlease                       |
| 801201                | Balans | Winst en verlies - wijziging van lease                      |

## <a name="configure-posting-accounts"></a>Boekingsrekeningen configureren

Als u rekeningen wilt toewijzen aan de leaseboeken en groepen die zijn gemaakt, moet u parameters voor Activa leasen configureren.

1. Ga naar **Activa leasen \> Instellingen \> Leaseboekingsparameters**.
2. Open op het tabblad **Rekeningen** het sneltabblad **Leaserekeningen**. Bepaal de hoofdrekeningen voor financiële en operationele leases met het bijbehorende **Boekingstype**. In de voorgaande tabel worden de rekeningen weergegeven die zijn gerelateerd aan operationele en financiële leases.

    > [!NOTE]
    > Voor deze stap moet u afzonderlijke rekeningen instellen voor zowel operationele als financiële leases voor elk boekingstype, behalve **Verschuiving leaseonkosten** en **Toename/afname van de lease**. Bedrijven die aan het IFRS 16-boekhoudkader voldoen, moeten een hoofdrekening voor de operationele lease toevoegen. Het systeem gebruikt deze rekening echter niet, hoewel het een verplicht veld is, omdat alle leases onder IFRS 16 als financiële leases worden geclassificeerd.
    >[!NOTE]
    > **Toename/afname lease** wordt gebruikt als boekingstype voor extra activaoverwegingen, waaronder **Initiële directe kosten, Leasebonus, Vooruitbetalingen voor leases en Ontmantelingskosten**, maar het boekt naar de hoofdrekening van het activum met gebruiksrecht, die standaard **Leaseactivum** is.        
    
3. Als u een specifieke leasegroep wilt selecteren die overeenkomt met de hoofdrekening, selecteert u in het veld **Rekeningcode** de optie **Groep**. Selecteer vervolgens in het veld **Rekening-/groepnummer** de leasegroep die u wilt toewijzen aan de hoofdrekening.
4. Als u rekeningcodes wilt toewijzen aan de administratiekosten die zijn ingesteld in het systeem, selecteert u op het sneltabblad **Administratieve kosten** in het veld **Onkostentype** een kostenpost. Wijs vervolgens de financiële en operationele rekeningen toe die voor elk boek moeten worden gebruikt.

    > [!NOTE]
    > De geselecteerde financiële of operationele rekening wordt gedebiteerd wanneer de factuur voor de geplande onkosten wordt geboekt.
    > **Verschuiving leaseonkosten** wordt gebruikt als boekingstype voor transacties van administratieve kosten, maar boekt naar de gedefinieerde **Tegenrekening** in de **Betalingschemaregels voor administratieve kosten** in de leasedetails of het leaseboekformulier.   


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
