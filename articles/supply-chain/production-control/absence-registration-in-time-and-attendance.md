---
title: Verzuimregistratie in Tijd en aanwezigheid
description: In dit onderwerp wordt uitgelegd hoe u verzuimregistraties afhandelt in Tijd en aanwezigheid.
author: johanhoffmann
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JMGParameters, JmgAbsenceCalendar
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 16b338010662f8c2115fcc38f6830b58c49259e2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425182"
---
# <a name="absence-registration-in-time-and-attendance"></a>Verzuimregistratie in Tijd en aanwezigheid

[!include [banner](../includes/banner.md)]

In dit onderwerp worden de concepten voor verzuim beschreven en wordt uitgelegd hoe u verzuim afhandelt in Tijd en aanwezigheid.

## <a name="absence-that-is-based-on-regular-work-hours"></a>Verzuim dat is gebaseerd op de normale kantooruren

Werknemers worden beschouwd als afwezig voor alle uren die ze niet werken tijdens hun normale werkuren. Normale werkuren worden gedefinieerd in het standaardtijdprofiel van een werknemer.

Een werknemer kan bijvoorbeeld werken op basis van een dagprofiel met een inkloktijd van 07:00 uur en een uitkloktijd van 15:00 uur. Als de werknemer om 09:00 uur inklokt, wordt hij van 07:00 tot 09:00 uur als afwezig beschouwd voor die dag.

In dat geval dienen werknemers een reden voor hun afwezigheid in te voeren. Ze kunnen een reden opgeven door een verzuimcode te selecteren.

## <a name="absence-codes"></a>Verzuimcodes

Verzuimcodes definiëren de verschillende verzuimtypen. Verzuimcodes worden gedefinieerd door het bedrijf.

Verschillende regels kunnen worden toegepast op verzuimcodes. Een verzuimcode kan bijvoorbeeld zo worden geconfigureerd dat op basis hiervan salaris wordt ingehouden of wordt uitgekeerd.

Een bedrijf kan bijvoorbeeld een verzuimcode **Te laat** definiëren voor werknemers die zonder goede reden te laat komen. Het bedrijf definieert ook een verzuimcode **Interne cursus** die werknemers kunnen gebruiken voor de tijd die ze besteden aan het bijwonen van interne cursussen. Deze verzuimcodes kunnen zo worden ingesteld dat met **Te laat** salaris van een werknemer wordt ingehouden en met **Interne cursus** geen salaris wordt ingehouden.

U kunt automatische verzuimcodes instellen. Deze verzuimcodes kunnen worden gebruikt voor het berekenen van de gewerkte tijd door een werknemer wanneer er geen verzuim is geregistreerd. Het tijdprofiel van de werknemer bepaalt of de verzuimcode voor standaardtijd of flextijd wordt gebruikt.

### <a name="set-up-standard-time-and-flex-time"></a>Standaardtijd en flextijd instellen

- Configureer de parameters voor standaardtijd en flextijd met de opties **Verzuim automatisch invoegen** en **Flextijd automatisch invoegen-** op de pagina **Parameters in Tijd en aanwezigheid**.

## <a name="absence-groups"></a>Verzuimgroepen

Verzuimcodes worden gegroepeerd in verzuimgroepen. U gebruikt verzuimgroepen om groepscodes met gemeenschappelijke kenmerken te groeperen. Voorbeelden zijn onder andere verzuimcodes voor een geldig verzuim of verzuim vanwege een doktersafspraak, verlof of een ziek kind.

## <a name="planned-absence"></a>Gepland verzuim

Als u weet dat een werknemer een periode afwezig is, bijvoorbeeld vanwege een aanstaande vakantie, kunt u gepland verzuim gebruiken. U stelt gepland verzuim in door de verzuimcode zo te configureren dat rekening wordt gehouden met het geplande verzuim. Wanneer u een gepland verzuim instelt, wordt u tijdens de afwezigheidsperiode niet gevraagd om een verzuimcode wanneer gebruikerstijdregistraties worden berekend. Gepland verzuim kan voor één werknemer worden gedefinieerd, maar u kunt ook een batchtaak opgeven om het geplande verzuim voor werknemers bulksgewijs bij te werken.

### <a name="set-up-planned-absence"></a>Gepland verzuim instellen

1. Selecteer **HRM** &gt; **Medewerkers** &gt; **Werknemers** en selecteer een werknemer.
2. Selecteer **Tijd** &gt; **Tijdtoewijzingen** &gt; **Registratie van tijdverzuim** en stel het geplande verzuim in.

## <a name="interrupted-planned-absence"></a>Onderbroken gepland verzuim

Als u de optie **Onderbreken** toepast tijdens het instellen van een gepland verzuim, wordt het geplande verzuim onderbroken als de werknemer zich tijdens de periode van het geplande verzuim aanmeldt. Het geplande verzuim wordt gemarkeerd als **Onderbroken**, maar dit heeft verder geen effect op toekomstige berekeningen.

### <a name="set-up-a-planned-absence-for-interruption"></a>Een gepland verzuim voor onderbreking instellen

1. Open de pagina **Registratie van tijdverzuim** op de wijze die wordt beschreven in de procedure voor het instellen van gepland verzuim.
2. Selecteer **Onderbreken**.

De optie **Onderbreken** geldt als er tijd wordt geregistreerd via de werkvloerterminal of het werkvloerapparaat. De optie is niet van toepassing als de registraties worden ingevoerd op de berekenings- en goedkeuringspagina's, of op de pagina **Elektronische prikkaart**.

## <a name="examples-of-the-use-of-absence-in-a-flex-profile"></a>Voorbeelden van het gebruik van verzuim in een flextijdprofiel

Met de volgende drie voorbeelden wordt aangegeven hoe verzuim wordt berekend in een profiel met flexperioden.

In de voorbeelden wordt het volgende profiel gebruikt:

| Inklokken | Standaardtijd    | Pauze             | Standaardtijd | Flextijd-        | Uitklokken | Flextijd+        |
|----------|------------------|-------------------|---------------|--------------|-----------|--------------|
| 08:00 uur     | 09:00 tot 11:30 uur | 11:30 tot 12:00 uur | 12:00 tot 15:00 uur | 15:00 tot 16:00 uur | 16:00 uur      | 16:00 tot 18:00 uur |

### <a name="example-1-signing-out-during-a-flex--period"></a>Voorbeeld 1: Afmelden tijdens een periode Flextijd-

De werknemer klokt in om 08:00 uur en klokt uit om 15:30 uur. In dit geval wordt er geen verzuim berekend omdat de werknemer uitklokt tijdens een periode Flextijd- en er wordt een half uur afgetrokken van het flexsaldo van de werknemer.

### <a name="example-2-signing-out-in-during-standard-time-period"></a>Voorbeeld 2: Afmelden tijdens de periode Standaardtijd

De werknemer klokt in om 08:00 uur en klokt uit om 14:30 uur. In dit geval wordt er wel verzuim berekend omdat de werknemer uitklokt tijdens de periode Standaardtijd. Er wordt van 14:30 tot 16:00 uur verzuim berekend en er wordt een verzuimperiode van 1,5 uur geregistreerd. Voor die periode is een verzuimcode vereist.

### <a name="example-3-signing-out-during-a-flex-period"></a>Voorbeeld 3: Afmelden tijdens een periode Flextijd+

De werknemer klokt in om 08:00 uur en klokt uit om 16:30 uur. In dit geval wordt er geen verzuim berekend omdat de werknemer uitklokt tijdens een periode Flextijd+ en wordt er een half uur opgeteld bij het flexsaldo van de werknemer.

## <a name="absence-in-the-calculation-and-approval-process"></a>Verzuim in het berekenings- en goedkeuringsproces

Registraties van werknemerstijd moeten worden berekend en goedgekeurd voordat ze als salarisposten kunnen worden overgebracht naar de salarisadministratie.

Een fiatteur kan de tijdregistraties van een werknemer wijzigen. De fiatteur kan zelfs het verzuim wijzigen dat de werknemer heeft geregistreerd. Als de fiatteur handmatig een periode met een verzuimcode invoert, wordt de verzuimcode voor die periode niet overschreven door de standaardverzuimcode uit Parameters in Tijd en aanwezigheid.

Stel, een werknemer klokt in om 10:00 uur en selecteert een verzuimcode waarmee wordt aangegeven dat zij te laat is. Later informeert de werknemer haar supervisor dat ze van 08:00 tot 10:00 uur een doktersafspraak had. Een doktersafspraak mag niet resulteren in het inhouden van salaris. Daarom kan de supervisor in dit geval de twee verzuimuren van 08:00 tot 10:00 uur handmatig aanpassen door een verzuimcode in te voeren die op ziekte duidt.

### <a name="calculate-and-approve-absence"></a>Verzuim berekenen en goedkeuren

- Selecteer **Tijd en aanwezigheid** &gt; **Controleren en goedkeuren** &gt; **Goedkeuren of berekenen**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]