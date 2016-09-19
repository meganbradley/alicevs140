---
title: "CPropExchange::ExchangeBlobProp"
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
ms.assetid: d57153ae-c48a-44ed-a2a2-8300b95e5146
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropExchange::ExchangeBlobProp
Serializes a property that stores binary large object (BLOB) data.  
  
## Syntax  
  
```  
  
      virtual BOOL ExchangeBlobProp(  
   LPCTSTR pszPropName,  
   HGLOBAL* phBlob,  
   HGLOBAL hBlobDefault = NULL   
) = 0;  
```  
  
#### Parameters  
 `pszPropName`  
 The name of the property being exchanged.  
  
 `phBlob`  
 Pointer to a variable pointing to where the property is stored (variable is typically a member of your class).  
  
 `hBlobDefault`  
 Default value for the property.  
  
## Return Value  
 Nonzero if the exchange was successful; 0 if unsuccessful.  
  
## Remarks  
 The property's value is read from or written to, as appropriate, the variable referenced by `phBlob`. If `hBlobDefault` is specified, it will be used as the property's default value. This value is used if, for any reason, the control's serialization fails.  
  
 The functions **CArchivePropExchange::ExchangeBlobProp**, **CResetPropExchange::ExchangeBlobProp**, and **CPropsetPropExchange::ExchangeBlobProp** override this pure virtual function.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CPropExchange Class](../vs140/CPropExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [CPropExchange::ExchangeFontProp](../vs140/CPropExchange--ExchangeFontProp.md)   
 [CPropExchange::ExchangePersistentProp](../vs140/CPropExchange--ExchangePersistentProp.md)   
 [CPropExchange::ExchangeProp](../vs140/CPropExchange--ExchangeProp.md)