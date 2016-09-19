---
title: "Customizing Your Wizard"
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
ms.assetid: a3ff1c81-3eef-41e7-a6bc-2f98e4bf423f
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Customizing Your Wizard
You must consider the following common tasks as you customize the wizard you created with the [Custom Wizard](../vs140/Application-Settings--Custom-Wizard.md).  
  
-   In the .vsz file, specify any custom parameters necessary for your wizard to work. See [The .vsz File (Project Control)](../Topic/.Vsz%20File%20\(Project%20Control\).md) and [Predefined Custom Wizard Symbols](../vs140/Custom-Parameters-in-the-Wizard-.Vsz-File.md) for more information.  
  
     If you localize your wizard to several different languages, add those language parameters to the .vsz file. See [Localizing a Wizard to Multiple Languages](../vs140/Localizing-a-Wizard-to-Multiple-Languages.md) for more information.  
  
-   Customize the [template files](../vs140/Template-Files.md) (and [Templates.inf](../vs140/Templates.inf-File.md)) to specify the directives for user selections.  
  
-   Customize the [Default.js file](../vs140/JScript-File.md) to specify additional special handling for your wizard. You can write your own functions, and you can use functions provided in [Common.js](../vs140/Customizing-C---Wizards-with-Common-JScript-Functions.md).  
  
-   Design icons and other images that your HTML user interface will use.  
  
-   Design the HTML user interface.  
  
-   Add symbols to the HTML symbol table to match the buttons, controls, text boxes, and other elements that your wizard uses.  
  
     The following shows an excerpt of HTML provided by the Custom Wizard:  
  
    ```  
    <SYMBOL NAME="WIZARD_DIALOG_TITLE" TYPE=text VALUE="MyCustomWiz">  
          </SYMBOL>  
    <SYMBOL NAME="SAMPLE_CHECKBOX" TYPE=checkbox VALUE=true>  
          </SYMBOL>  
    ```  
  
     This wizard, titled MyCustomWiz, displays a check box that is selected by default.  
  
-   In the section marked `<SCRIPT LANGUAGE="JSCRIPT">` in the HTML files, add JScript function calls and access the Visual Studio Object Model to customize the behavior of your wizard. You must call these functions using `window.external`, as follows:  
  
    ```  
    window.external.AddSymbol("MAIN_FRAME_DEFAULT_STYLES", true);  
    window.external.AddSymbol("MAIN_FRAME_STYLE_FLAGS", "");  
    ```  
  
    > [!NOTE]
    >  The methods, properties, and events exposed through [Automation and Extensibility for Visual Studio](assetId:///f71a2253-3e68-4e5e-9a18-edbba816caf6), [Visual C++ Code Model](assetId:///dd6452c2-1054-44a1-b0eb-639a94a1216b), [Project Model](assetId:///06c1bbd9-4c79-4f97-ad6d-2b1dea8ecd1f), and [Wizard Model](assetId:///159395ac-33c7-47bf-ad42-4e1435ddc758) allow you to programmatically manage all aspects of the wizard project, from creation through build, in both the JScript files and .htm files.  
  
-   If necessary, customize the [.vsdir file](assetId:///e0a20da0-3680-4084-997e-dbe02db51da9), allowing information about the .vsz file and all other templates to be understood by the shell. For example, indicate the icon resource ID, flags, localized names, and so on.  
  
-   Create .htm files and template files in all languages for which your wizard needs to be localized. Add them to the appropriate project directories.  
  
-   [Provide context-sensitive Help](../vs140/Providing-Context-Sensitive-Help.md) for your wizard.  
  
## See Also  
 [Custom Wizard](../vs140/Custom-Wizard.md)   
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Steps to Designing a Wizard](../vs140/Steps-to-Designing-a-Wizard.md)   
 [Files Created for Your Wizard](../vs140/Files-Created-for-Your-Wizard.md)   
 [Providing Context-Sensitive Help](../vs140/Providing-Context-Sensitive-Help.md)   
 [Handling Errors in Wizards](../vs140/Handling-Errors-in-Wizards.md)