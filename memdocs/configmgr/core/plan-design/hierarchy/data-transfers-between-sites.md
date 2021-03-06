---
title: Gegevensoverdracht tussen sites
titleSuffix: Configuration Manager
description: Meer informatie over hoe Configuration Manager gegevens verplaatst tussen sites en hoe u de overdracht van de gegevens in uw netwerk kunt beheren.
ms.date: 08/09/2019
ms.prod: configuration-manager
ms.technology: configmgr-core
ms.topic: conceptual
ms.assetid: dc526e8d-fac3-4bb5-b206-03ad29b0ae11
author: mestew
ms.author: mstewart
manager: dougeby
ms.openlocfilehash: 6b6d4eab77d0543f9001cef2c1e2b618ba3e4328
ms.sourcegitcommit: bbf820c35414bf2cba356f30fe047c1a34c5384d
ms.translationtype: MT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/21/2020
ms.locfileid: "81720210"
---
# <a name="data-transfers-between-sites"></a>Gegevensoverdracht tussen sites

*Van toepassing op: Configuration Manager (huidige vertakking)*

Configuration Manager gebruikt *replicatie op basis van bestanden* en *database replicatie* om verschillende typen informatie tussen sites over te dragen. Meer informatie over hoe Configuration Manager gegevens verplaatst tussen sites en hoe u de overdracht van gegevens in uw netwerk kunt beheren.  

## <a name="types-of-replication"></a>Typen replicatie

### <a name="file-based-replication"></a><a name="bkmk_fileroute" />Replicatie op basis van een bestand

Configuration Manager maakt gebruik van op bestanden gebaseerde replicatie om gegevens op basis van bestanden over te dragen tussen sites in uw hiërarchie. Deze gegevens omvatten toepassingen en pakketten die u wilt implementeren naar distributie punten in onderliggende sites. Ook worden niet-verwerkte detectie gegevens records verwerkt die door de site worden overgedragen naar de bovenliggende site en vervolgens processen.  

Zie [replicatie op basis](file-based-replication.md)van een bestand voor meer informatie.

### <a name="database-replication"></a><a name="bkmk_dbrep" />Database replicatie

Configuration Manager database replicatie gebruikt SQL Server om gegevens over te dragen. Deze methode wordt gebruikt om wijzigingen in de site database samen te voegen met de informatie uit de Data Base op andere sites in de hiërarchie.

Zie [database replicatie](database-replication.md)voor meer informatie.

Zie [problemen met SQL-replicatie oplossen](../../servers/manage/replication/overview.md)voor hulp bij het oplossen van problemen met SQL-replicatie.

## <a name="see-also"></a>Zie ook

[Replicatie controleren](../../servers/manage/monitor-replication.md)
