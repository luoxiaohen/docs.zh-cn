---
title: "异常：try...finally 表达式 (F#)"
description: "了解如何使用 F # try … 最后表达式使您能够执行清理代码，即使的代码块将引发异常。"
keywords: "visual f#, f#, 函数编程"
author: cartermp
ms.author: phcart
ms.date: 05/16/2016
ms.topic: language-reference
ms.prod: .net
ms.technology: devlang-fsharp
ms.devlang: fsharp
ms.assetid: af06b20c-8d87-4496-a0aa-6fdfe8b3a786
ms.openlocfilehash: 2e2445c42bf8129ea81beef56cb725ac0e37d202
ms.sourcegitcommit: bd1ef61f4bb794b25383d3d72e71041a5ced172e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/18/2017
---
# <a name="exceptions-the-tryfinally-expression"></a><span data-ttu-id="c0e29-104">异常：try...finally 表达式</span><span class="sxs-lookup"><span data-stu-id="c0e29-104">Exceptions: The try...finally Expression</span></span>

<span data-ttu-id="c0e29-105">`try...finally`表达式使您能够执行清理代码，即使的代码块将引发异常。</span><span class="sxs-lookup"><span data-stu-id="c0e29-105">The `try...finally` expression enables you to execute clean-up code even if a block of code throws an exception.</span></span>


## <a name="syntax"></a><span data-ttu-id="c0e29-106">语法</span><span class="sxs-lookup"><span data-stu-id="c0e29-106">Syntax</span></span>

```fsharp
try
    expression1
finally
    expression2
```

## <a name="remarks"></a><span data-ttu-id="c0e29-107">备注</span><span class="sxs-lookup"><span data-stu-id="c0e29-107">Remarks</span></span>
<span data-ttu-id="c0e29-108">`try...finally`表达式可以用于执行中的代码*expression2*在前面的语法而不考虑是否在执行期间生成异常*expression1*。</span><span class="sxs-lookup"><span data-stu-id="c0e29-108">The `try...finally` expression can be used to execute the code in *expression2* in the preceding syntax regardless of whether an exception is generated during the execution of *expression1*.</span></span>

<span data-ttu-id="c0e29-109">一种*expression2*不影响整个表达式; 的值返回时不会发生异常的类型是中的最后一个值*expression1*。</span><span class="sxs-lookup"><span data-stu-id="c0e29-109">The type of *expression2* does not contribute to the value of the whole expression; the type returned when an exception does not occur is the last value in *expression1*.</span></span> <span data-ttu-id="c0e29-110">在异常确实发生，不返回任何值，并控制流将传输到下一步的匹配异常处理程序调用堆栈中向上。</span><span class="sxs-lookup"><span data-stu-id="c0e29-110">When an exception does occur, no value is returned and the flow of control transfers to the next matching exception handler up the call stack.</span></span> <span data-ttu-id="c0e29-111">如果找到没有异常处理程序，则程序终止。</span><span class="sxs-lookup"><span data-stu-id="c0e29-111">If no exception handler is found, the program terminates.</span></span> <span data-ttu-id="c0e29-112">执行匹配的处理程序中的代码或者程序终止中的代码之前`finally`执行分支。</span><span class="sxs-lookup"><span data-stu-id="c0e29-112">Before the code in a matching handler is executed or the program terminates, the code in the `finally` branch is executed.</span></span>

<span data-ttu-id="c0e29-113">下面的代码演示如何使用`try...finally`表达式。</span><span class="sxs-lookup"><span data-stu-id="c0e29-113">The following code demonstrates the use of the `try...finally` expression.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5701.fs)]

<span data-ttu-id="c0e29-114">向控制台输出如下所示。</span><span class="sxs-lookup"><span data-stu-id="c0e29-114">The output to the console is as follows.</span></span>

```
Closing stream
Exception handled.
```

<span data-ttu-id="c0e29-115">正如您可以看到输出中，在流关闭之前在外部异常已处理，和文件`test.txt`包含文本`test1`，指示已刷新缓冲区，并已将其写入到磁盘即使异常传输控制到外部异常处理程序。</span><span class="sxs-lookup"><span data-stu-id="c0e29-115">As you can see from the output, the stream was closed before the outer exception was handled, and the file `test.txt` contains the text `test1`, which indicates that the buffers were flushed and written to disk even though the exception transferred control to the outer exception handler.</span></span>

<span data-ttu-id="c0e29-116">请注意，`try...with`构造为单独从`try...finally`构造。</span><span class="sxs-lookup"><span data-stu-id="c0e29-116">Note that the `try...with` construct is a separate construct from the `try...finally` construct.</span></span> <span data-ttu-id="c0e29-117">因此，如果你的代码同时需要`with`块和一个`finally`块中，你必须将嵌套的两个构造，如下面的代码示例所示。</span><span class="sxs-lookup"><span data-stu-id="c0e29-117">Therefore, if your code requires both a `with` block and a `finally` block, you have to nest the two constructs, as in the following code example.</span></span>

[!code-fsharp[Main](../../../../samples/snippets/fsharp/lang-ref-2/snippet5702.fs)]

<span data-ttu-id="c0e29-118">在上下文中计算表达式，包括序列表达式和异步工作流， **try … 最后**表达式可能有一个自定义实现。</span><span class="sxs-lookup"><span data-stu-id="c0e29-118">In the context of computation expressions, including sequence expressions and asynchronous workflows, **try...finally** expressions can have a custom implementation.</span></span> <span data-ttu-id="c0e29-119">有关详细信息，请参阅[计算表达式](../computation-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="c0e29-119">For more information, see [Computation Expressions](../computation-expressions.md).</span></span>


## <a name="see-also"></a><span data-ttu-id="c0e29-120">另请参阅</span><span class="sxs-lookup"><span data-stu-id="c0e29-120">See Also</span></span>
[<span data-ttu-id="c0e29-121">异常处理</span><span class="sxs-lookup"><span data-stu-id="c0e29-121">Exception Handling</span></span>](index.md)

[<span data-ttu-id="c0e29-122">异常：`try...with` 表达式</span><span class="sxs-lookup"><span data-stu-id="c0e29-122">Exceptions: The `try...with` Expression</span></span>](the-try-with-expression.md)