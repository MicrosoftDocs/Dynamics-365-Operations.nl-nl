--- 
title: Een configuratie uploaden naar Lifecycle Services voor elektronische aangifte (ER)
description: In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken en uploaden.
author: NickSelin
manager: AnnBe
ms.date: 05/13/2016
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
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 3d9c2192bac8477e9c9376aab3e3b561da777569
ms.contentlocale: nl-nl
ms.lasthandoff: 03/26/2018

---
# <a name="upload-a-configuration-into-lifecycle-services-for-electronic-reporting-er"></a>Een configuratie uploaden naar Lifecycle Services voor elektronische aangifte (ER)

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe configuratie voor elektronische rapportage (ER) kan maken en uploaden.

In dit voorbeeld maakt u een configuratie en uploadt u deze naar LCS voor het voorbeeldbedrijf, Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd aangezien ER-configuraties tussen bedrijven worden gedeeld. Als u deze stappen wilt uitvoeren, moet u eerst de stappen in de procedure "Een configuratieprovider maken en deze als actief markeren" voltooien. Om deze stappen te kunnen uitvoeren is ook toegang tot LCS vereist.

1. Ga naar Organisatiebeheer > Werkruimten > Elektronische rapportage.
2. Selecteer ‘Litware, Inc.’ en stel het in als actief.
3. Klik op Configuraties.

## <a name="create-a-new-data-model-configuration"></a>Een nieuwe gegevensmodelconfiguratie maken
1. Klik op Configuratie maken om het dialoogvenster voor beëindigen te openen.
    * U maakt een configuratie die een voorbeeldgegevensmodel voor elektronische documenten bevat. Deze gegevensmodelconfiguratie wordt later in LCS geüpload.  
2. Typ 'Voorbeeldmodelconfiguratie' in het veld Naam.
    * Voorbeeldmodelconfiguratie  
3. Typ 'Voorbeeldmodelconfiguratie' in het veld Omschrijving.
    * Voorbeeldmodelconfiguratie  
4. Klik op Configuratie maken.
5. Klik op Modelontwerper.
6. Klik op Nieuw.
7. Typ 'Invoerpunt' in het veld Naam.
    * Invoerpunt  
8. Klik op Toevoegen.
9. Klik op Opslaan.
10. Sluit de pagina.
11. Klik op Status wijzigen.
12. Klik op Voltooien.
13. Klik op OK.

## <a name="register-a-new--repository"></a>Een nieuwe opslagplaats registreren
1. Sluit de pagina.
2. Klik op Opslagplaatsen.
    * Hiermee kunt u de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc openen.  
3. Klik op Toevoegen om het dialoogvenster te openen.
    * Hiermee kunt u een nieuwe opslagplaats toevoegen.  
4. Selecteer LCS in het veld Type opslagplaats van configuratie.
5. Klik op Opslagplaats maken.
6. Typ of selecteer een waarde in het veld Project.
    * Selecteer het gewenste LCS-project. U moet toegang tot het project hebben.  
7. Klik op OK.
    * Voer een nieuwe opslagplaats in.  
8. Markeer in de lijst de geselecteerde rij.
    * Selecteer de LCS-opslagplaatsrecord.  
    * Een geregistreerde opslagplaats wordt door de huidige provide gemarkeerd, wat betekent dat de enige configuraties in bezit van die provider in deze opslagplaats kunnen worden geplaatst en daarom naar het geselecteerde LCS-project kunnen worden geüpload.  
9. Klik op Openen.
    * Open de opslagplaats om de lijst met ER-configuraties weer te geven. De lijst is leeg als dit project nog niet voor delen van ER-configuraties is gebruikt.  
10. Sluit de pagina.
11. Sluit de pagina.

## <a name="upload-configuration-into-lcs"></a>Configuratie naar LCS uploaden
1. Klik op Configuraties.
2. Selecteer 'Voorbeeldmodelconfiguratie' in de structuur.
    * Selecteer een gemaakte configuratie die al is voltooid.  
3. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de versie van de geselecteerde configuratie met de status ‘Voltooid’.  
4. Klik op Status wijzigen.
5. Klik op Delen.
    * De configuratiestatus wordt gewijzigd van ‘Voltooid’ in ‘Gedeeld’ wanneer deze wordt gepubliceerd in LCS.  
6. Klik op OK.
7. Zoek en selecteer de gewenste record in de lijst.
    * Selecteer de configuratieversie met de status ‘Gedeeld’.  
    * De status van de geselecteerde versie is gewijzigd van ‘Voltooid’ in ‘Gedeeld’.  
8. Sluit de pagina.
9. Klik op Opslagplaatsen.
    * Hiermee kunt u de lijst met opslagplaatsen voor de configuratieprovider Litware, Inc openen.  
10. Klik op Openen.
    * Selecteer de LCS-opslagplaats en open deze.  
    * De geselecteerde configuratie wordt getoond als een activum van het geselecteerde LCS-project.  
    * Open LCS met https://lcs.dynamics.com. Open een project dat eerder is gebruikt voor opslagplaatsregistratie, open de ‘Activabibliotheek’ van dit project en vouw de inhoud van het activumtype ‘GER-configuratie’ uit; de geüploade ER-configuratie is beschikbaar. De geüploade LCS-configuratie kan naar een ander Microsoft Dynamics 365 for Finance and Operations-exemplaar worden geïmporteerd als providers toegang tot dit LCS-project hebben.  


