---
title: "COleCurrency::SetStatus"
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
ms.assetid: 630bef17-53c6-4aad-9147-1a1f478bdf20
caps.latest.revision: 13
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::SetStatus
Call this member function to set the status (validity) of this **COleCurrency** object.  
  
## Syntax  
  
```  
  
      void SetStatus(   
   CurrencyStatus status    
);  
```  
  
#### Parameters  
 *status*  
 The new status for this **COleCurrency** object.  
  
## Remarks  
 The *status* parameter value is defined by the `CurrencyStatus` enumerated type, which is defined within the **COleCurrency** class.  
  
 `enum CurrencyStatus{`  
  
 `valid = 0,`  
  
 `invalid = 1,`  
  
 `null = 2,`  
  
 `};`  
  
 For a brief description of these status values, see the following list:  
  
-   **COleCurrency::valid** Indicates that this **COleCurrency** object is valid.  
  
-   **COleCurrency::invalid** Indicates that this **COleCurrency** object is invalid; that is, its value may be incorrect.  
  
-   **COleCurrency::null** Indicates that this **COleCurrency** object is null, that is, that no value has been supplied for this object. (This is "null" in the database sense of "having no value," as opposed to the C++ **NULL**.)  
  
    > [!CAUTION]
    >  This function is for advanced programming situations. This function does not alter the data in this object. It will most often be used to set the status to null or invalid. Note that the assignment operator ([operator =](../vs140/COleCurrency--operator-=.md)) and [SetCurrency](../vs140/COleCurrency--SetCurrency.md) do set the status to of the object based on the source value(s).  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)   
 [COleCurrency::operator =](../vs140/COleCurrency--operator-=.md)   
 [COleCurrency::SetCurrency](../vs140/COleCurrency--SetCurrency.md)   
 [COleCurrency::m_status](../vs140/COleCurrency--m_status.md)