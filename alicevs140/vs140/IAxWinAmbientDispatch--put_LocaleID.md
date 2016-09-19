---
title: "IAxWinAmbientDispatch::put_LocaleID"
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
ms.assetid: a99e8d2c-c5e0-47f8-a761-98641f8c4845
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_LocaleID
The **LocaleID** property specifies the ambient locale ID of the container.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_LocaleID )(  
   LCID lcidLocaleID   
);  
```  
  
#### Parameters  
 *lcidLocaleID*  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses the user's default locale as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)