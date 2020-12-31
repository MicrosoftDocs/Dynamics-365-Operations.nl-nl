---
title: Nieuwe documentgebruikersinterface in bedrijfsdocumentbeheer
description: Dit onderwerp biedt informatie over het gebruik van de nieuwe documentgebruikersinterface (UI) in de functie voor bedrijfsdocumentbeheer van het ER-raamwerk (elektronische rapportage).
author: v-anamir
manager: AnnBe
ms.date: 05/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERBDWorkspace, ERBDParameters
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-anamir
ms.search.validFrom: 2019-08-01
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 2cb6e0da4af07b9b8486bf1e5bda29523cbd08e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681347"
---
# <a name="new-document-user-interface-in-business-document-management"></a>Nieuwe documentgebruikersinterface in bedrijfsdocumentbeheer

[!include [banner](../includes/banner.md)]

Beheer van bedrijfsdocumenten stelt zakelijke gebruikers in staat zakelijke documentsjablonen te bewerken met een Microsoft 365-service of de juiste Microsoft Office-bureaubladtoepassing. Wijzigingen kunnen ontwerpwijzigingen of nieuwe implementaties bevatten, of gebruikers kunnen tijdelijke aanduidingen toevoegen om extra gegevens op te nemen zonder de broncode te hoeven wijzigen. Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md) voor meer informatie over het werken met beheer van bedrijfsdocumenten.

De nieuwe documentgebruikersinterface (UI) is duidelijker en gemakkelijker te gebruiken. In het gebied **Bedrijfsdocument** worden alleen de sjablonen weergegeven die beschikbaar zijn voor de huidige provider.

Met de knop **Nieuw document** kunnen gebruikers een sjabloon maken en bewerken in een configuratie voor elektronische rapporteringsindeling die door een andere provider wordt geleverd. In het voorbeeld in dit onderwerp is de provider Microsoft.

## <a name="make-the-new-document-ui-in-business-document-management-available"></a>De nieuwe documentgebruikersinterface in Beheer van bedrijfsdocumenten beschikbaar maken

Als u de nieuwe documentgebruikersinterface wilt gebruiken in Beheer van bedrijfsdocumenten, moet u de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** inschakelen in het werkgebied **Functiebeheer**.

Voer de volgende stappen uit om deze functie in te schakelen voor alle rechtspersonen.

1. Selecteer in het werkgebied **Functiebeheer** op het tabblad **Nieuw** de functie **Office-achtige UI-ervaring voor Beheer van bedrijfsdocumenten** in de lijst.
2. Selecteer **Nu inschakelen** om de geselecteerde functie in te schakelen.
3. Vernieuw de pagina om de nieuwe functie te openen.

### <a name="edit-templates-that-are-owned-by-other-providers"></a>Sjablonen bewerken die eigendom zijn van andere providers

1. Selecteer **Nieuw document** in het werkgebied **Beheer van bedrijfsdocumenten**.

    ![Het werkgebied Beheer van bedrijfsdocumenten](./media/BDM_overview_new_template1.png)

2. Selecteer in het dialoogvenster het document dat u als sjabloon wilt gebruiken, en selecteer vervolgens **Document maken**.

    ![Dialoogvenster Bedrijfsdocumenten](./media/BDM_overview_new_template2.png)

3. Wijzig in het dialoogvenster Nieuw in het veld **Titel** de gewenste titel. De titeltekst wordt gebruikt als naam voor de nieuwe ER-indelingsconfiguratie die automatisch wordt gemaakt. De conceptversie van deze configuratie (**Kopie FTI-rapport klant (GER)**) bevat de bewerkte sjabloon en wordt gebruikt om deze ER-indeling uit te voeren voor de huidige gebruiker. De oorspronkelijke sjabloon uit de ER-basisindelingsconfiguratie wordt gebruikt om deze ER-indeling voor elke andere gebruiker uit te voeren.
4. Wijzig in het veld **Naam** de naam van de eerste revisie van de bewerkbare sjabloon die automatisch wordt gemaakt.
5. Wijzig in het veld **Opmerking** de opmerkingen voor de automatisch gemaakte revisie van de bewerkbare sjabloon.
6. Selecteer **OK** om het begin van het bewerkingsproces te bevestigen.

    ![Dialoogvenster om document te maken](./media/BDM_overview_new_template3.png)

De knop **Nieuw document** wordt gebruikt om een sjabloon te maken en bewerken in een ER-indelingsconfiguratie die door een andere provider wordt geleverd. In dit voorbeeld is de provider Microsoft. Wanneer u **Nieuw document** selecteert, ziet u alle sjablonen die eigendom zijn van huidige en andere providers. Nadat u de sjabloon hebt geselecteerd, wordt deze geopend om te worden bewerkt. De bewerkte sjabloon wordt vervolgens opgeslagen in een nieuwe ER-indelingsconfiguratie die automatisch wordt gegenereerd.

Zie [Overzicht van Beheer van bedrijfsdocumenten](er-business-document-management.md)voor meer informatie.
