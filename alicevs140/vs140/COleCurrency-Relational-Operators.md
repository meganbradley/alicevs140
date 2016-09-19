---
title: "COleCurrency Relational Operators"
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
ms.assetid: 94f2d16a-f3d1-4c3b-8fc9-77aec76383c4
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency Relational Operators
Compare two currency values and return nonzero if the condition is true; otherwise 0.  
  
## Syntax  
  
```  
  
      BOOL operator ==(  
   const COleCurrency& cur   
) const;  
BOOL operator !=(  
   const COleCurrency& cur   
) const;  
BOOL operator <(  
   const COleCurrency& cur   
) const;  
BOOL operator >(  
   const COleCurrency& cur   
) const;  
BOOL operator <=(  
   const COleCurrency& cur   
) const;  
BOOL operator >=(  
   const COleCurrency& cur   
) const;  
```  
  
## Remarks  
  
> [!NOTE]
>  The return value of the ordering operations (**<**, **<=**, **>**, **>=**) is undefined if the status of either operand is null or invalid. The equality operators (`==`, `!=`) consider the status of the operands.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#20](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#20)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)