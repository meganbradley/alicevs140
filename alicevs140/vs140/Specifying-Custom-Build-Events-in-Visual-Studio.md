---
title: "Specifying Custom Build Events in Visual Studio"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 69e935a5-e208-4bcd-865c-3e5f9b047ca8
caps.latest.revision: 15
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Specifying Custom Build Events in Visual Studio
By specifying a custom build event, you can automatically run commands before a build starts or after it finishes. For example, you can run a .bat file before a build starts or copy new files to a folder after the build is complete. Build events run only if the build successfully reaches those points in the build process.  
  
 For specific information about the programming language that you’re using, see the following topics:  
  
-   Visual Basic--[How to: Specify Build Events](../vs140/How-to--Specify-Build-Events--Visual-Basic-.md).  
  
-   Visual C# and F#--[How to: Specify Build Events (C#)](../vs140/How-to--Specify-Build-Events--C#-.md).  
  
-   Visual C++--[Specifying Build Events](../vs140/Specifying-Build-Events.md).  
  
## Syntax  
 Build events follow the same syntax as DOS commands, but you can use macros to create build events more easily. For a list of available macros, see [Pre-build Event/Post-build Event Command Line Dialog Box](../vs140/Pre-build-Event-Post-build-Event-Command-Line-Dialog-Box.md).  
  
 For best results, follow these formatting tips:  
  
-   Add a `call` statement before all build events that run .bat files.  
  
     Example: `call C:\MyFile.bat`  
  
     Example: `call C:\MyFile.bat call C:\MyFile2.bat`  
  
-   Enclose file paths in quotation marks.  
  
     Example (for [!INCLUDE[win8](../vs140/includes/win8_md.md)]): "%ProgramFiles(x86)%\Microsoft SDKs\Windows\v8.0A\Bin\NETFX 4.0 Tools\gacutil.exe" -if "$(TargetPath)"  
  
-   Separate multiple commands by using line breaks.  
  
-   Include wildcards as needed.  
  
     Example: `for %I in (*.txt *.doc *.html) do copy %I c:\`*mydirectory*`\`  
  
    > [!NOTE]
    >  `%I` in the code above should be `%%I` in batch scripts.  
  
## See Also  
 [Building in Visual Studio](../vs140/Compiling-and-Building-in-Visual-Studio.md)   
 [Pre-build Event/Post-build Event Command Line Dialog Box](../vs140/Pre-build-Event-Post-build-Event-Command-Line-Dialog-Box.md)   
 [MSBuild Special Characters](../vs140/MSBuild-Special-Characters.md)   
 [Walkthrough: Building an Application](../vs140/Walkthrough--Building-an-Application.md)