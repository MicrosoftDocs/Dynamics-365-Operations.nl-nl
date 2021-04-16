---
title: Goedkeuringswerkstromen voor lease gebruiken
description: In dit onderwerp wordt uitgelegd hoe u werkstromen gebruikt om activaleases goed te keuren en hoe u de status en historie van de werkstromen bijhoudt.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2f9fc8e337206111b0f2ac1cca87131abe7f283c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827525"
---
# <a name="use-lease-approval-workflows"></a>Goedkeuringswerkstromen voor lease gebruiken

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u werkstromen gebruikt om activaleases goed te keuren en hoe u de status en historie van de werkstromen bijhoudt. Met behulp van werkstromen kunt u het beheer van leasegoedkeuringen consistent maken door een standaardset goedkeuringsstappen te bieden en specifieke gebruikers toe te wijzen die elke stap van het proces goedkeuren. Een fiatteur kan een lease goedkeuren, deze weigeren, een wijziging aanvragen of deze toewijzen aan een andere gebruiker voor goedkeuring. Door werkstromen kan het goedkeuringsproces beter zichtbaar worden, doordat u de status en historie kunt bijhouden. Daarnaast kunt u een gecentraliseerde werklijst bekijken waarin de taken en goedkeuringen worden vermeld die aan specifieke fiatteurs zijn toegewezen.

Voordat u deze procedure gaat gebruiken, moet u ervoor zorgen dat ten minste één werkstroom voor het goedkeuren van leases is gemaakt. Als er geen werkstroom bestaat, maakt u er een. Zie [Goedkeuringswerkstromen voor lease instellen](set-up-lease-wrkflw.md) voor meer informatie over hoe u een werkstroom kunt instellen.

1. Dien een lease in voor goedkeuring. Selecteer op de pagina **Boekdetails** voor de lease de optie **Werkstroom** en selecteer vervolgens **Indienen**.
2. In het dialoogvenster dat wordt weergegeven, kunt u een opmerking toevoegen. De aangewezen fiatteur ziet deze opmerking samen met de lease. Wanneer u klaar bent met het invoeren van de opmerking, selecteert u **Indienen**. De lease wordt ingediend bij het werkstroomsysteem en de fiatteur ontvangt deze ter goedkeuring.
3. Als u de leases wilt weergeven die zijn toegewezen voor goedkeuring, gaat u naar **Modules \> Algemeen \> Werkitems \> Aan mij toegewezen werkitems**.
4. Selecteer op de pagina **Aan mij toegewezen werkitems** de koppeling **Lease-id** voor de lease die u wilt weergeven. De pagina die wordt weergegeven, is afhankelijk van de leaseboeken en leasedetails waartoe u toegang hebt.
5. Wanneer u klaar bent met het bekijken van de lease, selecteert u **Werkstroom** en beslist u welke actie moet worden ondernomen. De opties zijn **Goedkeuren**, **Afgewezen**, **Wijziging aanvragen**, **Delegeren** en **Geannuleerd**. U kunt ook **Historie weergeven** selecteren als u de goedkeuringshistorie voor de geselecteerde lease wilt bekijken.
6. Nadat u een actie hebt geselecteerd, voert u een opmerking in om de actie te beschrijven. Wanneer u klaar bent met het invoeren van de opmerking, selecteert u de actie **Goedgekeurd** in de lijst.
7. Als u de goedkeuringsacties wilt weergeven, gaat u terug naar de pagina **Leasedetails** op de pagina **Leaseoverzicht** en selecteert u vervolgens **Werkstroom \> Hostorie weergeven**.

    U kunt de werkstroomactiviteiten weergeven op de pagina **Werkstroomhistorie**. Op deze pagina worden de werkstroomstappen weergegeven die voor de specifieke lease zijn genomen. U kunt ook het veld **Werkitems** gebruiken om de status van de toegewezen werkitems te bekijken.

8. Als u een werkstroom wilt stoppen, selecteert u op de pagina **Werkstroomhistorie** de optie **Intrekken**. Voer in het dialoogvenster dat verschijnt een opmerking in en selecteer vervolgens **OK**.
9. Als u een werkstroom wilt deactiveren of een eerder gemaakte werkstroom wilt activeren, gaat u naar **Activa leasen \> Instellingen \> Leasewerkstroom**. Selecteer vervolgens op de pagina **Leasewerkstroom** **Werkstroom \> Versies**. Als u een huidige werkstroom wilt deactiveren, selecteert u de actieve lease in het dialoogvenster Leaseversie en selecteert u **Deactiveren**. Als u een bestaande werkstroom wilt activeren, selecteert u de werkstroom en selecteert u **Activeren**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]