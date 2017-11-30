---
title: "IHostIoCompletionManager::SetMaxThreads 方法"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: IHostIoCompletionManager.SetMaxThreads
api_location: mscoree.dll
api_type: COM
f1_keywords: IHostIoCompletionManager::SetMaxThreads
helpviewer_keywords:
- IHostIoCompletionManager::SetMaxThreads method [.NET Framework hosting]
- SetMaxThreads method, IHostIoCompletionManager interface [.NET Framework hosting]
ms.assetid: ebad4f40-d9f1-4dc6-9b27-a89c9eb3926f
topic_type: apiref
caps.latest.revision: "9"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 084cbf5509583a45f09bcf903e833f4890c5651e
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="ihostiocompletionmanagersetmaxthreads-method"></a><span data-ttu-id="d2da8-102">IHostIoCompletionManager::SetMaxThreads 方法</span><span class="sxs-lookup"><span data-stu-id="d2da8-102">IHostIoCompletionManager::SetMaxThreads Method</span></span>
<span data-ttu-id="d2da8-103">将最大主机分配的线程数设置为服务输入/输出请求。</span><span class="sxs-lookup"><span data-stu-id="d2da8-103">Sets the maximum number of threads that the host allots to service I/O requests.</span></span>  
  
## <a name="syntax"></a><span data-ttu-id="d2da8-104">语法</span><span class="sxs-lookup"><span data-stu-id="d2da8-104">Syntax</span></span>  
  
```  
HRESULT SetMaxThreads (  
    [in] DWORD dwMaxIoCompletionThreads  
);  
```  
  
#### <a name="parameters"></a><span data-ttu-id="d2da8-105">参数</span><span class="sxs-lookup"><span data-stu-id="d2da8-105">Parameters</span></span>  
 `dwMaxIoCompletionThreads`  
 <span data-ttu-id="d2da8-106">[in]最大线程数以分配给输入/输出请求。</span><span class="sxs-lookup"><span data-stu-id="d2da8-106">[in] The maximum number of threads to allot for I/O requests.</span></span>  
  
## <a name="return-value"></a><span data-ttu-id="d2da8-107">返回值</span><span class="sxs-lookup"><span data-stu-id="d2da8-107">Return Value</span></span>  
  
|<span data-ttu-id="d2da8-108">HRESULT</span><span class="sxs-lookup"><span data-stu-id="d2da8-108">HRESULT</span></span>|<span data-ttu-id="d2da8-109">描述</span><span class="sxs-lookup"><span data-stu-id="d2da8-109">Description</span></span>|  
|-------------|-----------------|  
|<span data-ttu-id="d2da8-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2da8-110">S_OK</span></span>|<span data-ttu-id="d2da8-111">`SetMaxThreads`已成功返回。</span><span class="sxs-lookup"><span data-stu-id="d2da8-111">`SetMaxThreads` returned successfully.</span></span>|  
|<span data-ttu-id="d2da8-112">HOST_E_CLRNOTAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="d2da8-112">HOST_E_CLRNOTAVAILABLE</span></span>|<span data-ttu-id="d2da8-113">公共语言运行时 (CLR) 尚未加载到进程中，或 CLR 处于不能运行托管的代码或成功处理调用的状态。</span><span class="sxs-lookup"><span data-stu-id="d2da8-113">The common language runtime (CLR) has not been loaded into a process, or the CLR is in a state in which it cannot run managed code or process the call successfully.</span></span>|  
|<span data-ttu-id="d2da8-114">HOST_E_TIMEOUT</span><span class="sxs-lookup"><span data-stu-id="d2da8-114">HOST_E_TIMEOUT</span></span>|<span data-ttu-id="d2da8-115">调用操作已超时。</span><span class="sxs-lookup"><span data-stu-id="d2da8-115">The call timed out.</span></span>|  
|<span data-ttu-id="d2da8-116">HOST_E_NOT_OWNER</span><span class="sxs-lookup"><span data-stu-id="d2da8-116">HOST_E_NOT_OWNER</span></span>|<span data-ttu-id="d2da8-117">调用方不拥有该锁。</span><span class="sxs-lookup"><span data-stu-id="d2da8-117">The caller does not own the lock.</span></span>|  
|<span data-ttu-id="d2da8-118">HOST_E_ABANDONED</span><span class="sxs-lookup"><span data-stu-id="d2da8-118">HOST_E_ABANDONED</span></span>|<span data-ttu-id="d2da8-119">事件已被取消时被阻塞的线程，或者纤程正在等待它。</span><span class="sxs-lookup"><span data-stu-id="d2da8-119">An event was canceled while a blocked thread or fiber was waiting on it.</span></span>|  
|<span data-ttu-id="d2da8-120">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="d2da8-120">E_FAIL</span></span>|<span data-ttu-id="d2da8-121">出现未知的灾难性故障。</span><span class="sxs-lookup"><span data-stu-id="d2da8-121">An unknown catastrophic failure occurred.</span></span> <span data-ttu-id="d2da8-122">如果某方法返回 E_FAIL，CLR 不再可用进程内。</span><span class="sxs-lookup"><span data-stu-id="d2da8-122">When a method returns E_FAIL, the CLR is no longer usable within the process.</span></span> <span data-ttu-id="d2da8-123">到托管方法的后续调用会返回 HOST_E_CLRNOTAVAILABLE。</span><span class="sxs-lookup"><span data-stu-id="d2da8-123">Subsequent calls to hosting methods return HOST_E_CLRNOTAVAILABLE.</span></span>|  
|<span data-ttu-id="d2da8-124">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="d2da8-124">E_NOTIMPL</span></span>|<span data-ttu-id="d2da8-125">主机未提供的实现`SetMaxThreads`。</span><span class="sxs-lookup"><span data-stu-id="d2da8-125">The host does not provide an implementation of `SetMaxThreads`.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="d2da8-126">备注</span><span class="sxs-lookup"><span data-stu-id="d2da8-126">Remarks</span></span>  
 <span data-ttu-id="d2da8-127">`SetMaxThreads`CLR 提供了机会设置线程可供 I/O 端口上的服务请求的最大数目。</span><span class="sxs-lookup"><span data-stu-id="d2da8-127">`SetMaxThreads` provides the CLR with an opportunity to set the maximum number of threads that are available to service requests on I/O ports.</span></span> <span data-ttu-id="d2da8-128">诸如实现、 性能或可伸缩性之类的原因，主机可能需要对的线程池大小的独有控制。</span><span class="sxs-lookup"><span data-stu-id="d2da8-128">A host might need exclusive control over the size of the thread pool, for reasons such as implementation, performance, or scalability.</span></span> <span data-ttu-id="d2da8-129">主机不为此，需要实现`SetMaxThreads`。</span><span class="sxs-lookup"><span data-stu-id="d2da8-129">For this reason, the host is not required to implement `SetMaxThreads`.</span></span> <span data-ttu-id="d2da8-130">在这种情况下，主机应通过此方法返回 E_NOTIMPL。</span><span class="sxs-lookup"><span data-stu-id="d2da8-130">In this case, a host should return E_NOTIMPL from this method.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="d2da8-131">要求</span><span class="sxs-lookup"><span data-stu-id="d2da8-131">Requirements</span></span>  
 <span data-ttu-id="d2da8-132">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="d2da8-132">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="d2da8-133">**标头：** MSCorEE.h</span><span class="sxs-lookup"><span data-stu-id="d2da8-133">**Header:** MSCorEE.h</span></span>  
  
 <span data-ttu-id="d2da8-134">**库：**作为 MSCorEE.dll 中的资源</span><span class="sxs-lookup"><span data-stu-id="d2da8-134">**Library:** Included as a resource in MSCorEE.dll</span></span>  
  
 <span data-ttu-id="d2da8-135">**.NET framework 版本：**[!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="d2da8-135">**.NET Framework Versions:** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="d2da8-136">另请参阅</span><span class="sxs-lookup"><span data-stu-id="d2da8-136">See Also</span></span>  
 [<span data-ttu-id="d2da8-137">ICLRIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="d2da8-137">ICLRIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/iclriocompletionmanager-interface.md)  
 [<span data-ttu-id="d2da8-138">IHostIoCompletionManager 接口</span><span class="sxs-lookup"><span data-stu-id="d2da8-138">IHostIoCompletionManager Interface</span></span>](../../../../docs/framework/unmanaged-api/hosting/ihostiocompletionmanager-interface.md)