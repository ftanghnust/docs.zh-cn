---
title: ISymUnmanagedWriter::GetDebugInfo 方法
ms.date: 03/30/2017
api_name:
- ISymUnmanagedWriter.GetDebugInfo
api_location:
- diasymreader.dll
api_type:
- COM
f1_keywords:
- ISymUnmanagedWriter::GetDebugInfo
helpviewer_keywords:
- ISymUnmanagedWriter::GetDebugInfo method [.NET Framework debugging]
- GetDebugInfo method [.NET Framework debugging]
ms.assetid: dd31c210-6829-45eb-927e-cc53932638b7
topic_type:
- apiref
author: mairaw
ms.author: mairaw
ms.openlocfilehash: c1e9a2261ab5fd06e0514efdddf8a8e952a6e3d1
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="isymunmanagedwritergetdebuginfo-method"></a>ISymUnmanagedWriter::GetDebugInfo 方法
返回编译器编写可移植可执行 (PE) 文件头中的调试目录项所需的信息。 符号编写器填写所有字段除外`TimeDateStamp`和`PointerToRawData`。 （编译器负责适当地设置这两个字段。）  
  
 编译器应调用此方法，发出数据 blob 到 PE 文件，设置`PointerToRawData`字段 IMAGE_DEBUG_DIRECTORY 指向发出的数据，并 IMAGE_DEBUG_DIRECTORY 写入 PE 文件中。 编译器还应设置`TimeDateStamp`字段等于`TimeDateStamp`正在生成的 PE 文件。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT GetDebugInfo(  
    [in, out] IMAGE_DEBUG_DIRECTORY *pIDD,  
    [in]  DWORD cData,  
    [out] DWORD *pcData,  
    [out, size_is(cData),  
        length_is(*pcData)] BYTE data[]);  
```  
  
#### <a name="parameters"></a>参数  
 `pIDD`  
 [在中，out]指向符号编写器将填写 IMAGE_DEBUG_DIRECTORY 的指针。  
  
 `cData`  
 [in]A`DWORD`包含调试数据的大小。  
  
 `pcData`  
 [out]指向的指针`DWORD`接收包含调试数据所需的缓冲区的大小。  
  
 `data`  
 [out]指向的缓冲区，则大到足以保留符号存储区的调试数据的指针。  
  
## <a name="return-value"></a>返回值  
 如果该方法成功; 则为 S_OK否则为 E_FAIL 或某些其他错误代码。  
  
## <a name="requirements"></a>要求  
 **标头：** CorSym.idl、 CorSym.h  
  
## <a name="see-also"></a>请参阅  
 [ISymUnmanagedWriter 接口](../../../../docs/framework/unmanaged-api/diagnostics/isymunmanagedwriter-interface.md)
