---
title: "Build Events Dialog Box (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3a81a7c7-39f9-47a8-ba5a-b351227f380e
caps.latest.revision: 6
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Build Events Dialog Box (Visual Basic)
Use the **Build Events** dialog box to specify build configuration instructions. You can also specify the conditions under which any pre-build or post-build events are run. For more information, see [How to: Specify Build Events](../vs140/How-to--Specify-Build-Events--Visual-Basic-.md).  
  
 **Pre-build event command line**  
 Specifies any commands to execute before the build starts. To type long commands, click **Edit Pre-build** to display the [Pre-build Event/Post-build Event Command Line Dialog Box](../vs140/Pre-build-Event-Post-build-Event-Command-Line-Dialog-Box.md).  
  
> [!NOTE]
>  Pre-build events do not run if the project is up-to-date and no build is triggered.  
  
 **Post-build event command line**  
 Specifies any commands to execute after the build ends. To type long commands, click **Edit Post-build** to display the **Pre-build Event/Post-build Event Command Line d**ialog box.  
  
> [!NOTE]
>  Add a `call` statement before all post-build commands that run .bat files. For example, `call C:\MyFile.bat` or `call C:\MyFile.bat call C:\MyFile2.bat`.  
  
 **Run the post-build event**  
 Specifies the conditions for the post-build event to run, as shown in the following table.  
  
|Option|Result|  
|------------|------------|  
|**Always**|Post-build event will run, regardless of whether the build succeeds.|  
|**On successful build**|Post-build event will run if the build succeeds. The event will run even for a project that is up-to-date, as long as the build succeeds. This is the default setting.|  
|**When the build updates the project output**|Post-build event will run only when the compiler's output file (.exe or .dll) differs from the previous compiler output file. A post-build event is not run if a project is up-to-date.|  
  
## See Also  
 [Compile Page, Project Designer (Visual Basic)](../vs140/Compile-Page--Project-Designer--Visual-Basic-.md)   
 [How to: Specify Build Events](../vs140/How-to--Specify-Build-Events--Visual-Basic-.md)   
 [Pre-build Event/Post-build Event Command Line Dialog Box](../vs140/Pre-build-Event-Post-build-Event-Command-Line-Dialog-Box.md)