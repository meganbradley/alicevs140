---
title: "Walkthrough: Compiling a C++-CX Program on the Command Line"
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
H1: Walkthrough: Compiling a C++/CX Program on the Command Line
ms.assetid: 626f5544-69ed-4736-83a9-f11389b371b2
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Compiling a C++-CX Program on the Command Line
You can create Visual C++ programs that target the Windows Runtime and build them on the command line. Visual C++ supports Visual C++ component extensions (C++/CX), which has additional types and operators to target the Windows Runtime programming model. You can use C++/CX to build apps for Windows Phone 8.1, Windows Store, and Windows desktop. For more information, see [A Tour of C++/CX](http://msdn.microsoft.com/magazine/dn166929.aspx) and [Component Extensions for Runtime Platforms](../Topic/Component%20Extensions%20for%20Runtime%20Platforms.md).  
  
 In this walkthrough, you use a text editor to create a basic C++/CX program, and then compile it on the command line. (You can use your own C++/CX program instead of typing the one that's shown, or you can use a C++/CX code sample from another help article. This technique is useful for building and testing small modules that contain no UI elements.)  
  
> [!NOTE]
>  You can also use the Visual Studio IDE to compile C++/CX programs. Because the IDE includes design, debugging, emulation, and deployment support that isn't available on the command line, we recommend that you use the IDE to build Windows Store apps. For more information, see [Create a basic C++ Store app](http://msdn.microsoft.com/library/windows/apps/dn263168).  
  
## Prerequisites  
 You must understand the fundamentals of the C++ language.  
  
## Compiling a C++/CX Program  
 To enable compilation for C++/CX, you must use the [/ZW](../vs140/-ZW--Windows-Runtime-Compilation-.md) compiler option. The Visual C++ compiler generates an .exe file that targets the Windows Runtime, and links to the required libraries.  
  
#### To compile a C++/CX application on the command line  
  
1.  Open a **Developer Command Prompt** window. (On the **Start** window, open **Apps**. Open the **Visual Studio Tools** folder under your version of [!INCLUDE[vsprvs](../vs140/includes/vsprvs_md.md)], and then choose the **Developer Command Prompt** shortcut.) For more information about how to open a Command Prompt window, see [Setting the Path and Environment Variables for Command-Line Builds](../vs140/Setting-the-Path-and-Environment-Variables-for-Command-Line-Builds.md).  
  
     Administrator credentials may be required to successfully compile the code, depending on the computer's operating system and configuration. To run the Command Prompt window as an administrator, open the shortcut menu for **Developer Command Prompt** and then choose **Run as administrator**.  
  
2.  At the command prompt, enter **notepad basiccx.cpp**.  
  
     Choose **Yes** when you are prompted to create a file.  
  
3.  In Notepad, enter these lines:  
  
    ```cpp  
    using namespace Platform;  
  
    int main(Platform::Array<Platform::String^>^ args)  
    {  
        Platform::Details::Console::WriteLine("This is a C++/CX program.");  
    }  
  
    ```  
  
4.  On the menu bar, choose **File**, **Save**.  
  
     You have created a Visual C++ source file that uses the Windows Runtime [Platform](assetId:///b160e822-d424-43d2-ba60-57b0e81f259c) namespace.  
  
5.  At the command prompt, enter **cl /EHsc /ZW basiccx.cpp /link /SUBSYSTEM:CONSOLE**. The cl.exe compiler compiles the source code into an .obj file, and then runs the linker to generate an executable program named basiccx.exe. (The [/EHsc](../vs140/-EH--Exception-Handling-Model-.md) compiler option specifies the C++ exception-handling model, and the [/link](../vs140/-link--Pass-Options-to-Linker-.md) flag specifies a console application.)  
  
6.  To run the basiccx.exe program, at the command prompt, enter **basiccx**.  
  
     The program displays this text and exits:  
  
 **This is a C++/CX program.**  
  
## See Also  
 [Visual C++ Guided Tour](assetId:///499cb66f-7df1-45d6-8b6b-33d94fd1f17c)   
 [C++ Language Reference](../vs140/C---Language-Reference.md)   
 [Building a C/C++ Program](../vs140/Building-C-C---Programs.md)   
 [Compiler Options](../vs140/Compiler-Options.md)