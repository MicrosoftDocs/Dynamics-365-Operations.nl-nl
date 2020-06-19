---
title: Afdelingen maken en deze opnemen in de afdelingenhiërarchie
description: Een afdeling is een operationele eenheid die een categorie of functioneel onderdeel van een organisatie voorstelt. Een afdeling is verantwoordelijk voor een specifiek gebied van de organisatie, zoals verkoop, boekhouding of HR. U kunt afdelingen gebruiken om te rapporteren over functiegebieden. Afdelingen zijn mogelijk verantwoordelijk voor winst en verlies.
author: andreabichsel
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
ms.search.form: HierarchyDesigner, OMOperatingUnit, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 8dbaddf0165f36db07378e817639fd8b17a4a96f
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2020
ms.locfileid: "3428892"
---
# <a name="create-departments-and-include-them-in-the-department-hierarchy"></a>Afdelingen maken en deze opnemen in de afdelingenhiërarchie

Een afdeling is een operationele eenheid die een categorie of functioneel onderdeel van een organisatie voorstelt. Een afdeling is verantwoordelijk voor een specifiek gebied van de organisatie, zoals verkoop, boekhouding of HR. U kunt afdelingen gebruiken om te rapporteren over functiegebieden. Afdelingen zijn mogelijk verantwoordelijk voor winst en verlies.

Een afdeling kan ook een groep kostenplaatsen bevatten. Posities kunnen worden toegewezen aan afdelingen. Als u een afdeling wilt toevoegen, klikt u op **Human Resources** &gt; **Afdelingen** &gt; **Afdeling**. In de volgende tabel worden de velden beschreven die beschikbaar zijn.

| Veld               | Beschrijving                                                                                                                                                                                                       |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Naam                | Geef een naam op voor de afdeling.                                                                                                                                                                                  |
| Nummer afdeling   | Een standaardwaarde kan automatisch worden gegenereerd als er een nummerreekscode is toegewezen aan de verwijzing naar het **Organisatienummer** op de pagina **Nummerreeksen**.                                                 |
| Zoeknaam         | Voer een naam of een acroniem in die u kunt gebruiken om de afdeling te zoeken.                                                                                                                                            |
| Memo                | Voer hier aanvullende gegevens in.                                                                                                                                                                            |
| In hiërarchie        | Een ingeschakeld selectievakje geeft aan dat de afdeling is opgenomen in de afdelingshiërarchie. Voor informatie over hoe u een afdeling aan de afdelingshiërarchie toevoegt, zie de informatie later in dit artikel. |
| DUNS-nummer         | DUNS staat voor Data Universal Number System. Dit is een nummer van negen cijfers dat door Dun & Bradstreet is uitgegeven.                                                                                                     |
| Beheerder             | Voer de persona in die de afdeling beheert.                                                                                                                                                                    |
| Adressen           | Voeg de adresgegevens voor de afdeling toe. Voeg bijvoorbeeld het adres voor het gebouw in waarin de afdeling zich bevindt.                                                                          |
| Contactgegevens | Voeg contactgegevens voor de afdeling toe. Voeg bijvoorbeeld een telefoonnummer toe voor de servicedesk in de afdeling.                                                                                           |

Als u een afdeling wilt toevoegen aan de afdelingshiërarchie, volgt u deze stappen.

1.  Klik op **Human resources** &gt; **Afdelingen** &gt; **Afdelingshiërarchie**.
2.  Klik op **Bewerken** en selecteer de organisatie waar de afdeling onder moet vallen.
3.  Klik op **Invoegen** en selecteer **Afdeling** in de lijst.
4.  Selecteer in de lijst van afdelingen die wordt weergegeven, de afdeling om aan de hiërarchie toe te voegen.
5.  Sla de wijzigingen op. U ontvangt een bericht dat er een conceptversie van de hiërarchie is gemaakt.
6.  Wanneer u klaar bent, klikt u op **Publiceren** in de hiërarchieontwerper. U kunt een ingangsdatum invoeren waarmee wordt aangegeven wanneer de hiërarchie moet worden gepubliceerd. Als u bijvoorbeeld een nieuwe afdeling wilt toevoegen aan het begin van het volgende kalenderjaar, stelt u de ingangsdatum in op 1 januari van het nieuwe kalenderjaar. De wijzigingen in de hiërarchie worden op die datum van kracht.

## <a name="steps-for-creating-a-department"></a>Stappen voor het maken van een afdeling
Raadpleeg het artikel [Nieuwe afdelingen definiëren](../fin-and-ops/hr/tasks/define-new-departments.md) voor de stapsgewijze procedure voor het maken van een nieuwe afdeling. 
