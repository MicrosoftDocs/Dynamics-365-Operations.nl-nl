---
title: Sjabloonstuklijsten
description: Met een sjabloonstuklijst beschikt u over een gestandaardiseerde lijst onderdelen voor serviceobjecten die regelmatig worden onderhouden.
author: ShylaThompson
manager: AnnBe
ms.date: 09/19/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f9c61ecd79f38301f46e3c21a33ec2801f33d19f
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "341299"
---
# <a name="template-boms"></a>Sjabloonstuklijsten    

[!include [banner](../includes/banner.md)]


Met een sjabloonstuklijst beschikt u over een gestandaardiseerde lijst onderdelen voor serviceobjecten die regelmatig worden onderhouden. De onderdelen die in de sjabloonstuklijst worden vermeld, vertegenwoordigen de afzonderlijke subonderdelen van het serviceobject. Door een sjabloonstuklijst op een serviceobject toe te passen, kunt u een record van de subonderdelen bijhouden die voor het serviceobject zijn vervangen.

Als u een sjabloonstuklijst wilt toepassen op een serviceovereenkomst of een serviceorder, koppelt u deze aan een serviceobjectrelatie.


> [!NOTE]
> <P>U kunt slechts één sjabloonstuklijst toepassen op een serviceobject.</P>

## <a name="create-a-template-bom"></a>Een sjabloonstuklijst maken

De volgende tabel bevat informatie over de verschillende methoden die u kunt gebruiken om een sjabloonstuklijst te maken.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Methode</p></th>
<th><p>Omchrijving</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Productie</p></td>
<td><p>De sjabloonstuklijst is gebaseerd op een productieorder. Deze optie is alleen van toepassing als u in een productieomgeving werkt. Het voordeel is dat u een actuele, gedetailleerde lijst hebt van de onderdelen van een item.</p></td>
</tr>
<tr class="even">
<td><p>Artikel BOM</p></td>
<td><p>De sjabloonstuklijst is gebaseerd op de stuklijst van een artikel. Het onderdeel stuklijst, in tegenstelling tot de productiestuklijst is een statische lijst van de onderdelen van een item.</p></td>
</tr>
<tr class="odd">
<td><p>Bestaande sjabloon</p></td>
<td><p>De sjabloon is gebaseerd op een bestaande sjabloonstuklijst.</p></td>
</tr>
<tr class="even">
<td><p>Handmatig</p></td>
<td><p>Als u weet welke onderdelen worden meestal vervangen op serviceobject, kunt u uw sjabloonstuklijst handmatig maken. Deze methode zorgt ervoor dat de onderdelen die zijn opgenomen in de sjabloon overeenkomen met de werkelijke behoeften van uw werkplek.</p></td>
</tr>
</tbody>
</table>


## <a name="apply-the-template-bom-to-a-service-agreement-or-service-order"></a>De sjabloonstuklijst toepassen op een serviceovereenkomst of een serviceorder

U kunt een sjabloonstuklijst toepassen op een serviceovereenkomst, een serviceorder of allebei. De serviceovereenkomst betreft meestal een langdurige relatie met een klant. De historie van vervangingen die is vastgelegd in de servicestuklijst, is nuttige informatie om op te nemen in de serviceovereenkomst.

U kunt ook een sjabloonstuklijst op een serviceorder toepassen om de historie van de service te registreren die is uitgevoerd op een serviceobject.

## <a name="copy-the-history-of-a-service-bom"></a>De historie van een servicestuklijst kopiëren

U kunt de historie van een servicestuklijstregel verplaatsen van de ene serviceovereenkomst naar de andere. Door de servicehistorie te kopiëren tussen serviceovereenkomsten, kunt u de vervangingen bijhouden voor een artikel.

**Voorbeeld**

U hebt een serviceovereenkomst van drie jaar afgesloten voor de auto van een klant. Tijdens die periode wordt de klant gewend aan de goede service die het bedrijf levert. Dus na het verlopen van de overeenkomst wil de klant een nieuwe instellen. Nu kunt u onderhandelen over een gunstigere overeenkomst voor het bedrijf. Aangezien de historie van vervangen onderdelen in de toekomst handig van pas kan komen, kopieert u de historie van de servicestuklijst naar de nieuwe overeenkomst.

## <a name="modify-the-template-bom"></a>De sjabloonstuklijst aanpassen

Als een sjabloonstuklijst niet aan een serviceobject is gekoppeld, kunt u de regels erin wijzigen of verwijderen. Nadat de sjabloonstuklijst aan een serviceobject is gekoppeld, kunt u alleen de lokale versie van de stuklijst nog aanpassen. Als u de instelling van een lokale versie van een sjabloonstuklijst wilt dupliceren, kunt u een nieuwe sjabloonstuklijst maken op basis van de lokale versie. Zie voor meer informatie [Een servicestuklijst wijzigen](modify-service-bom.md).

Als u een artikel in de stuklijst vervangt, kunt u de vervanging registreren op de stuklijstregel in de stuklijstontwikkelaar. U kunt desgewenst een serviceorderregel maken voor een vervangingsobject. Als u een serviceorderregel hebt gemaakt, kunt u het vervangingsartikel factureren. Als u geen serviceorderregel maakt voor een vervanging, wordt de vervanging geregistreerd om de historie van het serviceobject bij te houden.

## <a name="change-how-information-on-the-bom-line-is-displayed"></a>Wijzigen hoe gegevens in de stuklijstregel worden weergegeven

U kunt de manier wijzigen waarop stuklijstregelinformatie wordt weergegeven voor alle sjabloon- en servicestuklijsten. De wijzigingen worden toegepast op alle sjabloonstuklijsten en servicestuklijsten. Dit omvat de lijsten die zijn gekoppeld aan serviceobjecten.

## <a name="set-up-number-sequences-for-template-boms"></a>Nummerreeksen instellen voor sjabloonstuklijsten

Om sjabloonstuklijsten te gebruiken, moet u twee nummerreeksen instellen. Stel één nummerreeks in voor de sjabloonstuklijst en één voor het stuklijstregelnummer.


> [!NOTE]
> <P>Nummerreeksen worden gebruikt om id's toe te wijzen aan records die deze vereisen. Voordat u een nummerreeks aan een sjabloonstuklijst of een regelnummer stuklijstgeschiedenis kunt toewijzen, moet u nummerreekscodes instellen.</P>


## <a name="set-up-number-sequences"></a>Nummerreeksen instellen

1.  Op de pagina **Nummerreeksen** kunt u nummerreeksen maken voor sjabloonstuklijsten en het regelnummer voor de stuklijstgeschiedenis. 

2.  Klik op **Servicebeheer** \> **Instellen** \> **Parameters voor servicebeheer**.

3.  Klik op **Nummerreeksen** en selecteer vervolgens een nummerreekscode voor de nummerreeksverwijzingen die u hebt gemaakt in het formulier **Nummerreeksen**.

4.  Sluit het formulier om de wijzigingen op te slaan.


> [!NOTE]
> <P>Het regelnummer stuklijstgeschiedenis wordt gebruikt om de transacties in de stuklijstgeschiedenis aan een serviceovereenkomst of serviceorder te koppelen. Het nummer wordt niet weergegeven in de gebruikersinterface.</P>



## <a name="see-also"></a>Zie ook

[Een sjabloonstuklijst maken](create-template-bom.md)

[Sjabloonstuklijsten in objectrelaties beheren](manage-template-boms-on-object-relations.md)

[Een servicestuklijst wijzigen](modify-service-bom.md)

 


