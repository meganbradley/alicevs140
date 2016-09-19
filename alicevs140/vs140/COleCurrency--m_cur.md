---
title: "COleCurrency::m_cur"
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
ms.assetid: d5eb1810-88e8-46d2-b4f1-ae1ce6ab466d
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::m_cur
The underlying [CURRENCY](assetId:///5e81273c-7289-45c7-93c0-32c1553f708e) structure for this **COleCurrency** object.  
  
## Remarks  
  
> [!CAUTION]
>  Changing the value in the **CURRENCY** structure accessed by the pointer returned by this function will change the value of this **COleCurrency** object. It does not change the status of this **COleCurrency** object.  
  
 For more information, see the [CURRENCY](assetId:///5e81273c-7289-45c7-93c0-32c1553f708e) entry in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::COleCurrency](../vs140/COleCurrency--COleCurrency.md)   
 [COleCurrency::operator CURRENCY](../vs140/COleCurrency--operator-CURRENCY.md)   
 [COleCurrency::SetCurrency](../vs140/COleCurrency--SetCurrency.md)