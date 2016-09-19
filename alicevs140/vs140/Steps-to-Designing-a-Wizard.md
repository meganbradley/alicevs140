---
title: "Steps to Designing a Wizard"
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
ms.assetid: dc22746b-99e3-4569-a8b4-b3d7cbabf8f2
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Steps to Designing a Wizard
You can use a wizard to create and configure common project starter files. Like any project, creating a wizard takes planning. The following steps describe one way to familiarize yourself with the Visual C++ Custom Wizard and apply it to your own projects.  
  
1.  Examine the [custom wizard samples](assetId:///6afa2143-062c-4a68-81ca-66cbf4b95261) included with Visual Studio.  
  
2.  Lay the groundwork for the type of project the wizard should create. Like all application construction, this process can go through many hands and many different iterations.  
  
3.  Create your project with the Visual C++ [Custom Wizard](../vs140/Creating-a-Custom-Wizard.md), specifying user interface and page number options.  
  
    > [!NOTE]
    >  If you indicate no user interface (that is, if you clear **User interface** in [Application Settings, Custom Wizard](../vs140/Application-Settings--Custom-Wizard.md) in the Custom Wizard), your wizard sets the custom parameter WIZARD_UI=**FALSE** and creates project template files with no user input and no .htm files. As a result, you do not specify page numbers. See [The .vsz File (Project Control)](../Topic/.Vsz%20File%20\(Project%20Control\).md) for more information.  
  
4.  [Examine the basic project](../vs140/Examining-the-Basic-Wizard-Project.md) that the Custom Wizard created for you.  
  
5.  If your wizard has a user interface, run the wizard to [learn more about the mechanics of the custom wizard](../Topic/Examining%20the%20Mechanics%20of%20a%20Wizard.md).  
  
6.  [Customize the basic wizard](../vs140/Customizing-Your-Wizard.md).  
  
7.  [Add context-sensitive help](../vs140/Providing-Context-Sensitive-Help.md).  
  
8.  [Provide error handling](../vs140/Handling-Errors-in-Wizards.md) for the JScript and HTML code.  
  
9. Build and test the wizard.  
  
10. Debug your wizard. See [Debugging Script and Web Applications](../vs140/Debugging-Web-Applications-and-Script.md) for more information.  
  
    > [!NOTE]
    >  When you are debugging JScript, you cannot perform mixed-mode debugging with native code.  
  
## See Also  
 [Creating a Custom Wizard](../vs140/Creating-a-Custom-Wizard.md)   
 [Custom Wizard](../vs140/Custom-Wizard.md)   
 [Files Created for Your Wizard](../vs140/Files-Created-for-Your-Wizard.md)