---
title: Отключение отслеживания запросов - EF6
author: divega
ms.date: 2016-10-23
ms.prod: entity-framework
ms.author: divega
ms.manager: avickers
ms.technology: entity-framework-6
ms.topic: article
ms.assetid: f80ac260-c2dc-484d-94a3-3424fd862f8b
caps.latest.revision: 3
ms.openlocfilehash: 8310f2dab9e7ed9197a8c3e875e47e4f7b72d279
ms.sourcegitcommit: f05e7b62584cf228f17390bb086a61d505712e1b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/08/2018
ms.locfileid: "39122294"
---
# <a name="no-tracking-queries"></a><span data-ttu-id="f1cd4-102">и без отслеживания</span><span class="sxs-lookup"><span data-stu-id="f1cd4-102">No-Tracking Queries</span></span>
<span data-ttu-id="f1cd4-103">Иногда может потребоваться вернуться к сущности на основе запроса, но нет элементов, отслеживаемые по контексту.</span><span class="sxs-lookup"><span data-stu-id="f1cd4-103">Sometimes you may want to get entities back from a query but not have those entities be tracked by the context.</span></span> <span data-ttu-id="f1cd4-104">Это может привести к повышению производительности, при запросе большого количества сущностей в сценариях только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f1cd4-104">This may result in better performance when querying for large numbers of entities in read-only scenarios.</span></span> <span data-ttu-id="f1cd4-105">Методы, представленные в этом разделе, также применимы к моделям, созданным с помощью Code First и конструктора EF.</span><span class="sxs-lookup"><span data-stu-id="f1cd4-105">The techniques shown in this topic apply equally to models created with Code First and the EF Designer.</span></span>  

<span data-ttu-id="f1cd4-106">Новый метод расширения AsNoTracking позволяет любому запросу, чтобы выполняться таким образом.</span><span class="sxs-lookup"><span data-stu-id="f1cd4-106">A new extension method AsNoTracking allows any query to be run in this way.</span></span> <span data-ttu-id="f1cd4-107">Пример:</span><span class="sxs-lookup"><span data-stu-id="f1cd4-107">For example:</span></span>  

``` csharp
using (var context = new BloggingContext())
{
    // Query for all blogs without tracking them
    var blogs1 = context.Blogs.AsNoTracking();

    // Query for some blogs without tracking them
    var blogs2 = context.Blogs
                        .Where(b => b.Name.Contains(".NET"))
                        .AsNoTracking()
                        .ToList();
}
```  