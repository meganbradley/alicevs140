---
title: "IDebugEngine3::SetSymbolPath"
ms.custom: na
ms.date: 09/19/2016
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - vs-ide-sdk
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 47b48f84-8a96-401f-84df-0baa8a96d26e
caps.latest.revision: 14
translation.priority.mt: 
  - de-de
  - ja-jp
---
# IDebugEngine3::SetSymbolPath
Sets the path or paths that are searched for debugging symbols.  
  
## Syntax  
  
```cpp#  
HRESULT SetSymbolPath (  
   LPOLESTR            szSymbolSearchPath,  
   LPOLESTR            szSymbolCachePath,  
   LOAD_SYMBOLS_FLAGS  Flags  
);  
```  
  
```c#  
int SetSymbolPath(  
   string                    szSymbolSearchPath,   
   string                    szSymbolCachePath,   
   enum_LOAD_SYMBOLS_FLAGS   Flags  
);  
```  
  
#### Parameters  
  
|Parameter|Description|  
|---------------|-----------------|  
|`szSymbolSearchPath`|[in] String containing the symbol search path or paths. See "Remarks" for details. Cannot be null.|  
|`szSymbolCachePath`|[in] String containing the local path where symbols can be cached. Cannot be null.|  
|`Flags`|[in] Not used; always set to 0.|  
  
## Return Value  
 If successful, returns S_OK; otherwise returns an error code.  
  
## Remarks  
 The string `szSymbolSearchPath` is a list of one or more paths, separated by semicolons, to search for symbols. These paths can be a local path, a UNC-style path, or a URL. These paths can also be a mix of different types. If the path is UNC (for example, \\\Symserver\Symbols), then the debug engine should determine if the path is to a symbol server and should be able to load symbols from that server, caching them in the path specified by `szSymbolCachePath`.  
  
 The symbol path can also contain one or more cache locations. Caches are listed in priority order, with the highest priority cache first, and separated by * symbols. For example:  
  
```  
\\symbols\symbols;\\someotherserver\symbols;c:\symbols\httpsymbols*http://msdl.microsoft.com  
```  
  
 The [IDebugEngine3::LoadSymbols](../vs140/IDebugEngine3--LoadSymbols.md) method performs the actual load of the symbols.  
  
## See Also  
 [IDebugEngine3::LoadSymbols](../vs140/IDebugEngine3--LoadSymbols.md)   
 [IDebugEngine3](../vs140/IDebugEngine3.md)