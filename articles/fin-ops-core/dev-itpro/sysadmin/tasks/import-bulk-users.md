---
title: Gebruikers importeren vanuit Azure Active Directory
description: Deze procedure kan worden gebruikt door systeembeheerders om handmatig geselecteerde gebruikers te importeren of een groot aantal gebruikers te importeren vanuit Azure Active Directory.
author: peakerbl
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce8c98add0c6d5fb07b3ba5338037d9a12b1d8e50a2d2039b0231d3d305c9ebe
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748283"
---
# <a name="import-users-from-azure-active-directory"></a>Gebruikers importeren vanuit Azure Active Directory

[!include [banner](../../includes/banner.md)]

## <a name="import-select-users"></a>Geselecteerde gebruikers importeren

Deze procedure kan worden gebruikt door systeembeheerders om een geselecteerde gebruikers te importeren vanuit Azure Active Directory (Azure AD).

1. Gebruiker wordt geïmporteerd met het huidige sessiebedrijf als standaardbedrijf. Wijzig het huidige bedrijf indien van toepassing voordat u gebruikers importeert.
2. Ga naar **Systeembeheer > Gebruikers > Gebruikers**.
3. Klik op **Gebruikers importeren**.
4. Selecteer de gebruikers die moeten worden geïmporteerd en selecteer vervolgens **Gebruikers importeren**.

Nadat het importeren is voltooid, moet u rollen toewijzen aan gebruikers.

## <a name="import-users-in-bulk"></a>Gebruikers bulksgewijs importeren

Deze procedure kan worden gebruikt door systeembeheerders om een groot aantal gebruikers van Azure Active Directory te importeren.
Het is niet mogelijk om gebruikers te selecteren wanneer u de optie Batch importeren gebruikt.

## <a name="run-the-import-as-a-batch-job"></a>De import uitvoeren als een batchtaak
1. Gebruiker wordt geïmporteerd met het huidige sessiebedrijf als standaardbedrijf. Wijzig het huidige bedrijf indien van toepassing voordat u gebruikers importeert.
2. Ga naar **Systeembeheer > Gebruikers > Gebruikers**.
3. Klik op **Batch importeren**.
4. Vouw de sectie **Op de achtergrond uitvoeren** uit.
4. Selecteer **Ja** in het veld **Batchverwerking**.
6. Typ of selecteer een waarde in het veld **Batchgroep**. Deze stap is optioneel.  
7. Selecteer **Ja** in het veld **Privé**. Deze stap is optioneel.  
8. Selecteer **Ja** in het veld **Kritieke taak**. Deze stap is optioneel.  
9. Selecteer een optie in het veld **Categorie bewaken**.
10. Klik op **OK**.

Nadat het importeren is voltooid, moet u rollen toewijzen aan gebruikers.

## <a name="run-in-a-sandbox-environment"></a>Uitvoeren in een sandbox-omgeving
1. Selecteer **Batch importeren**.
2. Selecteer **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]