---
title: "How to: Change the Appearance of a DataRepeater Control (Visual Studio)"
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
ms.assetid: 2af6dfce-760b-489e-b863-8da967f315c3
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Change the Appearance of a DataRepeater Control (Visual Studio)
You can change the appearance of a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control at design time by setting properties or at run time by handling the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem?qualifyHint=False> event.  
  
 Properties that you set at design time when the item template section of the control is selected will be repeated for each <xref:Microsoft.VisualBasic.PowerPacks.DataRepeaterItem?qualifyHint=False> at run time. Appearance-related properties of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control itself will be visible at run time only if a part of the container is left uncovered (for example, if the <xref:System.Windows.Forms.Control.Padding?qualifyHint=False> property is set to a large value).  
  
 At run time, appearance-related properties can be set based on conditions. For example, in a scheduling application, you might change the background color of an item to warn users when an item is past due. In the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem?qualifyHint=False> event handler, if you set a property in a conditional statement such as `If…Then`, you must also use an `Else` clause to specify the appearance when the condition is not met.  
  
### To change the appearance at design time  
  
1.  In the Windows Forms Designer, select the item template (upper) region of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
2.  In the Properties window, select a property and change the value. Common properties that affect appearance include <xref:System.Windows.Forms.Control.BackColor?qualifyHint=False>, <xref:System.Windows.Forms.Control.BackgroundImage?qualifyHint=False>, <xref:System.Windows.Forms.Panel.BorderStyle?qualifyHint=False>, and <xref:System.Windows.Forms.Control.ForeColor?qualifyHint=False>.  
  
### To change the appearance at run time  
  
1.  In the Code Editor, in the Event drop-down list, click **DrawItem**.  
  
2.  In the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem?qualifyHint=False> event handler, add code to set the properties:  
  
     [!CODE [VbPowerPacksDataRepeaterAppearance#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterAppearance#1)]  
  
## Example  
 Some common customizations for the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control include displaying the rows in alternating colors and changing the color of a field based on a condition. The following example shows how to perform these customizations. This example assumes that you have a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control that is bound to the Products table in the Northwind database.  
  
 [!CODE [VbPowerPacksDataRepeaterAlternateBackColor#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksDataRepeaterAlternateBackColor#1)]  
  
 Note that for both of these customizations, you must provide code to set the properties for both sides of the condition. If you do not specify the `Else` condition, you will see unexpected results at run time.  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater.DrawItem?qualifyHint=False>   
 [Introduction to the DataRepeater Control (Visual Basic)](../Topic/Introduction%20to%20the%20DataRepeater%20Control%20\(Visual%20Studio\).md)   
 [Troubleshooting the DataRepeater Control (Visual Basic)](../vs140/Troubleshooting-the-DataRepeater-Control--Visual-Studio-.md)   
 [How to: Display Bound Data in a DataRepeater Control (Visual Basic)](../Topic/How%20to:%20Display%20Bound%20Data%20in%20a%20DataRepeater%20Control%20\(Visual%20Studio\).md)   
 [How to: Display Unbound Data in a DataRepeater Control (Visual Basic)](../vs140/How-to--Display-Unbound-Controls-in-a-DataRepeater-Control--Visual-Studio-.md)   
 [How to: Display Item Headers in a DataRepeater Control (Visual Basic)](../vs140/How-to--Display-Item-Headers-in-a-DataRepeater-Control--Visual-Studio-.md)