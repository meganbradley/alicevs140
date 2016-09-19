---
title: "IAxWinAmbientDispatch::get_OptionKeyPath"
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
ms.assetid: ce4d35aa-3eca-49b9-87ed-86af033e56cb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::get_OptionKeyPath
The **OptionKeyPath** property specifies the registry key path to user settings.  
  
## Syntax  
  
```  
  
      STDMETHOD( get_OptionKeyPath )(  
   BSTR* pbstrOptionKeyPath   
);  
```  
  
#### Parameters  
 *pbstrOptionKeyPath*  
 [out] The address of a variable to receive the current value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)   
 [IDocHostUIHandler::GetOptionKeyPath](https://msdn.microsoft.com/en-us/library/aa753258.aspx)