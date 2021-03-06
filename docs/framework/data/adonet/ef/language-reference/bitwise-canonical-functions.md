---
title: "按位规范函数"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-ado
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 993868ca-16e3-47b6-9915-c29cd63b0a21
caps.latest.revision: "2"
author: douglaslMS
ms.author: douglasl
manager: craigg
ms.workload: dotnet
ms.openlocfilehash: 1d703b2467d508324f3eb39b822c239484ac1c6e
ms.sourcegitcommit: ed26cfef4e18f6d93ab822d8c29f902cff3519d1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/17/2018
---
# <a name="bitwise-canonical-functions"></a>按位规范函数
[!INCLUDE[esql](../../../../../../includes/esql-md.md)] 包含按位规范函数。  
  
## <a name="remarks"></a>备注  
 下表列出了 [!INCLUDE[esql](../../../../../../includes/esql-md.md)] 按位规范函数。 如果提供 `Null` 输入，则这些函数返回 `Null`。 这些函数的返回类型与自变量类型相同。 如果函数采用多个自变量，则这些自变量必须具有相同的类型。 若要对不同类型执行位运算，需要显式强制转换为同一类型。  
  
|函数|描述|  
|--------------|-----------------|  
|`BitWiseAnd (` `value1` `,`  `value2` `)`|按照 `value1` 和 `value2` 的类型返回 `value1` 和 `value2` 的位与结果。<br /><br /> **参数**<br /><br /> A `Byte`， `Int16`， `Int32`，和`Int64`。<br /><br /> **示例**<br /><br /> `-- The following example returns 1.`<br /><br /> `BitWiseAnd(1,3)`|  
|`BitWiseNot (` `value` `)`|返回 `value` 的位求反结果。<br /><br /> **参数**<br /><br /> A `Byte`， `Int16`， `Int32`，和`Int64`。<br /><br /> **示例**<br /><br /> `-- The following example returns -4.`<br /><br /> `BitWiseNot(3)`|  
|`BitWiseOr (` `value1` `,`  `value2` `)`|按照 `value1` 和 `value2` 的类型返回 `value1` 和 `value2` 的位或结果。<br /><br /> **参数**<br /><br /> A `Byte`， `Int16`，`Int32`和`Int64`。<br /><br /> **示例**<br /><br /> `-- The following example returns 3.`<br /><br /> `BitWiseOr(1,3)`|  
|`BitWiseXor (` `value1` `,`  `value2` `)`|按照 `value1` 和 `value2` 的类型返回 `value1` 和 `value2` 位异或结果。<br /><br /> **参数**<br /><br /> A `Byte`， `Int16`，`Int32`和`Int64`。<br /><br /> **示例**<br /><br /> `-- The following example returns 2.`<br /><br /> `BitWiseXor (1,3)`|  
  
## <a name="see-also"></a>请参阅  
 [规范函数](../../../../../../docs/framework/data/adonet/ef/language-reference/canonical-functions.md)
