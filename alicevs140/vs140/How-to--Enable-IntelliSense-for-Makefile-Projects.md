---
title: "How to: Enable IntelliSense for Makefile Projects"
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
ms.assetid: 9443f453-f18f-4f12-a9a1-ef9dbf8b188f
caps.latest.revision: 17
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Enable IntelliSense for Makefile Projects
IntelliSense fails to operate in the IDE for Visual C++ makefile projects when certain project settings, or compiler options, are set up incorrectly. Use this procedure to configure Visual C++ makefile projects, so that IntelliSense works when makefile projects are open in the Visual Studio development environment.  
  
### To enable IntelliSense for makefile projects in the IDE  
  
1.  Open the **Property Pages** dialog box. For details, see [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md).  
  
2.  Expand the **Configuration Properties** node.  
  
3.  Select the **NMake** property page, and then modify properties under **IntelliSense** as appropriate.  
  
    -   Set the **Preprocessor Definitions** property to define any preprocessor symbols in your makefile project. See [/D (Preprocessor Definitions)](../Topic/-D%20\(Preprocessor%20Definitions\).md), for more information.  
  
    -   Set the **Include Search Path** property to specify the list of directories that the compiler will search to resolve file references that are passed to preprocessor directives in your makefile project. See [/I (Additional Include Directories)](../vs140/-I--Additional-Include-Directories-.md), for more information.  
  
         For projects that are built using CL.EXE from a Command Window, set the **INCLUDE** environment variable to specify directories that the compiler will search to resolve file references that are passed to preprocessor directives in your makefile project.  
  
    -   Set the **Forced Includes** property to specify which header files to process when building your makefile project. See [/FI (Name Forced Include File)](../Topic/-FI%20\(Name%20Forced%20Include%20File\).md), for more information.  
  
    -   Set the **Assembly Search Path** property to specify the list of directories that the compiler will search to resolve references to .NET assemblies in your project. See [/AI (Specify Metadata Directories)](../Topic/-AI%20\(Specify%20Metadata%20Directories\).md), for more information.  
  
    -   Set the **Forced Using Assemblies** property to specify which .NET assemblies to process when building your makefile project. See [/FU (Name Forced #using File)](../vs140/-FU--Name-Forced-#using-File-.md), for more information.  
  
    -   Set the **Additional Options** property to specify additional compiler switches to be used by Intellisense when parsing C++ files.  
  
4.  Click **OK** to close the property pages.  
  
5.  Use the **Save All** command to save the modified project settings.  
  
 The next time you open your makefile project in the Visual Studio development environment, run the **Clean Solution** command and then the **Build Solution** command on your makefile project. IntelliSense should work properly in the IDE.  
  
## See Also  
 [Using IntelliSense](../vs140/Using-IntelliSense.md)   
 [NMAKE Reference](../vs140/NMAKE-Reference.md)   
 [How to: Create a C++ Project From Existing Code](../vs140/How-to--Create-a-C---Project-from-Existing-Code.md)