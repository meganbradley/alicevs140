---
title: "COleCurrency::operator +=, -="
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
ms.assetid: 1805c36c-cacf-4c58-b4a1-3b769afb95bf
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::operator +=, -=
Allow you to add and subtract a **COleCurrency** value to and from this **COleCurrency** object.  
  
## Syntax  
  
```  
  
      const COleCurrency& operator +=(  
   const COleCurrency& cur   
);  
const COleCurrency& operator -=(  
   const COleCurrency& cur   
);  
```  
  
## Remarks  
 If either of the operands is null, the status of this **COleCurrency** object is set to null.  
  
 If the arithmetic operation overflows, the status of this **COleCurrency** object is set to invalid.  
  
 If either of the operands is invalid and the other is not null, the status of this **COleCurrency** object is set to invalid.  
  
 For more information on the valid, invalid, and null status values, see the [m_status](../vs140/COleCurrency--m_status.md) member variable.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#17](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#17)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::operator +, -](../vs140/COleCurrency--operator-----.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)