---
title: "How to: Print a Scrollable Form (Visual Basic)"
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
ms.assetid: 1196e1cf-b77f-4928-a3e4-85b51ba3787d
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Print a Scrollable Form (Visual Basic)
The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm?qualifyHint=False> component enables you to quickly print an image of a form without using a <xref:System.Drawing.Printing.PrintDocument?qualifyHint=False> component. By default, only the currently visible part of the form is printed; if a user has resized the form at run time, the image may not print as intended. The following procedure shows how to print the complete client area of a scrollable form, even if the form has been resized.  
  
 The PowerPack controls are no longer included in Visual Studio, but you can download them from the [Download Center](http://www.microsoft.com/en-us/download/details.aspx?id=25169).  
  
### To print the complete client area of a scrollable form  
  
1.  In the **Toolbox**, click the **Visual Basic PowerPacks** tab and then drag the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm?qualifyHint=False> component onto the form.  
  
     The <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm?qualifyHint=False> component will be added to the component tray.  
  
2.  In the **Properties** window, set the <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction?qualifyHint=False> property to <xref:System.Drawing.Printing.PrintAction.PrintToPrinter?qualifyHint=False>.  
  
3.  Add the following code in the appropriate event handler (for example, in the `Click` event handler for a **Print**`Button`).  
  
    ```  
    PrintForm1.Print(Me, PowerPacks.Printing.PrintForm.PrintOption.Scrollable)  
    ```  
  
    > [!NOTE]
    >  On some operating systems, text or graphics drawn by <xref:System.Drawing.Graphics?qualifyHint=False> methods may not print correctly. In this case, you will not be able to print with the `Scrollable` parameter.  
  
## See Also  
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.PrintAction?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.PowerPacks.Printing.PrintForm.Print?qualifyHint=False>   
 [PrintForm Component](../Topic/PrintForm%20Component%20\(Visual%20Basic\).md)   
 [How to: Print the Client Area of a Form](../vs140/How-to--Print-the-Client-Area-of-a-Form--Visual-Basic-.md)   
 [How to: Print Client and Non-client Areas of a Form](../vs140/How-to--Print-Client-and-Non-Client-Areas-of-a-Form--Visual-Basic-.md)