---
title: "How to: Read From a Text File (C# Programming Guide)"
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
ms.assetid: 92246c5b-e819-4eea-9370-1a9460e12de3
caps.latest.revision: 19
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Read From a Text File (C# Programming Guide)
This example reads the contents of a text file by using the static methods <xref:System.IO.File.ReadAllText?qualifyHint=False> and <xref:System.IO.File.ReadAllLines?qualifyHint=False> from the <xref:System.IO.File?qualifyHint=True> class.  
  
 For an example that uses <xref:System.IO.StreamReader?qualifyHint=False>, see [How to: Read a Text File One Line at a Time (Visual C#)](../Topic/How%20to:%20Read%20a%20Text%20File%20One%20Line%20at%20a%20Time%20\(Visual%20C%23\).md).  
  
> [!NOTE]
>  The files that are used in this example are created in the topic [How to: Write to a Text File (C# Programming Guide)](../Topic/How%20to:%20Write%20to%20a%20Text%20File%20\(C%23%20Programming%20Guide\).md).  
  
## Example  
 [!CODE [csFilesandFolders#4](../CodeSnippet/VS_Snippets_VBCSharp/csFilesAndFolders#4)]  
  
## Compiling the Code  
 Copy the code and paste it into a C# console application.  
  
 If you are not using the text files from [How to: Write to a Text File (C# Programming Guide)](../Topic/How%20to:%20Write%20to%20a%20Text%20File%20\(C%23%20Programming%20Guide\).md), replace the argument to `ReadAllText` and `ReadAllLines` with the appropriate path and file name on your computer.  
  
## Robust Programming  
 The following conditions may cause an exception:  
  
-   The file doesn't exist or doesn't exist at the specified location. Check the path and the spelling of the file name.  
  
## .NET Framework Security  
 Do not rely on the name of a file to determine the contents of the file. For example, the file `myFile.cs` might not be a C# source file.  
  
## See Also  
 <xref:System.IO?qualifyHint=True>   
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [Files, Folders and Drives](../Topic/File%20System%20and%20the%20Registry%20\(C%23%20Programming%20Guide\).md)