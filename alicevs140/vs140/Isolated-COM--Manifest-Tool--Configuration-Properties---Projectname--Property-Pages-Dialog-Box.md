---
title: "Isolated COM, Manifest Tool, Configuration Properties, &lt;Projectname&gt; Property Pages Dialog Box"
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
ms.assetid: 457582b8-cfde-49c0-92e3-3a6b9e8c08eb
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Isolated COM, Manifest Tool, Configuration Properties, &lt;Projectname&gt; Property Pages Dialog Box
Use this dialog box to specify **Isolated COM** options for [Mt.exe](http://msdn.microsoft.com/library/aa375649).  
  
 To access this property page dialog box, open the property pages for your project or your property sheet. Expand the **Manifest Tool** node under **Common Properties**, and then select **Isolated COM**.  
  
## Task List  
  
-   [How to: Build Isolated Applications to Consume COM Components](../vs140/How-to--Build-Isolated-Applications-to-Consume-COM-Components.md)  
  
## UIElement List  
 **Type Library File**  
 Uses the /tlb option to specify the name of the type library file (.tlb file) that the manifest tool will use to generate the manifest file.  
  
 **Registrar Script File**  
 Uses the /rgs option to specify the name of the registrar script file (.rgs file) that the manifest tool will use to generate the manifest file.  
  
 **Component File Name**  
 Uses the /dll option to specify the name of the resource that the manifest tool will generate. You must enter a value for this property when values for either **Type Library File** or **Registrar Script File** are specified.  
  
 **Replacements File**  
 Uses the /replacements option to specify the full path to the file that contains values for replaceable strings in the .rgs file.  
  
## See Also  
 [Isolated Applications](http://msdn.microsoft.com/library/aa375190)   
 [Side-by-side Assemblies](_win32_side_by_side_assemblies)   
 [ClickOnce Application Manifest](../vs140/ClickOnce-Application-Manifest.md)   
 [Manifest Tool Property Pages](../vs140/Manifest-Tool-Property-Pages.md)   
 [How to: Open Project Property Pages](../vs140/How-to--Open-Project-Property-Pages.md)   
 [How to: Edit Project Property Sheets](../vs140/How-to--Edit-Project-Property-Sheets.md)