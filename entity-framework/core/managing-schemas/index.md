---
title: Управление схемами баз данных — EF Core
author: bricelam
ms.date: 10/30/2017
ms.openlocfilehash: c1ebe33b5575cab76a54721ef86ecbcb7ff8b98b
ms.sourcegitcommit: dadee5905ada9ecdbae28363a682950383ce3e10
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/27/2018
ms.locfileid: "42994389"
---
# <a name="managing-database-schemas"></a>Управление схемами баз данных
EF Core предоставляет два основных способа синхронизации схемы базы данных и модели EF Core. Чтобы выбрать один из них, определите, что является истинным — ваша схема базы данных или модель EF Core.

Если истинной должна быть модель EF Core, используйте [миграции][1]. При внесении изменений в модель EF Core этот подход постепенно применяет соответствующие изменения схемы к базе данных, чтобы она оставалась совместимой с вашей моделью EF Core.

Используйте [реконструирование][2], если хотите сделать истинной схему базы данных. Этот подход позволяет формировать DbContext и классы типов сущностей, реконструируя схему базы данных в модель EF Core.

> [!NOTE]
> [API создания и удаления][3] также позволяют создать схему базы данных из модели EF Core. Но они предназначены главным образом для тестирования, создания прототипов и других сценариев, где допустимо удаление базы данных.


  [1]: migrations/index.md
  [2]: scaffolding.md
  [3]: ensure-created.md
