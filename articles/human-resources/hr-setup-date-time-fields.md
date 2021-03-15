---
title: Velden Datum en Tijd begrijpen
description: Begrijp wat u kunt verwachten wanneer u datum- en tijdvelden gebruikt in Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d843eb8cefcd0f2f45c8956cd451f88ca6336efb
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130442"
---
# <a name="understand-date-and-time-fields"></a>Datum- en tijdvelden begrijpen

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

**Datum- en tijdvelden** vormen een fundamenteel concept in Dynamics 365 Human Resources. Het is belangrijk om te begrijpen hoe u werkt met de **Datum- en tijd**-gegevens in formulieren, uit Dataverse en uit externe bronnen.

## <a name="understanding-the-difference-between-date-and-date-and-time-field-data-types"></a>Het verschil tussen veldgegevenstypen Datum en Datum en tijd

Een veld **Datum en tijd** bevat informatie over de tijdzone, het veld **Datum** niet. Een veld **Datum** bevat dezelfde informatie op elke locatie. Wanneer u een datum in een veld **Datum** invoert, wordt diezelfde datum naar de database geschreven.

Wanneer gegevens worden weergegeven in een veld **Datum en tijd**, worden de datum en tijd aangepast op basis van de tijdzone van de gebruiker die is ingesteld in het formulier **Gebruikersopties** (**Algemeen > Instellingen > Gebruikersopties**). De datum- en tijdgegevens die u in het veld invoert, zijn mogelijk niet hetzelfde als de gegevens die naar de database worden geschreven.

[![Het formulier Gebruikersopties](./media/useroptionsform.png)](./media/useroptionsform.png)

## <a name="understanding-date-and-time-fields-in-forms"></a>Datum- en tijdvelden in formulieren begrijpen 

De gegevens in een veld **Datum en tijd** die u ziet op het scherm, komen niet overeen met de gegevens die in de database zijn opgeslagen als de tijdzone van de gebruiker niet is ingesteld op UTC (Coordinated Universal Time). De gegevens een veld **Datum en tijd** worden altijd als UTC opgeslagen.

[![Het formulier Medewerker in UTC](./media/worker-form.png)](./media/worker-form.png)

## <a name="understand-date-and-time-fields-in-the-database"></a>Datum- en tijdvelden in de database begrijpen 

Wanneer in Human Resources een waarde voor **Datum en tijd** naar de database wordt geschreven, worden de gegevens opgeslagen in UTC. Op deze manier kunnen gebruikers de gegevens in **Datum en tijd** weergeven in relatie tot de tijdzone die is gedefinieerd in hun gebruikersopties.
 
In het vorige voorbeeld is de begintijd een moment, niet een bepaalde datum. Als de tijdzone van de aangemelde gebruiker wordt gewijzigd van GMT+12:00 in GMT UTC, wordt dezelfde record die net is gemaakt, weergegeven met 30-04-2019 12:00:00 in plaats van 01-05-2019 12:00:00.
  
In het onderstaande voorbeeld wordt het dienstverband van medewerker 000724 op hetzelfde moment actief, ongeacht de tijdzone. De medewerker wordt actief op 30-04-2019 in de tijdzone GMT, wat hetzelfde is als 01-05-2019 in de tijdzone GMT+12:00. Beide verwijzen naar hetzelfde moment en niet naar een bepaalde datum. 

[![Het formulier Medewerker in GMT](./media/worker-form2.png)](./media/worker-form2.png)

## <a name="date-and-time-data-in-data-management-framework-excel-dataverse-and-power-bi"></a>Datum- en tijdgegevens in Data Management Framework, Excel, Dataverse en Power BI 

Data Management Framework, de Excel-invoegtoepassing, Dataverse en Power BI-rapportage zijn allemaal ontworpen om rechtstreeks met gegevens te werken op databaseniveau. Omdat er geen client is om de gegevens in **Datum en tijd** aan te passen aan de tijdzone van de gebruiker, worden alle waarden voor **Datum en tijd** in UTC weergegeven. Dit kan leiden tot enkele onjuiste aannames bij het invoeren of weergeven van gegevens.  
 
Bij gegevens voor **Datum en tijd** die worden ingediend via DMF, Excel of Dataverse, wordt er voor de database van uitgegaan dat deze in UTC zijn. Dit kan leiden tot verwarring wanneer de ingediende waarde voor **Datum en tijd** niet wordt weergegeven zoals verwacht omdat de gebruiker die de gegevens weergeeft niet de tijdzone UTC heeft ingesteld. 
 
Hetzelfde kan in tegengestelde richting gebeuren wanneer er gegevens worden geëxporteerd. De gegevens bij **Datum en tijd** in de geëxporteerde DMF-entiteit kunnen verschillen van wat wordt weergegeven in de Dynamics-client. 
 
Wanneer u externe bronnen zoals DMF gebruikt om gegevens te bekijken of op te geven, moet u er rekening mee houden dat er standaard van uitgegaan wordt dat de waarden voor **Datum en tijd** in UTC zijn, ongeacht de tijdzone van de computer van de gebruiker of de huidige tijdzone-instellingen van de gebruiker. 

## <a name="examples-of-the-same-record-being-displayed-in-different-product-areas"></a>Voorbeelden van dezelfde record die in verschillende productgebieden wordt weergegeven 

**Human Resources met de tijdzone ingesteld op UTC**

[![Het formulier Werknemer ingesteld op UTC](./media/worker-form3.png)](./media/worker-form3.png)

**Human Resources met de tijdzone ingesteld op GMT +12:00** 

[![Het formulier Werknemer ingesteld op GMT](./media/worker-form4.png)](./media/worker-form4.png)

**Excel via OData**

[![Excel via OData](./media/Excelviaodata.png)](./media/Excelviaodata.png)

**DMF-fasering**

[![DMF-fasering](./media/DMFStaging.png)](./media/DMFStaging.png)

**DMF-export**

[![DMF-export](./media/DMFexport.png)](./media/DMFexport.png)

**Excel via Dataverse**

[![Excel via Dataverse](./media/ExcelCDS.png)](./media/ExcelCDS.png)

## <a name="see-also"></a>Zie ook

[Datum- en tijdgegevens](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/date-time-zones)<br></br>
[Voorkeurstijdzones van gebruiker](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/organization-administration/tasks/set-users-preferred-time-zone) 


[!INCLUDE[footer-include](../includes/footer-banner.md)]