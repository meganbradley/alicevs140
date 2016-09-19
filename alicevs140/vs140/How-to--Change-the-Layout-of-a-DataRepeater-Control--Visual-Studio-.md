---
title: "How to: Change the Layout of a DataRepeater Control (Visual Studio)"
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
ms.assetid: 33aa8fd5-ac63-4bd0-ba13-8c2ab17e7824
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Change the Layout of a DataRepeater Control (Visual Studio)
The <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control can be displayed in either a vertical (items scroll vertically) or horizontal (items scroll horizontally) orientation. You can change the orientation at design time or at run time by changing the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle?qualifyHint=False> property. If you change the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle?qualifyHint=False> property at run time, you may also want to resize the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate?qualifyHint=False> and reposition the child controls.  
  
> [!NOTE]
>  If you reposition controls on the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate?qualifyHint=False> at run time, you will need to call the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate?qualifyHint=False> and <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate?qualifyHint=False> methods at the beginning and end of the code block that repositions the controls.  
  
### To change the layout at design time  
  
1.  In the Windows Forms Designer, select the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
    > [!NOTE]
    >  You must select the outer border of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control by clicking in the lower region of the control, not in the upper <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate?qualifyHint=False> region.  
  
2.  In the Properties window, set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle?qualifyHint=False> property to either <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Vertical?qualifyHint=False> or <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal?qualifyHint=False>.  
  
### To change the layout at run time  
  
1.  Add the following code to a button or menu `Click` event handler:  
  
     [!CODE [VbPowerPacksDataRepeaterLayout#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterLayout#1)]  
  
2.  In most cases, you will want to add code similar to that shown in the Example section to resize the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate?qualifyHint=False> and rearrange controls to fit the new orientation.  
  
## Example  
 The following example shows how to respond to the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyleChanged?qualifyHint=False> event in an event handler. This example requires that you have a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control named `DataRepeater1` on a form and that its <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate?qualifyHint=False> contain two <xref:System.Windows.Forms.TextBox?qualifyHint=False> controls named `TextBox1` and `TextBox2`.  
  
 [!CODE [VbPowerPacksDataRepeaterLayout#2](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterLayout#2)]  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.BeginResetItemTemplate?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.EndResetItemTemplate?qualifyHint=False>   
 [Introduction to the DataRepeater Control (Visual Basic)](../Topic/Introduction%20to%20the%20DataRepeater%20Control%20\(Visual%20Studio\).md)   
 [Troubleshooting the DataRepeater Control (Visual Basic)](../vs140/Troubleshooting-the-DataRepeater-Control--Visual-Studio-.md)   
 [How to: Change the Appearance of a DataRepeater Control (Visual Basic)](../vs140/How-to--Change-the-Appearance-of-a-DataRepeater-Control--Visual-Studio-.md)