---
title: EU-invoercertificaten
description: Dit artikel biedt informatie over EU-invoercertificaten (Europese Unie).
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustEntryCertificateJour_W, CustParameters, CustTable, SalesTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11464
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b3346a5229d0cc9e7af74f17ea6a327e5ba253a
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1561477"
---
# <a name="eu-entry-certificates"></a>EU-invoercertificaten

[!include [banner](../includes/banner.md)]

Dit artikel biedt informatie over EU-invoercertificaten (Europese Unie).

U kunt de volgende taken uitvoeren voor een EU (Europese Unie)-invoercertificaat:

-   Maak een EU-invoercertificaat en geef het uit samen met een pakbon of een klantfactuur voor de levering van artikelen of diensten aan EU-landen/-regio´s.
-   Ontvang het EU-invoercertificaat dat door een EU-klant is ondertekend.
-   Upload het ondertekende EU-invoercertificaat dat is ontvangen van de klant of een derde die verantwoordelijk is voor levering van de artikelen aan de klant.
-   Koppel het geüploade EU-invoercertificaat met een klantfactuur.
-   Werk de status van het geselecteerde EU-invoercertificaat bij.

## <a name="prerequisites"></a>Vereisten
De volgende tabel geeft de vereisten weer waaraan moet worden voldaan voordat u start.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Categorie</th>
<th>Vereiste</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Land/regio</td>
<td>Het primaire adres van de rechtspersoon moet in een EG-lidstaat zijn.</td>
</tr>
<tr class="even">
<td>Verwante instellingstaken</td>
<td><ul>
<li>Selecteer op de pagina <strong>Parameters van module Klanten</strong> de opties <strong>Certificaatbeheer inschakelen</strong> en <strong>Verstrekken van invoercertificaat inschakelen</strong>.</li>
<li>Selecteer op de pagina <strong>Klanten</strong> op het sneltabblad <strong>Factuur en levering</strong> de optie <strong>Invoercertificaat vereist</strong> om aan te geven dat een EU-invoercertificaat voor de klant verplicht is. Schakel het selectievakje <strong>Uitgifte van invoercertificaat</strong> in om een EU-invoercertificaat van de rechtspersoon voor de klant uit te geven.</li>
<li>Selecteer op de pagina <strong>Parameters van module Klanten</strong> een nummerreekscode voor de verwijzing <strong>Invoercertificaat</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Gerelateerde transacties</td>
<td><ul>
<li>Een klantaccount maken.</li>
<li>Maak een verkooporder.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="creating-registering-and-uploading-an-eu-entry-certificate"></a>Een EU-invoercertificaat maken, registreren en uploaden
U kunt automatisch of handmatig een EU-invoercertificaat maken. Een EU-invoercertificaat wordt automatisch gemaakt en afgedrukt wanneer u een pakbon of factuur voor een klant boekt met de pagina **Pakbon boeken** of **Factuur boeken**. Als u handmatig een EU-invoercertificaat wilt maken of opnieuw afdrukken voor een klantfactuur, kunt u de pagina **Factuurjournaal** gebruiken. U kunt bovendien op de pagina **Invoercertificaatlogboek** gegevens invoeren over een EU-invoercertificaat dat door een derde is uitgegeven.

### <a name="creating-an-eu-entry-certificate-automatically-or-manually"></a>Automatisch of handmatig een EU-invoercertificaat maken

U kunt automatisch een EU-invoercertificaat maken door een pakbon te gebruiken op de pagina **Alle verkooporders** of door een factuur te gebruiken op de pagina **Verkooporder**. Om handmatig een EU-invoercertificaat te maken, kunt u een factuur op de pagina **Factuurjournaal** gebruiken. U moet echter de certificaatstatus van de factuur wijzigen voordat u handmatig maken een EU-invoercertificaat maakt.

### <a name="registering-an-eu-entry-certificate"></a>Een EU-invoercertificaat registreren

Als registratie vereist is kunt u de pagina **Invoercertificaatlogboek** gebruiken om een EU-invoercertificaat te registreren dat door een derde is uitgegeven.

### <a name="uploading-a-received-eu-entry-certificate"></a>Een ontvangen EU-invoercertificaat uploaden

Gebruik de pagina **Bijlagen** om een ontvangen EU-invoercertificaat te uploaden dat is getekend door een EU-klant. Nadat het certificaat is geüpload, kunt u het aan een factuur koppelen als bewijs dat de artikelen zijn geleverd. Dit bewijs is vereist als u een factuur moet uitgeven die geen belasting toegevoegde waarde (btw) bevat, en het wordt ook gebruikt tijdens de controle.

### <a name="optional-updating-the-certification-status-and-printing-status-of-an-invoice"></a>Optioneel: de certificaat- en afdrukstatus van een factuur bijwerken

U kunt de invoercertificaatstatus en de afdrukstatus van een klantfactuur bijwerken op de pagina **Factuurjournaal**.

## <a name="technical-information-for-system-administrators"></a>Technische informatie voor systeembeheerders
Als u geen toegang hebt tot de pagina's waarmee u deze taak kunt voltooien, moet u contact opnemen met uw systeembeheerder en de informatie opgeven die wordt beschreven in de volgende tabel.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Categorie</th>
<th>Vereiste</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Veiligheidstaken en -rollen</td>
<td>Om EU-invoercertificaten in te stellen en te maken voor artikelen of services, moet u lid zijn van een beveiligingsrol die de volgende functies bevat:
<ul>
<li><strong>Debiteurenadministrateur</strong> (CustInvoiceAccountsReceivableClerk)</li>
<li><strong>Medewerker klantenservice</strong> (TradeCustomerServiceRepresentative)</li>
<li><strong>Verkoopmedewerker</strong> (TradeSalesClerk)</li>
<li><strong>Verzendadministrateur</strong> (InventShippingClerk)</li>
</ul></td>
</tr>
</tbody>
</table>





