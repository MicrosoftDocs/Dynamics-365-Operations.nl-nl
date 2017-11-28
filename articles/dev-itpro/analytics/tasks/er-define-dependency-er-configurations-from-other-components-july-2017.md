--- 
title: "De afhankelijkheid van configuraties van andere onderdelen voor elektronische rapportage (ER) definiëren"
description: Voordat u deze stappen uitvoert, moet u eerst de stappen in de taakbegeleiding ER modeltoewijzingsconfiguraties uitvoeren en moet u toegang hebben tot Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7de5fbcaa9f287752e3ae4834eb48d622d263579
ms.openlocfilehash: 890f035a291dbec936594ceeabc5de284d160ad4
ms.contentlocale: nl-nl
ms.lasthandoff: 10/25/2017

---
# <a name="define-the-dependency-of-configurations-from-other-components-for-electronic-reporting-er"></a>De afhankelijkheid van configuraties van andere onderdelen voor elektronische rapportage (ER) definiëren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Voordat u deze stappen uitvoert, moet u eerst de stappen in de taakbegeleiding ER modeltoewijzingsconfiguraties uitvoeren en moet u toegang hebben tot Microsoft Dynamics Lifecycle Services (LCS).

Deze procedure laat zien hoe u een ER-configuratie ontwerpt en de afhankelijkheid opgeeft van andere softwareonderdelen, zodat u kunt helpen garanderen dat de configuratie goed is gedownload naar een specifieke versie van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition. In dit voorbeeld maakt u vereiste ER-configuraties voor het voorbeeldbedrijf, Litware, Inc. 

Deze procedure is bedoeld voor gebruikers met de rol Systeembeheerder of Elektronische aangifteontwikkelaar. De stappen kunnen in elk bedrijf worden uitgevoerd, omdat ER-configuraties tussen bedrijven worden gedeeld. 

1. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
    * Zorg ervoor dat de configuratiestructuur de configuratie 'Voorbeeldgegevensmodel' en de onderliggende items bevat. Voltooi anders de stappen in de taakbegeleider ER modeltoewijzingsconfiguraties beheren, en start deze gids opnieuw.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>De afhankelijkheid van ER-configuraties van andere onderdelen definiëren
1. Vouw in de structuur 'Voorbeeldgegevensmodel' uit.
2. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldtoewijzing'.
    * We hebben de conceptversie van de modeltoewijzingsconfiguratie 'Voorbeeldtoewijzing' geselecteerd. Nu definiëren we de afhankelijkheid ervan van andere softwareonderdelen. Deze stap wordt beschouwd als een vereiste voor het beheren van de download van de versie van deze configuratie uit een ER-opslagplaats en eventueel verder gebruik van deze versie.   
3. Vouw de sectie Vereisten uit.
    * De vereistengroep 'Implementaties' is in deze fase automatisch toegevoegd. Deze groep bevat de vereiste component die verwijst naar de gegevensmodelconfiguratie en heeft de vlag Implementatie ingeschakeld. Deze vlag betekent dat de voorbeeldconfiguratie 'Voorbeeldtoewijzing' wordt beschouwd als de implementatie van het gegevensmodel 'Voorbeeldgegevensmodel'. Dit onderdeel dwingt ER daarom de toewijzingsconfiguratie 'Voorbeeldtoewijzing' te downloaden uit een ER-opslagplaats wanneer de modelconfiguratie 'Voorbeeldgegevensmodel' wordt gedownload.   
4. Klik op Bewerken.
    * Eén enkele afhankelijkheid van de huidige versie van een configuratie van een softwareonderdeel kan worden opgegeven met behulp van de definitie van het onderdeeltype en de onderdeelversie of een reeks onderdeelversies.  
    * Gewenste afhankelijkheden kunnen worden gegroepeerd. Wanneer het groeperingstype 'Alle' is ingeschakeld, wordt ervan uitgegaan dat aan de afhankelijkheidsconditie van deze groep is voldaan wanneer aan elke afhankelijkheidsconditie van deze groep en onderliggende groep is voldaan. Wanneer het groeperingstype 'Een van de' is geselecteerd, wordt ervan uitgegaan dat aan de afhankelijkheidsconditie van deze groep is voldaan wanneer aan ten minste één afhankelijkheidsconditie van deze groep is voldaan.   
5. Klik op Nieuw.
6. Selecteer Vereist productonderdeel.
7. Selecteer Microsoft Dynamics 365 for Operations (1611).
8. Typ in het veld Versie '[7.1.1541.3036,8)'.
    * [7.1.1541.3036,8)  
    * Afhankelijkheden die u invoert, worden geëvalueerd wanneer deze configuratie wordt gedownload via een ER-opslagplaats. Deze configuratieversie wordt gedownload van de ER-opslagplaats als versie 1 van de configuratie van het 'Voorbeeldgegevensmodel' al bestaat of eerder is gedownload. Als het van tevoren is gedownload, moet het worden voltooid in Finance and Operations, met de versie 7.1.1541.3036 of hoger, maar niet hoger zijn dan de primaire versie 8.   
9. Klik op Opslaan.
10. Sluit de pagina.
11. Klik op Status wijzigen.
12. Klik op Voltooien.
13. Klik op OK.
14. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldtoewijzing (alternatief)'.
15. Klik op Bewerken.
16. Klik op Nieuw.
17. Selecteer Vereist productonderdeel.
18. Selecteer Microsoft Dynamics AX 7.0 RTW.
19. Typ in het veld Versie '[7.0.1265.3015,7.1)'.
    * [7.0.1265.3015,7.1)  
    * Afhankelijkheden worden geëvalueerd wanneer de configuratie wordt gedownload uit een ER-opslagplaats. Deze configuratieversie wordt gedownload van de ER-opslagplaats als versie 1 van de configuratie van het 'Voorbeeldgegevensmodel' al bestaat of eerder is gedownload. Als het van tevoren is gedownload, moet het worden voltooid in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, met de versie 7.0.1265.3015 of hoger, maar niet hoger zijn dan de kleine versie 1.   
20. Klik op Opslaan.
21. Sluit de pagina.
22. Klik op Status wijzigen.
23. Klik op Voltooien.
24. Klik op OK.

## <a name="configure-the-er-repository"></a>De ER-opslagplaats configureren
1. Sluit de pagina.
2. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Open de lijst met ER-opslagplaatsen voor de huidige ER-provider, ‘Litware, Inc.’.  
3. Markeer in de lijst de geselecteerde rij.
4. Klik op Opslagplaatsen.
5. Klik op Filters weergeven.
6. Voer een filterwaarde van 'LCS' in het veld 'Typenaam' in met de filteroperator 'bevat'.
    * Als de LCS-opslagplaats al is geregistreerd voor de huidige ER-provider, kunt u de resterende stappen in deze subtaak overslaan. Als de LCS-opslagplaats niet al is geregistreerd, voert u de resterende stappen uit.   
7. Klik op Toevoegen om het dialoogvenster te openen.
8. Selecteer 'LCS' in het veld Type opslagplaats van configuratie.
9. Klik op Opslagplaats maken.
10. Typ of selecteer een waarde in het veld Project.
    * Selecteer het gewenste LCS-project vanuit de opzoekactie in het veld 'Project'.  
11. Klik op OK.
12. Sluit de pagina.

## <a name="upload-configurations-to-lcs"></a>Configuraties uploaden naar LCS
1. Klik op Rapportconfiguraties.
2. Selecteer in de structuur 'Voorbeeldgegevensmodel'.
3. Selecteer de voltooide versie van deze configuratie.
4. Klik op Status wijzigen.
5. Klik op Delen.
6. Klik op OK.
    * Versie 1 van deze modelconfiguratie is geüpload naar LCS via het LCS-project voor de ER-opslagplaats die eerder is geconfigureerd.   
7. Vouw in de structuur 'Voorbeeldgegevensmodel' uit.
8. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldtoewijzing'.
9. Selecteer de voltooide versie van deze configuratie.
10. Klik op Status wijzigen.
11. Klik op Delen.
12. Klik op OK.
    * Versie 1.1 van deze modeltoewijzing is geüpload naar LCS via het LCS-project voor de ER-opslagplaats die eerder is geconfigureerd.   
13. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldtoewijzing (alternatief)'.
14. Selecteer de voltooide versie van deze configuratie.
15. Klik op Status wijzigen.
16. Klik op Delen.
17. Klik op OK.
    * Versie 1.1 van deze modeltoewijzing is geüpload naar LCS via het LCS-project voor de ER-opslagplaats die eerder is geconfigureerd.   

## <a name="evaluate-er-configuration-dependencies"></a>ER-afhankelijkheden evalueren
    * We verwijderen gemaakte configuraties uit het systeem en downloaden deze terug uit de LCS-opslagplaats.  
1. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldtoewijzing'.
2. Klik op Verwijderen.
3. Klik op Ja.
4. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldtoewijzing (alternatief)'.
5. Klik op Verwijderen.
6. Klik op Ja.
7. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldindeling'.
8. Klik op Verwijderen.
9. Klik op Ja.
10. Selecteer in de structuur 'Voorbeeldgegevensmodel'.
11. Klik op Verwijderen.
12. Klik op Ja.
13. Sluit de pagina.
    * Open de lijst met ER-opslagplaatsen voor de huidige ER-provider, ‘Litware, Inc.’.  
14. Klik op Opslagplaatsen.
15. Klik op Filters weergeven.
16. Voer een filterwaarde van 'LCS' in het veld 'Typenaam' in met de filteroperator 'bevat'.
17. Klik op Openen.
18. Selecteer in de structuur 'Voorbeeldgegevensmodel'.
    * Houd er rekening mee dat u een evaluatie kunt weergeven van of aan de vereiste voorwaarden is voldaan voor elke versie van de ER-configuraties voor de huidige opslagplaats. Als u deze evaluatie wilt controleren, klikt u op Vereisten controleren.   
19. Klik op Vereisten controleren.
20. Klik op Importeren.
21. Klik op Ja.
22. Sluit de pagina.
23. Sluit de pagina.
24. Sluit de pagina.
25. Ga naar Organisatiebeheer > Elektronische rapportage > Configuraties.
26. Vouw in de structuur 'Voorbeeldgegevensmodel' uit.
    * Houd er rekening mee dat de modeltoewijzingsconfiguratie 'Voorbeeldtoewijzing' is gedownload met de geselecteerde gegevensmodelconfiguratie. De twee bestanden worden samen gedownload omdat 'Voorbeeldtoewijzing' is gedefinieerd als implementatie van het geselecteerde gegevensmodel en omdat het toepasbaar is op Finance and Operations. De configuratie 'Voorbeeldtoewijzing (alternatief)' is niet gedownload omdat niet is voldaan aan de voorwaarde voor de vereiste toepassingsversie.   
    * Als u zich aanmeldt bij Dynamics 365 for Finance and Operations, Enterprise edition, dezelfde provider registreert, toegang krijgt tot hetzelfde LCS-project en dezelfde gegevensmodelconfiguratie downloadt, wordt de configuratie 'Voorbeeldtoewijzing (alternatief)' gedownload en wordt de configuratie 'Voorbeeldtoewijzing' overgeslagen.  


