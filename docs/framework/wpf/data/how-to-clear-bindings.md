---
title: "如何：清除绑定"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-wpf
ms.tgt_pltfrm: 
ms.topic: article
dev_langs:
- csharp
- vb
helpviewer_keywords:
- bindings [WPF], clearing
- clearing bindings [WPF]
- data binding [WPF], clearing bindings
ms.assetid: 73962a93-32a9-4bcd-9240-bcfbb239093a
caps.latest.revision: "12"
author: dotnet-bot
ms.author: dotnetcontent
manager: wpickett
ms.workload: dotnet
ms.openlocfilehash: af45d504eb4e7d45808f787925a90c8e0ed19476
ms.sourcegitcommit: 16186c34a957fdd52e5db7294f291f7530ac9d24
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/22/2017
---
# <a name="how-to-clear-bindings"></a>如何：清除绑定
此示例演示如何从对象中清除绑定。  
  
## <a name="example"></a>示例  
 若要清除从对象上的单个属性的绑定，请调用<xref:System.Windows.Data.BindingOperations.ClearBinding%2A>下面的示例中所示。 下面的示例删除从绑定<xref:System.Windows.Controls.TextBlock.TextProperty>的*mytext*、<xref:System.Windows.Controls.TextBlock>对象。  
  
 [!code-csharp[CodeOnlyBinding#ClearBinding](../../../../samples/snippets/csharp/VS_Snippets_Wpf/CodeOnlyBinding/CSharp/binding.cs#clearbinding)]
 [!code-vb[CodeOnlyBinding#ClearBinding](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/CodeOnlyBinding/VisualBasic/App.vb#clearbinding)]  
  
 清除绑定会移除绑定，这样依赖属性的值会更改为过去尚未绑定时的值。 此值可以是默认值、继承值或来自数据模板绑定的值。  
  
 若要清除从对象上的所有可能的属性的绑定，使用<xref:System.Windows.Data.BindingOperations.ClearAllBindings%2A>。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Windows.Data.BindingOperations>  
 [数据绑定概述](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [帮助主题](../../../../docs/framework/wpf/data/data-binding-how-to-topics.md)
