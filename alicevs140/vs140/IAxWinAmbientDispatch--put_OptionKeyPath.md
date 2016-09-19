---
title: "IAxWinAmbientDispatch::put_OptionKeyPath"
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
ms.assetid: 8b29a287-31e4-4572-b10b-2c825020fb0b
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_OptionKeyPath
The **OptionKeyPath** property specifies the registry key path to user settings.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_OptionKeyPath )(  
   BSTR bstrOptionKeyPath   
);  
```  
  
#### Parameters  
 *bstrOptionKeyPath*  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)   
 [IDocHostUIHandler::GetOptionKeyPath](https://msdn.microsoft.com/en-us/library/aa753258.aspx)