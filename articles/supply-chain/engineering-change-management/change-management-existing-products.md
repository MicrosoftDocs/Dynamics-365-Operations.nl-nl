---
title: Wijzigingsbeheer voor bestaande producten inschakelen
description: In dit onderwerp wordt uitgelegd hoe u wijzigingsbeheer voor bestaande producten kunt inschakelen. Het beschrijft ook gevallen waarin het vermogen om wijzigingsbeheer in te stellen beperkt is.
author: t-benebo
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-05-02
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: be7b17c1049f60379764c5424422ff1ac6ee1770
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830095"
---
# <a name="enable-change-management-on-existing-products"></a>Wijzigingsbeheer voor bestaande producten inschakelen

[!include [banner](../../includes/banner.md)]

In dit onderwerp wordt uitgelegd hoe u wijzigingsbeheer voor bestaande producten kunt inschakelen. Het beschrijft ook gevallen waarin het vermogen om wijzigingsbeheer in te stellen beperkt is.

Wanneer u wijzigingsbeheer inschakelt voor een bestaand product, kunt u versies van dat product maken en wijzigingen traceren die in het product zijn aangebracht gedurende de levensduur. U kunt deze wijzigingen dan bijhouden door wijzigingsorders te gebruiken. Als u wijzigingsbeheer wilt inschakelen, moet u de relevante producten converteren naar *technische artikelen* (ook wel technische producten genoemd). Technische producten zijn producten waarvoor versiebeheer wordt uitgevoerd en die worden beheerd via wijzigingsbeheer. Er is een wizard beschikbaar die u begeleidt bij het conversieproces.

## <a name="turn-on-the-feature-in-your-system"></a>De functie inschakelen in uw systeem

Voer de volgende taken uit om deze mogelijkheid te gebruiken:

1. Schakel technisch wijzigingsbeheer en de bijbehorende configuratiesleutel in zoals beschreven in [Overzicht van technisch wijzigingsbeheer](product-engineering-overview.md).
1. Schakel de functie *Wijzigingsbeheer voor bestaande producten inschakelen* in functiebeheer in. Zie [Overzicht van functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) voor meer informatie.

## <a name="restrictions-and-limitations"></a>Beperkingen en limieten

Niet alle producttypen kunnen naar alle andere typen worden geconverteerd. De volgende beperkingen gelden:

- Wanneer u een product converteert naar een technisch product, blijft het een *product*. Het wordt geen *productmodel*.
- Wanneer u een productmodel met een specifieke set dimensies converteert, blijven die dimensies na de wijziging behouden. Als u bijvoorbeeld een productmodel met de groottedimensie converteert, blijft de groottedimensie behouden.

Als u dus een verschillend product hebt, kunt u dit alleen wijzigen in een technisch product dat de productdimensie niet bijhoudt in transacties (dat wil zeggen de versiedimensie wordt niet gebruikt). Zie de resterende secties voor meer informatie over deze kwesties.

## <a name="prepare-for-conversion-by-creating-all-required-engineering-product-categories"></a>Voorbereiden op conversie door alle vereiste categorieën voor technische producten te maken

Er moet een *categorie voor technische producten* worden toegewezen aan elk technisch product. U doet deze toewijzing wanneer u de wizard **Converteren naar technisch product** uitvoert. Categorieën voor technische producten moeten bestaan voor alle relevante standaardproducten *voordat* u deze producten kunt converteren.

De categorie voor technische producten vormt een basis voor het maken van een technisch product en legt een set standaardwaarden en -beleidsregels vast. De categorie voor technische producten moet overeenkomen met het product dat u eraan toewijst. Het producttype en de dimensiegroep moeten bijvoorbeeld overeenkomen met het product en de bijbehorende categorie voor technische producten. Zie [Technische versies en categorieën van technische producten](engineering-versions-product-category.md) voor meer informatie.

> [!IMPORTANT]
> Met de wizard **Converteren naar technisch product** kunnen alleen producten worden geconverteerd naar technische producten waarbij de versie niet wordt bijgehouden in transacties. Daarom moet de optie **Versie in transacties traceren** worden ingesteld op *Nee* voor categorieën voor technische producten die u maakt om bestaande producten te converteren.

Zie [Technische versies en categorieën van technische producten](engineering-versions-product-category.md) voor meer informatie over het maken van categorieën voor technische producten.

## <a name="run-the-convert-to-engineering-product-wizard"></a>De wizard Converteren naar technisch product uitvoeren

Met de wizard **Conversie naar technisch product** kunt u een of meer bestaande producten converteren naar technische producten. De wizard converteert de producten naar technische producten (versieproducten) waarbij de versie niet wordt bijgehouden in transacties (dat wil zeggen de versiedimensie wordt niet gebruikt). Nadat de conversie is voltooid, kunt u de producten beheren via Beheer voor technische wijzigingen.

De conversie is permanent. U kunt deze dus niet later omkeren. 

Elk geconverteerd technisch product wordt nog steeds vrijgegeven in dezelfde bedrijven waarin het oorspronkelijke product is vrijgegeven. De technische stuklijst en routes worden echter niet automatisch vrijgegeven voor die bedrijven.

Voer de volgende stappen uit om de wizard **Converteren naar technisch product** uit te voeren en een product naar een technisch product te converteren.

1. Ga naar **Productgegevensbeheer \> Producten \> Vrijgegeven producten**.
1. Schakel in het raster het selectievakje in voor elk product dat u wilt converteren.
1. Selecteer in het actievenster op het tabblad **Technicus** in de groep **Beheer voor technische wijzigingen** de optie **Converteren naar technisch product** om de wizard te openen.
1. De eerste pagina van de wizard is de **welkomstpagina**. Als u nog niet op de hoogte bent van het conversieproces, leest u de informatie op deze pagina zorgvuldig. Wanneer u klaar bent om door te gaan, selecteert u **Volgende**.
1. Op de pagina **Details selecteren voor de producten die moeten worden geconverteerd** wordt elk product weergegeven dat u hebt geselecteerd voordat u de wizard hebt geopend. Controleer de lijst. Gebruik de knoppen **Nieuw** en **Verwijderen** op de werkbalk om naar behoefte producten toe te voegen en te verwijderen.
1. Gebruik de volgende velden boven aan het raster om standaardwaarden toe te wijzen aan elk product dat wordt weergegeven. (U kunt deze waarden voor afzonderlijke producten wijzigen nadat de conversie is voltooid.) Standaardwaarden worden niet toegewezen aan producten aan welke al een relevante waarde is toegewezen.

    - **Standaardcategorie voor technische producten** – Selecteer een eerste categorie voor technische producten die u aan elk weergegeven product wilt toewijzen. De categorie die u selecteert, wordt alleen toegepast op producten die compatibel zijn met de categorie.
    - **Standaardversie** – Voer de eerste productversie in die aan elk vermeld product moet worden toegewezen. Elk technisch product heeft minimaal één technische versie.
    - **Standaardstatus voor de levenscyclus** – Selecteer de eerste status voor de levenscyclus die u aan elk vermeld product wilt toewijzen.
    - **Huidige stuklijst maakt deel uit van het technische product** – Schakel dit selectievakje in als de huidige stuklijst voor elk vermeld product als stuklijst voor het technische product moet worden gebruikt.

    Zie de volgende stap voor meer informatie over productinstellingen.

1. Controleer elk product in het raster en evalueer hoe goed de standaardwaarden die u hebt toegewezen, hierop van toepassing zijn. Controleer voor elke rij de volgende informatie en stel de relevante velden in:

    - **Productnummer** – het productnummer.
    - **Productnaam** – De naam van het product.
    - **Technische categorie** – Selecteer de categorie technische producten waarbij het product moet horen nadat het is geconverteerd. Er moet al een geschikte categorie bestaan voor elk product, zoals is uitgelegd in de vorige sectie van dit onderwerp. U moet aan elk product een categorie toewijzen.
    - **Versie** – Voer de productversie in die aan het product moet worden toegewezen nadat het is geconverteerd. U kunt bijvoorbeeld een nummer selecteren dat past in de nummerreeks die uw categorie al gebruikt. Voor elke technische versie worden de technisch relevante gegevens opgeslagen die specifiek zijn voor die versie. Zie [Technische versies en categorieën van technische producten](engineering-versions-product-category.md) voor meer informatie.
    - **Status van productlevenscyclus** – selecteer de status van de productlevenscyclus waarin het product moet worden omgezet nadat het is geconverteerd. Met de status van de productlevenscyclus kunt u bepalen welke transacties zijn toegestaan voor een bepaalde technische versie. Zie voor meer informatie [Levenscyclusstatussen en transacties van producten](product-lifecycle-state-transactions.md).
    - **Heeft stuklijst** – Een ingeschakeld selectievakje geeft aan dat het product een stuklijst heeft. De instelling van dit selectievakje kan u helpen om te beslissen hoe u het selectievakje **Huidige stuklijst maakt deel uit van het technische product** moet instellen.
    - **Huidige stuklijst maakt deel uit van het technische product** – Schakel dit selectievakje in als de huidige stuklijst van het product als stuklijst voor het technische product moet worden gebruikt. De stuklijst wordt vervolgens beheerd door Beheer voor technische wijzigingen. Als het product geen stuklijst heeft of als u liever later handmatig een stuklijst maakt voor het geconverteerde product, schakelt u dit selectievakje uit.
    - **Heeft fouten** – Een ingeschakeld selectievakje geeft aan dat de productinstellingen een of meer fouten bevatten. Het producttype of de dimensiegroep komt bijvoorbeeld mogelijk niet overeen in de categorie. Producten met fouten worden overgeslagen en niet geconverteerd.

1. Als u klaar bent, selecteert u **Valideren** op de werkbalk om de productinstellingen te valideren. Voor elke rij wordt het selectievakje **Heeft fouten** bijgewerkt om de status van het product aan te geven. Pas de waarden aan totdat de instelling van elk product geen fouten bevat.
1. Wanneer alle producten juist zijn ingesteld, selecteert u **Volgende** om door te gaan.
1. Op de pagina **Selectie bevestigen** wordt het aantal producten weergegeven dat geen fouten bevat en dus gereed is voor conversie. Het geeft ook het aantal producten weer dat wordt overgeslagen vanwege fouten. Als u de conversie als batchtaak wilt uitvoeren, stelt u de optie **Uitvoeren in batch** in op *Ja*.
1. Selecteer **Voltooien** om de instellingen toe te passen en de producten te converteren naar technische producten.

> [!NOTE]
> Als uw systeem zo is ingesteld dat producten handmatig worden geaccepteerd voordat ze worden vrijgegeven, moet u elk geconverteerd product accepteren via de pagina **Openstaande productreleases** in de juiste bedrijven. Zie [Het product controleren en accepteren voordat u het in het lokale bedrijf vrijgeeft](engineering-scenarios.md#accept) voor meer informatie.
