---
title: System.ServiceModel.Channels.ConnectionPoolCloseException
ms.date: 03/30/2017
ms.assetid: 8358898e-129e-4fac-a6bf-bf3aa4293ae2
ms.openlocfilehash: f3474fc1bb0ed0d11df6289ed6470447d815f5ce
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="systemservicemodelchannelsconnectionpoolcloseexception"></a>System.ServiceModel.Channels.ConnectionPoolCloseException
关闭此连接池中的连接时发生异常。  
  
## <a name="description"></a>描述  
 此错误级别跟踪指示关闭 Windows Communication Foundation (WCF) 的连接池功能使用的连接池时已发生错误。 一种可能的原因是一个池连接或一组池连接在 CloseTimeout 内未成功关闭。 当引发此异常时，将中止该池内所有剩余的未关闭连接，并放弃其他池内的未关闭连接。  
  
## <a name="see-also"></a>请参阅  
 [跟踪](../../../../../docs/framework/wcf/diagnostics/tracing/index.md)  
 [使用跟踪来排除应用程序故障](../../../../../docs/framework/wcf/diagnostics/tracing/using-tracing-to-troubleshoot-your-application.md)  
 [管理和诊断](../../../../../docs/framework/wcf/diagnostics/index.md)
