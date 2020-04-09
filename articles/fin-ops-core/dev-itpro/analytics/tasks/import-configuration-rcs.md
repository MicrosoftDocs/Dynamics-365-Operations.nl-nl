---
title: (ER) Configuraties importeren uit RCS
description: Dit onderwerp biedt informatie over de manier waarop een gebruiker een nieuwe versie van een ER‑configuratie kan importeren uit RCS.
author: NickSelin
manager: AnnBe
ms.date: 07/03/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ea2bfd2514be666d05165410ca27041a86464715
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143218"
---
# <a name="er-import-configurations-from-rcs"></a>(ER) Configuraties importeren uit RCS

[!include [banner](../../includes/banner.md)]

In de volgende stappen wordt uitgelegd hoe een gebruiker met de rol van systeembeheerder of ontwikkelaar voor elektronische rapportage een nieuwe versie van een ER-configuratie uit Microsoft Regulatory Configuration Service (RCS) kan importeren. In dit voorbeeld selecteert u de versie van de ER‑configuratie die is geconfigureerd in een RCS‑exemplaar en importeert u deze in het huidige exemplaar voor voorbeeldbedrijf Litware, Inc. Deze stappen kunnen in elk bedrijf worden uitgevoerd omdat ER‑configuraties tussen bedrijven worden gedeeld. Als u deze stappen wilt uitvoeren, moet u eerst de stappen voltooien in het onderwerp [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). Als u deze stappen wilt voltooien, moet u ook toegang hebben tot een RCS‑exemplaar met minimaal één ER‑configuratie in de status **Voltooid** of **Gedeeld**.

1. Ga naar **Organisatiebeheer** > **Werkruimten** > **Elektronische rapportage**. 
2. Controleer of de configuratieprovider voor het voorbeeldbedrijf Litware, Inc. beschikbaar is en gemarkeerd als **Actief**. Als u deze configuratieprovider niet ziet, voltooit u de stappen in het onderwerp [Configuratieproviders maken en deze als actief markeren](er-configuration-provider-mark-it-active-2016-11.md). 
3. Als u geen RCS-omgeving hebt ingericht voor uw bedrijf, klik dan op de link **Regulatory services ‑ Configuratie** en volg de instructies om een RCS-omgeving in te richten. 
4. Klik op **Parameters elektronische rapportage**. 
5. Klik op het tabblad **RCS**. 
6. Als de RCS-omgeving al is ingericht voor uw bedrijf, gebruikt u de weergave op de pagina met url's om deze te openen. 
7. Sluit de pagina. 

## <a name="register-a-new-er-repository"></a>Een nieuwe ER‑opslagplaats registreren. 
1. Markeer in de lijst de geselecteerde rij. 
2. Selecteer Litware, Inc. provider. 
3. Klik op Opslagplaatsen. 
4. Klik op Toevoegen om het dialoogvenster te openen. 
5. Selecteer 'RCS' in het veld Type opslagplaats van configuratie. 
6. Klik op Opslagplaats maken. 
7. Typ of selecteer een waarde in het veld RCS‑omgeving weergavenaam. 
8. Selecteer het gewenste RCS-exemplaar. U kunt er ook meerdere hebben. 
9. Klik op OK. 

## <a name="import-er-configurations-from-rcs-based-repository"></a>ER-configuraties downloaden uit de RCS-gebaseerde opslagplaats
1. Klik op **Filters weergeven**. 
2. Voer een filterwaarde van 'RCS' in het veld **Naam** met gebruik van de de filteroperator **begint met**. 
3. Wanneer u de geselecteerde opslagplaats opent, op de pagina **Verbinden met Regulatory Configuration Services** klik dan op de link **Klik hier om verbinding te maken met de Regulatory Configuration Services**. 
4. Klik op **Openen**. 
5. Klik op **Sluiten**. 
6. Selecteer de gewenste versie van de ER‑configuratie en Klik op **Importeren** om deze in het huidige exemplaar te plaatsen.

