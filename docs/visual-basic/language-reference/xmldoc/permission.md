---
title: '&lt;权限&gt;(Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- <permission> XML tag
- permission XML tag
ms.assetid: 0edf0500-5cd7-49c0-9255-64c48f972b77
ms.openlocfilehash: 4fafebf94be350951672f01f2d17bd00d4bab69a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="ltpermissiongt-visual-basic"></a>&lt;权限&gt;(Visual Basic)
指定成员所需的权限。  
  
## <a name="syntax"></a>语法  
  
```xml  
<permission cref="member">description</permission>  
```  
  
#### <a name="parameters"></a>参数  
 `member`  
 对可从当前编译环境调用的成员或字段的引用。 编译器检查是否存在给定的代码元素，并将 `member` 转换为输出 XML 中规范的元素名称。 括起`member`用引号引起来 ("")。  
  
 `description`  
 对成员访问权限的说明。  
  
## <a name="remarks"></a>备注  
 使用`<permission>`标记记录成员的访问权限。 使用<xref:System.Security.PermissionSet>类可指定访问成员。  
  
 使用 [/doc](../../../visual-basic/reference/command-line-compiler/doc.md) 进行编译可以将文档注释处理到文件中。  
  
## <a name="example"></a>示例  
 此示例使用`<permission>`标记来描述的<xref:System.Security.Permissions.FileIOPermission>所需的`ReadFile`方法。  
  
 [!code-vb[VbVbcnXmlDocComments#7](../../../visual-basic/language-reference/xmldoc/codesnippet/VisualBasic/permission_1.vb)]  
  
## <a name="see-also"></a>请参阅  
 [XML 注释标记](../../../visual-basic/language-reference/xmldoc/recommended-xml-tags-for-documentation-comments.md)
