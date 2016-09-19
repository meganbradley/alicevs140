---
title: "COleCurrency::m_status"
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
ms.assetid: 5caf9bba-b628-4a35-b573-cfd05d48d043
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# COleCurrency::m_status
The type of this data member is the enumerated type `CurrencyStatus`, which is defined within the **COleCurrency** class.  
  
## Syntax  
  
```  
enum CurrencyStatus{  
   valid = 0,  
   invalid = 1,  
   null = 2,  
};  
```  
  
## Remarks  
 For a brief description of these status values, see the following list:  
  
-   **COleCurrency::valid** Indicates that this **COleCurrency** object is valid.  
  
-   **COleCurrency::invalid** Indicates that this **COleCurrency** object is invalid; that is, its value may be incorrect.  
  
-   **COleCurrency::null** Indicates that this **COleCurrency** object is null, that is, that no value has been supplied for this object. (This is "null" in the database sense of "having no value," as opposed to the C++ **NULL**.)  
  
 The status of a **COleCurrency** object is invalid in the following cases:  
  
-   If its value is set from a **VARIANT** or `COleVariant` value that could not be converted to a currency value.  
  
-   If this object has experienced an overflow or underflow during an arithmetic assignment operation, for example `+=` or **\*=**.  
  
-   If an invalid value was assigned to this object.  
  
-   If the status of this object was explicitly set to invalid using [SetStatus](../vs140/COleCurrency--SetStatus.md).  
  
 For more information on operations that may set the status to invalid, see the following member functions:  
  
-   [COleCurrency](../vs140/COleCurrency--COleCurrency.md)  
  
-   [operator =](../vs140/COleCurrency--operator-=.md)  
  
-   [operator +, -](../vs140/COleCurrency--operator-----.md)  
  
-   [operator +=, -=](../vs140/COleCurrency--operator--=---=.md)  
  
-   [operator *, /](../vs140/COleCurrency--operator-----.md)  
  
-   [operator *=, /=](../vs140/COleCurrency--operator--=---=.md)  
  
    > [!CAUTION]
    >  This data member is for advanced programming situations. You should use the inline member functions [GetStatus](../vs140/COleCurrency--GetStatus.md) and [SetStatus](../vs140/COleCurrency--SetStatus.md). See `SetStatus` for further cautions regarding explicitly setting this data member.  
  
## Requirements  
 **Header:** afxdisp.h  
  
## See Also  
 [COleCurrency Class](../vs140/COleCurrency-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleCurrency::GetStatus](../vs140/COleCurrency--GetStatus.md)   
 [COleCurrency::SetStatus](../vs140/COleCurrency--SetStatus.md)