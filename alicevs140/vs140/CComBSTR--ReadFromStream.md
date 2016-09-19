---
title: "CComBSTR::ReadFromStream"
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
ms.assetid: ffcc22f9-8cd3-42d8-87b6-12dbfaf3d5a2
caps.latest.revision: 14
robots: noindex,nofollow
translation.priority.ht: 
  - de-de
  - ja-jp
---
# CComBSTR::ReadFromStream
Sets the [m_str](../vs140/CComBSTR--m_str.md) member to the `BSTR` contained in the specified stream.  
  
## Syntax  
  
```  
  
      HRESULT ReadFromStream(  
   IStream* pStream   
) throw( );  
```  
  
#### Parameters  
 `pStream`  
 [in] A pointer to the [IStream](http://msdn.microsoft.com/library/windows/desktop/aa380034) interface on the stream containing the data.  
  
## Return Value  
 A standard `HRESULT` value.  
  
## Remarks  
 **ReadToStream** requires the contents of the stream at the current position to be compatible with the data format written out by a call to [WriteToStream](../vs140/CComBSTR--WriteToStream.md).  
  
## Example  
 [!CODE [NVC_ATL_Utilities#44](../CodeSnippet/VS_Snippets_Cpp/NVC_ATL_Utilities#44)]  
  
## Requirements  
 **Header:** atlbase.h  
  
## See Also  
 [CComBSTR Class](../vs140/CComBSTR-Class.md)