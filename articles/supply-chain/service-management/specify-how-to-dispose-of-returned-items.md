---
title: Opgeven op welke wijze retourartikelen moeten worden afgestoten
description: Geef op op welke wijze retourartikelen moeten worden afgestoten.
author: sorenva
ms.date: 05/07/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3123f49ef5fbd07afa61b035a2f6dd4c0af2ce40
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679214"
---
# <a name="specify-how-to-dispose-of-returned-items"></a>Opgeven op welke wijze retourartikelen moeten worden afgestoten

[!include [banner](../includes/banner.md)]

Wanneer u een retourorder verwerkt, moet u een retourredencode opgeven om aan te geven waarom het product is geretourneerd. U moet ook een beschikkingscode en een beschikkingsactie opgeven om te bepalen wat er moet gebeuren met het geretourneerde product.

U kunt een beschikkingscode toepassen wanneer u de retourorder maakt, de artikelontvangst registreert of de pakbon voor een artikelontvangst bijwerkt en een quarantaineorder beëindigt.

U kunt alle beschikkingscodes maken die u nodig hebt ter ondersteuning van de bedrijfsprocessen. De volgende tabel bevat een set codes die meestal wordt gebruikt voor het toewijzen van een retourartikelbeschikking.

<table>
<colgroup>
<col />
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Beschikkingstype</p></th>
<th><p>Algemene code</p></th>
<th><p>Omschrijving</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Afstoting</p></td>
<td><p>SC</p></td>
<td><p>Uitval/vernietiging</p></td>
</tr>
<tr class="even">
<td><p>Afstoting</p></td>
<td><p>DC</p></td>
<td><p>Donaties aan liefdadigheidsinstelling</p></td>
</tr>
<tr class="odd">
<td><p>Afstoting</p></td>
<td><p>TD</p></td>
<td><p>Afstoting door derden</p></td>
</tr>
<tr class="even">
<td><p>Afstoting</p></td>
<td><p>SL</p></td>
<td><p>Hergebruik</p></td>
</tr>
<tr class="odd">
<td><p>Afstoting</p></td>
<td><p>TS</p></td>
<td><p>Verkoop aan derden (secundaire markten)</p></td>
</tr>
<tr class="even">
<td><p>Repareren/aanpassen</p></td>
<td><p>RW</p></td>
<td><p>Opnieuw maken</p></td>
</tr>
<tr class="odd">
<td><p>Repareren/aanpassen</p></td>
<td><p>RF</p></td>
<td><p>Opnieuw produceren/opknappen</p></td>
</tr>
<tr class="even">
<td><p>Repareren/aanpassen</p></td>
<td><p>MD</p></td>
<td><p>Aanpassen</p></td>
</tr>
<tr class="odd">
<td><p>Repareren/aanpassen</p></td>
<td><p>RP</p></td>
<td><p>Repareren</p></td>
</tr>
<tr class="even">
<td><p>Repareren/aanpassen</p></td>
<td><p>RV</p></td>
<td><p>Retour naar leverancier</p></td>
</tr>
<tr class="odd">
<td><p>Overige</p></td>
<td><p>AI</p></td>
<td><p>In huidige staat gebruiken</p></td>
</tr>
<tr class="even">
<td><p>Overige</p></td>
<td><p>RS</p></td>
<td><p>Herverkoop</p></td>
</tr>
<tr class="odd">
<td><p>Overige</p></td>
<td><p>EX</p></td>
<td><p>Uitwisselen</p></td>
</tr>
<tr class="even">
<td><p>Overige</p></td>
<td><p>MS</p></td>
<td><p>Overige</p></td>
</tr>
</tbody>
</table>


Voor elke beschikkingscode die u definieert, moet u een beschikkingsactie selecteren. De beschikkingsactie definieert de fysieke en financiële implicaties van beschikkingscodes. Bijvoorbeeld, bepaalt de beschikkingsactie de fysieke behandeling van het geretourneerde artikel, het financiële effect van het geretourneerde artikel, en of een vervangingsartikel aan de klant moet worden verstuurd. U kunt een onbeperkt aantal beschikkingscodes volgens uw bedrijfsbehoeften definiëren, maar zijn er slechts zes voorafgedefinieerde beschikkingsacties waaruit u kunt kiezen. De volgende tabel bevat de beschikkingsacties en hun definities.

<table>
<colgroup>
<col />
<col />
</colgroup>
<thead>
<tr class="header">
<th><p>Beschikkingsactie</p></th>
<th><p>Omschrijving</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Credit</strong></p></td>
<td><p>Retourneer het artikel naar de voorraad en crediteer de klant.</p></td>
</tr>
<tr class="even">
<td><p><strong>Alleen credit</strong></p></td>
<td><p>Crediteer de klant zonder te vereisen of te verwachten dat het artikel wordt geretourneerd.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Uitval</strong></p></td>
<td><p>Schrap het artikel en crediteer de klant.</p></td>
</tr>
<tr class="even">
<td><p><strong>Vervangen en crediteren</strong></p></td>
<td><p>Retourneer het artikel naar de voorraad, maak een vervangingsorder en crediteer de klant.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Vervangen en uitvallen</strong></p></td>
<td><p>Schrap het artikel, maak een vervangingsorder en crediteer de klant.</p></td>
</tr>
<tr class="even">
<td><p><strong>Retour naar klant</strong></p></td>
<td><p>Weiger het artikel en retourneer het aan de klant.</p></td>
</tr>
</tbody>
</table>

## <a name="select-a-disposition-code-for-a-quarantine-order"></a>Een beschikkingscode selecteren voor een quarantaineorder

1. Ga naar **Voorraadbeheer** \> **Periodiek** \> **Kwaliteitsbeheer** \> **Quarantaineorders**.
1. Voor een bestaande quarantaineorder selecteert u een actie in het veld **Beschikkingscode** op het tabblad **Overzicht**.

## <a name="see-also"></a>Zie ook

[Quarantaineorder (formulier)](/dynamicsax-2012//quarantine-order-form)

[Beschikkingscodes (formulier)](https://technet.microsoft.com/library/hh597113\(v=ax.60\))

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
