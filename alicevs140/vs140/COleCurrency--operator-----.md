---
title: "COleCurrency::operator *, -"
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
H1: COleCurrency::operator *, /
ms.assetid: 8e2790b5-c3c1-4568-8798-b550b5153f4a
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::operator *, -
Allow you to scale a **COleCurrency** value by an integral value.  
  
## Syntax  
  
```  
  
      COleCurrency operator *(  
   long nOperand   
) const;  
COleCurrency operator /(  
   long nOperand   
) const;  
```  
  
## Remarks  
 If the **COleCurrency** operand is null, the status of the resulting **COleCurrency** value is null.  
  
 If the arithmetic operation overflows or underflows, the status of the resulting **COleCurrency** value is invalid.  
  
 If the **COleCurrency** operand is invalid, the status of the resulting **COleCurrency** value is invalid.  
  
 For more information on the valid, invalid, and null status values, see the [m_status](../vs140/COleCurrency--m_status.md) member variable.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#18](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#18)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::operator *=, /=](../vs140/COleCurrency--operator--=---=.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)