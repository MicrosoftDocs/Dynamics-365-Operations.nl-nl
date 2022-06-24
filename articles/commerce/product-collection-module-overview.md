---
title: Productverzamelingsmodules
description: In dit artikel vindt u een overzicht van de productverzamelingmodules in Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 05/18/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 02a3d6314729f51d6c1dced5037f78d12355c09a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8871654"
---
# <a name="product-collection-modules"></a>Productverzamelingsmodules

[!include [banner](includes/banner.md)]

In dit artikel vindt u een overzicht van de productverzamelingmodules in Microsoft Dynamics 365 Commerce.

Productdetectie is een primair hulpmiddel dat detailhandelaren gebruiken om hun klanten op een e-commerce-website te benaderen. Modules voor productverzamelingen helpen u om aantrekkelijke winkelervaringen samen te stellen door een intuïtieve visuele interface te bieden die kan worden gebruikt om snel productverzamelingen te ontwerpen.

Modules voor productverzamelingen vertegenwoordigen fysieke producten en services op de website. Een productverzamelingsmodule wordt meestal gekoppeld aan een detailpagina waar klanten een product of service kunnen kopen of meer informatie kunnen bekijken. 

De bronnen voor productverzamelingen kunnen lijsten van vier typen zijn:

- Redactionele lijsten van producten die handmatig in Dynamics 365 Commerce zijn gedefinieerd als verwante producten voor een product of productlijsten
- Algoritmelijsten, zoals lijsten van nieuwe, best verkochte en trending producten
- Aanbevelingslijsten die zijn gebaseerd op machine learning
- Personalisatielijsten die gepersonaliseerde resultaten voor een klant ondersteunen. Klanten moeten zijn aangemeld bij de e-Commerce-site om gepersonaliseerde resultaten te zien. Gastgebruikers zien geen gepersonaliseerde resultaten. Klanten kunnen zich afmelden voor personalisatie via de [pagina voor accountbeheer](account-management.md).

In de volgende afbeelding ziet u de verschillende typen productverzamelingen die worden gebruikt op een e-commerce-site.

![Voorbeeld van de verschillende typen productverzamelingen op een e-commerce-site.](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Gebruik productverzamelingsmodules altijd om een groep producten van een vergelijkbaar type weer te geven.

## <a name="product-collection-modules-and-types"></a>Productverzamelingsmodules en typen

In de volgende tabel worden diverse typen productverzamelingsmodules beschreven in Dynamics 365 Commerce.

| Productverzamelingsmodule  | Type | Beschrijving |
|----------------------------|------|-------------|
| Categorie                   | Categorie | In deze module wordt een lijst met producten in een categorie weergegeven, zoals gedefinieerd door de navigatiecategoriehiërarchie die de detailhandelaar voor een kanaal heeft gemaakt. |
| Verwante producten           | Redactionele informatie | In deze module wordt een lijst met producten weergegeven die door een merchandisingmanager zijn geconfigureerd als gerelateerde producten in Commerce, voor het relatietype dat de auteur heeft geselecteerd. |
| Zoekresultaten             | Zoekquery | In dit type productverzamelingsmodule wordt een lijst met producten weergegeven die het meest overeenkomen met de zoekquery die de klant heeft ingevoerd. |
| Gecureerde lijsten met producten      | Redactionele informatie | In deze module worden aangepaste lijsten weergegeven die in Commerce zijn gemaakt door verkoopadviseurs en editors. |
| Nieuw                        | Algoritme | In deze module wordt een lijst met de nieuwste producten weergegeven die zijn gesorteerd in afzetkanalen en catalogi. Deze lijst kan gepersonaliseerde resultaten voor een aangemelde gebruiker bevatten als de auteur van de site die optie kiest. |
| Meest verkocht               | Algoritme | Deze module bevat een lijst met producten die worden gerangschikt op het hoogste verkoopaantal. Deze lijst kan gepersonaliseerde resultaten voor een aangemelde gebruiker bevatten als de auteur van de site die optie kiest. |
| Trending                   | Algoritme | In de lijst in deze module worden de best presterende producten gedurende een bepaalde periode weergegeven. Deze lijst kan gepersonaliseerde resultaten voor een aangemelde gebruiker bevatten als de auteur van de site die optie kiest. |
| Vaak samen gekocht | Kunstmatige intelligentie/Machine learning | Deze module maakt gebruik van machine learning voor het analyseren van inkooppatronen van consumenten en het aanbevelen van verwante artikelen die vaak samen met een bepaald product worden gekocht. Deze lijst kan gepersonaliseerde resultaten voor een aangemelde gebruiker bevatten als de auteur van de site die optie kiest. |
| Wat mensen ook leuk vinden           | Kunstmatige intelligentie/Machine learning | Deze module maakt gebruik van machine learning voor het analyseren van inkooppatronen van consumenten en het aanbevelen van artikelen die samenhangen met een bepaald product. Deze lijst kan gepersonaliseerde resultaten voor een aangemelde gebruiker bevatten als de auteur van de site die optie kiest. |
| Selectie voor u              | Kunstmatige intelligentie/Machine learning | Deze module maakt gebruik van machine learning voor het analyseren van de aankooppatronen van de aangemelde gebruiker en om persoonlijke aanbevelingen te bieden die zijn gebaseerd op die aankooppatronen. Voor een gastgebruiker wordt deze lijst samengevouwen. |

## <a name="supported-modules"></a>Ondersteunde modules 

De productverzamelingsmodule ondersteunt de [module voor snelle weergave](quick-view-module.md), waarmee gebruikers productgegevens kunnen bekijken en artikelen aan het winkelwagentje kunnen toevoegen via een productverzamelingspagina.

## <a name="add-a-product-collection-module-to-a-category-page"></a>Een productverzamelingsmodule aan een categoriepagina toevoegen

Voer deze stappen uit om een productverzamelingsmodule aan een categoriepagina toe te voegen.

1. Ga naar **Pagina's** en selecteer **Nieuw** om een nieuwe pagina te maken.
1. Voer in het dialoogvenster **Een nieuwe pagina maken** onder **Paginanaam** een geschikte paginanaam in en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een sjabloon kiezen** dezelfde sjabloon als die van de standaardpagina voor categorieën en selecteer vervolgens **Volgende**.
1. Selecteer onder **Een indeling kiezen** een pagina-indeling (bijvoorbeeld **Flexibele indeling**) en selecteer vervolgens **Volgende**.
1. Controleer de paginaconfiguratie onder **Controle en voltooien**. Selecteer **Terug** als u de pagina-informatie wilt bewerken. Als de paginagegevens juist zijn, selecteert u **Pagina maken**. 
1. Selecteer het beletselteken (**...**) in het vak **Subvoettekst** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Container** en selecteer vervolgens **OK**.
1. Selecteer het weglatingsteken (**...**) in het vak **Container** en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Modules selecteren** de module **Productverzameling** en selecteer vervolgens **OK**.  
1. Selecteer **Een productlijst toevoegen** in het deelvenster met eigenschappen voor de productverzamelingsmodule.
1. Selecteer in het dialoogvenster **Productlijstconfiguratie selecteren** het type lijst en de lijstbron, voer het aantal artikelen in en selecteer eventuele andere opties die beschikbaar zijn voor het lijsttype. Configureer andere opties die beschikbaar zijn voor het lijsttype. Meer informatie over lijsttypen vindt u in de tabel hieronder. 
1. Selecteer **OK**.
1. Selecteer **Opslaan** en vervolgens **Preview** om de pagina te bekijken.
1. Selecteer **Bewerken voltooien** om de pagina in te checken en selecteer **Publiceren** om te publiceren.

In de volgende tabel worden de lijsttypen weergegeven die beschikbaar zijn voor het dialoogvenster **Productlijstconfiguratie selecteren**.

| Type                       | Beschrijving | Gebruik | Paginacontext | Specifieke context | Persoonlijke instellingen |
|----------------------------|-------------|-------|--------------|------------------|-----------------|
| Producten per categorie       | Een lijst met producten die tot een bepaalde categorie behoren. Deze categorie wordt bepaald door de paginacontext of de context die de auteur heeft opgegeven. | Dit type lijst kan worden gebruikt op elke pagina (bijvoorbeeld een startpagina, categoriepagina, marketingpagina of pagina met productdetails \[PDP\]) om een specifieke categorie producten te promoten. | Categorie uit de paginacontext, indien beschikbaar (bijvoorbeeld een categoriepagina) | De auteur kan een specifieke categorie als context voor de lijst opgeven. | Niet van toepassing |
| Verwante producten           | Een lijst met producten die door een verkoopmanager in Commerce zijn geconfigureerd als gerelateerde producten voor het relatietype. | Dit type lijst wordt voornamelijk gebruikt op PDP's, maar kan op elke pagina worden gebruikt als een bovenliggend product wordt gebruikt. | Product van de pagina, relatietype (verplicht) | Het product kan worden geselecteerd in de kiezer en het relatietype wordt gebruikt. | Niet van toepassing |
| Gecureerd                    | Een aangepaste lijst die in Commerce is gemaakt door verkoopadviseurs en editors. | Verrijkte categoriepagina, startpagina, uitcheck-, winkelwagen- en productpagina's | Niet van toepassing | Niet van toepassing | Niet van toepassing |
| Algoritme                | <ul><li>**Nieuw**: een lijst met de nieuwste producten die zijn gesorteerd in afzetkanalen en catalogi.</li><li>**Best verkocht**: een lijst met producten die worden gerangschikt op het hoogste verkoopaantal.</li><li>**Trending**: een lijst met de best presterende producten gedurende een bepaalde periode.</li></ul> | Startpagina, verrijkte categoriepagina, en uitcheck- en winkelwagenpagina's | Categorie uit de paginacontext (bijvoorbeeld een categoriepagina) | De categorie die door de site-auteur wordt bepaald | Ondersteund |
| Vaak samen gekocht | Een lijst die gebruikmaakt van machine learning voor het analyseren van inkooppatronen van consumenten en het aanbevelen van verwante artikelen die vaak samen met een bepaald product worden gekocht. | Dit type lijst is alleen van toepassing op de winkelwagenpagina. | Winkelwagen | Niet van toepassing | Ondersteund |
| Wat mensen ook leuk vinden           | Een lijst die gebruikmaakt van machine learning voor het analyseren van inkooppatronen van consumenten en het aanbevelen van artikelen die samenhangen met een bepaald product. | Dit type lijst wordt gebruikt op PDP's om producten weer te geven die andere klanten hebben gekocht. | Productcontext van de pagina | Het product dat door de site-auteur wordt geleverd | Ondersteund |
| Selectie voor u              | Een lijst die gebruikmaakt van machine learning om de voorkeuren van de klant te bepalen. | Dit type lijst kan op elke pagina worden gebruikt. | Niet van toepassing| Niet van toepassing | Ondersteund | 

## <a name="additional-resources"></a>Aanvullende bronnen

[Overzicht van modulebibliotheek](starter-kit-overview.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsrijke-blokmodule](add-content-rich-block.md)

[Containermodule](add-container-module.md)

[Module met vakje voor kopen](add-buy-box.md)

[Overzicht productaanbevelingen](product-recommendations.md)

[Module voor snelle weergave](quick-view-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
