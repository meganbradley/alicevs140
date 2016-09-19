---
title: "IAxWinAmbientDispatch::put_AllowContextMenu"
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
ms.assetid: acb99154-932b-45fd-aa08-dd2837ecaafb
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_AllowContextMenu
The **AllowContextMenu** property specifies whether the hosted control is allowed to display its own context menu.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_AllowContextMenu )(  
   VARIANT_BOOL bAllowContextMenu   
);  
```  
  
#### Parameters  
 *bAllowContextMenu*  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses `VARIANT_TRUE` as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)   
 [IDocHostUIHandler::ShowContextMenu](https://msdn.microsoft.com/en-us/library/aa753264.aspx)