---
title: 如何：对控件应用 FocusVisualStyle
ms.date: 03/30/2017
helpviewer_keywords:
- properties [WPF], FocusVisualStyle
- FocusVisualStyle property [WPF]
ms.assetid: 363de99e-8ecc-438c-ac4a-f9147432ebd6
ms.openlocfilehash: 34af5ca6f5ce6b3714d7d7e0d707841cdfc61349
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="how-to-apply-a-focusvisualstyle-to-a-control"></a>如何：对控件应用 FocusVisualStyle
此示例演示如何在资源中创建焦点视觉样式并将样式应用到控件中，使用<xref:System.Windows.FrameworkElement.FocusVisualStyle%2A>属性。  
  
## <a name="example"></a>示例  
 下面的示例定义创建该控件是中的键盘焦点时，才应用的更多控制组合样式[!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)]。 这通过定义具有的样式来实现<xref:System.Windows.Controls.ControlTemplate>，然后设置时为资源引用该样式<xref:System.Windows.FrameworkElement.FocusVisualStyle%2A>属性。  
  
 类似于边框外部矩形位于外部的矩形区域。 除非进行修改，否则使用样式的大小调整<xref:System.Windows.FrameworkElement.ActualHeight%2A>和<xref:System.Windows.FrameworkElement.ActualWidth%2A>其中应用焦点视觉样式的矩形控件。 此示例将设置为负值<xref:System.Windows.FrameworkElement.Margin%2A>使略有显示在具有焦点的控件外部边框。  
  
 [!code-xaml[FEFocusVisualStyle#XAML](../../../../samples/snippets/csharp/VS_Snippets_Wpf/FEFocusVisualStyle/CS/page1.xaml#xaml)]  
  
 A<xref:System.Windows.FrameworkElement.FocusVisualStyle%2A>是附加到来自任何控件模板样式通过显式样式或主题样式; 控件的主样式可以仍将创建使用<xref:System.Windows.Controls.ControlTemplate>并将该样式设置为<xref:System.Windows.FrameworkElement.Style%2A>属性。  
  
 一个主题或 UI，应始终使用视觉样式的焦点而不是使用另一个用于每个可获得焦点的元素。 有关详细信息，请参阅[样式的焦点在控件和 FocusVisualStyle](../../../../docs/framework/wpf/advanced/styling-for-focus-in-controls-and-focusvisualstyle.md)。  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Windows.FrameworkElement.FocusVisualStyle%2A>  
 [样式设置和模板化](../../../../docs/framework/wpf/controls/styling-and-templating.md)  
 [为控件中的焦点设置样式以及 FocusVisualStyle](../../../../docs/framework/wpf/advanced/styling-for-focus-in-controls-and-focusvisualstyle.md)
