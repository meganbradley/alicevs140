---
title: "How to: Search Data in a DataRepeater Control (Visual Studio)"
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
ms.assetid: a8ab5d17-b94f-43c4-8dd7-d0450226d73f
caps.latest.revision: 13
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Search Data in a DataRepeater Control (Visual Studio)
When you are using a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control that contains many records, you may want to let users search for a specific record. Rather than searching the data in the control itself, you can implement a search by querying the underlying <xref:System.Windows.Forms.BindingSource?qualifyHint=False>. If the item is found, you can then use the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.CurrentItemIndex?qualifyHint=False> property to select the item and scroll it into view.  
  
### To implement search  
  
1.  Drag a <xref:System.Windows.Forms.TextBox?qualifyHint=False> control from the **Toolbox** onto the form that contains the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
2.  In the Properties window, change the **Name** property to **SearchTextBox**.  
  
3.  Drag a <xref:System.Windows.Forms.Button?qualifyHint=False> control from the **Toolbox** onto the form that contains the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
4.  In the Properties window, change the **Name** property to **SearchButton**. Change the **Text** property to **Search**.  
  
5.  Double-click the <xref:System.Windows.Forms.Button?qualifyHint=False> control to open the Code Editor, and add the following code to the `SearchButton_Click` event handler.  
  
     [!CODE [VbPowerPacksDataRepeaterSearch#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterSearch#1)]  
  
     Replace *ProductsBindingSource* with the name of the <xref:System.Windows.Forms.BindingSource?qualifyHint=False> for your <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>, and replace *ProductID* with the name of the field that you want to search.  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>   
 [Introduction to the DataRepeater Control (Visual Basic)](../Topic/Introduction%20to%20the%20DataRepeater%20Control%20\(Visual%20Studio\).md)   
 [Troubleshooting the DataRepeater Control (Visual Basic)](../vs140/Troubleshooting-the-DataRepeater-Control--Visual-Studio-.md)   
 [How to: Change the Appearance of a DataRepeater Control (Visual Basic)](../vs140/How-to--Change-the-Appearance-of-a-DataRepeater-Control--Visual-Studio-.md)