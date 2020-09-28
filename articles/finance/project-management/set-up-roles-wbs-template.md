---
title: Rollen configureren in structuursjablonen voor werkspecificaties
description: Dit onderwerp bevat informatie over het instellen van rolgegevens in structuursjablonen voor werkspecificaties.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5dfb429eae933ba4d687ec4cbd417d2f78308e47
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760516"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>Rollen configureren in structuursjablonen voor werkspecificaties

[!include [banner](../includes/banner.md)]

Projectmanagers kunnen structuursjablonen voor werkspecificaties (WBS) configureren die ze kunnen toepassen wanneer ze een WBS voor nieuwe projecten maken. Projectmanagers kunnen rollen toevoegen wanneer ze een sjabloon maken. Gebruik de volgende procedure om een rol toe te wijzen aan een WBS-sjabloon. 

1. Selecteer **Projectbeheer en boekhouding** > **Instellen** > **Projecten** > **Structuursjablonen voor werkspecificatie**.
2. Selecteer een WBS-sjabloon en selecteer **Details**.
3. Selecteer een taak in de lijst en selecteer in het veld **Rol** een rol die u aan de taak wilt toewijzen.

## <a name="work-with-a-wbs"></a>Werken met een WBS

U kunt een nieuwe WBS maken, of u kunt een WBS van een bestaande WBS-sjabloon kopiëren. Een projectmanager kan de resources eenvoudig beheren door rollen aan nieuwe taken op de WBS toe te wijzen. Rollen kunnen worden vervangen wanneer een resource is verworven of nadat een bevestigde resource is geïdentificeerd die aan de taak gaat werken. Deze flexibiliteit stelt projectmanagers in staat om de volgende taken uit te voeren:

- Het aantal resources bepalen dat nodig is voor WBS-werkpakketten.
- Projectkosten ramen.
- Een voorlopig budget opstellen.
- De activiteitsduur schatten op basis van rollen en resources.
- Enkele projectbeheersplannen ontwikkelen, op basis van de beschikbare projectgegevens.

Extra opties zijn toegevoegd aan de WBS, om beter gebruik te kunnen maken van de resourcingfunctionaliteit.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Optie</th>
<th>Beschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Resourcetoewijzingen</td>
<td>Geef de toegewezen resources weer, de datums, het aantal uren, en het boekingstype voor taken op de WBS.</td>
</tr>
<tr class="even">
<td>Team automatisch genereren</td>
<td>Voeg automatisch geplande resources toe door rollen te gebruiken die aan een taak zijn gekoppeld. Finance suggereert automatisch geplande resources door middel van de op rollen gebaseerde beslissingsanalyse met meerdere criteria. Nadat de rollen en de inzet (uren) voor taken in de WBS zijn ingesteld en de structuur is vrijgegeven, selecteert u <strong>Team automatisch genereren</strong>. Het vereiste aantal geplande resources wordt toegevoegd aan de WBS en het tabblad <strong>Projectteam en planning</strong>.</td>
</tr>
<tr class="odd">
<td>Resource (vervolgkeuzelijst)</td>
<td>Op de pagina <strong>Resourcetoewijzing starten</strong> kunt u resources vast of variabel boeken, op basis van de opgegeven tijdsduur. U kunt de weergaveinstellingen aanpassen om de duur van resourceactiviteiten weer te geven en in te stellen. U kunt resources selecteren en toewijzen op het niveau van het werkpakket met de volgende opties:
<ul>
<li><strong>Accepteren</strong> Wijzigingen bevestigen aan de resource die aan een taak is toegewezen.</li>
<li><strong>Annuleren</strong> Wijzigingen annuleren aan de resource die aan een taak is toegewezen.</li>
<li><strong>Automatisch toewijzen:</strong> er wordt automatisch een beschikbare bemande resource met een overeenkomende rol geselecteerd en toegewezen aan de geselecteerde taak.</li>
</ul></td>
</tr>
</tbody>
</table>

1. Op de pagina **Alle projecten** selecteert u het project **XYZ-upgrade Fase 2**.
2. Selecteer **Plan** > **Activiteiten** > **Structuur voor werkspecificatie**.
3. Selecteer **Nieuw** en voeg de volgende activiteiten voor niveau 1 aan de WBS toe:

    - Initiëren
    - Planning
    - In uitvoering
    - Bewaking en controle
    - Sluiten

4. Stel de datums en inzet (uren) in, zoals in de volgende afbeelding.

    [![De datums en inzet instellen](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. Selecteer de taakregel **Initiëren** en selecteer in het veld **Rol** de waarde **Senior projectmanager**.
6. Selecteer **Publiceren**.
7. Selecteer op dezelfde regel in het veld **Resource** de naam **Daniel Goldschmidt** en selecteer **Accepteren**.
8. Selecteer de taakregel **Planning** en selecteer in het veld **Rol** de rol **Bedrijfsanalyst**.
9. Selecteer **Publiceren** en **Team automatisch genereren**.
10. Selecteer **Ja** in het dialoogvenster dat wordt geopend.
11. Controleer in het veld **Resource** of de waarde **Bedrijfsanalyst 1** is.
12. Open voor de resource **Bedrijfsanalist 1** de zoekopdracht en selecteer **Formulier voor resourcetoewijzing openen**. Selecteer een werknemer voor de taak.
13. Selecteer **Variabel boeken** &gt; **Volledige capaciteit**.

    > [!NOTE] 
    > U ontvangt geen waarschuwing dat de opgegeven resource nu 2 is, omdat het aantal resources 1 blijft.

14. Valideer op de pagina **Structuur voor werkspecificatie** de resourcetoewijzing voor de WBS en selecteer **Opslaan**.
