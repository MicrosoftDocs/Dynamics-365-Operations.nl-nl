---
title: Goedkeuringswerkstromen voor lease instellen
description: In het onderwerp wordt uitgelegd hoe u een goedkeuringswerkstroom instelt die wordt uitgevoerd wanneer er een nieuwe lease wordt gemaakt.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: d2135458873963dc7c930b4bcef0c508c7d9635f
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992834"
---
# <a name="set-up-lease-approval-workflows"></a>Goedkeuringswerkstromen voor lease instellen

[!include [banner](../includes/banner.md)]

In het onderwerp wordt uitgelegd hoe u een goedkeuringswerkstroom instelt die wordt uitgevoerd wanneer er een nieuwe lease wordt gemaakt. Zie [Goedkeuringswerkstromen voor lease gebruiken](use-create-lease-wrkflw.md) voor meer informatie over hoe u de werkstroom kunt gebruiken. 

1. Ga naar **Activa leasen \> Instellingen \> Leasewerkstroom**.
2. Selecteer **Nieuw** op de pagina **Leasewerkstroom**.
3. Selecteer in het dialoogvenster dat verschijnt, onder **Werkstroomtype**, de koppeling **Leasewerkstroom**.

    De toepassing wordt geopend. Nadat deze is uitgevoerd, kunt u zich aanmelden bij Azure Active Directory (Azure AD) en wordt u omgeleid naar de werkstroomtoepassing.

4. Sleep het element **Goedkeuring leasewerkstroom** naar de werkstroom.
5. Verbind één knooppunt van **Start** naar **Goedkeuring leasewerkstroom**. Sluit **Goedkeuring leasewerkstroom** vervolgens aan op **Einde**.
6. Dubbelklik op **Goedkeuring leasewerkstroom**.
7. Selecteer **Eigenschappen** en voer vervolgens onder **Basisinstellingen** een naam voor de werkstroom in.

    Op deze pagina kunt u ook meer parameters voor de werkstroom instellen. Als u **Automatische acties** hebt ingeschakeld, neemt het systeem automatisch een specifieke actie. Meldingen kunnen worden verzonden als deze zijn opgegeven op het tabblad **Meldingen**. Op het tabblad **Geavanceerde instellingen** kunt u een definitieve fiatteur opgeven, een tijdslimiet instellen en specifieke acties toewijzen die moeten worden voltooid.

8. Wanneer u klaar bent met het instellen van de werkstroomparameters, selecteert u **Sluiten**.
9. Selecteer **Stap 1** en selecteer vervolgens **Eigenschappen**.
10. Voer onder **Basisinstellingen** een naam in voor de stap, maak een onderwerpregel voor de goedkeuring en geef instructies op voor de goedkeuring.
11. Selecteer op de pagina **Toewijzing** het toewijzingstype.
12. Selecteer **Gebruiker**, selecteer de gebruikers die leases goedkeuren en selecteer **Sluiten** om specifieke gebruikers aan de goedkeuring toe te wijzen.
13. Selecteer **Opslaan en sluiten** om de werkstroom te maken. Selecteer **OK** wanneer u daarom wordt gevraagd.
14. Selecteer op de pagina **Werkstroom maken**, de optie **Sluiten**.
14. Selecteer de nieuwe werkstroom en selecteer vervolgens **Versies**. Selecteer vervolgens **Actief maken** om ervoor te zorgen dat de werkstroom actief is.
15. Selecteer **Sluiten**. De nieuwe actieve versie wordt weergegeven.
