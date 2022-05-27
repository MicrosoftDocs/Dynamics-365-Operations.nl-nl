---
title: Grootboekjournaaltypen
description: Dit onderwerp beschrijft de journaaltypes die u kunt instellen voor financiële journalen.
author: kweekley
ms.date: 10/10/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup
audience: Application User
ms.reviewer: kfend
ms.custom: 15631
ms.assetid: 81613b31-bc3c-43a0-8474-e01c9a482c40
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e49d101bbbe576e0fcf2e9b243f4f29124fbd85
ms.sourcegitcommit: 602a319f4720b39a56b7660b530236912d484391
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/06/2022
ms.locfileid: "8722264"
---
# <a name="ledger-journal-types"></a>Grootboekjournaaltypen

[!include [banner](../includes/banner.md)]

Dit onderwerp beschrijft de journaaltypes die u kunt instellen voor financiële journalen. Gebruik de pagina **Journaalnamen** voor het instellen van journalen die u in heel Dynamics 365 Finance kunt gebruiken.

| Journaaltype                      | Doel                       | Transacties invoeren op deze pagina                                |
|-----------------------------------|-------------------------------|----------------------------------------------------------------|
| Toewijzing                        | Toewijzingstransacties maken in een toewijzingsjournaal. Voordat u een toewijzingsjournaal kunt maken, moet u een toewijzingsregel maken op de pagina **Grootboektoewijzingsregel**.      | Toewijzingsaanvraag verwerken             |
| Goedkeuring                          | Goedgekeurde leveranciersfacturen boeken op de betreffende grootboekrekeningen.  | Factuurgoedkeuringsjournaal                                       |
| Omkering van bankcheque               | Een geboekte cheque omkeren. Om dit journaaltype te gebruiken, schakelt u de optie **Controleproces voor betalingsomkeringen gebruiken** op de pagina **Parameters voor cash- en bankbeheer**.   | Omkeringen van cheques, omkeringen van betalingen                   |
| Annulering van bankdepositostrook    | Een depositostrook annuleren. Om dit journaaltype te gebruiken, schakelt u de optie **Controleproces voor annuleringen van bankdepositostroken gebruiken** op de pagina **Parameters voor cash- en bankbeheer**.   | Annulering van depositostrookbetalingen            |
| Budget                            | Budgettoewijzingen verwerken. Om dit journaaltype te gebruiken, schakelt u de optie **Aanwending van budget inschakelen** in op de pagina **Grootboekparameters**. De budgetjournaalposten bevatten informatie die is gebaseerd op de grootboekrekeningen die zijn gedefinieerd op de pagina **Boekdefinities**.                                                        |                                                                |
| Door de klant geaccepteerde wissel  | Acceptatietransacties van klanten maken voor wissels.             | Journaal met getrokken wissels, Journaal met hertrokken wissels |
| Bankremise van klant          | Een remisebestand voor een wissel maken dat kan worden verzonden naar de bank van uw organisatie. Om dit journaaltype te gebruiken, schakelt u de optie **Automatische vereffening** in op de pagina **Parameters** **van module Klanten**.            | Remise                                                     |
| Door klant getrokken wissel    | Transacties voor door klant getrokken wissels maken. Om dit journaaltype te gebruiken, schakelt u de optie **Getrokken journaal automatisch maken en boeken tijdens boeken van facturen** op de pagina **Betalingsmethoden - klanten**.   | Journaal met getrokken wissels                                  |
| Betaling van klant                  | Klantbetalingstransacties maken.                             | Betalingsjournaal             |
| Door klant geprotesteerde wissel | Transacties voor door klant geprotesteerde wissels maken.                    | Journaal met geprotesteerde wissels                               |
| Door klant hertrokken wissel  | Transacties voor door klant hertrokken wissels maken.                     | Journaal met hertrokken wissels                                |
| Door klant afgerekende wissel  | Transacties voor door klant afgerekende wissels maken.                       | Journaal met afgerekende wissels                                |
| Dagelijks                             | Dagelijkse transacties in een algemeen journaal maken.                          | Algemeen journaal                                                |
| Schrapping                       | Schrappingstransacties maken in een schrappingsdagboek. Om dit journaaltype te gebruiken, selecteert u de opties **Gebruiken voor proces voor financiële schrapping** en **Gebruiken voor financieel consolidatieproces** op de pagina **Rechtspersonen**. Voordat u dit journaaltype gebruikt, moet u een grootboekschrappingregel maken op de pagina **Schrappingregel grootboek**. | Schrapping                                                    |
| Vaste-activabudget                | Budgetregistervermeldingen voor vaste activa maken.                                                                                                                                                                                                                                                                                                                 | Vaste-activabudget                                             |
| Facturenregister                  | Basisinformatie over leveranciersfacturen registreren.                                                                                                                                                                                                                                                                                                           | Facturenregister                                               |
| Salarisvoorschot              | Geef betalingen uit die zijn gebaseerd op salarisbetalingsafschriften In dit journaal kunt u niet handmatig transacties invoeren. U moet betalingsafschriften maken en deze afschriften indienen voor betaling.                                                                                                                                                              |                                                                |
| Periodiek                          | Periodieke transacties maken voor het periodiek journaal.                                                                                                                                                                                                                                                                                                      | Periodieke journalen                                              |
| Vaste activa boeken                 | Vaste-activatransacties boeken.                                                                                                                                                                                                                                                                                                                              | Vaste activa                                                   |
| Project - uitgaven                | Projectonkostentransacties maken.                                                                                                                                                                                                                                                                                                                        | Expense                                                        |
| Correctie aangiftevaluta     | Correcties maken in de aangiftevaluta voor saldi op grootboekrekeningen.               | Correctiejournalen aangiftevaluta                         |
| Statistische transacties            | Statistische transacties maken.                                                                                                                                                                                                                                                                                                                            |                                                                |
| Bankremise van leverancier            | Een remisebestand voor een promesse maken dat kan worden verzonden naar de bank van uw organisatie.                                                                                                                                                                                                                                                                      | Remisejournaal                                             |
| Voorschot van leverancier               | Leveranciervoorschottransacties maken.                                                                                                                                                                                                                                                                                                                    | Betalingsjournaal                                                |
| Door leverancier getrokken promesse       | Promessen van leveranciers trekken als een betalingsmethode. Om dit journaaltype te gebruiken, schakelt u de optie **Getrokken journaal automatisch maken en boeken tijdens boeken van facturen** op de pagina **Betalingsmethoden - leveranciers**.                                                                                                                                          | Journaal met getrokken promessen                                   |
| Pool van leveranciersfacturen exclusief boeking | Leveranciersfactuurtransacties maken die nog niet zijn geboekt naar een tijdelijke ontvangstrekening.                                                                                                                                                                                                                                                             | Leveranciersfactuurpool met uitzondering van boekingsdetails                  |
| Pool van leveranciersfacturen               | Transacties voor pool van leveranciersfacturen maken.                                                                                                                                                                                                                                                                                                                    |                                                                |
| Registratie van leveranciersfactuur          | Leveranciersfacturen in een journaal boeken.                                                                                                                                                                                                                                                                                                                 | Factuurjournaal                                                |
| Door leverancier hertrokken promesse     | Een promesse te hertrekken die eerder is gehonoreerd door de bank van uw organisatie.                                                                                                                                                                                                                                                                      | Journaal met hertrokken promessen                                 |
| Door leverancier afgerekende promesse     | Transacties voor door leverancier afgerekende promessen maken.                                                                                                                                                                                                                                                                                                          | Journaal met afgerekende promessen                                 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
