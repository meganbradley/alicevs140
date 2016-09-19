---
title: "How to: Display Command Line Arguments (C# Programming Guide)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - CSharp
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b8479f2d-9e05-4d38-82da-2e61246e5437
caps.latest.revision: 21
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Display Command Line Arguments (C# Programming Guide)
Arguments provided to an executable on the command-line are accessible through an optional parameter to `Main`. The arguments are provided in the form of an array of strings. Each element of the array contains one argument. White-space between arguments is removed. For example, consider these command-line invocations of a fictitious executable:  
  
|Input on Command-line|Array of strings passed to Main|  
|----------------------------|-------------------------------------|  
|**executable.exe a b c**|"a"<br /><br /> "b"<br /><br /> "c"|  
|**executable.exe one two**|"one"<br /><br /> "two"|  
|**executable.exe "one two" three**|"one two"<br /><br /> "three"|  
  
> [!NOTE]
>  When you are running an application in Visual Studio, you can specify command-line arguments in the [Debug Page, Project Designer](../vs140/Debug-Page--Project-Designer.md).  
  
## Example  
 This example displays the command line arguments passed to a command-line application. The output shown is for the first entry in the table above.  
  
 [!CODE [csProgGuideMain#9](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideMain#9)]  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Command-line Building With csc.exe](../vs140/Command-line-Building-With-csc.exe.md)   
 [Main and Command Line Arguments](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md)   
 [How to: Access Command Line Arguments using foreach (C#)](../Topic/How%20to:%20Access%20Command-Line%20Arguments%20Using%20foreach%20\(C%23%20Programming%20Guide\).md)   
 [Main() Return Values (C#)](../vs140/Main---Return-Values--C#-Programming-Guide-.md)