---
title: "CRBTree::~CRBTree"
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
ms.topic: reference
ms.assetid: 7212ef93-8858-4626-9853-1142001346cf
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CRBTree::~CRBTree
The destructor.  
  
## Syntax  
  
```  
  
~CRBTree( ) throw( );  
  
```  
  
## Remarks  
 Frees any allocated resources. Calls [CRBTree::RemoveAll](../vs140/CRBTree--RemoveAll.md) to delete all elements.  
  
## Requirements  
 **Header:** atlcoll.h  
  
## See Also  
 [CRBTree Class](../vs140/CRBTree-Class.md)