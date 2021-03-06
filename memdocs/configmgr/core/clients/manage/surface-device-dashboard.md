---
title: Surface Device-dash board
titleSuffix: Configuration Manager
description: Bekijk informatie over Surface-apparaten met behulp van het dash board.
author: aczechowski
ms.author: aaroncz
manager: dougeby
ms.date: 07/30/2018
ms.topic: conceptual
ms.prod: configuration-manager
ms.technology: configmgr-client
ms.assetid: 7397fc17-3ae8-4525-8386-aea8a9cffa06
ms.openlocfilehash: f9b9c49bde16754b7a60112905f14da2cd5e48eb
ms.sourcegitcommit: 214fb11771b61008271c6f21e17ef4d45353788f
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2020
ms.locfileid: "82906279"
---
# <a name="surface-device-dashboard-in-configuration-manager"></a>Dash board van Surface-apparaat in Configuration Manager

*Van toepassing op: Configuration Manager (huidige vertakking)*

Vanaf versie 1802 biedt het Surface Device-dash board informatie over Surface-apparaten die in uw omgeving in één oogopslag worden gevonden. <!--1355788-->

## <a name="open-the-surface-device-dashboard"></a>Het Surface Device-dash board openen

Voer de volgende stappen uit om het Surface Device-dash board te openen: 

1. Open de Configuration Manager-console. 
2. Klik op het knoop punt **bewaking** . 
3. Klik op **Surface devices**om het dash board te laden.

**Surface Device-dash board** 
 ![ Surface Device-dash board](media/Surface-device-dashboard.PNG)



## <a name="reviewing-information-in-the-surface-device-dashboard"></a>Informatie bekijken in het Surface Device-dash board

Het Surface Device-dash board toont drie grafieken voor uw omgeving. 

- **Percentage van Surface-apparaten** : geeft u het percentage Surface-apparaten in uw omgeving.

    ![Grafiek percentage van Surface-apparaten](media/Percent-Surface-Devices.PNG)
- **Surface-modellen** : hier wordt het aantal apparaten per surface model weer gegeven. 
  - Als u de muis aanwijzer boven een grafiek sectie houdt, geeft u het percentage Surface-apparaten weer dat door het model is geselecteerd. 

       ![Grafiek van oppervlak modellen](media/Surface-Models-Hover.PNG)
  - Als u op een grafiek gedeelte klikt, gaat u naar een lijst met apparaten voor het model. 
      ![Lijst met apparaten voor Surface model](media/Surface-Model-Device-List.PNG)

- **Top vijf van firmware versies**: geeft een grafiek weer met de vijf meest voorkomende firmware modellen in uw omgeving. 
  - Als u de muis aanwijzer boven een grafiek sectie houdt, geeft u het aantal Surface-apparaten weer dat de firmware versie is geselecteerd. Vanaf Configuration Manager versie 1806, klikken op een grafiek sectie, wordt een lijst met relevante apparaten weer gegeven. <!--1358654-->
     ![Lijst met apparaten voor Surface model](media/Surface-Firmware-Hover.PNG)


## <a name="more-information"></a>Meer informatie

Zie de [Surface](https://www.microsoft.com/surface) -website voor meer informatie over Surface-apparaten.

Zie [updates van Surface drivers beheren](https://support.microsoft.com/help/4098906)voor meer informatie over het implementeren van Surface firmware-updates in Configuration Manager.




