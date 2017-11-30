---
title: "QualifierSet_Get 函数 （非托管 API 参考）"
description: "QualifierSet_Get 函数获取命名的限定符。"
ms.date: 11/06/2017
ms.prod: .net-framework
ms.technology: dotnet-clr
ms.topic: reference
api_name: QualifierSet_Get
api_location: WMINet_Utils.dll
api_type: DLLExport
f1_keywords: QualifierSet_Get
helpviewer_keywords: QualifierSet_Get function [.NET WMI and performance counters]
topic_type: Reference
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: aaf5de5b8e16ee2f96c7bc29dbb09f93298dd185
ms.sourcegitcommit: a53799f81351ad9afb3007cd68846ce6aeeb10cb
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/15/2017
---
# <a name="qualifiersetget-function"></a><span data-ttu-id="849a9-103">QualifierSet_Get 函数</span><span class="sxs-lookup"><span data-stu-id="849a9-103">QualifierSet_Get function</span></span>
<span data-ttu-id="849a9-104">获取指定的命名的限定符。</span><span class="sxs-lookup"><span data-stu-id="849a9-104">Gets the specified named qualifier.</span></span>  

[!INCLUDE[internalonly-unmanaged](../../../../includes/internalonly-unmanaged.md)]
  
## <a name="syntax"></a><span data-ttu-id="849a9-105">语法</span><span class="sxs-lookup"><span data-stu-id="849a9-105">Syntax</span></span>  
  
```  
HRESULT QualifierSet_Get (
   [in] int                  vFunc, 
   [in] IWbemQualifierSet*   ptr, 
   [in] LPCWSTR              wszName,
   [in] LONG                 lFlags,
   [out] VARIANT*            pVal,
   [out] LONG*               plFlavor                 
); 
```  

## <a name="parameters"></a><span data-ttu-id="849a9-106">参数</span><span class="sxs-lookup"><span data-stu-id="849a9-106">Parameters</span></span>

`vFunc`   
<span data-ttu-id="849a9-107">[in]未使用此参数。</span><span class="sxs-lookup"><span data-stu-id="849a9-107">[in] This parameter is unused.</span></span>

`ptr`   
<span data-ttu-id="849a9-108">[in]指向的指针[IWbemQualifierSet](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx)实例。</span><span class="sxs-lookup"><span data-stu-id="849a9-108">[in] A pointer to an [IWbemQualifierSet](https://msdn.microsoft.com/library/aa391860(v=vs.85).aspx) instance.</span></span>

`wszName`   
<span data-ttu-id="849a9-109">[in]请求其值的限定符的名称。</span><span class="sxs-lookup"><span data-stu-id="849a9-109">[in] The name of the qualifier whose value is requested.</span></span>

`lFlags`   
<span data-ttu-id="849a9-110">[in]保留。</span><span class="sxs-lookup"><span data-stu-id="849a9-110">[in] Reserved.</span></span> <span data-ttu-id="849a9-111">此参数必须为 0。</span><span class="sxs-lookup"><span data-stu-id="849a9-111">This parameter must be 0.</span></span>

`pVal`   
<span data-ttu-id="849a9-112">[out]成功时，正确的类型和值限定符。</span><span class="sxs-lookup"><span data-stu-id="849a9-112">[out] When successful, the correct type and value for the qualifier.</span></span> <span data-ttu-id="849a9-113">如果函数失败，`VARIANT`指向`pVal`则不会修改。</span><span class="sxs-lookup"><span data-stu-id="849a9-113">If the function fails, the `VARIANT` pointed to by `pVal` is not modified.</span></span> <span data-ttu-id="849a9-114">如果此参数为`null`，则将忽略参数。</span><span class="sxs-lookup"><span data-stu-id="849a9-114">If this parameter is `null`, the parameter is ignored.</span></span>

`plFlavor`   
<span data-ttu-id="849a9-115">[out]指向接收请求的限定符的限定符风格位长时间的指针。</span><span class="sxs-lookup"><span data-stu-id="849a9-115">[out] A pointer to a LONG that receives the qualifier flavor bits for the requested qualifier.</span></span> <span data-ttu-id="849a9-116">如果不想风格信息，此参数可以为`null`。</span><span class="sxs-lookup"><span data-stu-id="849a9-116">If flavor information is not desired, this parameter can be `null`.</span></span> 

## <a name="return-value"></a><span data-ttu-id="849a9-117">返回值</span><span class="sxs-lookup"><span data-stu-id="849a9-117">Return value</span></span>

<span data-ttu-id="849a9-118">此函数返回以下值中定义*WbemCli.h*标头文件，或者你可以定义它们常量作为在代码中：</span><span class="sxs-lookup"><span data-stu-id="849a9-118">The following values returned by this function are defined in the *WbemCli.h* header file, or you can define them as constants in your code:</span></span>

|<span data-ttu-id="849a9-119">返回的常量</span><span class="sxs-lookup"><span data-stu-id="849a9-119">Constant</span></span>  |<span data-ttu-id="849a9-120">值</span><span class="sxs-lookup"><span data-stu-id="849a9-120">Value</span></span>  |<span data-ttu-id="849a9-121">描述</span><span class="sxs-lookup"><span data-stu-id="849a9-121">Description</span></span>  |
|---------|---------|---------|
|`WBEM_E_INVALID_PARAMETER` | <span data-ttu-id="849a9-122">0x80041008</span><span class="sxs-lookup"><span data-stu-id="849a9-122">0x80041008</span></span> | <span data-ttu-id="849a9-123">参数不是有效的。</span><span class="sxs-lookup"><span data-stu-id="849a9-123">A parameter is not valid.</span></span> |
|`WBEM_E_NOT_FOUND` | <span data-ttu-id="849a9-124">0x80041002</span><span class="sxs-lookup"><span data-stu-id="849a9-124">0x80041002</span></span> | <span data-ttu-id="849a9-125">指定的限定符不存在。</span><span class="sxs-lookup"><span data-stu-id="849a9-125">The specified qualifier does not exist.</span></span> |
|`WBEM_S_NO_ERROR` | <span data-ttu-id="849a9-126">0</span><span class="sxs-lookup"><span data-stu-id="849a9-126">0</span></span> | <span data-ttu-id="849a9-127">函数调用成功。</span><span class="sxs-lookup"><span data-stu-id="849a9-127">The function call was successful.</span></span>  |
  
## <a name="remarks"></a><span data-ttu-id="849a9-128">备注</span><span class="sxs-lookup"><span data-stu-id="849a9-128">Remarks</span></span>

<span data-ttu-id="849a9-129">此函数包装对的调用[IWbemQualifierSet::Get](https://msdn.microsoft.com/library/aa391867(v=vs.85).aspx)方法。</span><span class="sxs-lookup"><span data-stu-id="849a9-129">This function wraps a call to the [IWbemQualifierSet::Get](https://msdn.microsoft.com/library/aa391867(v=vs.85).aspx) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="849a9-130">要求</span><span class="sxs-lookup"><span data-stu-id="849a9-130">Requirements</span></span>  
 <span data-ttu-id="849a9-131">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="849a9-131">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="849a9-132">**标头：** WMINet_Utils.idl</span><span class="sxs-lookup"><span data-stu-id="849a9-132">**Header:** WMINet_Utils.idl</span></span>  
  
 <span data-ttu-id="849a9-133">**.NET framework 版本：**[!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span><span class="sxs-lookup"><span data-stu-id="849a9-133">**.NET Framework Versions:** [!INCLUDE[net_current_v472plus](../../../../includes/net-current-v472plus.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="849a9-134">请参阅</span><span class="sxs-lookup"><span data-stu-id="849a9-134">See also</span></span>  
[<span data-ttu-id="849a9-135">WMI 和性能计数器 （非托管 API 参考）</span><span class="sxs-lookup"><span data-stu-id="849a9-135">WMI and Performance Counters (Unmanaged API Reference)</span></span>](index.md)