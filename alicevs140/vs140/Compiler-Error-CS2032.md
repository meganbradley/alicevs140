---
title: "Compiler Error CS2032"
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
ms.topic: error-reference
ms.assetid: 534e2d2f-d209-43dd-abc9-e5ea5b01efc4
caps.latest.revision: 16
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error CS2032
Character 'character' is not allowed on the command-line or in response files  
  
 Response files and the command line options for csc.exe cannot contain ASCII control characters in the range 0-31 or the pipe (`|`) character.  
  
 Compiler error CS2032 is difficult to demonstrate from the command line because the command line processor and the integrated development environment (IDE) filter out characters that are not valid. The following procedure generates the error by using a [response file](../vs140/@--C#-Compiler-Options-.md).  
  
### To generate this error  
  
1.  In the **My Documents** folder, create a text file that is named CS2032.rsp, and then enter the following compiler options in it:  
  
    ```c#  
    /target:exe /out:cs|2032.exe cs2032.cs  
    ```  
  
2.  In the **My Documents** folder, create a text file that is named cs2032.cs and that contains whatever you want.  
  
3.  Open **Start**, and then choose **All Programs**, **Microsoft Visual Studio 2010**, **Visual Studio Tools**, **Visual Studio Command Prompt**.  
  
     The **Visual Studio Command Prompt** window opens.  
  
4.  In the **Visual Studio Command Prompt** window, change the current directory to C:\Users\\*YourUsername*\Documents.  
  
5.  Run the following command from the **Visual Studio Command Prompt**: `csc @cs2032.rsp`  
  
6.  The CS2032 error message appears because the response file, CS2032.rsp, contains a pipe character.