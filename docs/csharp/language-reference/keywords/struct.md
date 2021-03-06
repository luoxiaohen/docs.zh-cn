---
title: struct（C# 参考）
ms.date: 07/20/2015
ms.prod: .net
ms.technology:
- devlang-csharp
ms.topic: article
f1_keywords:
- struct_CSharpKeyword
helpviewer_keywords:
- struct keyword [C#]
- structs [C#], struct keyword
ms.assetid: ff3dd9b7-dc93-4720-8855-ef5558f65c7c
caps.latest.revision: 23
author: BillWagner
ms.author: wiwagn
ms.openlocfilehash: e8a848d5543291ef335e72cb7806158827e865dd
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="struct-c-reference"></a>struct（C# 参考）
`struct` 类型是一种值类型，通常用来封装小型相关变量组，例如，矩形的坐标或库存商品的特征。 下面的示例显示了一个简单的结构声明：  
  
```  
public struct Book  
{  
    public decimal price;  
    public string title;  
    public string author;  
}  
```  
  
## <a name="remarks"></a>备注  
 结构还可以包含[构造函数](../../../csharp/programming-guide/classes-and-structs/constructors.md)、[常量](../../../csharp/programming-guide/classes-and-structs/constants.md)、[字段](../../../csharp/programming-guide/classes-and-structs/fields.md)、[方法](../../../csharp/programming-guide/classes-and-structs/methods.md)、[属性](../../../csharp/programming-guide/classes-and-structs/properties.md)、[索引器](../../../csharp/programming-guide/indexers/index.md)、[运算符](../../../csharp/programming-guide/statements-expressions-operators/operators.md)、[事件](../../../csharp/programming-guide/events/index.md)和[嵌套类型](../../../csharp/programming-guide/classes-and-structs/nested-types.md)，但如果同时需要上述几种成员，则应当考虑改为使用类作为类型。  
  
 有关示例，请参阅[使用结构](../../../csharp/programming-guide/classes-and-structs/using-structs.md)。  
  
 结构可以实现接口，但它们无法继承另一个结构。 因此，结构成员无法声明为 `protected`。  
  
 有关详细信息，请参阅[结构](../../../csharp/programming-guide/classes-and-structs/structs.md)。  
  
## <a name="examples"></a>示例  
 有关示例和详细信息，请参阅[使用结构](../../../csharp/programming-guide/classes-and-structs/using-structs.md)。  
  
## <a name="c-language-specification"></a>C# 语言规范  
 有关示例，请参阅[使用结构](../../../csharp/programming-guide/classes-and-structs/using-structs.md)。  
  
## <a name="see-also"></a>另请参阅  
 [C# 参考](../../../csharp/language-reference/index.md)  
 [C# 编程指南](../../../csharp/programming-guide/index.md)  
 [C# 关键字](../../../csharp/language-reference/keywords/index.md)  
 [默认值表](../../../csharp/language-reference/keywords/default-values-table.md)  
 [内置类型表](../../../csharp/language-reference/keywords/built-in-types-table.md)  
 [类型](../../../csharp/language-reference/keywords/types.md)  
 [值类型](../../../csharp/language-reference/keywords/value-types.md)  
 [类](../../../csharp/language-reference/keywords/class.md)  
 [接口](../../../csharp/language-reference/keywords/interface.md)  
 [类和结构](../../../csharp/programming-guide/classes-and-structs/index.md)
