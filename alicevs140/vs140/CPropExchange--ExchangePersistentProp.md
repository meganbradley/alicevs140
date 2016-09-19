---
title: "CPropExchange::ExchangePersistentProp"
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
ms.assetid: 2d484797-bdd6-40cb-a148-9ff32d3e21b3
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CPropExchange::ExchangePersistentProp
Exchanges a property between the control and a file.  
  
## Syntax  
  
```  
  
      virtual BOOL ExchangePersistentProp(  
   LPCTSTR pszPropName,  
   LPUNKNOWN* ppUnk,  
   REFIID iid,  
   LPUNKNOWN pUnkDefault   
) = 0;  
```  
  
#### Parameters  
 `pszPropName`  
 The name of the property being exchanged.  
  
 `ppUnk`  
 A pointer to a variable containing a pointer to the property's **IUnknown** interface (this variable is typically a member of your class).  
  
 `iid`  
 Interface ID of the interface on the property that the control will use.  
  
 `pUnkDefault`  
 Default value for the property.  
  
## Return Value  
 Nonzero if the exchange was successful; 0 if unsuccessful.  
  
## Remarks  
 If the property is being loaded from the file to the control, the property is created and initialized from the file. If the property is being stored, its value is written to the file.  
  
 The functions **CArchivePropExchange::ExchangePersistentProp**, **CResetPropExchange::ExchangePersistentProp**, and **CPropsetPropExchange::ExchangePersistentProp** override this pure virtual function.  
  
## Requirements  
 **Header:** afxctl.h  
  
## See Also  
 [CPropExchange Class](../vs140/CPropExchange-Class.md)   
 [Hierarchy Chart](../vs140/Hierarchy-Chart.md)   
 [COleControl::DoPropExchange](../vs140/COleControl--DoPropExchange.md)   
 [CPropExchange::ExchangeBlobProp](../vs140/CPropExchange--ExchangeBlobProp.md)   
 [CPropExchange::ExchangeFontProp](../vs140/CPropExchange--ExchangeFontProp.md)   
 [CPropExchange::ExchangeProp](../vs140/CPropExchange--ExchangeProp.md)