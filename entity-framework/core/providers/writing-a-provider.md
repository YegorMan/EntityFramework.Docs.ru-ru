---
title: "Разработка поставщика базы данных - EF Core"
author: anmiller
ms.author: divega
ms.date: 10/27/2016
ms.assetid: 1165e2ec-e421-43fc-92ab-d92f9ab3c494
ms.technology: entity-framework-core
uid: core/providers/writing-a-provider
ms.openlocfilehash: 9d6d3748a9097b3b8eeee2a8a516c53f3b2afa58
ms.sourcegitcommit: 01a75cd483c1943ddd6f82af971f07abde20912e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2017
---
# <a name="writing-a-database-provider"></a><span data-ttu-id="820d9-102">Разработка поставщика базы данных</span><span class="sxs-lookup"><span data-stu-id="820d9-102">Writing a Database Provider</span></span>

<span data-ttu-id="820d9-103">Сведения о создании поставщика Entity Framework Core базы данных см. в разделе [, требуется написать поставщик EF Core](https://blog.oneunicorn.com/2016/11/11/so-you-want-to-write-an-ef-core-provider/) по [Vickers Артуром](https://github.com/ajcvickers).</span><span class="sxs-lookup"><span data-stu-id="820d9-103">For information about writing an Entity Framework Core database provider, see [So you want to write an EF Core provider](https://blog.oneunicorn.com/2016/11/11/so-you-want-to-write-an-ef-core-provider/) by [Arthur Vickers](https://github.com/ajcvickers).</span></span>

<span data-ttu-id="820d9-104">База кода EF Core является открытым исходным кодом и содержит несколько поставщиков базы данных, которые могут использоваться в качестве ссылки.</span><span class="sxs-lookup"><span data-stu-id="820d9-104">The EF Core code base is open source and contains several database providers that can be used as a reference.</span></span> <span data-ttu-id="820d9-105">Исходный код можно найти в https://github.com/aspnet/EntityFramework.</span><span class="sxs-lookup"><span data-stu-id="820d9-105">You can find the source code at https://github.com/aspnet/EntityFramework.</span></span>

## <a name="the-providers-beware-label"></a><span data-ttu-id="820d9-106">Поставщики Берегитесь метки</span><span class="sxs-lookup"><span data-stu-id="820d9-106">The providers-beware label</span></span>

<span data-ttu-id="820d9-107">После начала работы над поставщика следить за [ `providers-beware` ](https://github.com/aspnet/EntityFramework/labels/providers-beware) метка на нашем GitHub проблемы и запросы на получение.</span><span class="sxs-lookup"><span data-stu-id="820d9-107">Once you begin work on a provider, watch for the [`providers-beware`](https://github.com/aspnet/EntityFramework/labels/providers-beware) label on our GitHub issues and pull requests.</span></span> <span data-ttu-id="820d9-108">Мы используем эту метку для выявления изменений, которые могут влиять на модули записи поставщика.</span><span class="sxs-lookup"><span data-stu-id="820d9-108">We use this label to identify changes that may impact provider writers.</span></span>

## <a name="suggested-naming-of-third-party-providers"></a><span data-ttu-id="820d9-109">Предлагаемые именования сторонних поставщиков</span><span class="sxs-lookup"><span data-stu-id="820d9-109">Suggested naming of third party providers</span></span>

<span data-ttu-id="820d9-110">Мы советуем использовать с помощью следующих именования для пакетов NuGet.</span><span class="sxs-lookup"><span data-stu-id="820d9-110">We suggest using the following naming for NuGet packages.</span></span> <span data-ttu-id="820d9-111">Это согласуется с именами пакетов, предоставляемых EF основная группа.</span><span class="sxs-lookup"><span data-stu-id="820d9-111">This is consistent with the names of packages delivered by the EF Core team.</span></span>

`<Optional project/company name>.EntityFrameworkCore.<Database engine name>`

<span data-ttu-id="820d9-112">Например:</span><span class="sxs-lookup"><span data-stu-id="820d9-112">For example:</span></span>
* `Microsoft.EntityFrameworkCore.SqlServer`
* `Npgsql.EntityFrameworkCore.PostgreSQL`
* `EntityFrameworkCore.SqlServerCompact40`