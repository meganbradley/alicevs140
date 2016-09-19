---
title: "CComBSTR::WriteToStream"
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
ms.assetid: 382d86dd-ef93-44e2-b8cc-45b183842b0f
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::WriteToStream
Saves the [m_str](../vs140/CComBSTR--m_str.md) member to a stream.  
  
## Syntax  
  
```  
  
      HRESULT WriteToStream(  
   IStream* pStream   
) throw( );  
```  
  
#### Parameters  
 `pStream`  
 [in] A pointer to the [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) interface on a stream.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 You can recreate a BSTR from the contents of the stream using the [ReadFromStream](../vs140/CComBSTR--ReadFromStream.md) function.  
  
## Example  
 [!CODE [NVC_ATL_Utilities#45](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#45)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)   
 [CComBSTR::ReadFromStream](../vs140/CComBSTR--ReadFromStream.md)