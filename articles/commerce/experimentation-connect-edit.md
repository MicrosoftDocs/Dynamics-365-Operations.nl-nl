---
title: Een experiment verbinden en variaties bewerken
description: In dit artikel wordt beschreven hoe u een experiment in een service van derden verbindt met Dynamics 365 Commerce en hoe u variaties voor het experiment bewerkt.
author: sushma-rao
ms.date: 06/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.openlocfilehash: dcdbd61976402ddd719ece184a86692fbc7c628d
ms.sourcegitcommit: ddcb62bb5fbf26a1178c2bb1aec45a3d2362339e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/07/2022
ms.locfileid: "8942817"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Een experiment verbinden en variaties bewerken

In dit artikel wordt beschreven hoe u uw experiment in Commerce verbindt en hoe u wijzigingen in uw variaties kunt aanpassen zodat u ze kunt afstemmen met uw hypothese. 

In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke artikelen behandeld.

[ ![Traject van gebruiker voor experimenten - verbinden en bewerken.](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Nadat u [uw experiment hebt ingesteld](experimentation-setup.md) in een service van derden, verbindt u het experiment in Dynamics 365 Commerce en bewerkt u de experimentvariaties.

## <a name="connect-your-experiment"></a>Uw experiment verbinden
Als u uw experiment wilt verbinden, start u de wizard **Experiment verbinden**. De wizard leidt u door de stappen die nodig zijn om uw experiment te verbinden. Wanneer u de wizard voltooit, wordt uw experiment verbonden en worden variaties gemaakt en kunnen ze worden bewerkt.

Voer de volgende stappen uit om aan de slag te gaan met uw experiment in Commerce Site Builder.

1. Selecteer **Experimenten** in het linkernavigatievenster en om de wizard **Experiment verbinden** te starten en selecteer vervolgens **Verbinden**. U kunt de wizard ook openen vanaf een pagina of fragmenteditor door deze te bewerken en **Experiment verbinden** te selecteren op de opdrachtbalk.

    > [!NOTE]
    > - Een pagina kan slechts met één experiment tegelijk worden verbonden. Als u een pagina wilt verbinden met een ander experiment, verwijdert u eerst het experiment waarmee de pagina momenteel is verbonden.
    > - U kunt alleen experimenten uitvoeren op pagina's met een aangepaste indeling. Als uw pagina een vooraf ingestelde indeling heeft, zet u deze eerst om in een aangepaste indeling. U kunt dit doen door naar de pagina te gaan en op de opdrachtbalk **Converteren naar aangepaste indeling** te selecteren. Zie [Vooraf ingestelde en aangepaste indelingen](templates-layouts-overview.md#preset-and-custom-layouts) voor meer informatie over indelingen. 

1. Als u verbinding wilt maken met een experiment via het tabblad **Experimenten** in het linkernavigatievenster, selecteert u de naam van de experiment in de lijst die verschijnt.
1. Selecteer de pagina of het fragment waarop u het experiment wilt uitvoeren.
1. In de laatste stap van de wizard selecteert u de optie **Variaties genereren en wizard afsluiten**. Er worden variaties voor het experiment gemaakt. 

> [!NOTE]
> Als u wilt plannen wanneer uw experiment wordt gepubliceerd naar uw live site, moet u ervoor zorgen dat de inhoud die u aan het experiment wilt koppelen, beschikbaar is in een publicatiegroep *voordat* u het experiment verbindt. Zie [Werken met publicatiegroepen](publish-groups.md) voor meer informatie over publicatiegroepen.

## <a name="edit-your-variations"></a>Uw variaties bewerken

Wanneer u de wizard **Experiment verbinden** afsluit, worden variaties voor u gemaakt. Volg de onderstaande stappen om de variaties zo te bewerken dat deze de keuzes weergeven die u in de experimenthypothese moet controleren.

1. Gebruik in de editorweergave het vervolgkeuzemenu voor variaties onder de opdrachtbalk om elke variatie te bewerken op basis van uw oorspronkelijke hypothese. U kunt ook een besturingselement of basisvariatie instellen door een van de variaties ongewijzigd te laten.
1. Selecteer de module waarop u een experiment wilt uitvoeren, selecteer het weglatingsteken (...) en selecteer vervolgens **Toevoegen aan experiment**.

> [!NOTE]
> U kunt ook een besturingselement of basisvariatie instellen door een van de variaties ongewijzigd te laten.

## <a name="previous-step"></a>Vorige stap
[Een experiment instellen](experimentation-setup.md) 


## <a name="next-step"></a>Volgende stap
[Preview van een experiment weergeven en een experiment publiceren](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
