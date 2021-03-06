---
title: private（C# 参考）
ms.date: 07/20/2015
f1_keywords:
- private_CSharpKeyword
- private
helpviewer_keywords:
- private keyword [C#]
ms.assetid: 654c0bb8-e6ac-4086-bf96-7474fa6aa1c8
ms.openlocfilehash: 89bc23e91bf693f0a95b75dffe2399cb7e865b50
ms.sourcegitcommit: 89c93d05c2281b4c834f48f6c8df1047e1410980
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/15/2018
---
# <a name="private-c-reference"></a>private（C# 参考）
`private` 关键字是一个成员访问修饰符。 
   
 > 本页涵盖 `private` 访问。 `private` 关键字也是 [`private protected`](./private-protected.md) 访问修饰符的一部分。
  
私有访问是允许的最低访问级别。 私有成员只有在声明它们的类和结构体中才是可访问的，如以下示例所示：  
  
```csharp  
class Employee  
{  
    private int i;  
    double d;   // private access by default  
}  
```  

 同一体中的嵌套类型也可以访问那些私有成员。  
  
 在声明私有成员的类或结构外引用它会导致编译时错误。  
  
 有关 `private` 和其他访问修饰符的比较，请参阅[可访问性级别](../../../csharp/language-reference/keywords/accessibility-levels.md)和[访问修饰符](../../../csharp/programming-guide/classes-and-structs/access-modifiers.md)。  
  
## <a name="example"></a>示例  
 在此示例中，`Employee` 类包含两个私有数据成员 `name` 和 `salary`。 作为私有成员，它们只能通过成员方法来访问。 添加名为 `GetName` 和 `Salary` 的公共方法，以便可以对私有成员进行受控的访问。 通过公共方法访问 `name` 成员，而通过公共只读属性访问 `salary` 成员。 （有关详细信息，请参阅[属性](../../../csharp/programming-guide/classes-and-structs/properties.md)。）  
  
 [!code-csharp[csrefKeywordsModifiers#10](../../../csharp/language-reference/keywords/codesnippet/CSharp/private_1.cs)]  
  
## <a name="c-language-specification"></a>C# 语言规范  
 [!INCLUDE[CSharplangspec](~/includes/csharplangspec-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [C# 参考](../../../csharp/language-reference/index.md)  
 [C# 编程指南](../../../csharp/programming-guide/index.md)  
 [C# 关键字](../../../csharp/language-reference/keywords/index.md)  
 [访问修饰符](../../../csharp/language-reference/keywords/access-modifiers.md)  
 [可访问性级别](../../../csharp/language-reference/keywords/accessibility-levels.md)  
 [修饰符](../../../csharp/language-reference/keywords/modifiers.md)  
 [public](../../../csharp/language-reference/keywords/public.md)  
 [受保护](../../../csharp/language-reference/keywords/protected.md)  
 [internal](../../../csharp/language-reference/keywords/internal.md)
