---
title: Een e-commercesite kopiëren
description: In dit artikel wordt beschreven hoe u een bestaande e-commercesite binnen of tussen e-commerceomgevingen kopieert in Microsoft Dynamics 365 Commerce Site Builder.
author: psimolin
ms.date: 06/03/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: cb53a76b2ebe5b511bf5009727f20f20755e5720
ms.sourcegitcommit: 13c7a1cc4c90417e3e88db59b7d2165b3c40a56c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2022
ms.locfileid: "8935739"
---
# <a name="copy-an-e-commerce-site"></a>Een e-commercesite kopiëren

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u een bestaande e-commercesite binnen of tussen e-commerceomgevingen kopieert in Microsoft Dynamics 365 Commerce Site Builder.

Dynamics 365 Commerce ondersteunt het kopiëren of maken van sites als een selfservicebewerking in Commerce Site Builder. Sites kunnen in één e-commerceomgeving of tussen twee e-commerceomgevingen worden gekopieerd. De gebruiker die de sitekopieerbewerking start, moet een tenantbeheerder zijn in zowel de bron- als doelomgevingen voor e-commerce.

Met de sitekopieerbewerking wordt alle e-commerce-inhoud van de bronsite gekopieerd. Deze inhoud omvat pagina's, fragmenten, sjablonen, URL's en activa. Voordat u een nieuwe site kunt gebruiken, moet u deze eerst initialiseren via het first run experience-proces (FRE). Kanalen kunnen in Site Builder worden toegewezen en beheerd via **Site-instellingen \> Kanalen**.

De duur van de sitekopieerbewerking is voornamelijk afhankelijk van het aantal activa op de bronsite. Voor uitzonderlijk grote locaties is het raadzaam om in plaats daarvan de kopieerbewerking voor de omgeving te gebruiken. (Deze bewerking wordt ook wel de gegevensoverdracht genoemd).

> [!NOTE]
> - De bronsite is alleen-lezen voor de duur van de sitekopieerbewerking.
> - Alleen gepubliceerde versies van documenten worden gekopieerd. Als er geen versies zijn gepubliceerd, worden alleen de laatste versies gekopieerd.
> - De versiehistorie voor inhoud is niet beschikbaar op de doelsite.

## <a name="copy-a-site-within-an-e-commerce-environment"></a>Een site in een e-commerceomgeving kopiëren

Volg deze stappen om een site in een e-commerceomgeving te kopiëren.

1. Meld u aan bij Site Builder voor de omgeving waarin u de kopieerbewerking wilt uitvoeren.
1. Open de lijstweergave met sites door **Sites wisselen** te selecteren in de rechterbovenhoek en vervolgens **Sites beheren**.
1. Zoek de site die u wilt kopiëren of klonen en selecteer de site met het selectievakje naast de sitenaam.
1. Selecteer **Site kopiëren** op de opdrachtbalk.
1. Voer in het fly-outmenu **Site kopiëren** in het veld **Nieuwe sitenaam** een naam in voor de nieuwe site. De nieuwe sitenaam moet uniek zijn in de e-commerceomgeving. De velden **Brontenant** en **Bronsite** worden automatisch ingesteld op de informatie voor de huidige tenants en de geselecteerde site.
1. Selecteer **Kopie maken**.

Nadat de informatie is gevalideerd, wordt met een melding aangegeven dat er een nieuwe sitekopieertaak is gemaakt. U kunt de voortgang van de taak controleren in het [rechterdeelvenster van de pagina **Tenanttaken**](#monitor-the-site-copy-operation). Wanneer de kopieerbewerking is voltooid, wordt de nieuwe locatie weergegeven in de sitelijstweergave.

In de volgende afbeelding ziet u een voorbeeld van een fly-outmenu **Site kopiëren** in Commerce Site Builder.

![Het fly-outmenu Site kopiëren in Site Builder.](media/site-copy_1.png)

## <a name="copy-a-site-between-two-e-commerce-environments"></a>Een site kopiëren tussen e-commerceomgevingen

Volg deze stappen om een site tussen twee e-commerceomgevingen te kopiëren.

1. Meld u aan bij Site Builder voor uw doelomgeving.
1. Selecteer **Site kopiëren** op de opdrachtbalk.
1. Voer in het fly-outmenu **Site kopiëren** in het veld **Nieuwe sitenaam** een naam in voor de nieuwe site. De nieuwe sitenaam moet uniek zijn in de e-commerceomgeving.
1. Selecteer in het veld **Brontenant** de naam van de brontenant.
1. Selecteer in het veld **Bronite** de bronsite.
1. Selecteer **Kopie maken**.

> [!NOTE]
> Tenantbeheerdersmachtigingen zijn vereist voor zowel de bron- als de doelomgevingen voor e-commerce.

Nadat de informatie is gevalideerd, wordt met een melding aangegeven dat er een nieuwe sitekopieertaak is gemaakt. U kunt de voortgang van de taak controleren in het [rechterdeelvenster van de pagina **Tenanttaken**](#monitor-the-site-copy-operation). Wanneer de kopieerbewerking is voltooid, wordt de nieuwe locatie weergegeven in de sitelijstweergave.

## <a name="map-channels-during-the-site-copy-operation-optional"></a>Kanalen toewijzen tijdens de bewerking voor het kopiëren van sites (optioneel)

Bronkanalen en landinstellingen kunnen als onderdeel van de bewerking voor het kopiëren van de site worden toegewezen aan doelkanalen en -landinstellingen. Als de kanaaltoewijzing wordt uitgevoerd als onderdeel van de bewerking voor het kopiëren van de site, is het niet nodig de site te initialiseren met behulp van het FRE-proces en de kanalen in site-instellingen te configureren. 

Volg deze stappen om alle kanalen en landinstellingen in de huidige staat (1-op-1) in Site Builder toe te wijzen.

1. Open de lijstweergave met sites door **Sites wisselen** te selecteren in de rechterbovenhoek en vervolgens **Sites beheren**.
1. Zoek de site die u wilt kopiëren of klonen en selecteer de site met het selectievakje naast de sitenaam.
1. Selecteer **Site kopiëren** op de opdrachtbalk.
1. Voer in het fly-outmenu **Site kopiëren** waarden in voor **Nieuwe sitenaam**, **Brontenant** en **Bronsite** (als deze nog niet aanwezig is).
1. Selecteer **Kanaaltoewijzingen toevoegen**.
1. Selecteer **Bronkanaal** in het fly-outmenu **Sitekanalen en landinstellingen configureren** en selecteer vervolgens het bronkanaal.  
1. Selecteer **Doelkanaal** en selecteer vervolgens hetzelfde kanaal als het bronkanaal. 
1. Selecteer **Een landinstelling toevoegen**.
1. Selecteer **Landinstelling voor bron** en selecteer vervolgens de landinstelling voor de bron.
1. Selecteer **Landinstelling van bestemming** en selecteer vervolgens dezelfde landinstelling als voor de bron. 
1. Voer voor **URL-pad** een uniek URL-pad in dat momenteel niet wordt gebruikt in de doelomgeving.
1. Herhaal stap 8-11 voor elke landinstellingen die u voor het kanaal wilt toewijzen.
1. Selecteer **Toepassing**.
1. Herhaal stap 6-11 voor elk bronkanaal.
1. Selecteer **Sluiten**.
1. Controleer de configuratie op nauwkeurigheid en selecteer vervolgens **Site kopiëren**.

> [!NOTE]
> Alle bronkanalen en -landinstellingen moeten worden toegewezen en kunnen slechts één keer worden toegewezen.

## <a name="monitor-the-site-copy-operation"></a>De sitekopieerbewerking controleren

Als u de voortgang van de sitekopieerbewerking wilt controleren, gaat u als volgt te werk.

1. Meld u aan bij Site Builder voor uw doelomgeving.
1. Selecteer **Tenanttaken** in het linkerdeelvenster.
1. Zoek en selecteer op de pagina **Tenanttaken** de kopieertaak voor de site in de lijst. Aan de rechterkant ziet u een deelvenster met de status en details van de geselecteerde taak.

U kunt een taak annuleren die de status **In uitvoering** heeft. Selecteer de taak in de lijst en selecteer vervolgens **Annuleren** op de opdrachtbalk.

U kunt een taak met de status **Mislukt** of **Voltooid met fouten** opnieuw proberen. Selecteer de taak in de lijst en selecteer vervolgens **Opnieuw proberen** op de opdrachtbalk.

> [!NOTE]
> De verwerking van videobestanden kan doorgaan nadat een sitekopieerbewerking is voltooid.

In de volgende afbeelding ziet u een voorbeeld van het rechterdeelvenster van de pagina **Tenanttaken** in Site Builder.

![Taakdetails in het rechterdeelvenster van de pagina Tenanttaken in Site Builder.](media/site-copy_2.png)

## <a name="initialize-a-new-site-by-using-the-fre-process"></a>Een nieuwe site initialiseren met het FRE-proces

Voordat u de nieuwe site kunt gebruiken, moet u deze eerst initialiseren via het first run experience-proces (FRE).

Volg deze stappen om een nieuwe site te initialiseren met het FRE-proces.

1. Meld u aan bij Site Builder voor de nieuwe site.
1. Open de lijstweergave met sites door **Sites wisselen** te selecteren in de rechterbovenhoek en vervolgens **Sites beheren**.
1. Zoek en selecteer de nieuwe site die u wilt initialiseren.
1. Selecteer een domein in het dialoogvenster **Uw site instellen** in het veld **Een domein selecteren**. Alle domeinen die aan de e-commerceomgeving zijn gekoppeld tijdens de initialisatie, kunnen worden geselecteerd.
1. Selecteer in het veld **Selecteer een standaardkanaal** het gekoppelde online winkelkanaal. Het geselecteerde kanaal biedt assortimenten en andere informatie die is opgeslagen in Commerce Headquarters.
1. Selecteer in het veld **Een standaardtaal selecteren** de standaard ontwerptaal. Alle talen die zijn geconfigureerd voor het geselecteerde online winkelkanaal, zijn beschikbaar voor selectie.
1. In het veld **Pad** bestaat de waarde uit het basisdomein en een optioneel URL-pad dat u kunt invoeren. U kunt het URL-pad leeg laten als het kanaal wordt gebruikt via de domeinbasis of als u deze informatie later in de weergave van de kanaalconfiguratie in Site Builder wilt invoeren. Het sitepad moet uniek zijn in de e-commerceomgeving.
1. Selecteer **OK**. De site wordt geïnitialiseerd met de door u geleverde informatie en u gaat naar de sitebeheerweergave.

In de volgende afbeelding ziet u een voorbeeld van het dialoogvenster **Uw site instellen** in Commerce Site Builder.

![Het dialoogvenster Uw site instellen in Site Builder.](media/site-copy_3.png)

## <a name="additional-resources"></a>Aanvullende bronnen

[Uw domeinnaam configureren](configure-your-domain-name.md)

[Een nieuwe e-commerce-tenant implementeren](deploy-ecommerce-site.md)

[Een Dynamics 365 Commerce-site koppelen aan een online kanaal](associate-site-online-store.md)

[robots.txt-bestanden beheren](manage-robots-txt-files.md)

[URL-omleidingen in bulk uploaden](upload-bulk-redirects.md)

[Een B2C-tenant instellen in Commerce](set-up-b2c-tenant.md)

[Aangepaste pagina's voor gebruikersaanmeldingen instellen](custom-pages-user-logins.md)

[Meerdere B2C-tenants configureren in een Commerce-omgeving](configure-multi-b2c-tenants.md)

[Ondersteuning voor een CDN (contentleveringsnetwerk) toevoegen](add-cdn-support.md)

[Detectie van winkels op basis van de locatie inschakelen](enable-store-detection.md)
