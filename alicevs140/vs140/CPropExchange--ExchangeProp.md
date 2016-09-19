---
title: "CPropExchange::ExchangeProp"
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
ms.assetid: 7bc96006-3027-4c97-89e8-63b89878756c
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropExchange::ExchangeProp
Exchanges a property between a storage medium and the control.  
  
## Syntax  
  
```  
  
      virtual BOOL ExchangeProp(  
   LPCTSTR pszPropName,  
   VARTYPE vtProp,  
   void* pvProp,  
   const void* pvDefault = NULL   
) = 0;  
```  
  
#### Parameters  
 `pszPropName`  
 The name of the property being exchanged.  
  
 `vtProp`  
 A symbol specifying the type of the property being exchanged. Possible values are:  
  
|Symbol|Property Type|  
|------------|-------------------|  
|`VT_I2`|**short**|  
|`VT_I4`|**long**|  
|`VT_BOOL`|**BOOL**|  
|`VT_BSTR`|`CString`|  
|`VT_CY`|**CY**|  
|`VT_R4`|**float**|  
|`VT_R8`|**double**|  
  
 `pvProp`  
 A pointer to the property's value.  
  
 *pvDefault*  
 Pointer to a default value for the property.  
  
## Return Value  
 Nonzero if the exchange was successful; 0 if unsuccessful.  
  
## Remarks  
 If the property is being loaded from the medium to the control, the property's value is retrieved from the medium and stored in the object pointed to by `pvProp`. If the property is being stored to the medium, the value of the object pointed to by `pvProp` is written to the medium.  
  
 The functions **CArchivePropExchange::ExchangeProp**, **CResetPropExchange::ExchangeProp**, and **CPropsetPropExchange::ExchangeProp** override this pure virtual function.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CPropExchange Class](../vs140/CPropExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [CPropExchange::ExchangeBlobProp](../vs140/CPropExchange--ExchangeBlobProp.md)   
 [CPropExchange::ExchangeFontProp](../vs140/CPropExchange--ExchangeFontProp.md)   
 [CPropExchange::ExchangePersistentProp](../vs140/CPropExchange--ExchangePersistentProp.md)