---
title: "HTML Files"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b6ed080-6560-418b-b908-d84d71bdf145
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# HTML Files
A wizard can contain a user interface, which is an HTML interface. Along with Default.htm, a wizard can contain any number of .htm files, which you can indicate in the **Number of Pages** box in the [Custom Wizard](../vs140/Custom-Wizard.md). Each .htm file represents an HTML page of your wizard, and the HTML page is accessible using `Next` and **Back** buttons, tabs, or any other format you specify in your wizard design.  
  
 The HTML contains:  
  
-   The SYMBOL tag, which identifies the default for user-defined options. Symbols are written into the symbol table when the user clicks **Finish**, such as:  
  
```  
<SYMBOL NAME='HEADER_FILE' VALUE='MyHeader.h' TYPE=text></SYMBOL>  
```  
  
 In the wizard user interface (UI), the text box identified in the symbol table as "HEADER_FILE" contains the default text "MyHeader.h". You can change this value in the wizard UI, and the resulting value is written to the project's symbol table when you click **Finish**, such as:  
  
```  
<SYMBOL NAME='CHECKBOX1' TYPE=checkbox VALUE=false></SYMBOL>  
```  
  
 In the wizard UI, the check box identified in the symbol table as "CHECKBOX1" is cleared by default. You can select this box in the HTML UI, and the resulting value is written to the symbol table when you click **Finish**.  
  
 Each .htm file records user selections to the symbols table.  
  
-   An include for [Common.js](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md), which contains commonly used and helpful JScript functions, and Default.js.  
  
-   References to the project's images to display in the HTML.  
  
-   HTML text and formatting that customize the appearance of the wizard's user interface  
  
-   JScript functions that access the Visual C++ Wizard Object Model to provide customized behavior from within the wizard. These functions are in the HTML page section headed <SCRIPT LANGUAGE='JSCRIPT'\>, as shown in the following example.  
  
    > [!NOTE]
    >  To access the Wizard and Environment Object Models from HTML, prepend the object model item with "window.external."  
  
    ```  
    function InitDocument(document)  
    {  
       setDirection();  
  
       if (window.external.FindSymbol('DOCUMENT_FIRST_LOAD'))  
       {  
          // This function sets the default symbols based   
          // on the values specified in the SYMBOL tags above  
          //  
          window.external.SetDefaults(document);  
       }  
  
       // Load the document and initialize the controls   
       // with the appropriate symbol values  
       //  
       window.external.Load(document);  
    }  
    ```  
  
 The following is a sample console application wizard:  
  
```  
<SYMBOL NAME='WIZARD_DIALOG_TITLE' TYPE=text VALUE='Console Application Wizard'></SYMBOL>  
  
<SYMBOL NAME='EMPTY_PROJECT' TYPE=checkbox VALUE=false></SYMBOL>  
<SYMBOL NAME='SUPPORT_ATL' TYPE=checkbox VALUE=false></SYMBOL>  
<SYMBOL NAME='SUPPORT_MFC' TYPE=checkbox VALUE=false></SYMBOL>  
```  
  
## See Also  
 [Files Created for Your Wizard](../vs140/Files-Created-for-Your-Wizard.md)   
 [Custom Wizard](../vs140/Custom-Wizard.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Designing a Wizard](../Topic/Designing%20a%20Wizard.md)