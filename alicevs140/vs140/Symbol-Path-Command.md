---
title: "Symbol Path Command"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-general
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b697ef2d-3f5d-40df-b113-7068a5bec0d4
caps.latest.revision: 11
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Symbol Path Command
Sets the list of directories for the debugger to search for symbols.  
  
## Syntax  
  
```  
Debug.SymbolPath pathname1;pathname2;... pathnameN  
```  
  
## Arguments  
 `pathname`  
 Optional. A semi-colon delimited list of paths for the debugger to search for symbols.  
  
## Remarks  
 If no `pathname` is specified, the command lists the current symbol paths.  
  
## Example  
 This example adds two paths to the list of symbol directories.  
  
```  
Debug.SymbolPath C:\Symbol Path 1;C:\Symbol Path 2  
```  
  
## Example  
 This example displays a semi-colon delimited list of current symbol paths.  
  
```  
Debug.SymbolPath  
```  
  
## See Also  
 [Command Window](../vs140/Command-Window.md)   
 [Visual Studio Commands with Arguments](../vs140/Visual-Studio-Commands.md)