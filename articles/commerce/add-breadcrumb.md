---
title: Breadcrumb-module
description: In dit artikel wordt beschreven wat breadcrumb-modules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: fe5dfea7e579d54d11be35eb657a1c1f617a5724
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277080"
---
# <a name="breadcrumb-module"></a>Breadcrumb-module

[!include [banner](includes/banner.md)]

In dit artikel wordt beschreven wat breadcrumb-modules zijn en hoe u ze toevoegt aan sitepagina's in Microsoft Dynamics 365 Commerce.

Breadcrumb-modules worden gebruikt om secundaire navigatie uit te voeren op sitepagina's. Ze worden meestal boven aan een pagina weer gegeven, onder de koptekst. Hoewel u breadcrumb-modules aan elke pagina kunt toevoegen, worden ze meestal op de pagina's met productgegevens (PDP's) gebruikt om de hiërarchie van productcategorieën weer te geven zodat u snel door een locatie kunt navigeren. Een breadcrumb-module kan ook worden gebruikt om de koppeling Terug naar resultaten weer te geven wanneer gebruikers een PDP openen vanuit een zoek- of lijstpagina. Op deze manier kunnen gebruikers snel terugkeren naar de gefilterde lijstpagina om door te gaan met winkelen.

Op pagina's met een productcategoriecontext, zoals PDP's en categoriepagina's, wordt in breadcrumb-modules de categoriehiërarchie weergegeven. Op pagina's zonder categoriecontext worden in breadcrumb-modules standaard de **&lt;Hoofdmap van de site&gt; / &lt;Huidige pagina&gt;** weergegeven. Breadcrumb-modules kunnen ook handmatig op andere typen sitepagina's worden geconfigureerd om koppelingen naar specifieke pagina's op de site weer te geven.

> [!NOTE]
> De breadcrumb-module is beschikbaar in Dynamics 365 Commerce versie 10.0.12.

De volgende afbeelding toont een voorbeeld van een breadcrumb-module waarin de categoriehiërarchie op een PDP wordt weergegeven.

![Voorbeeld van een breadcrumb-module.](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a>Instellingen van breadcrumb-module

De breadcrumb-module is gebaseerd op de instelling **Breadcrumb-weergavetype voor PDP** die wordt gedefinieerd bij **Site-instellingen \> Uitbreidingen** in Site builder. Voor deze instelling bestaan drie mogelijke waarden:

- **Categoriehiërarchie weergeven**: wanneer deze waarde wordt geselecteerd, wordt in de breadcrumb-module de volledige categoriehiërarchie weergegeven van het product dat op de PDP wordt weergegeven.
- **Terug naar resultaten weergeven**: wanneer deze waarde wordt geselecteerd, wordt in de breadcrumb-module de koppeling "Terug naar resultaten" weergegeven op een PDP als de gebruiker de PDP opent vanuit een module die de koppeling "Terug naar resultaten" toestaat. Deze functie is beschikbaar wanneer gebruikers navigeren vanuit de pagina's categorie, zoeken, lijst en aanbevelingslijsten. Ter ondersteuning van deze functionaliteit hebben modules voor productverzameling en zoekresultaten een eigenschap met de naam **Terug naar resultaten van PDP toestaan**. Deze eigenschap geeft u de flexibiliteit om te bepalen welke modules de koppelingsfunctionaliteit "Terug naar resultaten" op de PDP moeten ondersteunen. Wanneer bijvoorbeeld **Terug naar resultaten weergeven** wordt geselecteerd voor de instelling **Breadcrumb-weergavetype voor PDP** van de breadcrumb-module, en **Terug naar resultaten van PDP toestaan** is geselecteerd voor de zoekmodule van de zoekpagina, wordt de koppeling Terug naar resultaten weergegeven wanneer gebruikers navigeren vanaf de zoekpagina naar een PDP.
- **Categoriehiërarchie weergeven en terug naar resultaten**: deze waarde is een combinatie van de voorgaande twee. Wanneer deze waarde wordt geselecteerd, worden in de breadcrumb-module zowel de hiërarchie van de volledige categorie als de koppeling Terug naar resultaten weergegeven (als deze is geconfigureerd) op een PDP.

> [!IMPORTANT]
> Deze instellingen zijn beschikbaar in Dynamics 365 Commerce versie 10.0.12. Als u een oudere versie van Dynamics 365 Commerce bijwerkt, moet u het bestand appsettings.json handmatig bijwerken. Zie [Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file) voor instructies voor het bijwerken van het appsettings.json.

## <a name="breadcrumb-module-properties"></a>Eigenschappen van Breadcrumb-module

| Naam van eigenschap. | Waarden | Beschrijving |
|---------------|--------|-------------|
| Basis | Tekst of koppeling| Deze optionele eigenschap specificeert de koppelingstekst en een koppelingsdoel voor de hoofdmap van de breadcrumb-site. Als deze eigenschap niet is geconfigureerd, wordt er geen hoofdmap gedefinieerd. |
| Breadcrumb-koppeling | Koppelen | Deze optionele eigenschap geeft koppelingen aan voor een handmatig geconfigureerde breadcrumb als deze koppelingen vereist zijn. Koppelingen worden weergegeven in de volgorde waarin ze worden vermeld. |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a>Een breadcrumb-module toevoegen aan een nieuwe pagina

Voer de volgende stappen uit om een breadcrumb-module aan een PDP toe te voegen en de vereiste eigenschappen in te stellen.

1. Ga naar **Site-instellingen \> Uitbreidingen** en selecteer vervolgens voor **Breadcrumb-weergavetype voor PDP** de optie **Categoriehiërarchie weergeven**.
1. Ga naar **Sjablonen** en selecteer de PDP-sjabloon.
1. Selecteer in het vak **Container** met de koopvakmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Breadcrumb** en selecteer vervolgens **OK**.
1. Selecteer **Opslaan**, selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.
1. Ga naar **Pagina's** en open een PDP die de PDP-sjabloon gebruikt. Maak een PDP als deze nog niet bestaat.
1. Selecteer in het vak **Container** met de koopvakmodule het weglatingsteken (**...**) en selecteer vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Breadcrumb** en selecteer vervolgens **OK**.
1. Selecteer **Koppelingstekst** in het deelvenster Eigenschappen van het **Breadcrumb**-vak onder **Hoofdmap**.
1. Voer in het dialoogvenster **Koppelingstekst** de optie **Start** in en selecteer vervolgens onder **Koppelingsdoel** **Een koppeling toevoegen**.
1. Selecteer in het dialoogvenster **Een koppeling toevoegen** een koppeling voor de breadcrumb-hoofdmap en selecteer vervolgens **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de sjabloon in te checken en selecteer **Publiceren** om te publiceren.

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Navigatiemenumodule](nav-menu-module.md)

[Siteselectiemodule](site-selector.md)

[Overzicht van de standaard landingspagina voor categorieën en pagina met zoekresultaten](category-search-page-overview.md)

[Productverzamelingsmodules](product-collection-module-overview.md)

[Module met vakje voor kopen](add-buy-box.md)

[Updates voor SDK's en modulebibliotheken](e-commerce-extensibility/sdk-updates.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
