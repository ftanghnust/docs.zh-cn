---
title: ICorDebugManagedCallback2 接口
ms.date: 03/30/2017
api_name:
- ICorDebugManagedCallback2
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugManagedCallback2
helpviewer_keywords:
- ICorDebugManagedCallback2 interface [.NET Framework debugging]
ms.assetid: cf7b7cfa-1c4b-4d8c-be70-4f9ed15a788b
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 22f4b2cb1bafefefaf3a3fc207af76c80c0c9798
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="icordebugmanagedcallback2-interface"></a>ICorDebugManagedCallback2 接口
提供支持调试器异常处理和托管调试助手 (MDA) 的方法。 `ICorDebugManagedCallback2` 是的逻辑扩展[ICorDebugManagedCallback](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)接口。  
  
## <a name="methods"></a>方法  
  
|方法|描述|  
|------------|-----------------|  
|[ChangeConnection 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-changeconnection-method.md)|通知调试器与指定连接关联的任务组已更改。|  
|[CreateConnection 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-createconnection-method.md)|通知调试器已创建新的连接。|  
|[DestroyConnection 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-destroyconnection-method.md)|通知调试器已终止指定的连接。|  
|[Exception 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exception-method.md)|通知调试器搜索异常处理程序已开始。|  
|[ExceptionUnwind 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-exceptionunwind-method.md)|提供在异常展开过程中的状态通知。|  
|[FunctionRemapComplete 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-functionremapcomplete-method.md)|通知调试器执行代码已切换到新版本的已编辑函数。|  
|[FunctionRemapOpportunity 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-functionremapopportunity-method.md)|通知调试器执行代码已达到经过编辑的函数的早期版本中的序列点。|  
|[MDANotification 方法](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback2-mdanotification-method.md)|提供了执行代码遇到托管调试助手 (MDA) 消息的通知。|  
  
## <a name="remarks"></a>备注  
 `ICorDebugManagedCallback2`接口扩展`ICorDebugManagedCallback`接口来处理.NET Framework 2.0 版中引入的新调试事件。  
  
 调试器必须实现`ICorDebugManagedCallback2`如果它调试.NET Framework 2.0 应用程序。 实例`ICorDebugManagedCallback`或`ICorDebugManagedCallback2`作为回调对象传递[icordebug:: Setmanagedhandler](../../../../docs/framework/unmanaged-api/debugging/icordebug-setmanagedhandler-method.md)。  
  
> [!NOTE]
>  此接口不支持跨计算机或跨进程远程调用。  
  
## <a name="requirements"></a>要求  
 **平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** CorDebug.idl、 CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v20plus](../../../../includes/net-current-v20plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [使用托管调试助手诊断错误](../../../../docs/framework/debug-trace-profile/diagnosing-errors-with-managed-debugging-assistants.md)  
 [调试接口](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [ICorDebugManagedCallback 接口](../../../../docs/framework/unmanaged-api/debugging/icordebugmanagedcallback-interface.md)
