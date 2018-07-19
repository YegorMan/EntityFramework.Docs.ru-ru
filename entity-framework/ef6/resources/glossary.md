---
title: Глоссарий Entity Framework - EF6
author: divega
ms.date: 2016-10-23
ms.prod: entity-framework
ms.author: divega
ms.manager: avickers
ms.technology: entity-framework-6
ms.topic: article
ms.assetid: 3f05ffdd-49bc-499c-9732-4a368bf5d2d7
caps.latest.revision: 3
ms.openlocfilehash: cbd61838afc23dfb37cee7c624c65476c5270099
ms.sourcegitcommit: bdd06c9a591ba5e6d6a3ec046c80de98f598f3f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/10/2018
ms.locfileid: "39122734"
---
# <a name="entity-framework-glossary"></a><span data-ttu-id="81c08-102">Глоссарий Entity Framework</span><span class="sxs-lookup"><span data-stu-id="81c08-102">Entity Framework Glossary</span></span>
## <a name="code-first"></a><span data-ttu-id="81c08-103">Code First</span><span class="sxs-lookup"><span data-stu-id="81c08-103">Code First</span></span>
<span data-ttu-id="81c08-104">Создание модели Entity Framework с помощью кода.</span><span class="sxs-lookup"><span data-stu-id="81c08-104">Creating an Entity Framework model using code.</span></span> <span data-ttu-id="81c08-105">Модели можно ориентироваться и существующей базы данных, или новую базу данных.</span><span class="sxs-lookup"><span data-stu-id="81c08-105">The model can target and existing database or a new database.</span></span>

## <a name="context"></a><span data-ttu-id="81c08-106">Контекст</span><span class="sxs-lookup"><span data-stu-id="81c08-106">Context</span></span>
<span data-ttu-id="81c08-107">Класс, представляющий сеанс с базой данных, позволяя запрашивать и сохранять данные.</span><span class="sxs-lookup"><span data-stu-id="81c08-107">A class that represents a session with the database, allowing you to query and save data.</span></span> <span data-ttu-id="81c08-108">Контекст является производным от класса DbContext или ObjectContext.</span><span class="sxs-lookup"><span data-stu-id="81c08-108">A context derives from the DbContext or ObjectContext class.</span></span>

## <a name="convention-code-first"></a><span data-ttu-id="81c08-109">Соглашение об (Code First)</span><span class="sxs-lookup"><span data-stu-id="81c08-109">Convention (Code First)</span></span>
<span data-ttu-id="81c08-110">Правило, которое используют Entity Framework для определения вида модели из классов.</span><span class="sxs-lookup"><span data-stu-id="81c08-110">A rule that Entity Framework uses to infer the shape of you model from your classes.</span></span>

## <a name="database-first"></a><span data-ttu-id="81c08-111">Сначала базы данных</span><span class="sxs-lookup"><span data-stu-id="81c08-111">Database First</span></span>
<span data-ttu-id="81c08-112">Создание модели Entity Framework, в конструкторе EF, нацеленный существующей базы данных.</span><span class="sxs-lookup"><span data-stu-id="81c08-112">Creating an Entity Framework model, using the EF Designer, that targets an existing database.</span></span>

## <a name="eager-loading"></a><span data-ttu-id="81c08-113">Безотложная загрузка</span><span class="sxs-lookup"><span data-stu-id="81c08-113">Eager loading</span></span>
<span data-ttu-id="81c08-114">Шаблон загрузка связанных данных, где запрос для одного типа сущности также загружает связанные сущности как часть запроса.</span><span class="sxs-lookup"><span data-stu-id="81c08-114">A pattern of loading related data where a query for one type of entity also loads related entities as part of the query.</span></span>

## <a name="ef-designer"></a><span data-ttu-id="81c08-115">Конструктор EF</span><span class="sxs-lookup"><span data-stu-id="81c08-115">EF Designer</span></span>
<span data-ttu-id="81c08-116">Визуальный конструктор в Visual Studio, можно создать модель Entity Framework с помощью полей и строк.</span><span class="sxs-lookup"><span data-stu-id="81c08-116">A visual designer in Visual Studio that allows you to create an Entity Framework model using boxes and lines.</span></span>

## <a name="entity"></a><span data-ttu-id="81c08-117">Объект</span><span class="sxs-lookup"><span data-stu-id="81c08-117">Entity</span></span>
<span data-ttu-id="81c08-118">Класс или объект, представляющий данные приложения, такие как клиенты, продукты и заказы.</span><span class="sxs-lookup"><span data-stu-id="81c08-118">A class or object that represents application data such as customers, products, and orders.</span></span>

## <a name="entity-data-model"></a><span data-ttu-id="81c08-119">EDM (модель данных с использованием сущностей)</span><span class="sxs-lookup"><span data-stu-id="81c08-119">Entity Data Model</span></span>
<span data-ttu-id="81c08-120">Модели, описывающий сущности и связи между ними.</span><span class="sxs-lookup"><span data-stu-id="81c08-120">A model that describes entities and the relationships between them.</span></span> <span data-ttu-id="81c08-121">EF использует модель EDM для описания концептуальной модели, для которого программы для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="81c08-121">EF uses EDM to describe the conceptual model against which the developer programs.</span></span> <span data-ttu-id="81c08-122">EDM строится на модели отношений сущностей, представленных аварийного восстановления. Питером Ченом.</span><span class="sxs-lookup"><span data-stu-id="81c08-122">EDM builds on the Entity Relationship model introduced by Dr. Peter Chen.</span></span> <span data-ttu-id="81c08-123">Модель EDM, первоначально был разработан с основной задачей функции становятся модели общих данных всей технологий разработки и серверных технологий от корпорации Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="81c08-123">The EDM was originally developed with the primary goal of becoming the common data model across a suite of developer and server technologies from Microsoft.</span></span> <span data-ttu-id="81c08-124">Модель EDM также используется как часть протокола OData.</span><span class="sxs-lookup"><span data-stu-id="81c08-124">EDM is also used as part of the OData protocol.</span></span>

## <a name="explicit-loading"></a><span data-ttu-id="81c08-125">Явная загрузка</span><span class="sxs-lookup"><span data-stu-id="81c08-125">Explicit loading</span></span>
<span data-ttu-id="81c08-126">Шаблон загрузка связанных данных, где связанные объекты загружаются путем вызова API.</span><span class="sxs-lookup"><span data-stu-id="81c08-126">A pattern of loading related data where related objects are loaded by calling an API.</span></span>

## <a name="fluent-api"></a><span data-ttu-id="81c08-127">Текучий API</span><span class="sxs-lookup"><span data-stu-id="81c08-127">Fluent API</span></span>
<span data-ttu-id="81c08-128">Интерфейс API, который может использоваться для настройки модели Code First.</span><span class="sxs-lookup"><span data-stu-id="81c08-128">An API that can be used to configure a Code First model.</span></span>

## <a name="foreign-key-association"></a><span data-ttu-id="81c08-129">Ассоциации внешнего ключа</span><span class="sxs-lookup"><span data-stu-id="81c08-129">Foreign key association</span></span>
<span data-ttu-id="81c08-130">Ассоциация между сущностями, где свойство, которое представляет внешний ключ включен в классе зависимой сущности.</span><span class="sxs-lookup"><span data-stu-id="81c08-130">An association between entities where a property that represents the foreign key is included in the class of the dependent entity.</span></span> <span data-ttu-id="81c08-131">Например продукт содержит свойства CategoryId.</span><span class="sxs-lookup"><span data-stu-id="81c08-131">For example, Product contains a CategoryId property.</span></span>

## <a name="identifying-relationship"></a><span data-ttu-id="81c08-132">Идентифицирующее отношение</span><span class="sxs-lookup"><span data-stu-id="81c08-132">Identifying relationship</span></span>
<span data-ttu-id="81c08-133">Отношение, в котором первичный ключ основной сущности является частью первичного ключа зависимой сущности.</span><span class="sxs-lookup"><span data-stu-id="81c08-133">A relationship where the primary key of the principal entity is part of the primary key of the dependent entity.</span></span> <span data-ttu-id="81c08-134">В таком отношении зависимая сущность не может существовать без основной.</span><span class="sxs-lookup"><span data-stu-id="81c08-134">In this kind of relationship, the dependent entity cannot exist without the principal entity.</span></span>

## <a name="independent-association"></a><span data-ttu-id="81c08-135">Независимое сопоставление</span><span class="sxs-lookup"><span data-stu-id="81c08-135">Independent association</span></span>
<span data-ttu-id="81c08-136">Ассоциации между сущностями там, где отсутствует свойство, представляющее внешний ключ в классе зависимой сущности.</span><span class="sxs-lookup"><span data-stu-id="81c08-136">An association between entities where there is no property representing the foreign key in the class of the dependent entity.</span></span> <span data-ttu-id="81c08-137">Например класс Product содержит связь категории, но нет свойства CategoryId.</span><span class="sxs-lookup"><span data-stu-id="81c08-137">For example, a Product class contains a relationship to Category but no CategoryId property.</span></span> <span data-ttu-id="81c08-138">Платформа Entity Framework отслеживает состояние ассоциации независимо от состояния сущностей в две ассоциации.</span><span class="sxs-lookup"><span data-stu-id="81c08-138">Entity Framework tracks the state of the association independently of the state of the entities at the two association ends.</span></span>

## <a name="lazy-loading"></a><span data-ttu-id="81c08-139">«Неспешная» загрузка</span><span class="sxs-lookup"><span data-stu-id="81c08-139">Lazy loading</span></span>
<span data-ttu-id="81c08-140">Шаблон загрузка связанных данных, где связанные объекты автоматически загружаются при обращении к свойству навигации.</span><span class="sxs-lookup"><span data-stu-id="81c08-140">A pattern of loading related data where related objects are automatically loaded when a navigation property is accessed.</span></span>

## <a name="model-first"></a><span data-ttu-id="81c08-141">Model First</span><span class="sxs-lookup"><span data-stu-id="81c08-141">Model First</span></span>
<span data-ttu-id="81c08-142">Создание модели Entity Framework, в конструкторе EF, который затем используется для создания новой базы данных.</span><span class="sxs-lookup"><span data-stu-id="81c08-142">Creating an Entity Framework model, using the EF Designer, that is then used to create a new database.</span></span>

## <a name="navigation-property"></a><span data-ttu-id="81c08-143">Свойство навигации</span><span class="sxs-lookup"><span data-stu-id="81c08-143">Navigation property</span></span>
<span data-ttu-id="81c08-144">Свойство сущности, которая ссылается на другую сущность.</span><span class="sxs-lookup"><span data-stu-id="81c08-144">A property of an entity that references another entity.</span></span> <span data-ttu-id="81c08-145">Например продукт содержит свойство навигации категория и категория содержит свойства навигации продуктов.</span><span class="sxs-lookup"><span data-stu-id="81c08-145">For example, Product contains a Category navigation property and Category contains a Products navigation property.</span></span>

## <a name="poco"></a><span data-ttu-id="81c08-146">POCO</span><span class="sxs-lookup"><span data-stu-id="81c08-146">POCO</span></span>
<span data-ttu-id="81c08-147">Управляющий объект Plain Old CLR.</span><span class="sxs-lookup"><span data-stu-id="81c08-147">Acronym for Plain-Old CLR Object.</span></span> <span data-ttu-id="81c08-148">Простой пользовательский класс, который не имеет зависимостей на любой платформе.</span><span class="sxs-lookup"><span data-stu-id="81c08-148">A simple user class that has no dependencies with any framework.</span></span> <span data-ttu-id="81c08-149">В контексте EF класс сущностей, который не является производным от класса EntityObject, реализующий интерфейсы или содержит все атрибуты, определенные в EF.</span><span class="sxs-lookup"><span data-stu-id="81c08-149">In the context of EF, a an entity class that does not derive from EntityObject, implements any interfaces or carries any attributes defined in EF.</span></span> <span data-ttu-id="81c08-150">Такие классы сущностей, которые связаны с инфраструктуру сохранения, также называются «сохраняемость».</span><span class="sxs-lookup"><span data-stu-id="81c08-150">Such entity classes that are decoupled from the persistence framework are also said to be "persistence ignorant".</span></span>  

## <a name="relationship-inverse"></a><span data-ttu-id="81c08-151">Обратная связь</span><span class="sxs-lookup"><span data-stu-id="81c08-151">Relationship inverse</span></span>
<span data-ttu-id="81c08-152">Противоположный конец связи, например, продукт. Категория и категория. Продукт.</span><span class="sxs-lookup"><span data-stu-id="81c08-152">The opposite end of a relationship, for example, product.Category and category.Product.</span></span>

## <a name="self-tracking-entity"></a><span data-ttu-id="81c08-153">Сущности с самостоятельным отслеживанием</span><span class="sxs-lookup"><span data-stu-id="81c08-153">Self-tracking entity</span></span>
<span data-ttu-id="81c08-154">Сущность, построенная на основе шаблона создания кода, которые помогут в разработке N-уровневых проектов.</span><span class="sxs-lookup"><span data-stu-id="81c08-154">An entity built from a code generation template that helps with N-Tier development.</span></span>

## <a name="table-per-concrete-type-tpc"></a><span data-ttu-id="81c08-155">Таблица на конкретный тип (TPC)</span><span class="sxs-lookup"><span data-stu-id="81c08-155">Table-per-concrete type (TPC)</span></span>
<span data-ttu-id="81c08-156">Метод сопоставления наследования, которой сопоставлен каждого неабстрактный тип в иерархии для разделения таблицы в базе данных.</span><span class="sxs-lookup"><span data-stu-id="81c08-156">A method of mapping the inheritance where each non-abstract type in the hierarchy is mapped to separate table in the database.</span></span>

## <a name="table-per-hierarchy-tph"></a><span data-ttu-id="81c08-157">Одна таблица на иерархию (TPH)</span><span class="sxs-lookup"><span data-stu-id="81c08-157">Table-per-hierarchy (TPH)</span></span>
<span data-ttu-id="81c08-158">Метод сопоставления наследования, где все типы в иерархии сопоставляются ту же таблицу в базе данных.</span><span class="sxs-lookup"><span data-stu-id="81c08-158">A method of mapping the inheritance where all types in the hierarchy are mapped to the same table in the database.</span></span> <span data-ttu-id="81c08-159">С связан дискриминатора столбцов используется для определения, какой тип каждой строки.</span><span class="sxs-lookup"><span data-stu-id="81c08-159">A discriminator column(s) is used to identify what type each row is associated with.</span></span>

## <a name="table-per-type-tpt"></a><span data-ttu-id="81c08-160">Одна таблица на тип (TPT)</span><span class="sxs-lookup"><span data-stu-id="81c08-160">Table-per-type (TPT)</span></span>
<span data-ttu-id="81c08-161">Метод сопоставления наследования, где общие свойства всех типов в иерархии, сопоставляются ту же таблицу в базе данных, но свойства, уникальные для каждого типа сопоставляются с отдельной таблицей.</span><span class="sxs-lookup"><span data-stu-id="81c08-161">A method of mapping the inheritance where the common properties of all types in the hierarchy are mapped to the same table in the database, but properties unique to each type are mapped to a separate table.</span></span>

## <a name="type-discovery"></a><span data-ttu-id="81c08-162">Обнаружение типа</span><span class="sxs-lookup"><span data-stu-id="81c08-162">Type discovery</span></span>
<span data-ttu-id="81c08-163">Процесс определения типов, которые должны быть частью модели Entity Framework.</span><span class="sxs-lookup"><span data-stu-id="81c08-163">The process of identifying the types that should be part of an Entity Framework model.</span></span>