---
title: "Error Handling in Wizard HTML Files"
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
ms.assetid: eb428a64-b681-4420-987d-92098bf98455
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Error Handling in Wizard HTML Files
When you create a wizard with a user interface, your project includes .htm files. Use these files to customize your project. See [The HTML Files](../vs140/HTML-Files.md) for more information.  
  
 Your project should include error handling. The following code provides you with an example of such code.  
  
### To handle errors in HTML  
  
1.  When you validate the fields, if you call a validation method in a DLL (which should set the error information), call `ReportError` with no parameters.  
  
    ```  
    function ValidateInput()  
    {  
       if (!window.external.ValidateFile(HEADER_FILE.value))  
       {  
          ReportError();  
          HEADER_FILE.focus();  
          return false;  
       }  
    }  
    ```  
  
2.  When you validate fields, if you validate the field using only the HTML script, call `SetErrorInfo` first and then call `ReportError` with no parameters.  
  
    ```  
    function OnWhatever()  
    {  
       if (!ValidateInput())  
          window.external.ReportErrror();  
       ....  
    }  
  
    function ValidateInput()  
    {  
       .....  
  
       if (HEADER_FILE.value == IMPL_FILE.value)  
       {  
          var L_ErrMsg_Text = "Header and implementation files cannot have the same name.";  
          SetErrorInfo(L_ErrMsg_Text);  
          bValid = false;  
       }  
       if (TYPE.value == "")  
       {  
          var L_ErrMsg4_Text = "Type cannot be blank.";  
          SetErrorInfo(L_ErrMsg4_Text);  
          bValid = false;  
       }  
       return bValid;  
    }  
    ```  
  
3.  Call `ReportError` with parameters:  
  
    ```  
    function ValidateInput()  
    {  
       if (!IsListed(strType))  
       {  
          var L_Invalid2_Text = "The variable type should be one of the types listed.";  
          window.external.ReportError(L_Invalid2_Text);  
          VariableType.focus();  
          return false;  
       }  
    }  
    ```  
  
4.  If you must go back to the **New Project** or **Add New Item** dialog box, return **VS_E_WIZBACKBUTTONPRESS**:  
  
    ```  
    try  
    {  
       oCM   = window.external.ProjectObject.CodeModel;  
    }  
    catch(e)  
    {  
       var L_NCBError_Text = "Cannot access the Class View information   
    file. Class View information will not be available.";  
       window.external.ReportError(L_NCBError_Text);  
       return VS_E_WIZARDBACKBUTTONPRESS;  
    ```  
  
## See Also  
 [Files Created for Your Wizard](../vs140/Files-Created-for-Your-Wizard.md)   
 [Customizing Your Wizard](../vs140/Customizing-Your-Wizard.md)