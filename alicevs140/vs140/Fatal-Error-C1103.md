---
title: "Fatal Error C1103"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-csharp
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9d276939-9c47-4235-9d20-76b8434f9731
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Fatal Error C1103
fatal error importing progid: 'message'  
  
 The compiler detected a problem importing a type library.  For example, you cannot specify a type library with progid and also specify `no_registry`.  
  
 For more information, see [The #import Directive](../vs140/#import-Directive--C---.md).  
  
 The following sample will generate C1103:  
  
```  
// C1103.cpp  
#import "progid:a.b.id.1.5" no_registry auto_search   // C1103  
```