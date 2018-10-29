---
title: Seleccione la versión de idioma de Visual Basic
description: Configurar el compilador para realizar la validación de sintaxis mediante una versión específica del compilador.
ms.date: 05/24/2018
ms.openlocfilehash: 7628b5a7c27f5b26171d42e44a58598ef3d5d49f
ms.sourcegitcommit: c93fd5139f9efcf6db514e3474301738a6d1d649
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/27/2018
ms.locfileid: "50194727"
---
# <a name="select-the-visual-basic-language-version"></a><span data-ttu-id="f6cff-103">Seleccione la versión de idioma de Visual Basic</span><span class="sxs-lookup"><span data-stu-id="f6cff-103">Select the Visual Basic language version</span></span>

<span data-ttu-id="f6cff-104">Valor predeterminado es la última versión principal del lenguaje que se ha liberado el compilador de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6cff-104">The Visual Basic compiler defaults to the latest major version of the language that has been released.</span></span> <span data-ttu-id="f6cff-105">Puede elegir compilar cualquier proyecto con una versión nueva del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="f6cff-105">You may choose to compile any project using a new point release of the language.</span></span> <span data-ttu-id="f6cff-106">Elegir la versión más reciente del lenguaje permite que el proyecto use las últimas características de ese lenguaje.</span><span class="sxs-lookup"><span data-stu-id="f6cff-106">Choosing a newer version of the language enables your project to make use of the latest language features.</span></span> <span data-ttu-id="f6cff-107">En otros escenarios, puede ser necesario validar que un proyecto se compile correctamente cuando se usa una versión anterior del lenguaje.</span><span class="sxs-lookup"><span data-stu-id="f6cff-107">In other scenarios, you may need to validate that a project compiles cleanly when using an older version of the language.</span></span>

<span data-ttu-id="f6cff-108">Esta capacidad hace que la decisión de instalar nuevas versiones del SDK y las herramientas en el entorno de desarrollo no esté vinculada a la decisión de incorporar nuevas características del lenguaje en un proyecto.</span><span class="sxs-lookup"><span data-stu-id="f6cff-108">This capability decouples the decision to install new versions of the SDK and tools in your development environment from the decision to incorporate new language features in a project.</span></span> <span data-ttu-id="f6cff-109">Puede instalar el SDK y las herramientas más recientes en el equipo de compilación.</span><span class="sxs-lookup"><span data-stu-id="f6cff-109">You can install the latest SDK and tools on your build machine.</span></span> <span data-ttu-id="f6cff-110">Cada proyecto se puede configurar para que, durante su compilación, se use una versión de lenguaje específica.</span><span class="sxs-lookup"><span data-stu-id="f6cff-110">Each project can be configured to use a specific version of the language for its build.</span></span>

<span data-ttu-id="f6cff-111">Hay tres maneras de establecer la versión de idioma:</span><span class="sxs-lookup"><span data-stu-id="f6cff-111">There are three ways to set the language version:</span></span>

- <span data-ttu-id="f6cff-112">Editar manualmente el [ **.vbproj** archivo](#edit-the-vbproj-file)</span><span class="sxs-lookup"><span data-stu-id="f6cff-112">Manually edit your [**.vbproj** file](#edit-the-vbproj-file)</span></span>
- <span data-ttu-id="f6cff-113">Establezca la versión de idioma [para varios proyectos en un subdirectorio](#configure-multiple-projects)</span><span class="sxs-lookup"><span data-stu-id="f6cff-113">Set the language version [for multiple projects in a subdirectory](#configure-multiple-projects)</span></span>
- <span data-ttu-id="f6cff-114">Configurar la [ `-langversion` opción del compilador](#set-the-langversion-compiler-option)</span><span class="sxs-lookup"><span data-stu-id="f6cff-114">Configure the [`-langversion` compiler option](#set-the-langversion-compiler-option)</span></span>

## <a name="edit-the-vbproj-file"></a><span data-ttu-id="f6cff-115">Edite el archivo vbproj</span><span class="sxs-lookup"><span data-stu-id="f6cff-115">Edit the vbproj file</span></span>

<span data-ttu-id="f6cff-116">Puede establecer la versión de idioma su **.vbproj** archivo.</span><span class="sxs-lookup"><span data-stu-id="f6cff-116">You can set the language version in your **.vbproj** file.</span></span> <span data-ttu-id="f6cff-117">Agregue el siguiente elemento:</span><span class="sxs-lookup"><span data-stu-id="f6cff-117">Add the following element:</span></span>

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

<span data-ttu-id="f6cff-118">El valor `latest` usa la versión secundaria más reciente del lenguaje Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6cff-118">The value `latest` uses the latest minor version of the Visual Basic language.</span></span> <span data-ttu-id="f6cff-119">Los valores válidos son:</span><span class="sxs-lookup"><span data-stu-id="f6cff-119">Valid values are:</span></span>

|<span data-ttu-id="f6cff-120">Valor</span><span class="sxs-lookup"><span data-stu-id="f6cff-120">Value</span></span>|<span data-ttu-id="f6cff-121">Significado</span><span class="sxs-lookup"><span data-stu-id="f6cff-121">Meaning</span></span>|
|------------|-------------|
|<span data-ttu-id="f6cff-122">default</span><span class="sxs-lookup"><span data-stu-id="f6cff-122">default</span></span>|<span data-ttu-id="f6cff-123">El compilador acepta toda la sintaxis de lenguaje válida de la última versión principal que puede admitir.</span><span class="sxs-lookup"><span data-stu-id="f6cff-123">The compiler accepts all valid language syntax from the latest major version that it can support.</span></span>|
|<span data-ttu-id="f6cff-124">9</span><span class="sxs-lookup"><span data-stu-id="f6cff-124">9</span></span>|<span data-ttu-id="f6cff-125">El compilador acepta solo la sintaxis que se incluye en Visual Basic 9.0 o inferior.</span><span class="sxs-lookup"><span data-stu-id="f6cff-125">The compiler accepts only syntax that is included in Visual Basic 9.0 or lower.</span></span>|
|<span data-ttu-id="f6cff-126">10</span><span class="sxs-lookup"><span data-stu-id="f6cff-126">10</span></span>|<span data-ttu-id="f6cff-127">El compilador acepta solo la sintaxis que se incluye en Visual Basic 10.0 o inferior.</span><span class="sxs-lookup"><span data-stu-id="f6cff-127">The compiler accepts only syntax that is included in Visual Basic 10.0 or lower.</span></span>|
|<span data-ttu-id="f6cff-128">11</span><span class="sxs-lookup"><span data-stu-id="f6cff-128">11</span></span>|<span data-ttu-id="f6cff-129">El compilador acepta solo la sintaxis que se incluye en Visual Basic 11.0 o inferior.</span><span class="sxs-lookup"><span data-stu-id="f6cff-129">The compiler accepts only syntax that is included in Visual Basic 11.0 or lower.</span></span>|
|<span data-ttu-id="f6cff-130">12</span><span class="sxs-lookup"><span data-stu-id="f6cff-130">12</span></span>|<span data-ttu-id="f6cff-131">El compilador acepta solo la sintaxis que se incluye en Visual Basic 12.0 o inferior.</span><span class="sxs-lookup"><span data-stu-id="f6cff-131">The compiler accepts only syntax that is included in Visual Basic 12.0 or lower.</span></span>|
|<span data-ttu-id="f6cff-132">14</span><span class="sxs-lookup"><span data-stu-id="f6cff-132">14</span></span>|<span data-ttu-id="f6cff-133">El compilador acepta solo la sintaxis que se incluye en Visual Basic 14.0 o inferior.</span><span class="sxs-lookup"><span data-stu-id="f6cff-133">The compiler accepts only syntax that is included in Visual Basic 14.0 or lower.</span></span>|
|<span data-ttu-id="f6cff-134">15</span><span class="sxs-lookup"><span data-stu-id="f6cff-134">15</span></span>|<span data-ttu-id="f6cff-135">El compilador acepta solo la sintaxis que se incluye en Visual Basic 15.0 o inferior.</span><span class="sxs-lookup"><span data-stu-id="f6cff-135">The compiler accepts only syntax that is included in Visual Basic 15.0 or lower.</span></span>|
|<span data-ttu-id="f6cff-136">15.3</span><span class="sxs-lookup"><span data-stu-id="f6cff-136">15.3</span></span>|<span data-ttu-id="f6cff-137">El compilador acepta solo la sintaxis que se incluye en Visual Basic 15.3 o inferior.</span><span class="sxs-lookup"><span data-stu-id="f6cff-137">The compiler accepts only syntax that is included in Visual Basic 15.3 or lower.</span></span>|
|<span data-ttu-id="f6cff-138">15.5</span><span class="sxs-lookup"><span data-stu-id="f6cff-138">15.5</span></span>|<span data-ttu-id="f6cff-139">El compilador acepta solo la sintaxis que se incluye en Visual Basic 15.5 o inferior.</span><span class="sxs-lookup"><span data-stu-id="f6cff-139">The compiler accepts only syntax that is included in Visual Basic 15.5 or lower.</span></span>|
|<span data-ttu-id="f6cff-140">latest</span><span class="sxs-lookup"><span data-stu-id="f6cff-140">latest</span></span>|<span data-ttu-id="f6cff-141">El compilador acepta toda la sintaxis de lenguaje válida que puede admitir.</span><span class="sxs-lookup"><span data-stu-id="f6cff-141">The compiler accepts all valid language syntax that it can support.</span></span>|

<span data-ttu-id="f6cff-142">Las cadenas especiales `default` y `latest` se resuelven en las versiones de lenguaje principal y secundaria respectivamente más recientes que haya instaladas en el equipo de compilación.</span><span class="sxs-lookup"><span data-stu-id="f6cff-142">The special strings `default` and `latest` resolve to the latest major and minor language versions installed on the build machine, respectively.</span></span>

## <a name="configure-multiple-projects"></a><span data-ttu-id="f6cff-143">Configurar varios proyectos</span><span class="sxs-lookup"><span data-stu-id="f6cff-143">Configure multiple projects</span></span>

<span data-ttu-id="f6cff-144">Puede crear un archivo **Directory.build.props** que contenga el elemento `<LangVersion>` para configurar varios directorios.</span><span class="sxs-lookup"><span data-stu-id="f6cff-144">You can create a **Directory.build.props** file that contains the `<LangVersion>` element to configure multiple directories.</span></span> <span data-ttu-id="f6cff-145">Por lo general, esto se hace en el directorio de la solución.</span><span class="sxs-lookup"><span data-stu-id="f6cff-145">You typically do that in your solution directory.</span></span> <span data-ttu-id="f6cff-146">Agregue lo siguiente a un archivo **Directory.build.props** en el directorio de la solución:</span><span class="sxs-lookup"><span data-stu-id="f6cff-146">Add the following to a **Directory.build.props** file in your solution directory:</span></span>

```xml
<Project>
 <PropertyGroup>
   <LangVersion>15.5</LangVersion>
 </PropertyGroup>
</Project>
```

<span data-ttu-id="f6cff-147">Ahora, las compilaciones en cada subdirectorio del directorio que contiene ese archivo usará la sintaxis de la versión 15.5 de Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="f6cff-147">Now, builds in every subdirectory of the directory containing that file will use Visual Basic version 15.5 syntax.</span></span> <span data-ttu-id="f6cff-148">Para obtener más información, consulte el artículo [Personalizar una compilación](/visualstudio/msbuild/customize-your-build.md).</span><span class="sxs-lookup"><span data-stu-id="f6cff-148">For more information, see the article on [Customize your build](/visualstudio/msbuild/customize-your-build.md).</span></span>

## <a name="set-the-langversion-compiler-option"></a><span data-ttu-id="f6cff-149">Establecer la opción del compilador langversion</span><span class="sxs-lookup"><span data-stu-id="f6cff-149">Set the langversion compiler option</span></span>

<span data-ttu-id="f6cff-150">Puede usar la opción de la línea de comandos `-langversion`.</span><span class="sxs-lookup"><span data-stu-id="f6cff-150">You can use the `-langversion` command-line option.</span></span> <span data-ttu-id="f6cff-151">Para obtener más información, consulte el artículo sobre la opción del compilador [-langversion](../reference/command-line-compiler/langversion.md).</span><span class="sxs-lookup"><span data-stu-id="f6cff-151">For more information, see the article on the [-langversion](../reference/command-line-compiler/langversion.md) compiler option.</span></span> <span data-ttu-id="f6cff-152">Puede ver una lista de los valores válidos escribiendo `vbc -langversion:?` .</span><span class="sxs-lookup"><span data-stu-id="f6cff-152">You can see a list of the valid values by typing  `vbc -langversion:?` .</span></span>