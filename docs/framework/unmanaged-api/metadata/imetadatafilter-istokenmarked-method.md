---
title: "IMetaDataFilter::IsTokenMarked 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IMetaDataFilter.IsTokenMarked
api_location: mscoree.dll
api_type: COM
f1_keywords: IMetaDataFilter::IsTokenMarked
helpviewer_keywords:
- IMetaDataFilter::IsTokenMarked method [.NET Framework metadata]
- IsTokenMarked method [.NET Framework metadata]
ms.assetid: 7d90dcee-0206-4540-807b-06982fe65f1a
topic_type: apiref
caps.latest.revision: "9"
author: mairaw
ms.author: mairaw
manager: wpickett
ms.openlocfilehash: 832f1e57e55245a84d093a41c627613d5fbe6902
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="imetadatafilteristokenmarked-method"></a><span data-ttu-id="e8007-102">IMetaDataFilter::IsTokenMarked 方法</span><span class="sxs-lookup"><span data-stu-id="e8007-102">IMetaDataFilter::IsTokenMarked Method</span></span>
<span data-ttu-id="e8007-103">获取一个值，该值指定元数据标记是否已标记为已处理。</span><span class="sxs-lookup"><span data-stu-id="e8007-103">Gets a value indicating whether the specified metadata token has been marked as processed.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="e8007-104">语法</span><span class="sxs-lookup"><span data-stu-id="e8007-104">Syntax</span></span>  
  
```  
HRESULT IsTokenMarked (  
    [in]  mdToken  tk,   
    [out] BOOL     *pIsMarked  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="e8007-105">参数</span><span class="sxs-lookup"><span data-stu-id="e8007-105">Parameters</span></span>  
 `tk`  
 <span data-ttu-id="e8007-106">[in]要检查处理标记的标记。</span><span class="sxs-lookup"><span data-stu-id="e8007-106">[in] The token to examine for a processing mark.</span></span>  
  
 `pIsMarked`  
 <span data-ttu-id="e8007-107">[out]一个值，是`true`如果`tk`处理; 否则为`false`。</span><span class="sxs-lookup"><span data-stu-id="e8007-107">[out] A value that is `true` if `tk` has been processed; otherwise `false`.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="e8007-108">要求</span><span class="sxs-lookup"><span data-stu-id="e8007-108">Requirements</span></span>  
 <span data-ttu-id="e8007-109">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="e8007-109">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="e8007-110">**标头：** Cor.h</span><span class="sxs-lookup"><span data-stu-id="e8007-110">**Header:** Cor.h</span></span>  
  
 <span data-ttu-id="e8007-111">**库：**用作 MsCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="e8007-111">**Library:** Used as a resource in MsCorEE.dll</span></span>  
  
 <span data-ttu-id="e8007-112">**.NET framework 版本：**[!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="e8007-112">**.NET Framework Versions:** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="e8007-113">另请参阅</span><span class="sxs-lookup"><span data-stu-id="e8007-113">See Also</span></span>  
 [<span data-ttu-id="e8007-114">IMetaDataFilter 接口</span><span class="sxs-lookup"><span data-stu-id="e8007-114">IMetaDataFilter Interface</span></span>](../../../../docs/framework/unmanaged-api/metadata/imetadatafilter-interface.md)