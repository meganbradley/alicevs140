---
title: "IAxWinAmbientDispatch::put_DocHostFlags"
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
ms.assetid: 4cdb30d5-1b34-4f1a-baca-fbcca0d32945
caps.latest.revision: 12
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IAxWinAmbientDispatch::put_DocHostFlags
The **DocHostFlags** property specifies the user interface capabilities of the host object.  
  
## Syntax  
  
```  
  
      STDMETHOD( put_DocHostFlags )(  
   DWORD dwDocHostFlags   
);  
```  
  
#### Parameters  
 *dwDocHostFlags*  
 [in] The new value of this property.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 The ATL host object implementation uses **DOCHOSTUIFLAG_NO3DBORDER** as the default value of this property.  
  
## Requirements  
 **Header:** atliface.h  
  
## See Also  
 [IAxWinAmbientDispatch Interface](../vs140/IAxWinAmbientDispatch-Interface.md)   
 [IDocHostUIHandler::GetHostInfo](https://msdn.microsoft.com/en-us/library/aa753257.aspx)