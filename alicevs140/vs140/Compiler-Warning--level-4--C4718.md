---
title: "Compiler Warning (level 4) C4718"
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
ms.assetid: 29507f8a-b024-42c1-a3b8-f35d1f2641f3
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Warning (level 4) C4718
'function call' : recursive call has no side effects, deleting  
  
 A function contains a recursive call, but otherwise has no side effects. A call to this function is being deleted. The correctness of the program is not affected, but the behavior is. Whereas leaving the call in could result in a runtime stack overflow exception, deleting the call removes that possibility.