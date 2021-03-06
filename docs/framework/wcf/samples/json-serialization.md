---
title: JSON 序列化
ms.date: 03/30/2017
ms.assetid: 3c2c4747-7510-4bdf-b4fe-64f98428ef4a
ms.openlocfilehash: 389bdc8b064bda9870b33a2e4c46fdf90bb7f3ad
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="json-serialization"></a>JSON 序列化
此示例演示如何使用 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 序列化和反序列化 JavaScript Object Notation (JSON) 格式的数据。 此序列化引擎将 JSON 数据转换为 [!INCLUDE[dnprdnshort](../../../../includes/dnprdnshort-md.md)] 类型的实例，然后重新转换为 JSON 数据。 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 支持同一类型，如 <xref:System.Runtime.Serialization.DataContractSerializer>。 JSON 数据格式在编写异步 JavaScript 和 XML (AJAX) 样式的 Web 应用程序时特别有用。 AJAX 支持 Windows Communication Foundation (WCF) 中进行了优化通过 ScriptManager 控件与 ASP.NET AJAX 一起使用。 有关如何使用 ASP.NET AJAX 的 Windows Communication Foundation (WCF) 的示例，请参阅[AJAX 示例](http://msdn.microsoft.com/library/f3fa45b3-44d5-4926-8cc4-a13c30a3bf3e)。  
  
> [!NOTE]
>  本主题的最后介绍了此示例的设置过程和生成说明。  
  
 此示例使用 `Person` 数据协定演示序列化和反序列化。  

```csharp
[DataContract]
class Person
{
    [DataMember]
    internal string name;

    [DataMember]
    internal int age;
}
```

 若要将 `Person` 类型的实例序列化为 JSON，首先创建 <xref:System.Runtime.Serialization.Json.DataContractJsonSerializer> 并使用 `WriteObject` 方法将 JSON 数据编写成流。  

```csharp
Person p = new Person();
//Set up Person object...
MemoryStream stream1 = new MemoryStream();
DataContractJsonSerializer ser = new DataContractJsonSerializer(typeof(Person));
ser.WriteObject(stream1, p);
```

 内存流包含有效的 JSON 数据。
  
```json  
{"age":42,"name":"John"}  
```  
  
 此示例演示从 JSON 数据反序列化为对象。 然后重绕流并调用 `ReadObject`。  

```csharp
Person p2 = (Person)ser.ReadObject(stream1);
```

 检查 `p2` 对象显示 JSON 数据已正确反序列化。  
  
> [!IMPORTANT]
>  您的计算机上可能已安装这些示例。 在继续操作之前，请先检查以下（默认）目录：  
>   
>  `<InstallDrive>:\WF_WCF_Samples`  
>   
>  如果此目录不存在，请转到[Windows Communication Foundation (WCF) 和针对.NET Framework 4 的 Windows Workflow Foundation (WF) 示例](http://go.microsoft.com/fwlink/?LinkId=150780)下载所有 Windows Communication Foundation (WCF) 和[!INCLUDE[wf1](../../../../includes/wf1-md.md)]示例。 此示例位于以下目录：  
>   
>  `<InstallDrive>:\WF_WCF_Samples\WCF\Basic\Ajax\JsonSerialization`  
  
#### <a name="to-set-up-build-and-run-the-sample"></a>设置、生成和运行示例  
  
1.  生成解决方案 JsonSerialization.sln 中所述[生成 Windows Communication Foundation 示例](../../../../docs/framework/wcf/samples/building-the-samples.md)。  
  
2.  运行生成的控制台应用程序。  
  
## <a name="see-also"></a>请参阅
