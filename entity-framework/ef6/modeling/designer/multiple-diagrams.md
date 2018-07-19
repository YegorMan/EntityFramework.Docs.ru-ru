---
title: Несколько диаграмм на каждую модель - EF6
author: divega
ms.date: 2016-10-23
ms.prod: entity-framework
ms.author: divega
ms.manager: avickers
ms.technology: entity-framework-6
ms.topic: article
ms.assetid: b95db5c8-de8d-43bd-9ccc-5df6a5e25e1b
caps.latest.revision: 3
ms.openlocfilehash: 3a022b3e44ecd4b6b62224cb6494c794397a9739
ms.sourcegitcommit: 390f3a37bc55105ed7cc5b0e0925b7f9c9e80ba6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/09/2018
ms.locfileid: "39122582"
---
# <a name="multiple-diagrams-per-model"></a><span data-ttu-id="1ee2c-102">Несколько диаграмм на модель</span><span class="sxs-lookup"><span data-stu-id="1ee2c-102">Multiple Diagrams per Model</span></span>
> [!NOTE]
> <span data-ttu-id="1ee2c-103">**EF5 и более поздних версий только** -функции, интерфейсы API, и т.д., описанных на этой странице появились в Entity Framework 5.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-103">**EF5 Onwards Only** - The features, APIs, etc. discussed in this page were introduced in Entity Framework 5.</span></span> <span data-ttu-id="1ee2c-104">При использовании более ранней версии могут быть неприменимы некоторые или все сведения.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-104">If you are using an earlier version, some or all of the information does not apply.</span></span>

<span data-ttu-id="1ee2c-105">Это видео и странице показано, как разделить модель на несколько схем, с помощью Entity Framework Designer (конструктор EF).</span><span class="sxs-lookup"><span data-stu-id="1ee2c-105">This video and page shows how to split a model into multiple diagrams using the Entity Framework Designer (EF Designer).</span></span> <span data-ttu-id="1ee2c-106">Можно использовать эту функцию, когда ваша модель становится слишком большим, чтобы просмотреть или изменить.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-106">You might want to use this feature when your model becomes too large to view or edit.</span></span>

<span data-ttu-id="1ee2c-107">В более ранних версиях конструктор EF одной схеме может иметь только каждого EDMX-файла.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-107">In earlier versions of the EF Designer you could only have one diagram per the EDMX file.</span></span> <span data-ttu-id="1ee2c-108">Начиная с Visual Studio 2012, можно использовать конструктор EF для разбиения в EDMX-файла на несколько схем.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-108">Starting with Visual Studio 2012, you can use the EF Designer to split your EDMX file into multiple diagrams.</span></span>

## <a name="watch-the-video"></a><span data-ttu-id="1ee2c-109">Просмотреть видео</span><span class="sxs-lookup"><span data-stu-id="1ee2c-109">Watch the video</span></span>
<span data-ttu-id="1ee2c-110">В этом видео показано, как разделить модель на несколько схем, с помощью Entity Framework Designer (конструктор EF).</span><span class="sxs-lookup"><span data-stu-id="1ee2c-110">This video shows how to split a model into multiple diagrams using the Entity Framework Designer (EF Designer).</span></span> <span data-ttu-id="1ee2c-111">Можно использовать эту функцию, когда ваша модель становится слишком большим, чтобы просмотреть или изменить.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-111">You might want to use this feature when your model becomes too large to view or edit.</span></span>

<span data-ttu-id="1ee2c-112">**Представленный**: Юлия Корнич</span><span class="sxs-lookup"><span data-stu-id="1ee2c-112">**Presented By**: Julia Kornich</span></span>

<span data-ttu-id="1ee2c-113">**Видео**: [WMV](http://download.microsoft.com/download/5/C/2/5C2B52AB-5532-426F-B078-1E253341B5FA/HDI-ITPro-MSDN-winvideo-multiplediagrams.wmv) | [MP4](http://download.microsoft.com/download/5/C/2/5C2B52AB-5532-426F-B078-1E253341B5FA/HDI-ITPro-MSDN-mp4video-multiplediagrams.m4v) | [WMV (ZIP)](http://download.microsoft.com/download/5/C/2/5C2B52AB-5532-426F-B078-1E253341B5FA/HDI-ITPro-MSDN-winvideo-multiplediagrams.zip)</span><span class="sxs-lookup"><span data-stu-id="1ee2c-113">**Video**: [WMV](http://download.microsoft.com/download/5/C/2/5C2B52AB-5532-426F-B078-1E253341B5FA/HDI-ITPro-MSDN-winvideo-multiplediagrams.wmv) | [MP4](http://download.microsoft.com/download/5/C/2/5C2B52AB-5532-426F-B078-1E253341B5FA/HDI-ITPro-MSDN-mp4video-multiplediagrams.m4v) | [WMV (ZIP)](http://download.microsoft.com/download/5/C/2/5C2B52AB-5532-426F-B078-1E253341B5FA/HDI-ITPro-MSDN-winvideo-multiplediagrams.zip)</span></span>

## <a name="ef-designer-overview"></a><span data-ttu-id="1ee2c-114">Общие сведения о конструкторе EF</span><span class="sxs-lookup"><span data-stu-id="1ee2c-114">EF Designer Overview</span></span>

<span data-ttu-id="1ee2c-115">При создании модели с помощью мастера моделей EDM конструкторе EF, EDMX-файл создается и добавляется в решение.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-115">When you create a model using the EF Designer’s Entity Data Model Wizard, an .edmx file is created and added to your solution.</span></span> <span data-ttu-id="1ee2c-116">Этот файл определяет форму сущностей и их сопоставлении в базу данных.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-116">This file defines the shape of your entities and how they map to the database.</span></span>

<span data-ttu-id="1ee2c-117">Конструктор EF состоит из следующих компонентов:</span><span class="sxs-lookup"><span data-stu-id="1ee2c-117">The EF Designer consists of the following components:</span></span>

-   <span data-ttu-id="1ee2c-118">Визуальную область конструктора для редактирования модели.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-118">A visual design surface for editing the model.</span></span> <span data-ttu-id="1ee2c-119">Сущности и взаимосвязи можно создавать, изменять или удалять.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-119">You can create, modify, or delete entities and associations.</span></span>
-   <span data-ttu-id="1ee2c-120">Объект **браузер моделей** окно, обеспечивающее три представления модели.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-120">A **Model Browser** window that provides tree views of the model.</span></span>  <span data-ttu-id="1ee2c-121">Сущности и связи расположены под *\[ModelName\]* папки.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-121">The entities and their associations are located under the *\[ModelName\]* folder.</span></span> <span data-ttu-id="1ee2c-122">В таблицах базы данных и ограничениях, находятся в разделе  *\[ModelName\]*. Папка Store.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-122">The database tables and constraints are located under the *\[ModelName\]*.Store folder.</span></span>
-   <span data-ttu-id="1ee2c-123">Объект **сведения о сопоставлении** окно для просмотра и редактирования сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-123">A **Mapping Details** window for viewing and editing mappings.</span></span> <span data-ttu-id="1ee2c-124">Типы сущностей и взаимосвязи можно сопоставить с таблицами базы данных, столбцами и хранимыми процедурами.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-124">You can map entity types or associations to database tables, columns, and stored procedures.</span></span> 

<span data-ttu-id="1ee2c-125">Окно поверхности визуальной разработки автоматически открывается после завершения работы мастера модели EDM.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-125">The visual design surface window is automatically opened when the Entity Data Model Wizard finishes.</span></span> <span data-ttu-id="1ee2c-126">Если браузер моделей не отображается, щелкните правой кнопкой мыши главную область конструктора и выберите **браузер моделей**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-126">If the Model Browser is not visible, right-click the main design surface and select **Model Browser**.</span></span>

<span data-ttu-id="1ee2c-127">На следующем снимке экрана показаны EDMX-файл открывается в конструкторе EF.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-127">The following screenshot shows an .edmx file opened in the EF Designer.</span></span> <span data-ttu-id="1ee2c-128">На снимке экрана показаны область визуального конструирования (слева) и **браузер моделей** окна (справа).</span><span class="sxs-lookup"><span data-stu-id="1ee2c-128">The screenshot shows the visual design surface (to the left) and the **Model Browser** window (to the right).</span></span>

![EFDesigner2](~/ef6/media/efdesigner2.png)

<span data-ttu-id="1ee2c-130">Чтобы отменить операцию в конструкторе EF, нажмите сочетание клавиш Ctrl-Z.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-130">To undo an operation done in the EF Designer, click Ctrl-Z.</span></span>

## <a name="working-with-diagrams"></a><span data-ttu-id="1ee2c-131">Работа со схемами</span><span class="sxs-lookup"><span data-stu-id="1ee2c-131">Working with Diagrams</span></span>

<span data-ttu-id="1ee2c-132">По умолчанию конструктор EF создает вызывается Diagram1 одной схеме.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-132">By default the EF Designer creates one diagram called Diagram1.</span></span> <span data-ttu-id="1ee2c-133">Если у вас есть диаграмму с большим числом сущностей и ассоциаций, будет наиболее как логически разделить их.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-133">If you have a diagram with a large number of entities and associations, you will most like want to split them up logically.</span></span> <span data-ttu-id="1ee2c-134">Начиная с Visual Studio 2012, можно просмотреть концептуальной модели на нескольких схемах.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-134">Starting with Visual Studio 2012, you can view your conceptual model in multiple diagrams.</span></span>   

<span data-ttu-id="1ee2c-135">По мере добавления новых схем, они отображаются в папке схемы в окне браузера модели.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-135">As you add new diagrams, they appear under the Diagrams folder in the Model Browser window.</span></span> <span data-ttu-id="1ee2c-136">Переименование диаграммы: выберите схему в окне браузера модели, щелкните один раз имя и введите новое имя.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-136">To rename a diagram: select the diagram in the Model Browser window, click once on the name, and type the new name.</span></span>  <span data-ttu-id="1ee2c-137">Можно также правой кнопкой мыши имя диаграммы и выберите **Переименовать**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-137">You can also right-click the diagram name and select **Rename**.</span></span>

<span data-ttu-id="1ee2c-138">Имя диаграммы отображается рядом с именем файла .edmx, в редакторе Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-138">The diagram name is displayed next to the .edmx file name, in the Visual Studio editor.</span></span> <span data-ttu-id="1ee2c-139">Например Model1.edmx\[Diagram1\].</span><span class="sxs-lookup"><span data-stu-id="1ee2c-139">For example Model1.edmx\[Diagram1\].</span></span>

![Имя_диаграммы](~/ef6/media/diagramname.png)

<span data-ttu-id="1ee2c-141">Содержимое схемы (форма и цвет сущностей и ассоциаций) хранится в. файл edmx.diagram.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-141">The diagrams content (shape and color of entities and associations) is stored in the .edmx.diagram file.</span></span> <span data-ttu-id="1ee2c-142">Чтобы просмотреть этот файл, выберите обозреватель решений и раскрыть EDMX-файл.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-142">To view this file, select Solution Explorer and unfold the .edmx file.</span></span> 

![DiagramFiles](~/ef6/media/diagramfiles.png)

<span data-ttu-id="1ee2c-144">Не следует изменять. edmx.diagram файл вручную, содержимое этого файла может быть перезаписан в конструкторе EF.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-144">You should not edit the .edmx.diagram file manually, the content of this file maybe overwritten by the EF Designer.</span></span>
 
## <a name="splitting-entities-and-associations-into-a-new-diagram"></a><span data-ttu-id="1ee2c-145">Разделение сущностей и ассоциаций в новую схему</span><span class="sxs-lookup"><span data-stu-id="1ee2c-145">Splitting Entities and Associations into a New Diagram</span></span>

<span data-ttu-id="1ee2c-146">Вы можете выбрать сущностей на существующую диаграмму (удерживайте клавишу Shift, чтобы выбрать несколько сущностей).</span><span class="sxs-lookup"><span data-stu-id="1ee2c-146">You can select entities on the existing diagram (hold Shift to select multiple entities).</span></span> <span data-ttu-id="1ee2c-147">Щелкните правой кнопкой мыши и выберите **переместить в новую схему**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-147">Click the right mouse button and select **Move to new Diagram**.</span></span> <span data-ttu-id="1ee2c-148">Новая схема, и выбранные сущности и их связи, перемещаются в схему.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-148">The new diagram is created and the selected entities and their associations are moved to the diagram.</span></span>

<span data-ttu-id="1ee2c-149">Кроме того, щелкните правой кнопкой мыши папку схемы в браузере моделей и выберите **добавить новую схему.**</span><span class="sxs-lookup"><span data-stu-id="1ee2c-149">Alternatively, you can right-click the Diagrams folder in Model Browser and select **Add new Diagram.**</span></span> <span data-ttu-id="1ee2c-150">Затем можно перетащить и перетаскивать сущности из папки типы сущностей в браузере моделей, в область конструктора.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-150">You can then drag and drop entities from under the Entity Types folder in Model Browser onto the design surface.</span></span>

<span data-ttu-id="1ee2c-151">Также можно вырезать или копировать из одной схемы сущностей (с помощью клавиш Ctrl + X или Ctrl + C) и вставить (с помощью ключа Ctrl + V) на другой.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-151">You can also cut or copy entities (using Ctrl-X or Ctrl-C keys) from one diagram and paste (using Ctrl-V key) on the other.</span></span> <span data-ttu-id="1ee2c-152">Если схема, в который копируются сущности уже содержит сущность с тем же именем, новую сущность создана и добавлена в модель.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-152">If the diagram into which you are pasting an entity already contains an entity with the same name, a new entity will be created and added to the model.</span></span>  <span data-ttu-id="1ee2c-153">Например: схемы 2 содержит сущность.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-153">For example: Diagram2 contains the Department entity.</span></span> <span data-ttu-id="1ee2c-154">Затем вы вставьте другой отдел на схемы 2.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-154">Then, you paste another Department on Diagram2.</span></span> <span data-ttu-id="1ee2c-155">Сущность Department1 создается и добавляется в концептуальную модель.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-155">The Department1 entity is created and added to the conceptual model.</span></span>   

<span data-ttu-id="1ee2c-156">Чтобы включить связанные сущности в схеме, щелкните правой кнопкой сущность и выберите **включать связанные**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-156">To include related entities in a diagram, rick-click the entity and select **Include Related**.</span></span> <span data-ttu-id="1ee2c-157">Это будет выполнено копирование связанных сущностей и ассоциаций в указанной схемы.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-157">This will make a copy of the related entities and associations in the specified diagram.</span></span>

## <a name="changing-the-color-of-entities"></a><span data-ttu-id="1ee2c-158">Изменение цвета сущностей</span><span class="sxs-lookup"><span data-stu-id="1ee2c-158">Changing the Color of Entities</span></span>

<span data-ttu-id="1ee2c-159">В дополнение к модели разделения на несколько схем, можно также изменить цвета в одной сущности.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-159">In addition to splitting a model into multiple diagrams, you can also change colors of your entities.</span></span>

<span data-ttu-id="1ee2c-160">Чтобы изменить цвет, выберите сущность (или несколько сущностей) в области конструктора.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-160">To change the color, select an entity (or multiple entities) on the design surface.</span></span> <span data-ttu-id="1ee2c-161">Затем щелкните правой кнопкой мыши и выберите **свойства**.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-161">Then, click the right mouse button and select **Properties**.</span></span> <span data-ttu-id="1ee2c-162">В окне «Свойства» выберите **цвет заливки** свойство.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-162">In the Properties window, select the **Fill Color** property.</span></span> <span data-ttu-id="1ee2c-163">Укажите цвет, с помощью допустимым именем цвета (например, красный цвет) или допустимый RGB (например, 255, 128, 128).</span><span class="sxs-lookup"><span data-stu-id="1ee2c-163">Specify the color using either a valid color name (for example, Red) or a valid RGB (for example, 255, 128, 128).</span></span> 

![Цвет](~/ef6/media/color.png)

## <a name="summary"></a><span data-ttu-id="1ee2c-165">Сводка</span><span class="sxs-lookup"><span data-stu-id="1ee2c-165">Summary</span></span>

<span data-ttu-id="1ee2c-166">В этом разделе мы рассмотрели разбиение модели на несколько схем, а также как указать другой цвет для сущности с помощью Entity Framework Designer.</span><span class="sxs-lookup"><span data-stu-id="1ee2c-166">In this topic we looked at how to split a model into multiple diagrams and also how to specify a different color for an entity using the Entity Framework Designer.</span></span> 