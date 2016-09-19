---
title: "&lt;regex&gt; typedefs"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e6a69067-106c-4a24-9e08-7c867a3a2260
caps.latest.revision: 11
---
# &lt;regex&gt; typedefs
||||  
|-|-|-|  
|[cmatch Typedef](#cmatch_typedef)|[cregex_iterator Typedef](#cregex_iterator_typedef)|[cregex_token_iterator Typedef](#cregex_token_iterator_typedef)|  
|[csub_match Typedef](#csub_match_typedef)|[regex Typedef](#regex_typedef)|[smatch Typedef](#smatch_typedef)|  
|[sregex_iterator Typedef](#sregex_iterator_typedef)|[sregex_token_iterator Typedef](#sregex_token_iterator_typedef)|[ssub_match Typedef](#ssub_match_typedef)|  
|[wcmatch Typedef](#wcmatch_typedef)|[wcregex_iterator Typedef](#wcregex_iterator_typedef)|[wcregex_token_iterator Typedef](#wcregex_token_iterator_typedef)|  
|[wcsub_match Typedef](#wcsub_match_typedef)|[wregex Typedef](#wregex_typedef)|[wsmatch Typedef](#wsmatch_typedef)|  
|[wsregex_iterator Typedef](#wsregex_iterator_typedef)|[wsregex_token_iterator Typedef](#wsregex_token_iterator_typedef)|[wssub_match Typedef](#wssub_match_typedef)|  
  
##  <a name="cmatch_typedef"></a>  cmatch Typedef  
 Type definition for char match_results.  
  
```  
typedef match_results<const char*> cmatch;  
```  
  
### Remarks  
 The type describes a specialization of template class [match_results](../vs140/match_results-Class.md) for iterators of type `const char*`.  
  
##  <a name="cregex_iterator_typedef"></a>  cregex_iterator Typedef  
 Type definition for char regex_iterator.  
  
```  
typedef regex_iterator<const char*> cregex_iterator;  
```  
  
### Remarks  
 The type describes a specialization of template class [regex_iterator](../vs140/regex_iterator-Class.md) for iterators of type `const char*`.  
  
##  <a name="cregex_token_iterator_typedef"></a>  cregex_token_iterator Typedef  
 Type definition for char regex_token_iterator  
  
```  
typedef regex_token_iterator<const char*> cregex_token_iterator;  
```  
  
### Remarks  
 The type describes a specialization of template class [regex_token_iterator](../vs140/regex_token_iterator-Class.md) for iterators of type `const char*`.  
  
##  <a name="csub_match_typedef"></a>  csub_match Typedef  
 Type definition for char sub_match.  
  
```  
typedef sub_match<const char*> csub_match;  
```  
  
### Remarks  
 The type describes a specialization of template class [sub_match](../vs140/sub_match-Class.md) for iterators of type `const char*`.  
  
##  <a name="regex_typedef"></a>  regex Typedef  
 Type definition for char basic_regex.  
  
```  
typedef basic_regex<char> regex;  
```  
  
### Remarks  
 The type describes a specialization of template class [basic_regex](../vs140/basic_regex-Class.md) for elements of type `char`.  
  
> [!NOTE]
>  High-bit characters will have unpredictable results with `regex`. Values outside the range of 0 to 127 may result in undefined behavior.  
  
##  <a name="smatch_typedef"></a>  smatch Typedef  
 Type definition for string match_results.  
  
```  
typedef match_results<string::const_iterator> smatch;  
```  
  
### Remarks  
 The type describes a specialization of template class [match_results](../vs140/match_results-Class.md) for iterators of type `string::const_iterator`.  
  
##  <a name="sregex_iterator_typedef"></a>  sregex_iterator Typedef  
 Type definition for string regex_iterator.  
  
```  
typedef regex_iterator<string::const_iterator> sregex_iterator;  
```  
  
### Remarks  
 The type describes a specialization of template class [regex_iterator](../vs140/regex_iterator-Class.md) for iterators of type `string::const_iterator`.  
  
##  <a name="sregex_token_iterator_typedef"></a>  sregex_token_iterator Typedef  
 Type definition for string regex_token_iterator.  
  
```  
typedef regex_token_iterator<string::const_iterator> sregex_token_iterator;  
```  
  
### Remarks  
 The type describes a specialization of template class [regex_token_iterator](../vs140/regex_token_iterator-Class.md) for iterators of type `string::const_iterator`.  
  
##  <a name="ssub_match_typedef"></a>  ssub_match Typedef  
 Type definition for string sub_match.  
  
```  
typedef sub_match<string::const_iterator> ssub_match;  
```  
  
### Remarks  
 The type describes a specialization of template class [sub_match](../vs140/sub_match-Class.md) for iterators of type `string::const_iterator`.  
  
##  <a name="wcmatch_typedef"></a>  wcmatch Typedef  
 Type definition for wchar_t match_results.  
  
```  
typedef match_results<const wchar_t *> wcmatch;  
```  
  
### Remarks  
 The type describes a specialization of template class [match_results](../vs140/match_results-Class.md) for iterators of type `const wchar_t*`.  
  
##  <a name="wcregex_iterator_typedef"></a>  wcregex_iterator Typedef  
 Type definition for wchar_t regex_iterator.  
  
```  
typedef regex_iterator<const wchar_t*> wcregex_iterator;  
```  
  
### Remarks  
 The type describes a specialization of template class [regex_iterator](../vs140/regex_iterator-Class.md) for iterators of type `const wchar_t*`.  
  
##  <a name="wcregex_token_iterator_typedef"></a>  wcregex_token_iterator Typedef  
 Type definition for wchar_t regex_token_iterator.  
  
```  
typedef regex_token_iterator<const wchar_t*> wcregex_token_iterator;  
```  
  
### Remarks  
 The type describes a specialization of template class [regex_token_iterator](../vs140/regex_token_iterator-Class.md) for iterators of type `const wchar_t*`.  
  
##  <a name="wcsub_match_typedef"></a>  wcsub_match Typedef  
 Type definition for wchar_t sub_match.  
  
```  
typedef sub_match<const wchar_t*> wcsub_match;  
```  
  
### Remarks  
 The type describes a specialization of template class [sub_match](../vs140/sub_match-Class.md) for iterators of type `const wchar_t*`.  
  
##  <a name="wregex_typedef"></a>  wregex Typedef  
 Type definition for wchar_t basic_regex.  
  
```  
typedef basic_regex<wchar_t> wregex;  
```  
  
### Remarks  
 The type describes a specialization of template class [basic_regex](../vs140/basic_regex-Class.md) for elements of type `wchar_t`.  
  
##  <a name="wsmatch_typedef"></a>  wsmatch Typedef  
 Type definition for wstring match_results.  
  
```  
typedef match_results<wstring::const_iterator> wsmatch;  
```  
  
### Remarks  
 The type describes a specialization of template class [match_results](../vs140/match_results-Class.md) for iterators of type `wstring::const_iterator`.  
  
##  <a name="wsregex_iterator_typedef"></a>  wsregex_iterator Typedef  
 Type definition for wstring regex_iterator.  
  
```  
typedef regex_iterator<wstring::const_iterator> wsregex_iterator;  
```  
  
### Remarks  
 The type describes a specialization of template class [regex_iterator](../vs140/regex_iterator-Class.md) for iterators of type `wstring::const_iterator`.  
  
##  <a name="wsregex_token_iterator_typedef"></a>  wsregex_token_iterator Typedef  
 Type definition for wstring regex_token_iterator.  
  
```  
typedef regex_token_iterator<wstring::const_iterator> wsregex_token_iterator;  
```  
  
### Remarks  
 The type describes a specialization of template class [regex_token_iterator](../vs140/regex_token_iterator-Class.md) for iterators of type `wstring::const_iterator`.  
  
##  <a name="wssub_match_typedef"></a>  wssub_match Typedef  
 Type definition for wstring sub_match.  
  
```  
typedef sub_match<wstring::const_iterator> wssub_match;  
```  
  
### Remarks  
 The type describes a specialization of template class [sub_match](../vs140/sub_match-Class.md) for iterators of type `wstring::const_iterator`.  
  
## See Also  
 [&lt;regex&gt;](../vs140/-regex-.md)