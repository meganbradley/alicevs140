---
title: "&lt;ios&gt; typedefs"
ms.custom: na
ms.date: 09/19/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b962632-3439-44de-bf26-20c67a7f0ff3
caps.latest.revision: 11
---
# &lt;ios&gt; typedefs
||||  
|-|-|-|  
|[ios](#ios)|[streamoff](#streamoff)|[streampos](#streampos)|  
|[streamsize](#streamsize)|[wios](#wios)|[wstreampos](#wstreampos)|  
  
##  <a name="ios"></a>  ios  
 Supports the ios class from the old iostream library.  
  
```  
typedef basic _ ios<char, char _ traits<char> > ios;  
  
```  
  
### Remarks  
 The type is a synonym for template class [basic_ios](../vs140/basic_ios-Class.md), specialized for elements of type `char` with default character traits.  
  
##  <a name="streamoff"></a>  streamoff  
 Supports internal operations.  
  
```  
#ifdef _WIN64  
    typedef __int64 streamoff;  
#else  
    typedef long streamoff;  
#endif  
```  
  
### Remarks  
 The type is a signed integer that describes an object that can store a byte offset involved in various stream positioning operations. Its representation has at least 32 value bits. It is not necessarily large enough to represent an arbitrary byte position within a stream. The value **streamoff(-1)** generally indicates an erroneous offset.  
  
##  <a name="streampos"></a>  streampos  
 Holds the current position of the buffer pointer or file pointer.  
  
```  
typedef fpos<mbstate _ t> streampos;  
  
```  
  
### Remarks  
 The type is a synonym for [fpos](../vs140/fpos-Class.md)< `mbstate_t`>.  
  
### Example  
  
```  
// ios_streampos.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
  
   ofstream x( "iostream.txt" );  
   x << "testing";  
   streampos y = x.tellp( );  
   cout << y << endl;  
}  
```  
  
  **7**    
##  <a name="streamsize"></a>  streamsize  
 Denotes the size of the stream.  
  
```  
#ifdef _WIN64  
    typedef __int64 streamsize;  
#else  
    typedef int streamsize;  
#endif  
```  
  
### Remarks  
 The type is a signed integer that describes an object that can store a count of the number of elements involved in various stream operations. Its representation has at least 16 bits. It is not necessarily large enough to represent an arbitrary byte position within a stream.  
  
### Example  
  After compiling and running the following program, look at the file test.txt to see the effect of setting `streamsize`.  
  
```  
// ios_streamsize.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
   char a[16] = "any such text";  
   ofstream x( "test.txt" );  
   streamsize y = 6;  
   x.write( a, y );  
}  
```  
  
##  <a name="wios"></a>  wios  
 Supports the wios class from the old iostream library.  
  
```  
typedef basic _ ios<wchar _ t, char _ traits<wchar _ t> > wios;  
  
```  
  
### Remarks  
 The type is a synonym for template class [basic_ios](../vs140/basic_ios-Class.md), specialized for elements of type `wchar_t` with default character traits.  
  
##  <a name="wstreampos"></a>  wstreampos  
 Holds the current position of the buffer pointer or file pointer.  
  
```  
typedef fpos<mbstate _ t> wstreampos;  
  
```  
  
### Remarks  
 The type is a synonym for [fpos](../vs140/fpos-Class.md)< `mbstate_t`>.  
  
### Example  
  
```  
// ios_wstreampos.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main( )   
{  
   using namespace std;  
   wofstream xw( "wiostream.txt" );  
   xw << L"testing";  
   wstreampos y = xw.tellp( );  
   cout << y << endl;  
}  
```  
  
  **7**    
## See Also  
 [&lt;ios&gt;](../vs140/-ios-.md)