---
title: "Compiler Warning (level 1) C4656"
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
ms.assetid: b5aaef74-2320-4345-a6ae-b813881a491c
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4656
'symbol' : data type is new or has changed since the last build, or is defined differently elsewhere  
  
 You added or changed a data type, making it new to your source code since the last successful build. Edit and Continue does not support changes to existing data types.  
  
 This warning will always be followed by [Fatal Error C1092](../vs140/Fatal-Error-C1092.md). For further information, see the [Supported Code Changes](../vs140/Supported-Code-Changes--C---.md).  
  
### To remove this warning without ending the current debug session  
  
1.  Change the data type back to its state prior to the error.  
  
2.  From the **Debug** menu, choose **Apply Code Changes**.  
  
### To remove this error without changing your source code  
  
1.  From the **Debug** menu, choose **Stop Debugging**.  
  
2.  From the **Build** menu, choose **Build**.