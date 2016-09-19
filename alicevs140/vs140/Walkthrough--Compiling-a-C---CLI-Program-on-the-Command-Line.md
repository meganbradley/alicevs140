---
title: "Walkthrough: Compiling a C++-CLI Program on the Command Line"
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
H1: Walkthrough: Compiling a C++/CLI Program on the Command Line
ms.assetid: cef41c88-faf9-439d-8423-25aa3f5674dd
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Compiling a C++-CLI Program on the Command Line
You can create Visual C++ programs that target the Common Language Runtime (CLR) and use the .NET Framework, and build them on the command line. Visual C++ supports the C++/CLI programming language, which has additional types and operators to target the .NET programming model. For an introduction to the C++/CLI language, see [Pure C++: Hello, C++/CLI](http://msdn.microsoft.com/magazine/cc163681.aspx). For general information, see [.NET Programming in Visual C++](../vs140/.NET-Programming-with-C---CLI--Visual-C---.md).  
  
 In this walkthrough, you use a text editor to create a basic C++/CLI program, and then compile it on the command line. (You can use your own C++/CLI program instead of typing the one that's shown, or you can use a C++/CLI code sample from another help article. This technique is useful for building and testing small modules that contain no UI elements.)  
  
> [!NOTE]
>  You can also use the Visual Studio IDE to compile C++/CLI programs. For more information, see [Walkthrough: Compiling a C++ Program that Targets the CLR in Visual Studio](../vs140/Walkthrough--Compiling-a-C---Program-that-Targets-the-CLR-in-Visual-Studio.md).  
  
## Prerequisites  
 You must understand the fundamentals of the C++ language.  
  
## Compiling a C++/CLI Program  
 The following steps show how to compile a C++/CLI console application that uses .NET Framework classes.  
  
 To enable compilation for C++/CLI, you must use the [/clr](../Topic/-clr%20\(Common%20Language%20Runtime%20Compilation\).md) compiler option. The Visual C++ compiler generates an .exe file that contains MSIL code—or mixed MSIL and native code—and links to the required .NET Framework libraries.  
  
#### To compile a C++/CLI application on the command line  
  
1.  Open a **Developer Command Prompt** window. (On the **Start** window, open **Apps**. Open the **Visual Studio Tools** folder under your version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], and then choose the **Developer Command Prompt** shortcut.) For more information about how to open a Command Prompt window, see [Setting the Path and Environment Variables for Command-Line Builds](../vs140/Setting-the-Path-and-Environment-Variables-for-Command-Line-Builds.md).  
  
     Administrator credentials may be required to successfully compile the code, depending on the computer's operating system and configuration. To run the Command Prompt window as an administrator, open the shortcut menu for **Developer Command Prompt** and then choose **Run as administrator**.  
  
2.  At the command prompt, enter **notepad basicclr.cpp**.  
  
     Choose **Yes** when you are prompted to create a file.  
  
3.  In Notepad, enter these lines:  
  
    ```  
    int main()  
    {  
        System::Console::WriteLine("This is a C++/CLI program.");  
    }  
    ```  
  
4.  On the menu bar, choose **File**, **Save**.  
  
     You have created a Visual C++ source file that uses a .NET Framework class (<xref:System.Console?qualifyHint=False>) in the <xref:System?qualifyHint=False> namespace.  
  
5.  At the command prompt, enter **cl /clr basicclr.cpp**. The cl.exe compiler compiles the source code into an .obj file that contains MSIL, and then runs the linker to generate an executable program named basicclr.exe.  
  
6.  To run the basicclr.exe program, at the command prompt, enter **basicclr**.  
  
     The program displays this text and exits:  
  
 **This is a C++/CLI program.**  
  
## See Also  
 [Visual C++ Guided Tour](assetId:///499cb66f-7df1-45d6-8b6b-33d94fd1f17c)   
 [C++ Language Reference](../vs140/C---Language-Reference.md)   
 [Building a C/C++ Program](../vs140/Building-C-C---Programs.md)   
 [Compiler Options](../vs140/Compiler-Options.md)