---
title: "Compiler Error C2957"
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
ms.assetid: 9cb4526f-4af8-47e9-b786-56192627ca72
caps.latest.revision: 9
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Compiler Error C2957
'delim' : invalid left delimiter : expected '<'  
  
 A generic class was ill formed.  
  
 The following sample generates C2957:  
  
```  
// C2957.cpp  
// compile with: /clr /LD  
generic << class T>   // C2957  
// try the following line instead  
// generic < class T>  
gc class C {};  
```