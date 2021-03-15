---
title: Een experiment verbinden en variaties bewerken
description: In dit onderwerp wordt beschreven hoe u een experiment in een service van derden verbindt met Dynamics 365 Commerce en hoe u variaties voor het experiment bewerkt.
author: sushma-rao
manager: AnnBe
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 2a33897d01dd98d446c2fb49e417abd9db9f403a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010019"
---
# <a name="connect-an-experiment-and-edit-variations"></a>Een experiment verbinden en variaties bewerken

In dit onderwerp wordt beschreven hoe u uw experiment in Commerce verbindt en hoe u wijzigingen in uw variaties kunt aanpassen zodat u ze kunt afstemmen met uw hypothese. 

In het volgende diagram ziet u alle stappen voor het instellen en uitvoeren van een experiment op een e-Commerce-website in Dynamics 365 Commerce. Extra stappen worden in afzonderlijke onderwerpen behandeld.

[ ![Traject van gebruiker voor experimenten - verbinden en bewerken](./media/experimentation_connect_edit.svg) ](./media/experimentation_connect_edit.svg#lightbox)

Nadat u [uw experiment hebt ingesteld](experimentation-setup.md) in een service van derden, verbindt u het experiment in Dynamics 365 Commerce en bewerkt u de experimentvariaties.

## <a name="planning-considerations"></a>Overwegingen bij het plannen

Voordat u uw experiment in Commerce verbindt, moet u enkele beslissingen nemen die van invloed zijn op de manier waarop uw inhoud door Commerce wordt beheerd.

### <a name="determine-the-scope-of-your-experiment"></a>Het bereik van uw experiment bepalen
Wanneer u een experiment verbindt, wordt u gevraagd het bereik van het experiment te definiëren. Experimenten worden gedefinieerd als een **gedeeltelijk** bereik of een **volledig** bereik.
- Kies **gedeeltelijk** als u een experiment wilt uitvoeren op een specifiek gedeelte van een pagina. Als u deze optie selecteert, moet u bepalen welke modules in het experiment worden opgenomen. Wijzigingen die worden aangebracht in delen van de standaardpagina of het fragment die niet zijn gerelateerd aan het experiment, worden automatisch gesynchroniseerd in verschillende variaties.
- Kies **volledig** als u een experiment wilt uitvoeren op een volledige pagina of in een volledig fragment. Er worden afzonderlijke kopieën van de standaardpagina of het standaardfragment gemaakt. U hoeft niet te selecteren welke modules in het experiment worden opgenomen, omdat het gehele bewerkingsoppervlak kan worden gewijzigd. U kunt modules naar behoefte toevoegen, verwijderen of opnieuw rangschikken. Als er echter wijzigingen zijn aangebracht in de standaardpagina of het standaardfragment waaraan het experiment is gekoppeld, moeten deze wijzigingen handmatig worden gesynchroniseerd in alle variaties.

<!-- not to editors, we're adding an image here to illustrate the difference. it will help.) -->

> [!NOTE]
> Als u uw experiment koppelt aan een pagina waarin een indeling wordt gebruikt, kunt u als bereik voor het experiment alleen **volledig** gebruiken.

### <a name="decide-if-you-want-to-schedule-when-your-experiment-is-published"></a>Bepaal of u wilt plannen wanneer uw experiment wordt gepubliceerd
Als u wilt plannen wanneer uw experiment wordt gepubliceerd naar uw live site, moet u ervoor zorgen dat de inhoud die u aan het experiment wilt koppelen, beschikbaar is in een publicatiegroep *voordat* u het experiment verbindt. 

Zie [Werken met publicatiegroepen](publish-groups.md) voor meer informatie over publicatiegroepen.


## <a name="connect-your-experiment"></a>Uw experiment verbinden
Als u uw experiment wilt verbinden, start u de wizard **Experiment verbinden**. De wizard leidt u door de stappen die nodig zijn om uw experiment te verbinden. Wanneer u de wizard voltooit, wordt uw experiment verbonden en worden variaties gemaakt en kunnen ze worden bewerkt.

Voer de volgende stappen uit om aan de slag te gaan met uw experiment in Commerce Site Builder.

1. Selecteer **Experimenten** in het linkernavigatievenster en om de wizard **Experiment verbinden** te starten en selecteer vervolgens **Verbinden**. U kunt de wizard ook openen vanaf een pagina of fragmenteditor door deze te bewerken en **Experiment verbinden** te selecteren op de opdrachtbalk.

    > [!NOTE]
    > Een pagina kan slechts met één experiment tegelijk worden verbonden. Als u een pagina wilt verbinden met een ander experiment, verwijdert u eerst het experiment waarmee de pagina momenteel is verbonden.

1. Kies de pagina of het fragment waarop u het experiment wilt uitvoeren.
1. Stel het experimentbereik in op **gedeeltelijk** of **volledig**, afhankelijk van de keuze die u hebt gemaakt in de sectie [Het bereik van uw experiment bepalen](#determine-the-scope-of-your-experiment).
    > [!NOTE]
    > De functievlag **Experimenten op pagina's of fragmenten** moet zijn ingeschakeld als u een experiment op een volledige pagina of in een volledig fragment wilt uitvoeren. Raadpleeg het onderwerp [Experimenten in Dynamics 365 Commerce](experimentation-overview.md) voor meer informatie.
    
1. In de laatste stap van de wizard selecteert u de optie **Variaties genereren en wizard afsluiten**. Er worden variaties voor het experiment gemaakt. 

## <a name="edit-your-variations"></a>Uw variaties bewerken
Wanneer u de wizard afsluit, worden er variaties voor u gemaakt. 

Vervolgens bewerkt u de variaties zodat deze de keuzes weergeven die u in de experimenthypothese moet controleren. Kies een van de volgende procedures die overeenkomen met het bereik dat u voor uw experiment hebt gekozen in de bovenstaande sectie [Het bereik van uw experiment bepalen](#determine-the-scope-of-your-experiment).

### <a name="edit-variations-for-experiments-with-partial-scope"></a>Variaties bewerken voor experimenten met een gedeeltelijk bereik
Voer de volgende stappen uit als u het bereik van uw experiment als **gedeeltelijk** hebt gedefinieerd in de wizard **Experiment verbinden**.

1. Gebruik in de editorweergave het vervolgkeuzemenu voor variaties onder de opdrachtbalk om elke variatie te bewerken op basis van uw oorspronkelijke hypothese. U kunt ook een besturingselement of basisvariatie instellen door een van de variaties ongewijzigd te laten.
1. Selecteer de module waarop u een experiment wilt uitvoeren, selecteer het weglatingsteken (...) en selecteer vervolgens **Toevoegen aan experiment**.

### <a name="edit-variations-for-experiments-with-entire-scope"></a>Variaties bewerken voor experimenten met een volledig bereik
Als u het bereik van uw experiment als **volledig** hebt gedefinieerd in de wizard **Experiment verbinden** terwijl u in de editorweergave werkt, gebruikt u het vervolgkeuzemenu voor variaties onder de opdrachtbalk om elke variatie te bewerken op basis van uw oorspronkelijke hypothese. 

> [!NOTE]
> In beide gevallen kunt u ook een besturingselement of basisvariatie instellen door een van de variaties ongewijzigd te laten.

## <a name="previous-step"></a>Vorige stap
[Een experiment instellen](experimentation-setup.md) 


## <a name="next-step"></a>Volgende stap
[Preview van een experiment weergeven en een experiment publiceren](experimentation-preview-publish.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]