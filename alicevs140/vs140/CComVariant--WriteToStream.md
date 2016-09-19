---
title: "CComVariant::WriteToStream"
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
ms.assetid: a600937b-8016-4278-988b-6de6d717bb3a
caps.latest.revision: 12
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComVariant::WriteToStream
Saves the underlying **VARIANT** to a stream.  
  
## Syntax  
  
```  
  
      HRESULT WriteToStream(  
   IStream* pStream   
);  
```  
  
#### Parameters  
 `pStream`  
 [in] A pointer to the [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) interface on a stream.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Requirements  
 **Header:** atlcomcli.h  
  
## See Also  
 [CComVariant Class](../vs140/CComVariant-Class.md)   
 [CComVariant::ReadFromStream](../vs140/CComVariant--ReadFromStream.md)