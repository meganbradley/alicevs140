---
title: "wbuffer_convert::wbuffer_convert"
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
ms.topic: article
ms.assetid: 4f6c35af-7526-42e9-bb2c-f9242db96b17
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# wbuffer_convert::wbuffer_convert
Constructs an object of type `wbuffer_convert`.  
  
## Syntax  
  
```  
wbuffer_convert(std::streambuf* _Bytebuf = 0,  
    Codecvt* _Pcvt = new Codecvt,  
    state_type _State = state_type());  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`_Bytebuf`|The byte-oriented stream buffer to store.|  
|`_Pcvt`|The object of type `Codecvt` to perform the conversion.|  
|`_State`|The object of type `cvtstate` representing the conversion state.|  
  
## Remarks  
 This constructor constructs a stream buffer object, initializes the object representing the underlying byte stream buffer to `_Bytebuf`, initializesthe conversion objectto `_Pcvt`, and initializes the conversion state object to `_State`.  
  
## Requirements  
 **Header:** <locale\>  
  
 **Namespace:** std  
  
## See Also  
 [wbuffer_convert Class](../vs140/wbuffer_convert-Class.md)