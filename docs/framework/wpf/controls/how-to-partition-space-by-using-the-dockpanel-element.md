---
title: Procedimiento Crear una partición del espacio mediante el elemento DockPanel
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- controls [WPF], DockPanel
- DockPanel control [WPF], partitioning space
- partitioning space [WPF]
ms.assetid: a219b9e5-b205-4438-89b5-0a137ac463ab
ms.openlocfilehash: 8b79b89e512ec9da27774188aeaeed8ebd5b1153
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/23/2019
ms.locfileid: "54577664"
---
# <a name="how-to-partition-space-by-using-the-dockpanel-element"></a>Procedimiento Crear una partición del espacio mediante el elemento DockPanel
En el ejemplo siguiente se crea una sencilla [!INCLUDE[TLA#tla_ui](../../../../includes/tlasharptla-ui-md.md)] framework usando un <xref:System.Windows.Controls.DockPanel> elemento. El <xref:System.Windows.Controls.DockPanel> divide el espacio disponible en sus elementos secundarios.  
  
## <a name="example"></a>Ejemplo  
 Este ejemplo se usa el <xref:System.Windows.Controls.DockPanel.Dock%2A> propiedad, que es una propiedad adjunta para acoplar dos idénticos <xref:System.Windows.Controls.Border> elementos en el <xref:System.Windows.Controls.Dock.Top> del espacio particionado. Una tercera <xref:System.Windows.Controls.Border> se acopla al elemento el <xref:System.Windows.Controls.Dock.Left>, con un ancho establecido en 200 píxeles. Un cuarto <xref:System.Windows.Controls.Border> está acoplado el <xref:System.Windows.Controls.Dock.Bottom> de la pantalla. La última <xref:System.Windows.Controls.Border> elemento rellena automáticamente el espacio restante.  
  
 [!code-cpp[DockPanelOvwSample#1](../../../../samples/snippets/cpp/VS_Snippets_Wpf/DockPanelOvwSample/CPP/DockPanel_Ovw_Sample.cpp#1)]
 [!code-csharp[DockPanelOvwSample#1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/DockPanelOvwSample/CSharp/DockPanel_Ovw_Sample.cs#1)]
 [!code-vb[DockPanelOvwSample#1](../../../../samples/snippets/visualbasic/VS_Snippets_Wpf/DockPanelOvwSample/VisualBasic/dockpanel_vb.vb#1)]
 [!code-xaml[DockPanelOvwSample#1](../../../../samples/snippets/xaml/VS_Snippets_Wpf/DockPanelOvwSample/XAML/default.xaml#1)]  
  
> [!NOTE]
>  De forma predeterminada, el último elemento secundario de un <xref:System.Windows.Controls.DockPanel> elemento rellena el espacio sin asignar restante. Si no desea este comportamiento, establezca `LastChildFill="False"`.  
  
 La aplicación compilada genera una nueva interfaz de usuario que tiene esta apariencia.  
  
 ![Escenario DockPanel típico.](../../../../docs/framework/wpf/controls/media/panel-intro-dockpanel.PNG "panel_intro_dockpanel")  
  
## <a name="see-also"></a>Vea también
- <xref:System.Windows.Controls.DockPanel>
- [Información general sobre elementos Panel](../../../../docs/framework/wpf/controls/panels-overview.md)
