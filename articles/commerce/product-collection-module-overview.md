---
title: Productverzamelingsmodules
description: In dit onderwerp vindt u een overzicht van de productverzamelingmodules in Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 44f78b55b8e67b7358be75aa63c40a0147507e26
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785462"
---
# <a name="product-collection-modules"></a>Productverzamelingsmodules  

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

In dit onderwerp vindt u een overzicht van de productverzamelingmodules in Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Overzicht

Productdetectie is een primair hulpmiddel dat detailhandelaren gebruiken om hun klanten op een e-commerce-website te benaderen. Modules voor productverzamelingen helpen u om aantrekkelijke winkelervaringen samen te stellen door een intuïtieve visuele interface te bieden die kan worden gebruikt om snel productverzamelingen te ontwerpen.

Modules voor productverzamelingen vertegenwoordigen fysieke producten en services op de website. Een productverzamelingsmodule wordt meestal gekoppeld aan een detailpagina waar klanten een product of service kunnen kopen of meer informatie kunnen bekijken. 

De bronnen voor productverzamelingen kunnen lijsten van drie typen zijn:

- Redactionele lijsten van producten die handmatig in Dynamics 365 Retail zijn gedefinieerd als verwante producten voor een product of productlijsten
- Algoritmelijsten, zoals lijsten van nieuwe, best verkochte en trending producten
- Aanbevelingslijsten die zijn gebaseerd op machine learning

In de volgende afbeelding ziet u de verschillende typen productverzamelingen die worden gebruikt op een e-commerce-site.

![Voorbeeld van de verschillende typen productverzamelingen op een e-commerce-site](./media/ProductCollectionsAcrossTheSiteUseProductPlacement.png)

> [!NOTE]
> Gebruik productverzamelingsmodules altijd om een groep producten van een vergelijkbaar type of thema weer te geven.

## <a name="product-collection-modules-and-types"></a>Productverzamelingsmodules en typen

In de volgende tabel worden diverse typen productverzamelingsmodules beschreven in Dynamics 365 Commerce.

| Productverzamelingsmodule  | Type | Beschrijving |
|----------------------------|------|-------------|
| Zoeken in categorie            | Redactionele informatie | Dit type productverzamelingsmodule gebruikt de hiërarchie van navigatiecategorieën die de detailhandelaar voor een afzetkanaal heeft gemaakt om een zoekstroom weer te geven voor producten die in een specifieke sitecategorie worden aangeboden. |
| Zoekresultaten             | Zoekquery | In dit type productverzamelingsmodule wordt een lijst met producten weergegeven die het meest overeenkomen met de zoekquery die de klant heeft ingevoerd. |
| Verwante producten           | Redactionele informatie | In dit type productverzamelingsmodule wordt een lijst met producten weergegeven die door een merchandisingmanager zijn geconfigureerd als gerelateerde producten in Retail, voor het relatietype dat de auteur heeft geselecteerd. |
| Gecureerde lijsten met producten      | Redactionele informatie | In dit type productverzamelingsmodule worden aangepaste lijsten weergegeven die door verkoopadviseurs en editors in Retail zijn gemaakt. |
| Nieuw                        | Algoritme | In dit type productverzamelingsmodule wordt een lijst weergegeven met de nieuwste producten die zijn gesorteerd in afzetkanalen en catalogi. |
| Meest verkocht               | Algoritme | In dit type productverzamelingsmodule wordt een lijst met producten weergegeven die worden gerangschikt op het hoogste verkoopaantal. |
| Trending                   | Algoritme | In dit type productverzamelingsmodule wordt een lijst weergegeven met de producten met de hoogste prestaties voor een bepaalde periode. |
| Vaak samen gekocht | Kunstmatige intelligentie/Machine learning | Dit type productverzamelingsmodule maakt gebruik van machine learning voor het analyseren van inkooppatronen van consumenten en het aanbevelen van verwante artikelen die vaak samen met een bepaald product worden gekocht. |
| Wat mensen ook leuk vinden           | Kunstmatige intelligentie/Machine learning | Dit type productverzamelingsmodule maakt gebruik van machine learning voor het analyseren van inkooppatronen van consumenten en het aanbevelen van artikelen die samenhangen met een bepaald product. |

## <a name="add-a-product-collection-module-to-a-category-page"></a>Een productverzamelingsmodule aan een categoriepagina toevoegen

Voer deze stappen uit om een productverzamelingsmodule aan een categoriepagina toe te voegen.

1. Ga in Dynamics 365 Commerce naar uw site en maak een pagina die dezelfde sjabloon gebruikt als de standaardpagina voor categorieën.
1. Selecteer in het paginaoverzicht het vak **Sub-voettekst** de knop met het weglatingsteken (**...**) en vervolgens **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de optie **Container** en selecteer vervolgens **OK**.
1. Selecteer in de containermodule de knop met het weglatingsteken en selecteer **Module toevoegen**.
1. Selecteer in het dialoogvenster **Module toevoegen** de optie **Productverzameling** en selecteer vervolgens **OK**.
1. Configureer instellingen door een geschikte gegevensbron en invoer voor de productverzameling te selecteren.
1. Selecteer **Een productlijst toevoegen** in het deelvenster met eigenschappen voor de productverzamelingsmodule.
1. Selecteer in het dialoogvenster **Productlijstconfiguratie selecteren** het type lijst, voer het aantal artikelen in en selecteer eventuele andere opties die beschikbaar zijn voor het lijsttype. Meer informatie over lijsttypen vindt u in de tabel hieronder. 
1. Selecteer **OK**.
1. Sla de pagina op en check deze in.

In de volgende tabel worden de lijsttypen weergegeven die beschikbaar zijn voor het dialoogvenster **Productlijstconfiguratie selecteren**.
   
| Type                       | Beschrijving | Algemene praktijk | Context die kan worden afgeleid van de paginacontext | Context waarmee de auteur de paginacontext kan overschrijven |
|----------------------------|-------------|------------------|-------------------------------------|-----------------------------------------------|
| Producten per categorie       | Een lijst met producten die tot een bepaalde categorie behoren. Deze categorie wordt bepaald door de paginacontext of de context die de auteur heeft opgegeven. | Verrijkte categoriepagina, startpagina, uitcheck-, winkelwagen- en productpagina's | Categorie | Categorie bepaald door auteur |
| Verwante producten           | Een lijst met producten die door een verkoopmanager in Retail zijn geconfigureerd als gerelateerde producten voor het relatietype. | Uitcheck-, winkelwagen- en productpagina's, voorkeurslijstpagina en klantaccountpagina | Product, relatietype (verplicht)  | Product, relatietype |
| Gecureerd                    | Een aangepaste lijst die in Retail is gemaakt door verkoopadviseurs en editors. | Verrijkte categoriepagina, startpagina, uitcheck-, winkelwagen- en productpagina's | Niet van toepassing | Lijstkiezer |
| Algoritme                | <ul><li>**Nieuw**: een lijst met de nieuwste producten die zijn gesorteerd in afzetkanalen en catalogi.</li><li>**Best verkocht**: een lijst met producten die worden gerangschikt op het hoogste verkoopaantal.</li><li>**Trending**: een lijst met de best presterende producten gedurende een bepaalde periode.</li></ul> | Startpagina, verrijkte categoriepagina, en uitcheck- en winkelwagenpagina's | Categorie | Categorie bepaald door auteur |
| Vaak samen gekocht | Een lijst die gebruikmaakt van machine learning voor het analyseren van inkooppatronen van consumenten en het aanbevelen van verwante artikelen die vaak samen met een bepaald product worden gekocht. | Productpagina's, en uitcheck- en winkelwagenpagina's | Product, winkelwagen | Winkelwagen opnemen |
| Wat mensen ook leuk vinden           | Een lijst die gebruikmaakt van machine learning voor het analyseren van inkooppatronen van consumenten en het aanbevelen van artikelen die samenhangen met een bepaald product. | Productpagina's, en uitcheck- en winkelwagenpagina's | Product, winkelwagen | Niet van toepassing |

## <a name="additional-resources"></a>Aanvullende resources

[Overzicht starterskit](starter-kit-overview.md)

[Carrouselmodule](add-carousel.md)

[Inhoudsrijke-blokmodule](add-content-rich-block.md)

[Module voor het plaatsen van inhoud](add-content-placement-modules.md)

[Module Container](add-container-module.md)

[Koopvakmodule](add-buy-box.md)

