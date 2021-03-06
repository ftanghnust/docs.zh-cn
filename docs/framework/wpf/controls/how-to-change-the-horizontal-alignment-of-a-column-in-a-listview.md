---
title: 如何：更改 ListView 中列的水平对齐方式
ms.date: 03/30/2017
helpviewer_keywords:
- ListView controls [WPF], horizontal alignment [WPF]
ms.assetid: b9573e44-9dad-4d14-939c-7859ca372758
ms.openlocfilehash: 31ee131e1cbd6e56ce5b0c29085c2d29e65dc40b
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-change-the-horizontal-alignment-of-a-column-in-a-listview"></a>如何：更改 ListView 中列的水平对齐方式
默认情况下，每个列中的内容<xref:System.Windows.Controls.ListViewItem>是左对齐。 你可以通过提供更改每个列的对齐方式<xref:System.Windows.DataTemplate>和设置<xref:System.Windows.FrameworkElement.HorizontalAlignment%2A>中元素的属性上<xref:System.Windows.DataTemplate>。 本主题说明如何<xref:System.Windows.Controls.ListView>对齐其内容默认情况下和如何更改中的一列的对齐方式<xref:System.Windows.Controls.ListView>。  
  
## <a name="example"></a>示例  
 在下面的示例中中的数据`Title`和`ISBN`列是左对齐。  
  
 [!code-xaml[ListViewHowTos#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#1)]  
[!code-xaml[ListViewHowTos#2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#2)]  
  
 若要更改的对齐方式`ISBN`列中，你需要指定<xref:System.Windows.Controls.Control.HorizontalContentAlignment%2A>每个属性<xref:System.Windows.Controls.ListViewItem>是<xref:System.Windows.HorizontalAlignment.Stretch>，以便在每个元素<xref:System.Windows.Controls.ListViewItem>可以跨或沿每一列的整个宽度放置。 因为<xref:System.Windows.Controls.ListView>绑定到数据源，你需要创建设置样式<xref:System.Windows.Controls.Control.HorizontalContentAlignment%2A>。 接下来，你需要使用<xref:System.Windows.DataTemplate>以显示内容而不是使用<xref:System.Windows.Controls.GridViewColumn.DisplayMemberBinding%2A>属性。 若要显示`ISBN`的每个模板，<xref:System.Windows.DataTemplate>只能包含<xref:System.Windows.Controls.TextBlock>具有其<xref:System.Windows.FrameworkElement.HorizontalAlignment%2A>属性设置为<xref:System.Windows.HorizontalAlignment.Right>。  
  
 下面的示例定义的样式和<xref:System.Windows.DataTemplate>使所需`ISBN`右对齐的列和更改<xref:System.Windows.Controls.GridViewColumn>引用<xref:System.Windows.DataTemplate>。  
  
 [!code-xaml[ListViewHowTos#3](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#3)]  
[!code-xaml[ListViewHowTos#4](../../../../samples/snippets/csharp/VS_Snippets_Wpf/ListViewHowTos/CSharp/Window1.xaml#4)]  
  
## <a name="see-also"></a>请参阅  
 [数据绑定概述](../../../../docs/framework/wpf/data/data-binding-overview.md)  
 [数据模板化概述](../../../../docs/framework/wpf/data/data-templating-overview.md)  
 [使用 XMLDataProvider 和 XPath 查询绑定到 XML 数据](../../../../docs/framework/wpf/data/how-to-bind-to-xml-data-using-an-xmldataprovider-and-xpath-queries.md)  
 [ListView 概述](../../../../docs/framework/wpf/controls/listview-overview.md)
