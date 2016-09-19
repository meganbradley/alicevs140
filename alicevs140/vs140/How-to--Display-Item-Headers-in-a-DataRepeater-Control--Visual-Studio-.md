---
title: "How to: Display Item Headers in a DataRepeater Control (Visual Studio)"
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
ms.assetid: 37321447-0ffa-43e1-bdc9-0480e392b90f
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Display Item Headers in a DataRepeater Control (Visual Studio)
The item header in a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control provides a visual indicator when a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem?qualifyHint=False> is selected. When the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle?qualifyHint=False> property is set to <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Vertical?qualifyHint=False> (the default), the item header is displayed to the left of each item. When the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle?qualifyHint=False> property is set to <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal?qualifyHint=False>, the item header is displayed at the top of each item.  
  
 When it is first selected, the item header is displayed in the color that is specified by the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor?qualifyHint=False> property, and a white arrow icon is displayed.  
  
> [!NOTE]
>  If you set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor?qualifyHint=False> to <xref:System.Drawing.Color.White?qualifyHint=False>, the selection symbol will not be visible when the item is first selected.  
  
 When a field in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem?qualifyHint=False> has focus, the color of the item header changes to the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemTemplate?qualifyHint=False> background color and the arrow icon changes to black. If data is changed, a pencil symbol is displayed in the item header.  
  
 The default width (or height when the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.LayoutStyle?qualifyHint=False> property is set to <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterLayoutStyles.Horizontal?qualifyHint=False>) of the item header is 15 pixels. You can change the width by setting the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize?qualifyHint=False> property.  
  
> [!NOTE]
>  If the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize?qualifyHint=False> property is set to a value that is less than 11, the indicator symbols in the item header will not be displayed.  
  
 You can hide the item headers by setting the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderVisible?qualifyHint=False> property to **False**. When <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderVisible?qualifyHint=False> is set to **False**, the only indication that an item is selected is a dotted line around the perimeter of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem?qualifyHint=False>.  
  
> [!NOTE]
>  You can also provide your own selection indicator by monitoring the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem.IsCurrent?qualifyHint=False> property of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem?qualifyHint=False> in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem?qualifyHint=False> event of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control. For more information, see <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem.IsCurrent?qualifyHint=False>.  
  
### To change the appearance of item headers  
  
1.  In the Windows Forms Designer, select the lower region of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
    > [!NOTE]
    >  You must select the lower region of the control. If you select the item template section, a different set of properties will appear in the Properties window.  
  
2.  In the Properties window, use the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor?qualifyHint=False> property to change the color of the item headers.  
  
    > [!NOTE]
    >  If you set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.SelectionColor?qualifyHint=False> to <xref:System.Drawing.Color.White?qualifyHint=False>, the selection symbol will not be visible when the item is first selected.  
  
3.  Use the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize?qualifyHint=False> property to change the width (or height) of the item headers.  
  
    > [!NOTE]
    >  If the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderSize?qualifyHint=False> property is set to a value that is less than 11, the indicator symbols in the item header will not be displayed.  
  
### To hide item headers  
  
1.  In the Windows Forms Designer, select the lower region of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
    > [!NOTE]
    >  You must select the lower region of the control. If you select the item template section, a different set of properties will appear in the Properties window.  
  
2.  In the Properties window, set the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.ItemHeaderVisible?qualifyHint=False> property to **False**.  
  
     When an item in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> is selected, the only indication will be a dotted line around the perimeter of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem?qualifyHint=False>.  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>   
 [Introduction to the DataRepeater Control (Visual Basic)](../Topic/Introduction%20to%20the%20DataRepeater%20Control%20\(Visual%20Studio\).md)   
 [How to: Change the Appearance of a DataRepeater Control (Visual Basic)](../vs140/How-to--Change-the-Appearance-of-a-DataRepeater-Control--Visual-Studio-.md)   
 [How to: Change the Layout of a DataRepeater Control (Visual Basic)](../vs140/How-to--Change-the-Layout-of-a-DataRepeater-Control--Visual-Studio-.md)   
 [Troubleshooting the DataRepeater Control (Visual Basic)](../vs140/Troubleshooting-the-DataRepeater-Control--Visual-Studio-.md)