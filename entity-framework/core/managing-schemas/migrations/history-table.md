---
title: Таблица журнала пользовательских миграции — EF Core
author: bricelam
ms.author: bricelam
ms.date: 11/07/2017
ms.openlocfilehash: 1a253972a8f4e410421ec8a77c079e588d368819
ms.sourcegitcommit: 2b787009fd5be5627f1189ee396e708cd130e07b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/13/2018
ms.locfileid: "45488820"
---
<a name="custom-migrations-history-table"></a>Таблица миграции пользовательского журнала
===============================
По умолчанию EF Core следит за миграций, которые были применены к базе данных, записав их в таблицу с именем `__EFMigrationsHistory`. По различным причинам можно настроить эту таблицу для удовлетворения ваших потребностей.

> [!IMPORTANT]
> Если вы настраиваете таблице журнала миграции *после* применение миграций, вы несете ответственность за обновление существующей таблицы в базе данных.

<a name="schema-and-table-name"></a>Имя схемы и таблицы
----------------------
Можно изменить схему и имя таблицы с помощью `MigrationsHistoryTable()` метод в `OnConfiguring()` (или `ConfigureServices()` на ASP.NET Core). Ниже приведен пример с помощью поставщика SQL Server EF Core.

``` csharp
protected override void OnConfiguring(DbContextOptionsBuilder options)
    => options.UseSqlServer(
        connectionString,
        x => x.MigrationsHistoryTable("__MyMigrationsHistory", "mySchema"));
```

<a name="other-changes"></a>Прочие изменения
-------------
Чтобы настроить дополнительные аспекты класса таблицы, переопределение и замените специфический для поставщика `IHistoryRepository` службы. Ниже приведен пример изменения имени столбца MigrationId для *идентификатор* на сервере SQL Server.

``` csharp
protected override void OnConfiguring(DbContextOptionsBuilder options)
    => options
        .UseSqlServer(connectionString)
        .ReplaceService<IHistoryRepository, MyHistoryRepository>();
```

> [!WARNING]
> `SqlServerHistoryRepository` находится внутри внутреннего пространства имен и может измениться в будущих версиях.

``` csharp
class MyHistoryRepository : SqlServerHistoryRepository
{
    public MyHistoryRepository(HistoryRepositoryDependencies dependencies)
        : base(dependencies)
    {
    }

    protected override void ConfigureTable(EntityTypeBuilder<HistoryRow> history)
    {
        base.ConfigureTable(history);

        history.Property(h => h.MigrationId).HasColumnName("Id");
    }
}
```
