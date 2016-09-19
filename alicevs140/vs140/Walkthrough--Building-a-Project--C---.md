---
title: "Walkthrough: Building a Project (C++)"
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
ms.assetid: d459bc03-88ef-48d0-9f9a-82d17f0b6a4d
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Building a Project (C++)
In this walkthrough, you deliberately introduce a Visual C++ syntax error in your code to learn what a compilation error looks like and how to fix it. When you compile the project, an error message indicates what the problem is and where it occurred.  
  
## Prerequisites  
  
-   This walkthrough assumes that you understand the fundamentals of the C++ language.  
  
-   It also assumes that you have completed the earlier related walkthroughs that are listed in [Using the Visual Studio IDE for C++ Desktop Development](../vs140/Using-the-Visual-Studio-IDE-for-C---Desktop-Development.md).  
  
### To fix compilation errors  
  
1.  In TestGames.cpp, delete the semicolon in the last line so that it resembles this:  
  
     `return 0`  
  
2.  On the menu bar, choose **Build**, **Build Solution**.  
  
3.  A message in the **Error List** window indicates that there was an error in the building of the project. The description looks something like this:  
  
     `error C2143: syntax error : missing ';' before '}'`  
  
     To view help information about this error, highlight it in the **Error List** window and then choose the F1 key.  
  
4.  Add the semicolon back to the end of the line that has the syntax error:  
  
     `return 0;`  
  
5.  On the menu bar, choose **Build**, **Build Solution**.  
  
     A message in the **Output** window indicates that the project compiled successfully.  
  
 **1>------ Build started: Project: Game, Configuration: Debug Win32 ------**  
**1>  TestGames.cpp**  
**1>  Game.vcxproj -> C:\Users\\<username\>\Documents\Visual Studio *<version\>*\Projects\Game\Debug\Game.exe**  
**========== Build: 1 succeeded, 0 failed, 0 up-to-date, 0 skipped ==========**  
  
## Next Steps  
 **Previous:** [Projects and Solutions (C++)](../vs140/Walkthrough--Working-with-Projects-and-Solutions--C---.md) &#124; **Next:**[Testing a Project (C++)](../vs140/Walkthrough--Testing-a-Project--C---.md)  
  
## See Also  
 [Visual C++ Guided Tour](assetId:///499cb66f-7df1-45d6-8b6b-33d94fd1f17c)   
 [DELETE_PENDING_Building and Debugging](assetId:///9f6ba537-5ea0-46fb-b6ba-b63d657d84f1)