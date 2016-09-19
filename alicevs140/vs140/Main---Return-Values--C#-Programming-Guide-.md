---
title: "Main() Return Values (C# Programming Guide)"
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
ms.assetid: c2f5a1d8-1676-4bea-bc7e-44a97e72d5bc
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Main() Return Values (C# Programming Guide)
The `Main` method can return `void`:  
  
 [!CODE [csProgGuideMain#12](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideMain#12)]  
  
 It can also return an `int`:  
  
 [!CODE [csProgGuideMain#13](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideMain#13)]  
  
 If the return value from `Main` is not used, returning `void` allows for slightly simpler code. However, returning an integer enables the program to communicate status information to other programs or scripts that invoke the executable file. The following example shows how the return value from `Main` can be accessed.  
  
## Example  
 In this example, a batch file is used to run a program and test the return value of the `Main` function. When a program is executed in Windows, any value returned from the `Main` function is stored in an environment variable called `ERRORLEVEL`. A batch file can determine the outcome of execution by inspecting the `ERRORLEVEL` variable. Traditionally, a return value of zero indicates successful execution. The following example is a simple program that returns zero from the `Main` function. The zero indicates that the program ran successfully. Save the program as MainReturnValTest.cs.  
  
 [!CODE [csProgGuideMain#14](../CodeSnippet/VS_Snippets_VBCSharp/csProgGuideMain#14)]  
  
## Example  
 Because this example uses a batch file, it is best to compile the code from a command prompt. Follow the instructions in [How to: Build from the Command Line](../vs140/How-to--Set-Environment-Variables-for-the-Visual-Studio-Command-Line.md) to enable command-line builds, or use the Visual Studio Command Prompt, available from the **Start** menu under **Visual Studio Tools**. From the command prompt, navigate to the folder in which you saved the program. The following command compiles MainReturnValTest.cs and produces the executable file MainReturnValTest.exe.  
  
 `csc MainReturnValTest.cs`  
  
 Next, create a batch file to run MainReturnValTest.exe and to display the result. Paste the following code into a text file and save it as `test.bat` in the folder that contains MainReturnValTest.cs and MainReturnValTest.exe. Run the batch file by typing `test` at the command prompt.  
  
 Because the code returns zero, the batch file will report success. However, if you change MainReturnValTest.cs to return a non-zero value and then re-compile the program, subsequent execution of the batch file will report failure.  
  
```  
rem test.bat  
@echo off  
MainReturnValTest  
@if "%ERRORLEVEL%" == "0" goto good  
  
:fail  
    echo Execution Failed  
    echo return value = %ERRORLEVEL%  
    goto end  
  
:good  
    echo Execution succeeded  
    echo Return value = %ERRORLEVEL%  
    goto end  
  
:end  
```  
  
## Sample Output  
 `Execution succeeded`  
  
 `Return value = 0`  
  
## See Also  
 [C# Programming Guide](../vs140/C#-Programming-Guide.md)   
 [C# Reference](../vs140/C#-Reference.md)   
 [Main() and Command Line Arguments (C#)](../Topic/Main\(\)%20and%20Command-Line%20Arguments%20\(C%23%20Programming%20Guide\).md)   
 [How to: Print Command Line Arguments (C#)](../vs140/How-to--Display-Command-Line-Arguments--C#-Programming-Guide-.md)   
 [How to: Access Command Line Arguments using foreach (C#)](../Topic/How%20to:%20Access%20Command-Line%20Arguments%20Using%20foreach%20\(C%23%20Programming%20Guide\).md)