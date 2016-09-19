---
title: "How to: Disable Adding and Deleting DataRepeater Items (Visual Studio)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 298d8f60-ddfe-4361-ab66-cf76d0df5220
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Disable Adding and Deleting DataRepeater Items (Visual Studio)
By default, users can add and delete items in a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control. Users can add a new item by pressing CTRL+N when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem?qualifyHint=False> has focus or by clicking the **AddNewItem** button on the <xref:System.Windows.Forms.BindingNavigator?qualifyHint=False> control. Users can delete an item by pressing DELETE when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItemEventArgs.DataRepeaterItem?qualifyHint=False> has focus or by clicking the **DeleteItem** button on the <xref:System.Windows.Forms.BindingNavigator?qualifyHint=False> control.  
  
 You can disable adding and/or deleting at design time or at run time.  
  
### To disable adding and deleting at design time  
  
1.  In the Windows Forms Designer, select the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
    > [!NOTE]
    >  You must select the lower section of the control. If you select the item template section, a different set of properties will be displayed.  
  
2.  In the Properties window, set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToAddItems?qualifyHint=False> property to **False**.  
  
3.  Set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.AllowUserToDeleteItems?qualifyHint=False> property to **False**.  
  
4.  In the Windows Forms Designer, select the <xref:System.Windows.Forms.BindingNavigator?qualifyHint=False> control, and then click the **AddNewItem** button (the button with a plus sign on it).  
  
5.  In the Properties window, set the <xref:System.Windows.Forms.ToolBarButton.Enabled?qualifyHint=False> property to **False**.  
  
6.  In the Windows Forms Designer, select the <xref:System.Windows.Forms.BindingNavigator?qualifyHint=False> control, and then click the **DeleteItem** button (the button with a red X on it).  
  
7.  In the Properties window, set the <xref:System.Windows.Forms.ToolBarButton.Enabled?qualifyHint=False> property to **False**.  
  
8.  In the Component Tray, select the <xref:System.Windows.Forms.BindingSource?qualifyHint=False> to which the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> is bound.  
  
9. In the Properties window, set the <xref:System.Windows.Forms.BindingSource.AllowNew?qualifyHint=False> property to **False**.  
  
10. In the Windows Forms Designer, double-click the **DeleteItem** button to open the Code Editor.  
  
11. In the Events drop-down list, select the `BindingNavigatorDeleteItem_EnabledChanged` event.  
  
12. Add the following code to the `BindingNavigatorDeleteItem_EnabledChanged` event handler:  
  
     [!CODE [VbPowerPacksDataRepeaterDisableAddDelete#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterDisableAddDelete#1)]  
  
    > [!NOTE]
    >  This step is necessary because the <xref:System.Windows.Forms.BindingSource?qualifyHint=False> will enable the **DeleteItem** button every time that the current record changes.  
  
### To disable adding and deleting at run time  
  
1.  In the Windows Forms Designer, double-click the form to open the Code Editor.  
  
2.  Add the following code to the `Form_Load` event:  
  
     [!CODE [VbPowerPacksDataRepeaterDisableAddDelete#2](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterDisableAddDelete#2)]  
  
3.  Add the following code to the `BindingNavigatorDeleteItem_EnabledChanged` event handler:  
  
     [!CODE [VbPowerPacksDataRepeaterDisableAddDelete#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterDisableAddDelete#1)]  
  
    > [!NOTE]
    >  This step is necessary because the <xref:System.Windows.Forms.BindingSource?qualifyHint=False> will enable the **DeleteItem** button every time that the current record changes.  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>   
 [Introduction to the DataRepeater Control (Visual Basic)](../Topic/Introduction%20to%20the%20DataRepeater%20Control%20\(Visual%20Studio\).md)   
 [Troubleshooting the DataRepeater Control (Visual Basic)](../vs140/Troubleshooting-the-DataRepeater-Control--Visual-Studio-.md)