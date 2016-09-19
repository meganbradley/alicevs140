---
title: "How to: Display Unbound Controls in a DataRepeater Control (Visual Studio)"
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
ms.assetid: f234fa40-5a13-4209-930e-7c5f81e86e66
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Display Unbound Controls in a DataRepeater Control (Visual Studio)
In addition to bound controls, you may want to add other controls to a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>, such as a static label or an image that is repeated on each item in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
> [!NOTE]
>  You must also have at least one bound control on the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> or nothing will be displayed at run time.  
  
### To add unbound controls to a DataRepeater  
  
1.  Drag a <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control from the **Visual Basic PowerPacks** tab in the **Toolbox** to a form or container control.  
  
2.  Drag the sizing and position handles to size and position the control.  
  
     You can also size and position the control by changing the **Size** and **Position** properties in the Properties window.  
  
3.  Add at least one data-bound control to the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control. For more information, see [How to: Display Bound Data in a DataRepeater Control (Visual Basic)](../Topic/How%20to:%20Display%20Bound%20Data%20in%20a%20DataRepeater%20Control%20\(Visual%20Studio\).md).  
  
4.  Drag a control from the **Toolbox** onto the item template region of the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control.  
  
     Note that the control has two rectangular regions. The inner region is the *item template*; controls added to the template will be repeated in each item in the <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False> control at run time. The outer region is the *viewport*, where the items will be displayed; controls that are added to this region will not be displayed at run time.  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks.DataRepeater?qualifyHint=False>   
 [Introduction to the DataRepeater Control (Visual Basic)](../Topic/Introduction%20to%20the%20DataRepeater%20Control%20\(Visual%20Studio\).md)   
 [Troubleshooting the DataRepeater Control (Visual Basic)](../vs140/Troubleshooting-the-DataRepeater-Control--Visual-Studio-.md)   
 [How to: Display Bound Data in a DataRepeater Control (Visual Basic)](../Topic/How%20to:%20Display%20Bound%20Data%20in%20a%20DataRepeater%20Control%20\(Visual%20Studio\).md)   
 [How to: Create a Master/Detail Form by Using Two DataRepeater Controls (Visual Basic)](../Topic/How%20to:%20Create%20a%20Master-Detail%20Form%20by%20Using%20Two%20DataRepeater%20Controls%20\(Visual%20Studio\).md)   
 [How to: Change the Appearance of a DataRepeater Control (Visual Basic)](../vs140/How-to--Change-the-Appearance-of-a-DataRepeater-Control--Visual-Studio-.md)