---
title: "Compiler Warning (level 1) C4176"
ms.custom: na
ms.date: 09/18/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: cfffb934-219a-4a63-9df6-ba54405bf766
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 1) C4176
'subcomponent' : unknown subcomponent for #pragma component browser  
  
 The **component** pragma contains an invalid subcomponent. To exclude references to a particular name, you must use the **references** option before the name.  
  
## Example  
  
```  
// C4176.cpp  
// compile with: /W1 /LD  
#pragma component(browser, off, i)  // C4176  
#pragma component(browser, off, references, i) // ok  
```