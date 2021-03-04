---
title: Beveiligingsdiagnose voor taakregistraties
description: Dit onderwerp bevat informatie over het analyseren en beheren van vereisten voor beveiligingsmachtigingen op basis van een taakregistratie.
author: Peakerbl
manager: AnnBe
ms.date: 05/05/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: ''
ms.dyn365.ops.version: Version 10.0.9
ms.openlocfilehash: 88eb90b35f1a9754cc4daa01d8f40cdf712db4f8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679785"
---
# <a name="security-diagnostics-for-task-recordings"></a>Beveiligingsdiagnose voor taakregistraties

[!include [banner](../../includes/banner.md)]

## <a name="before-you-begin"></a>Voordat u begint

Dit onderwerp bevat informatie over het analyseren en beheren van vereisten voor beveiligingsmachtigingen op basis van een taakregistratie. Voordat u de stappen in dit onderwerp uitvoert, moet u beschikken over een taakregistratie van het bedrijfsproces dat u wilt analyseren. Zie [Resources voor Taakrecorder](../../user-interface/task-recorder.md) om een bedrijfsproces vast te leggen. 

## <a name="manage-security-for-a-task-recording"></a>Beveiliging voor een taakregistratie beheren

1. Ga naar **Systeembeheer** > **Beveiliging** > **Beveiligingsdiagnose voor taakregistratie**.
2. Open de taakregistratie vanaf de locatie. Selecteer **Openen vanaf deze pc** of **Openen vanuit Lifecycle Services** en selecteer **Sluiten**.
3. Hiermee opent u de pagina **Details van beveiligingsmenuopdrachten** met de beveiligingsobjecten die nodig zijn voor het proces.

 > [!NOTE]
 > De menuopdrachten **Actie** en **Uitvoer** worden niet in de lijst opgenomen.

4. Selecteer een gebruiker in het veld **Gebruikers-id**. Als de gebruiker geen machtigingen heeft voor sommige menuopdrachten, wordt het veld **Ontbrekende machtigingen** bijgewerkt naar **Ja**.
  
  ![Pagina Details van beveiligingsmenuopdrachten](../media/Security-Menu-Item-Details.png)

5. Selecteer **Verwijzing toevoegen** om een lijst weer te geven met de beveiligingsobjecten, waaronder rollen, functies en bevoegdheden waarmee de ontbrekende machtiging wordt verleend.
6. Selecteer een beveiligingsobject in de lijst:

    - Als **Rol** wordt geselecteerd, selecteert u **Rol toevoegen aan gebruiker**. Hierdoor wordt de pagina **Gebruikers aan rollen toewijzen** geopend. Zie de pagina [Gebruikers aan beveiligingsrollen toewijzen](assign-users-security-roles.md) voor meer informatie.
    - Als **Functie** is geselecteerd, selecteert u **Functie toevoegen aan rol**, selecteert u de rollen waaraan de functie moet worden toegevoegd en selecteert u vervolgens **OK**.
    - Als **Bevoegdheid** is geselecteerd, selecteert u **Bevoegdheid toevoegen aan functies**, selecteert u de rollen waaraan de functie moet worden toegevoegd en selecteert u vervolgens **OK**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]