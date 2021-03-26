---
title: Veelgestelde vragen over financiële rapportage
description: In dit onderwerp vindt u antwoorden op eerdere vragen van andere gebruikers over financiële rapportage.
author: jiwo
manager: tfehr
ms.date: 01/13/2021
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2021-01-13
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2d49213ea18e09f04b026559bdca49fee1de0ef7
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5249296"
---
# <a name="financial-reporting-faq"></a>Veelgestelde vragen over financiële rapportage 

In dit onderwerp vindt u antwoorden op eerdere vragen van andere gebruikers over financiële rapportage. 


## <a name="how-do-i-restrict-access-to-a-report-using-tree-security"></a>Hoe beperk ik de toegang tot een rapport met Structuurbeveiliging?

Scenario: Het demobedrijf USMF wil de toegang tot een balansrapport beperken om te voorkomen dat alle gebruikers van functies voor financiële rapportage het rapport in D365 kunnen weergeven. Oplossing: U kunt Structuurbeveiliging gebruiken om de toegang tot één rapport te beperken, zodat alleen bepaalde gebruikers toegang hebben tot het rapport. 

1.  Meld u aan bij Report Designer voor financiële rapportage

2.  Maak een nieuwe structuurdefinitie (Bestand | Nieuw | Structuurdefinitie) a.    Dubbelklik op de regel **Samenvatting** in de kolom **Beveiliging van eenheid**.
  i.    Klik op Gebruikers en groepen.  
          1. Selecteer de gebruiker(s) of groep die toegang tot dit rapport wil(len) hebben. 
          
[![Gebruikersscherm](./media/FR-FAQ_users.png)](./media/FR-FAQ_users.png)

[![Beveiligingsscherm](./media/FR-FAQ_security.jpg)](./media/FR-FAQ_security.jpg)

  b.    Klik op **Opslaan**.
  
[![De knop Opslaan](./media/FR-FAQ_save.png)](./media/FR-FAQ_save.png)

3.  Voeg in uw rapportdefinitie uw nieuwe structuurdefinitie toe

[![Formulier voor structuurdefinitie](./media/FR-FAQ_tree-definition.jpg)](./media/FR-FAQ_tree-definition.jpg)

A.  Klik in de structuurdefinitie op Instellingen en schakel onder Rapporteringseenheden selecteren het selectievakje Alle rapporteringseenheden opnemen in

[![Formulier voor selectie van rapporteringseenheden](./media/FR-FAQ_reporting-unit-selection.jpg)](./media/FR-FAQ_reporting-unit-selection.jpg)

**Voor:** [![Schermopname van Voor](./media/FR-FAQ_before.png)](./media/FR-FAQ_before.png)

**Na:** [![Schermopname van Na](./media/FR-FAQ_after.png)](./media/FR-FAQ_after.png)

Opmerking: de reden voor het bovenstaande bericht is dat de gebruiker geen toegang heeft tot dat rapport nadat Beveiliging van eenheid is toegepast



## <a name="how-do-i-determine-which-accounts-do-not-matching-my-balances-in-d365"></a>Hoe bepaal ik welke rekeningen niet overeenkomen met mijn saldi in D365?

Wanneer u een rapport hebt dat niet overeenkomt met uw verwachtingen in D365, kunt u het volgende doen om die rekeningen en de afwijkingen te identificeren. 

### <a name="in-financial-reporter-report-designer"></a>In Report Designer voor financiële rapportage

1.  Maak een nieuwe rijdefinitie a.    Klik op Bewerken | Rijen invoegen uit dimensies i.  Selecteer MainAccount [![Scherm voor selectie van MainAccount](./media/FR-FAQ_selectmain_.png)](./media/FR-FAQ_selectmain_.png)
    
    ii. Klik op Ok b.    Sla de rijdefinitie op

2.  Maak een nieuwe kolomdefinitie     [![Een nieuwe kolomdefinitie maken](./media/FR-FAQ_column.png)](./media/FR-FAQ_column.png)

3.  Maak een nieuwe rapportdefinitie a.    Klik op instellingen en schakel de gemarkeerde selectievakjes uit [![Formulier Instellingen](./media/FR-FAQ_settings.png)](./media/FR-FAQ_settings.png)
   
4.  Genereer het rapport. 

5.  Exporteer het rapport naar Excel.

### <a name="in-d365"></a>In D365: 
1.  Klik op Grootboek | Query's en rapporten | Proefbalans a.    Parameters i.  Begindatum: Begin van boekjaar ii. Einddatum: de datum waarvoor u het rapport hebt gegenereerd iii.    Financiële-dimensieset ingesteld op Hoofdrekening ingesteld [![Formulier Hoofdrekening](./media/FR-FAQ_mainacct.png)](./media/FR-FAQ_mainacct.png)
      
  b.    Klik op Berekenen

2.  Exporteer het rapport naar Excel

U kunt de gegevens nu kopiëren uit het Excel-rapport in FR en het D365-proefbalansrapport om de kolommen Eindsaldo te vergelijken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]