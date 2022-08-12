---
title: Problemen met het instellen en installeren van Store Commerce oplossen
description: In dit artikel wordt beschreven hoe u problemen met het instellen en installeren in de Microsoft Dynamics 365 Commerce-app Store Commerce kunt oplossen.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 8af2c476ced05fc159a53131f8b51ad914a6c7c3
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/16/2022
ms.locfileid: "9168942"
---
# <a name="troubleshoot-store-commerce-setup-and-installation-issues"></a>Problemen met het instellen en installeren van Store Commerce oplossen

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u problemen met het instellen en installeren in de Microsoft Dynamics 365 Commerce-app Store Commerce kunt oplossen.

## <a name="i-cant-activate-the-app-and-i-receive-a-connectivity-error-message"></a>Ik kan de app niet activeren en er wordt een foutbericht over connectiviteit weergegeven

Nadat u de geldige CPOS (Cloud Point of Sale)-URL hebt opgegeven, wordt er mogelijk een foutbericht over connectiviteit weergegeven dat op het volgende voorbeeld lijkt:

> Er is een connectiviteitsfout opgetreden en uw apparaat kan geen verbinding maken met de CPOS. Het probleem kan liggen aan hoe de URL van de CPOS is getypt.

Controleer in dit geval de URL op typfouten of bepaal of de CPOS niet kan worden bereikt omdat deze offline is.

Controleer daarnaast of de CSU-versie (Cloud Scale Unit) niet 10.0.25 (9.35.\*.\*) of hoger is. CPOS-versie 10.0.25 of hoger is verplicht om de app Store Commerce te gebruiken.

## <a name="i-cant-install-the-app-because-modern-pos-is-already-installed"></a>Ik kan de app niet installeren omdat Modern POS al is geïnstalleerd

Tijdens de installatie wordt mogelijk een foutbericht weergegeven zoals in het volgende voorbeeld:

> Er is al een versie (9.\*.\*.\*) van dit product (Modern POS) geïnstalleerd via het verouderde installatieprogramma.

Als u de fout wilt herstellen, moet u de MPOS-app (Modern Point of Sale) voor alle gebruikers op de computer verwijderen en het vervolgens opnieuw proberen. U kunt bevestigen of MPOS voor alle gebruikers is verwijderd door de volgende PowerShell-opdracht uit te voeren.

```PowerShell
Get-AppxPackage | Where-Object {$_.PackageFullName -like "Microsoft.Dynamics.*.Pos"} | Remove-AppxPackage -Allusers
```

## <a name="i-cant-activate-the-app-because-of-an-invalid-url-or-an-error-state"></a>Ik kan de app niet activeren vanwege een ongeldige URL of een foutstatus

Als de ingevoerde CPOS-URL niet geldig is en u deze wilt wijzigen of als de app Store Commerce tijdens het activeren een foutstatus heeft, kunt u het proces opnieuw starten door de app opnieuw in te stellen. In de Store Commerce-app wordt alleen een geldige CPOS-URL opgeslagen.

Volg deze stappen om de app Store Commerce opnieuw in te stellen.

1. Selecteer de app in het menu **Start** van Windows en houd deze vast (of klik met de rechtermuisknop) en selecteer vervolgens **Meer \> App-instellingen**.
2. Blader omlaag op de pagina met app-instellingen tot u de knop **Opnieuw instellen** vindt.
3. Selecteer **Opnieuw instellen**. Bevestig, wanneer u hierom wordt gevraagd, dat u de app opnieuw wilt instellen.
