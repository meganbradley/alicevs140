---
title: "IAxWinAmbientDispatch::get_LocaleID"
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
ms.assetid: 5964fa0a-ef78-40fd-a5d1-f9c86f03ed10
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::get_LocaleID
The **LocaleID** property specifies the ambient locale ID of the container.  
  
## Syntax  
  
```  
  
      STDMETHOD( get_LocaleID )(  
   LCID* plcidLocaleID   
);  
```  
  
#### Parameters  
 *plcidLocaleID*  
 [out] The address of a variable to receive the current value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses the user's default locale as the default value of this property.  
  
 With this method you can discover the Ambient LocalID, that is, the LocaleID of the program your control is being used in. Once you know the LocaleID, you can call code to load locale-specific captions, error message text, and so forth from a resource file or satellite DLL.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)