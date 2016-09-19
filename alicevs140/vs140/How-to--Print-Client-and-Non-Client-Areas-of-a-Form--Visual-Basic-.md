---
title: "How to: Print Client and Non-Client Areas of a Form (Visual Basic)"
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
ms.assetid: 856bb0e4-dbc3-47e2-81cd-4b376cf07757
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Print Client and Non-Client Areas of a Form (Visual Basic)
The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm?qualifyHint=False> component enables you to quickly print an image of a form exactly as it appears on screen without using a <xref:System.Drawing.Printing.PrintDocument?qualifyHint=False> component. The following procedure shows how to print a form, including both the client area and the non-client area. The non-client area includes the title bar, borders, and scroll bars.  
  
 The PowerPack controls are no longer included in Visual Studio, but you can download them from the [Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=25169).  
  
### To print both the client and the non-client areas of a form  
  
1.  In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm?qualifyHint=False> component onto the form.  
  
     The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm?qualifyHint=False> component is added to the component tray.  
  
2.  In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction?qualifyHint=False> property to <xref:System.Drawing.Printing.PrintAction.PrintToPrinter?qualifyHint=False>.  
  
3.  Add the following code in the appropriate event handler (for example, in the `Click` event handler for a Print `Button`).  
  
    ```  
    PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.FullWindow)  
    ```  
  
    > [!NOTE]
    >  On some operating systems, text or graphics drawn by <xref:System.Drawing.Graphics?qualifyHint=False> methods may not print correctly. In this case, use the compatible printing method: `PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.CompatibleModeFullWindow`).  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.Print?qualifyHint=False>   
 [PrintForm Component](../Topic/PrintForm%20Component%20\(Visual%20Basic\).md)   
 [How to: Print a Scrollable Form](../vs140/How-to--Print-a-Scrollable-Form--Visual-Basic-.md)