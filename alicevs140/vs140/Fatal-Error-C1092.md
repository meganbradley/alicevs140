---
title: "Fatal Error C1092"
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
ms.topic: error-reference
ms.assetid: bcaa87f0-fbfc-4a33-844b-3b9f5d67f279
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1092
Edit and Continue does not support changes to data types; build required  
  
 You changed or added a data type since the last successful build.  
  
-   Edit and Continue does not support changes to existing data types, including class, struct, or enum definitions. You must stop debugging and build the application.  
  
-   Edit and Continue does not support the addition of new data types if a program database file, such as vc*x*0.pdb (where *x* is the major version of Visual C++ in use) is read-only. To add data types, the compiler must open the .pdb file in write mode.  
  
### To remove this error without ending the current debug session  
  
1.  Change the data type back to its state prior to the error.  
  
2.  From the **Debug** menu, choose **Apply Code Changes**.  
  
### To remove this error without changing your source code  
  
1.  From the **Debug** menu, choose **Stop Debugging**.  
  
2.  From the **Build** menu, choose **Build**.  
  
 For further information, see the [Supported Code Changes](../vs140/Supported-Code-Changes--C---.md).