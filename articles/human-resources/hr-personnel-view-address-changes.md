---
title: Adreswijzigingen weergeven en beheren
description: In dit onderwerp wordt uitgelegd hoe u adreswijzigingen kunt weergeven en beheren in Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 08/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Human Resources
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-07
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a69d723b45e834b022491c8eaf2a7fb580e54f1d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417924"
---
# <a name="view-and-manage-address-changes"></a>Adreswijzigingen weergeven en beheren

In dit onderwerp wordt beschreven hoe u adreswijzigingen kunt weergeven en beheren op de Werknemerselfservice-pagina **Persoonlijke gegevens bewerken** of de detailpagina **Medewerker** in Dynamics 365 Human Resources.

Veel organisaties willen dat werknemers hun persoonlijke gegevens beheren via een selfservicevoorziening. U kunt toestaan dat gebruikers hun adres bijwerken in het werkgebied **Werknemerselfservice**. U kunt deze wijzigingen vervolgens controleren in het werkgebied **Personeelsbeheer**. Als u deze functie wilt gebruiken, moet u het aantal dagen opgeven dat u wijzigingen wilt weergeven op de pagina **Human Resources-parameters**.

## <a name="configure-address-change-parameters"></a>Parameters voor adreswijziging configureren

Ga als volgt te werk om het aantal dagen in te stellen dat u wilt dat adreswijzigingen worden weergegeven in het werkgebied **Personeelsbeheer**:

1. Selecteer **Personeelsbeheer** in het navigatievenster.

2. Selecteer **Koppelingen**.

3. Selecteer **Human Resources-parameters**.

4. Voer in het veld **Aantal dagen** onder **Adreswijziging** het aantal dagen in dat u wilt dat adreswijzigingen worden weergegeven in het werkgebied **Personeelsbeheer**.

5. Sluit de pagina.

## <a name="create-or-change-an-employee-address"></a>Een werknemeradres maken of wijzigen

Werknemers kunnen hun eigen adres bijwerken in het werkgebied **Werknemerselfservice**. Volg deze stappen om een adres te maken of te wijzigen:

1. Selecteer de tegel **Werknemerselfservice** op de startpagina.

2. Selecteer **Persoonlijke gegevens bewerken**.

3. Selecteer **Toevoegen** om een adres toe te voegen. Als u een bestaand adres wilt bijwerken, selecteert u het adres uit de lijst en vervolgens **Bewerken**.

4. Voer de **Naam of een omschrijving** in.

5. Selecteer de vervolgkeuzelijst **Doel** en selecteer vervolgens het adrestype.

6. Voer **Land/regio** in.

7. Voer de **Postcode** in.

8. Voer de **Straat** in.

9. Voer **Plaats**, **Staat/provincie** en **District** in. Deze velden worden meestal automatisch ingesteld op basis van het veld **Postcode**.

10. Selecteer eventueel het veld **Primair** om een primair adres aan te duiden. Er kan slechts één adres worden gemarkeerd als het primaire adres. Als er al een ander adres is gemarkeerd als het primaire adres, moet u bevestigen dat u dit adres als het primaire adres wilt gebruiken.

11. Selecteer eventueel het veld **Privé** om aan te geven dat het een privé-adres is. Alleen gebruikers met expliciete machtigingen voor het weergeven van privé-adresgegevens kunnen dit adres bekijken.

12. Selecteer **OK**.

## <a name="create-or-change-a-worker-address"></a>Een werknemeradres maken of wijzigen

U kunt een adres bijwerken in het werkgebied **Personeelsbeheer**. Volg deze stappen om een adres te maken of te wijzigen:

1. Selecteer in het werkgebied **Personeelsbeheer** de optie **Koppelingen** en selecteer vervolgens **Werknemers**.

3. Selecteer de werknemer en vervolgens **Adressen**.

3. Selecteer **Toevoegen** om een adres toe te voegen. Als u een bestaand adres wilt bijwerken, selecteert u het adres uit de lijst en vervolgens **Bewerken**.

4. Voer de **Naam of een omschrijving** in.

5. Selecteer de vervolgkeuzelijst **Doel** en selecteer vervolgens het adrestype.

6. Voer **Land/regio** in.

7. Voer de **Postcode** in.

8. Voer de **Straat** in.

9. Voer **Plaats**, **Staat/provincie** en **District** in. Deze velden worden meestal automatisch ingesteld op basis van het veld **Postcode**.

10. Selecteer eventueel het veld **Primair** om een primair adres aan te duiden. Er kan slechts één adres worden gemarkeerd als het primaire adres. Als er al een ander adres is gemarkeerd als het primaire adres, moet u bevestigen dat u dit adres als het primaire adres wilt gebruiken.

11. Selecteer eventueel het veld **Privé** om aan te geven dat het een privé-adres is. Alleen gebruikers met expliciete machtigingen voor het weergeven van privé-adresgegevens kunnen dit adres bekijken.

12. Selecteer **OK**.
 
## <a name="create-a-future-change-for-an-address"></a>Een toekomstige wijziging voor een adres maken

In sommige gevallen wilt u mogelijk een adres bijwerken zodat het later kan worden gewijzigd. Dit is bijvoorbeeld handig als een werknemer op de 15e van de volgende maand verhuist.

1. Open de pagina **Adressen beheren** via **Meer opties > Geavanceerd** in een adresraster.

2. Selecteer **Nieuw** om een nieuw adres te maken.

3. Voer de gegevens van het adres in.

4. Selecteer het sneltabblad **Algemeen**.

5. Selecteer in het veld **Ingangsdatum** de datum waarop het nieuwe adres van kracht wordt.

6. Selecteer eventueel in het veld **Vervaldatum** de datum waarop het adres niet meer geldig is.

7. Sluit de pagina's.

## <a name="view-and-monitor-address-changes"></a>Adreswijzigingen weergeven en controleren

HR-medewerkers kunnen adreswijzigingen weergeven en controleren vanuit het werkgebied **Personeelsbeheer**. Als u de adreswijzigingen wilt weergeven, opent u de tegel **Personeelsbeheer** op de **Startpagina**. De adreswijzigingen worden weergegeven op een tegel in de rechterbovenhoek. Het nummer boven **Adreswijzigingen** geeft aan hoeveel adreswijzigingen zijn aangebracht in het aantal dagen dat is opgegeven op de pagina **Human Resources-parameters**. 

Wanneer u de tegel **Adreswijzigingen** selecteert, worden in een nieuwe pagina de details van eventuele adreswijzigingen weergegeven. U kunt desgewenst **Toekomstige adreswijzigingen opnemen** in de rechterbovenhoek selecteren om de adreswijzigingen met een toekomstige datum weer te geven.

> [!NOTE]
> Als u een waarschuwing of een e-mailbericht over deze adreswijzigingen wilt ontvangen, kunt u een nieuwe waarschuwingsregel maken op het tabblad **Opties** in het actievenster. Zie [Waarschuwingsregels maken](/fin-ops-core/fin-ops/get-started/create-alert-rules.md) voor meer informatie over het maken van waarschuwingsregels.<br><br>

> Als u een werkstroom voor de adreswijzigingen wilt configureren, kunt u de optie **Extern verzenden** in uw waarschuwingsregel selecteren en vervolgens Power Automate gebruiken om de zakelijke gebeurtenis te activeren en een werkstroom te configureren. Zie [Waarschuwingen als zakelijke gebeurtenissen](/fin-ops-core/dev-itpro/business-events/alerts-business-events.md) voor meer informatie.
