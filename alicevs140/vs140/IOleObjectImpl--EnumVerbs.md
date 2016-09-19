---
title: "IOleObjectImpl::EnumVerbs"
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
ms.assetid: a40c61f0-5b94-4d6b-9487-b4987846e059
caps.latest.revision: 14
translation.priority.ht: 
  - de-de
  - ja-jp
---
# IOleObjectImpl::EnumVerbs
Supplies an enumeration of registered actions (verbs) for this control by calling **OleRegEnumVerbs**.  
  
## Syntax  
  
```  
  
      STDMETHOD(EnumVerbs)(  
   IEnumOLEVERB** ppEnumOleVerb   
);  
```  
  
## Remarks  
 You can add verbs to your project's .rgs file. For example, see CIRCCTL.RGS in the [CIRC](../vs140/Visual-C---Samples.md) sample.  
  
 See [IOleObject::EnumVerbs](http://msdn.microsoft.com/library/windows/desktop/ms692781) in the [!INCLUDE[winSDK](../vs140/includes/winSDK_md.md)].  
  
## Requirements  
 **Header:** atlctl.h  
  
## See Also  
 [IOleObjectImpl Class](../vs140/IOleObjectImpl-Class.md)   
 [OleRegEnumVerbs](http://msdn.microsoft.com/library/windows/desktop/ms680061)   
 [IOleObjectImpl::EnumAdvise](../vs140/IOleObjectImpl--EnumAdvise.md)