---
title: "COleCurrency::SetCurrency"
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
ms.assetid: 833d28c8-c633-4b11-a4af-18aad70ffe1c
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::SetCurrency
Call this member function to set the units and fractional part of this **COleCurrency** object.  
  
## Syntax  
  
```  
  
      void SetCurrency(  
   long nUnits,  
   long nFractionalUnits   
);  
```  
  
#### Parameters  
 `nUnits`, `nFractionalUnits`  
 Indicate the units and fractional part (in 1/10,000's) of the value to be copied into this **COleCurrency** object.  
  
## Remarks  
 If the absolute value of the fractional part is greater than 10,000, the appropriate adjustment is made to the units, as shown in the third of the following examples.  
  
 Note that the units and fractional part are specified by signed long values. The fourth of the following examples shows what happens when the parameters have different signs.  
  
## Example  
 [!CODE [NVC_MFCOleContainer#14](../CodeSnippet/VS_Snippets_Cpp/NVC_MFCOleContainer#14)]  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::COleCurrency](../vs140/COleCurrency--COleCurrency.md)   
 [COleCurrency::operator =](../vs140/COleCurrency--operator-=.md)   
 [COleCurrency::m_cur](../vs140/COleCurrency--m_cur.md)