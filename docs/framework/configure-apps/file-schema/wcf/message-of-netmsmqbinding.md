---
title: '&lt;netMsmqBinding&gt; 的 &lt;message&gt;'
ms.date: 03/30/2017
ms.assetid: 6ebf0240-d7be-4493-b0fe-f00fd5989d77
ms.openlocfilehash: 0e947667c414079f24398b401456efd56bf9922c
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="ltmessagegt-of-ltnetmsmqbindinggt"></a>&lt;netMsmqBinding&gt; 的 &lt;message&gt;
在此 `netMsmqBinding` 绑定上定义 SOAP 消息安全设置。  
  
 \<system.ServiceModel>  
\<绑定 >  
\<netMsmqBinding>  
\<绑定 >  
\<安全 >  
\<message>  
  
## <a name="syntax"></a>语法  
  
```xml  
<netMsmqBinding>  
    <binding>  
      <security>  
         <message   
                      algorithmSuite="Basic128/Basic192/Basic256/Basic128Rsa15/Basic256Rsa15/TripleDes/TripleDesRsa15/Basic128Sha256/Basic192Sha256/TripleDesSha256/Basic128Sha256Rsa15/Basic192Sha256Rsa15/Basic256Sha256Rsa15/TripleDesSha256Rsa15"  
            clientCredentialType="None/Windows/UserName/Certificate/CardSpace" />  
    </security>  
</netMsmqBinding>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|algorithmSuite|设置消息加密和密钥包装算法，这些算法用于针对通过 MSMQ 传输发送的消息实现基于消息的安全性。<br /><br /> 默认值为 `Aes256`。 此属性的类型为 <xref:System.ServiceModel.Security.SecurityAlgorithmSuite>。|  
|clientCredentialType|指定针对通过 MSMQ 传输发送的消息执行客户端身份验证时要使用的凭据类型。 包括以下有效值：<br /><br /> -None： 允许服务与匿名客户端交互。 服务和客户端都不需要凭据。<br />-Windows： 使 SOAP 交换在已通过身份验证的 Windows 凭据上下文。 此设置总是执行基于 Kerberos 的身份验证。<br />-UserName： 使服务可以要求客户端进行身份验证使用 UserName 凭据。 在这种情况下，凭据需要指定使用`clientCredentials`行为**警告：** Windows Communication Foundation (WCF) 不支持发送密码摘要或派生密钥使用的密码，并使用这样的密钥为消息安全。 因此，WCF 将交换的安全性时使用 UserName 凭据。 此模式要求使用 `clientCredential` 行为和 `serviceCertificate` 在客户端指定服务证书。 <br /><br /> -Certificate： 使服务可以要求客户端进行身份验证使用的证书。 在此情况下，需要使用 `clientCredentials` 行为指定客户端凭据。 在此情况下，需要使用 `clientCredentials` 行为，通过指定 `serviceCertificate` 来指定服务凭据。<br />-CardSpace： 允许服务要求客户端进行身份验证使用 CardSpace。 必须在 `serviceCertiifcate` 行为中设置 `clientCredential`。<br /><br /> 默认值为 `Windows`。 此属性的类型为 <xref:System.ServiceModel.MessageCredentialType>。|  
  
### <a name="child-elements"></a>子元素  
 无  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<security>](../../../../../docs/framework/configure-apps/file-schema/wcf/security-of-netmsmqbinding.md)|定义绑定的安全设置。|  
  
## <a name="see-also"></a>请参阅  
 <xref:System.ServiceModel.Configuration.MessageSecurityOverMsmqElement>  
 <xref:System.ServiceModel.Configuration.NetMsmqSecurityElement.Message%2A>  
 <xref:System.ServiceModel.NetMsmqSecurity.Message%2A>  
 <xref:System.ServiceModel.MessageSecurityOverMsmq>  
 [WCF 中的队列](../../../../../docs/framework/wcf/feature-details/queues-in-wcf.md)  
 [保护服务和客户端的安全](../../../../../docs/framework/wcf/feature-details/securing-services-and-clients.md)  
 [绑定](../../../../../docs/framework/wcf/bindings.md)  
 [配置系统提供的绑定](../../../../../docs/framework/wcf/feature-details/configuring-system-provided-bindings.md)  
 [使用绑定来配置 Windows Communication Foundation 服务和客户端](http://msdn.microsoft.com/library/bd8b277b-932f-472f-a42a-b02bb5257dfb)  
 [\<绑定 >](../../../../../docs/framework/misc/binding.md)
