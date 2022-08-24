---
title: (ER) Configuraties importeren uit RCS
description: Dit artikel biedt informatie over de manier waarop een gebruiker een nieuwe versie van een ER‑configuratie kan importeren uit RCS.
author: kfend
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.search.form: ''
ms.openlocfilehash: 55e7a3ae23b708acecb5ac219b885f43b4c7aa0a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9290029"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Configuraties importeren uit RCS

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Regulatory Configuration Service (RCS) kan importeren. In dit voorbeeld selecteert u de versie van de ER‑configuratie die is geconfigureerd in een RCS‑exemplaar en importeert u deze in het huidige exemplaar voor voorbeeldbedrijf Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd omdat ER‑configuraties tussen bedrijven worden gedeeld. Als u deze stappen wilt uitvoeren, moet u eerst de stappen voltooien in het artikel [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). Als u deze stappen wilt voltooien, moet u ook toegang hebben tot een RCS‑exemplaar met minimaal één ER‑configuratie in de status **Voltooid** of **Gedeeld**.

1. Ga naar **Organisatiebeheer** > **Werkruimten** > **Elektronische rapportage**. 
2. Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooit u de stappen in het artikel [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). 
3. Als u geen RCS-omgeving hebt ingericht voor uw bedrijf, selecteert u de externe koppeling **Regulatory services ‑ Configuratie** en voert u de instructies uit voor het inrichten van een RCS-omgeving. 
4. Selecteer **Parameters elektronische rapportage**. 
5. Selecteer het tabblad **RCS**. 
6. Als de RCS-omgeving al is ingericht voor uw bedrijf, gebruikt u de weergave op de pagina met url's om deze te openen. 
7. Sluit de pagina. 

## <a name="register-a-new-er-repository"></a>Een nieuwe ER‑opslagplaats registreren. 
1. Markeer in de lijst de geselecteerde rij. 
2. Selecteer Litware, Inc. provider. 
3. Selecteer Opslagplaatsen. 
4. Selecteer Toevoegen om het uitklapvenster te openen. 
5. Selecteer 'RCS' in het veld Type opslagplaats van configuratie. 
6. Selecteer Opslagplaats maken. 
7. Typ of selecteer een waarde in het veld RCS‑omgeving weergavenaam. 
8. Selecteer het gewenste RCS-exemplaar. U kunt er ook meerdere hebben. 
9. Selecteer OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>ER-configuraties downloaden uit op RCS gebaseerde opslagplaats
1. Selecteer **Filters weergeven**. 
2. Voer een filterwaarde van 'RCS' in het veld **Naam** met gebruik van de de filteroperator **begint met**. 
3. Wanneer u de geselecteerde opslagplaats opent, selecteert u op de pagina **Verbinden met Regulatory Configuration Services** de koppeling **Klik hier om verbinding te maken met de Regulatory Configuration Services**. 
4. Selecteer **Openen**. 
5. Selecteer **Sluiten**. 
6. Selecteer de gewenste versie van de ER‑configuratie en selecteer **Importeren** om deze in het huidige exemplaar te plaatsen.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
