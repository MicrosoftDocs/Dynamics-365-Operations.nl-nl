--- 
title: Model beheren voor toewijzing van configuraties voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage ER-modeltoewijzingen (Electronic Reporting) kan beheren in aparte ER-configuraties.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 35fdc1e98897d449ce18fe38cc6b7896ca5c5278
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a>Model beheren voor toewijzing van configuraties voor elektronische aangifte (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker die is toegewezen aan de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage ER-modeltoewijzingen (Electronic Reporting) kan beheren in aparte ER-configuraties. In deze taakbegeleiding maakt u de vereiste ER-configuraties voor het voorbeeldbedrijf Litware, Inc. Voordat u deze taakbegeleiding uitvoert, moet u eerst de stappen uitvoeren in de Taakbegeleiding 'ER Een configuratieprovider maken' en deze als actief markeren. 

Omdat ER-configuraties worden gedeeld tussen bedrijven, kunt u deze taakbegeleider voltooien met behulp van de bedrijfsgegevensset van uw keuze. De functionaliteit voor deze taakbegeleider is beschikbaar als u een van de volgende hotfixes hebt geïnstalleerd: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 voor de Dynamics AX-7.0-versie of https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 voor de Dynamics 365 for Operations-versie.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
    * Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als actief. Als u deze configuratieprovider niet ziet, moet u eerst de stappen in de taakbegeleiding "Een configuratieprovider maken" en deze als actief markeren uitvoeren.   

## <a name="add-a-new-er-model-configuration"></a>Een nieuwe ER-modelconfiguratie toevoegen
1. Klik op Rapportconfiguraties.
    * Een nieuwe modelconfiguratie toevoegen. De naam moet uniek zijn in de structuur van configuraties.  
2. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
3. Typ 'Voorbeeldgegevensmodel' in het veld Naam.
    * Voorbeeldgegevensmodel  
4. Klik op Configuratie maken.
5. Klik op Ontwerper.
6. Klik op Nieuw om het verwijderdialoogvenster te openen.
7. Typ Basis in het veld Naam.
    * Basis  
8. Klik op Toevoegen.
9. Klik op Nieuw om het verwijderdialoogvenster te openen.
10. Typ "Bedrijf" in het veld Naam.
    * Bedrijf  
11. Klik op Toevoegen.
12. Voer in het veld Beschrijving de tekst, omschrijving van de rechtspersoon of het bedrijf in waar een gebruiker tijdens de uitvoering is aangemeld. 
    * Beschrijving van de rechtspersoon of het bedrijf waarin een gebruiker tijdens runtime is aangemeld.  
13. Klik op Basisverwijzing.
14. Klik op OK.
15. Klik op Opslaan.
16. Sluit de pagina.
17. Klik op Status wijzigen.
18. Klik op Voltooien.
19. Klik op OK.

## <a name="add-a-new-er-model-mapping-configuration"></a>Een nieuwe ER-modelgegevensmodelconfiguratie toevoegen
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
2. Voer in het veld Nieuw 'Modeltoewijzing gebaseerd op gegevensmodel Voorbeeldgegevensmodel' in.
3. Typ 'Voorbeeldtoewijzing' in het veld Naam.
    * Voorbeeldtoewijzing  
4. Klik op Configuratie maken.
5. Vouw de sectie Vereisten uit.
    * Houd er rekening mee dat de groep implementatievereisten automatisch is toegevoegd. De groep bevat de vereiste component die verwijst naar de bovenliggende gegevensmodelconfiguratie en is gemarkeerd als Implementatie. Dit betekent dat deze voorbeeldmodeltoewijzingsconfiguratie wordt beschouwd als de implementatie van het gegevensmodel, Voorbeeldgegevensmodel. Dit onderdeel dwingt ER daarom de modeltoewijzingsconfiguratie, Voorbeeldtoewijzing, te downloaden uit een ER-opslagplaats wanneer de modelconfiguratie, Voorbeeldgegevensmodel, wordt gedownload.   
6. Klik op Ontwerper.
    * De gemaakte modeltoewijzingsconfiguratie bevat een nieuwe lege toewijzing met dezelfde naam als de gemaakte configuratie. Wanneer een geselecteerde bovenliggende modelconfiguratie modeltoewijzingen bevat, worden deze naar een nieuwe modeltoewijzingsconfiguratie gekopieerd.   
7. Klik op Ontwerper.
8. Selecteer in de structuur 'Dynamics 365 for Operations\Tabel'.
9. Klik op Basis toevoegen.
10. Typ "Bedrijf" in het veld Naam.
    * Bedrijf  
11. Typ "CompanyInfo" in het veld Tabel.
    * CompanyInfo  
12. Klik op OK.
13. Vouw in de structuur 'Bedrijf' uit.
14. Vouw in de structuur 'Bedrijf\find()' uit.
15. Selecteer in de structuur 'Bedrijf\find()\Naam'.
16. Klik op Binden.
17. Klik op Opslaan.
18. Sluit de pagina.
19. Sluit de pagina.
20. Klik in het actievenster op Configuraties.
21. Klik op Gebruikersparameters.
22. Selecteer Ja in het veld Uitvoeringsinstellingen.
23. Klik op OK.
24. Klik op Bewerken.
25. Selecteer Ja in het veld Concept uitvoeren.

## <a name="add-a-new-er-format-configuration"></a>Een nieuwe ER-indelingsconfiguratie toevoegen
1. Selecteer in de structuur 'Voorbeeldgegevensmodel'.
2. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
3. Voer in het veld Nieuw 'Indeling gebaseerd op gegevensmodel Voorbeeldgegevensmodel' in.
4. Typ 'Voorbeeldindeling' in het veld Naam.
    * Voorbeeldindeling  
5. Klik op Configuratie maken.
6. Klik op Ontwerper.
7. Klik op Basis toevoegen om het dialoogvenster voor beëindiging te openen.
8. Selecteer "Text\String" in de structuur.
9. Klik op OK.
10. Klik op het tabblad Toewijzing.
11. Vouw in de structuur "model" uit.
12. Selecteer in de structuur 'model\Bedrijf'.
13. Klik op Binden.
14. Klik op Opslaan.
15. Sluit de pagina.
    * Voer de conceptversie van de gemaakte indeling uit voor testdoeleinden.  
16. Klik op Uitvoeren.
    * Klik op het sneltabblad Versies op Uitvoeren.  
17. Klik op OK.
    * Bekijk de uitvoer die de naam bevat van het bedrijf waarin de gebruiker die deze indelingsconfiguratie uitvoert, is aangemeld. De gemaakte modeltoewijzingsconfiguratie wordt gebruikt door deze indelingsconfiguratie omdat er slechts één configuratie beschikbaar is die vereiste modeltoewijzingen bevat.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Een alternatieve ER-modelgegevensmodelconfiguratie toevoegen
1. Selecteer in de structuur 'Voorbeeldgegevensmodel'.
2. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
3. Voer in het veld Nieuw 'Modeltoewijzing gebaseerd op gegevensmodel Voorbeeldgegevensmodel' in.
4. Typ 'Voorbeeldtoewijzing (alternatief)' in het veld Naam.
    * Voorbeeldtoewijzing (alternatief)  
5. Klik op Configuratie maken.
6. Klik op Ontwerper.
7. Klik op Ontwerper.
8. Selecteer in de structuur 'Dynamics 365 for Operations\Tabel'.
9. Klik op Basis toevoegen.
10. Typ "Bedrijf" in het veld Naam.
    * Bedrijf  
11. Typ "CompanyInfo" in het veld Tabel.
    * CompanyInfo  
12. Klik op OK.
13. Klik op Bewerken.
14. Selecteer "String\CONCATENATE" in de structuur.
15. Klik op Functie toevoegen.
16. Vouw in de structuur 'Bedrijf' uit.
17. Vouw in de structuur 'Bedrijf\find()' uit.
18. Selecteer in de structuur 'Bedrijf\find()\Naam'.
19. Klik op Gegevensbron toevoegen.
20. Typ een waarde in het veld Formule.
    * CONCATENATE(Bedrijf.'find()'.Naam, ";",  
21. Selecteer in de structuur 'Bedrijf\find()\Bedrijf(Gegevensgebied)'.
22. Klik op Gegevensbron toevoegen.
23. Typ een waarde in het veld Formule.
    * CONCATENATE(Company.'find()'. Naam, ';', Bedrijf.'find()'. Gegevensgebied)  
24. Klik op Opslaan.
25. Sluit de pagina.
26. Klik op Opslaan.
27. Sluit de pagina.
28. Sluit de pagina.
29. Selecteer Ja in het veld Concept uitvoeren.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Een bestaande ER-modeltoewijzingsconfiguratie gebruiken
1. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldindeling'.
2. Klik op Uitvoeren.
    * Houd er rekening mee dat de geselecteerde conceptversie van de ER-indelingsconfiguratie kan niet worden uitgevoerd omdat er meer dan één modeltoewijzingsconfiguratie beschikbaar is voor het niet-gedefinieerde gegevensmodel dat is geselecteerd als de gegevensbron van de lopende ER-indeling.   
    * Vervolgens definieert u de alternatieve modeltoewijzingsconfiguratie als de configuratie waaruit modeltoewijzingen worden gebruikt als gegevensbronnen voor het uitvoeren van de ER-indeling.   
3. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldtoewijzing (alternatief)'.
4. Selecteer in het veld Standaard voor modeltoewijzing de waarde Ja.
5. Selecteer in de structuur 'Voorbeeldgegevensmodel\Voorbeeldindeling'.
6. Klik op Uitvoeren.
7. Klik op OK.
    * Houd er rekening mee dat de standaardmodeltoewijzingsconfiguratie door deze indelingsconfiguratie wordt gebruikt voor het genereren van het elektronische document (de gemaakte uitvoer bevat de bedrijfscode).  


