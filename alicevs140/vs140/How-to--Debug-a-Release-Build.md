---
title: "How to: Debug a Release Build"
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
ms.assetid: d333e4d1-4e6c-4384-84a9-cb549702da25
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# How to: Debug a Release Build
You can debug a release build of an application.  
  
### To debug a release build  
  
1.  Open the **Property Pages** dialog box for the project. For details, see [Working with Project Properties](../vs140/Working-with-Project-Properties.md).  
  
2.  Click the **C/C++** node. Set **Debug Information Format** to [C7 compatible (/Z7)](../vs140/-Z7---Zi---ZI--Debug-Information-Format-.md) or **Program Database (/Zi)**.  
  
3.  Expand **Linker** and click the **General** node. Set **Enable Incremental Linking** to [No (/INCREMENTAL:NO)](../Topic/-INCREMENTAL%20\(Link%20Incrementally\).md).  
  
4.  Select the **Debugging** node. Set **Generate Debug Info** to [Yes (/DEBUG)](../Topic/-DEBUG%20\(Generate%20Debug%20Info\).md).  
  
5.  Select the **Optimization** node. Set **References** to [/OPT:REF](../Topic/-OPT%20\(Optimizations\).md) and **Enable COMDAT Folding** to [/OPT:ICF](../Topic/-OPT%20\(Optimizations\).md).  
  
6.  You can now debug your release build application. To find a problem, step through the code (or use Just-In-Time debugging) until you find where the failure occurs, and then determine the incorrect parameters or code.  
  
     If an application works in a debug build, but fails in a release build, one of the compiler optimizations may be exposing a defect in the source code. To isolate the problem, disable selected optimizations for each source code file until you locate the file and the optimization that is causing the problem. (To expedite the process, you can divide the files into two groups, disable optimization on one group, and when you find a problem in a group, continue dividing until you isolate the problem file.)  
  
     You can use [/RTC](../Topic/-RTC%20\(Run-Time%20Error%20Checks\).md) to try to expose such bugs in your debug builds.  
  
     For more information, see [Optimizing Your Code](../vs140/Optimizing-Your-Code.md).  
  
## See Also  
 [Fixing Release Build Problems](../vs140/Fixing-Release-Build-Problems.md)