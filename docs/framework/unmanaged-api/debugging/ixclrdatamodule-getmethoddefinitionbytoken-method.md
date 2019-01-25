---
title: Método IXCLRDataModule::GetMethodDefinitionByToken
ms.date: 01/16/2019
api.name:
- IXCLRDataModule::GetMethodDefinitionByToken Method
api.location:
- mscordacwks.dll
api.type:
- COM
f1.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method
helpviewer.keywords:
- IXCLRDataModule::GetMethodDefinitionByToken Method [.NET Framework debugging]
topic_type:
- apiref
author: cshung
ms.author: andrewau
ms.openlocfilehash: 1371b86f30324908a639b3b1bbae0ae007ba590a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54708095"
---
# <a name="ixclrdatamodulegetmethoddefinitionbytoken-method"></a><span data-ttu-id="96623-102">Método IXCLRDataModule::GetMethodDefinitionByToken</span><span class="sxs-lookup"><span data-stu-id="96623-102">IXCLRDataModule::GetMethodDefinitionByToken Method</span></span>

<span data-ttu-id="96623-103">Obtiene la definición del método correspondiente a un token de metadatos especificado.</span><span class="sxs-lookup"><span data-stu-id="96623-103">Gets the method definition corresponding to a given metadata token.</span></span>

[!INCLUDE[debugging-api-recommended-note](../../../../includes/debugging-api-recommended-note.md)]

## <a name="syntax"></a><span data-ttu-id="96623-104">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="96623-104">Syntax</span></span>

```
HRESULT GetMethodDefinitionByToken(
    [in] mdMethodDef token,
    [out] IXCLRDataMethodDefinition** methodDefinition
);
```

### <a name="parameters"></a><span data-ttu-id="96623-105">Parámetros</span><span class="sxs-lookup"><span data-stu-id="96623-105">Parameters</span></span>

<span data-ttu-id="96623-106">`token` [in] El token del método.</span><span class="sxs-lookup"><span data-stu-id="96623-106">`token` [in] The method token.</span></span>

<span data-ttu-id="96623-107">`methodDefinition` [out] La definición del método.</span><span class="sxs-lookup"><span data-stu-id="96623-107">`methodDefinition` [out] The method definition.</span></span>

## <a name="remarks"></a><span data-ttu-id="96623-108">Comentarios</span><span class="sxs-lookup"><span data-stu-id="96623-108">Remarks</span></span>

<span data-ttu-id="96623-109">El método proporcionado forma parte de la `IXCLRDataModule` interfaz y corresponde a la ranura de la tabla de métodos virtuales 25.</span><span class="sxs-lookup"><span data-stu-id="96623-109">The provided method is part of the `IXCLRDataModule` interface and corresponds to the 25th slot of the virtual method table.</span></span>

## <a name="requirements"></a><span data-ttu-id="96623-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96623-110">Requirements</span></span>

<span data-ttu-id="96623-111">**Plataformas:** Consulte [Requisitos del sistema](../../../../docs/framework/get-started/system-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="96623-111">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
<span data-ttu-id="96623-112">**Encabezado**: Ninguna</span><span class="sxs-lookup"><span data-stu-id="96623-112">**Header:** None</span></span>  
<span data-ttu-id="96623-113">**Biblioteca:** Ninguna</span><span class="sxs-lookup"><span data-stu-id="96623-113">**Library:** None</span></span>  
<span data-ttu-id="96623-114">**Versiones de .NET Framework:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span><span class="sxs-lookup"><span data-stu-id="96623-114">**.NET Framework Versions:** [!INCLUDE[net_current_v47plus](../../../../includes/net-current-v47plus.md)]</span></span>  
 
## <a name="see-also"></a><span data-ttu-id="96623-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="96623-115">See also</span></span>

- [<span data-ttu-id="96623-116">Depuración</span><span class="sxs-lookup"><span data-stu-id="96623-116">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)
- [<span data-ttu-id="96623-117">Interfaz IXCLRDataModule</span><span class="sxs-lookup"><span data-stu-id="96623-117">IXCLRDataModule Interface</span></span>](../../../../docs/framework/unmanaged-api/debugging/ixclrdatamodule-interface.md)