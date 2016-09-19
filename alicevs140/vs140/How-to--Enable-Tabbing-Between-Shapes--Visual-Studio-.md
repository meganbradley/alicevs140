---
title: "How to: Enable Tabbing Between Shapes (Visual Studio)"
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
ms.assetid: 09731b34-3900-4fcb-a9df-ce5280328433
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Enable Tabbing Between Shapes (Visual Studio)
Line and shape controls do not have `TabStop` or `TabIndex` properties, but you can still enable tabbing among them. In the following example, pressing both the CTRL and the TAB keys will tab between shapes; pressing only the TAB key will tab between the buttons.  
  
> [!NOTE]
>  Your computer might show different names or locations for some of the Visual Studio user interface elements in the following instructions. The Visual Studio edition that you have and the settings that you use determine these elements. For more information, see [Customizing Development Settings in Visual Studio](assetId:///22c4debb-4e31-47a8-8f19-16f328d7dcd3).  
  
### To enable tabbing among shapes  
  
1.  Drag three <xref:Microsoft.VisualBasic.PowerPacks.RectangleShape?qualifyHint=False> controls and two <xref:System.Windows.Forms.Button?qualifyHint=False> controls from the **Toolbox** to a form.  
  
2.  In the **Code Editor**, add an `Imports` or `using` statement at the top of the module:  
  
    ```vb#  
    Imports Microsoft.VisualBasic.PowerPacks  
    ```  
  
    ```c#  
    using Microsoft.VisualBasic.PowerPacks;  
    ```  
  
3.  Add the following code in an event procedure:  
  
     [!CODE [VbPowerPacksTabbing#1](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksTabbing#1)]  
  
4.  Add the following code in the `Button1_PreviewKeyDown` event procedure:  
  
     [!CODE [VbPowerPacksTabbing#2](../CodeSnippet/VS_Snippets_VBCSharp/VbPowerPacksTabbing#2)]  
  
## See Also  
 [How to: Draw Shapes with the OvalShape and RectangleShape Controls (Visual Basic)](../Topic/How%20to:%20Draw%20Shapes%20with%20the%20OvalShape%20and%20RectangleShape%20Controls%20\(Visual%20Studio\).md)   
 [How to: Draw Lines with the LineShape Control (Visual Basic)](../Topic/How%20to:%20Draw%20Lines%20with%20the%20LineShape%20Control%20\(Visual%20Studio\).md)   
 [Introduction to the Line and Shape Controls (Visual Basic)](../vs140/Introduction-to-the-Line-and-Shape-Controls--Visual-Studio-.md)