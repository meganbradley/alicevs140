---
title: "com::ptr Class"
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
ms.assetid: 0144d0e4-919c-45f9-a3f8-fbc9edba32bf
caps.latest.revision: 10
translation.priority.ht: 
  - de-de
  - ja-jp
---
# com::ptr Class
A wrapper for a COM object that can be used as a member of a CLR class.  The wrapper also automates lifetime management of the COM object, releasing all owned references on the object when its destructor is called. Analogous to [CComPtr](../vs140/CComPtr-Class.md).  
  
## Syntax  
  
```  
template<class _interface_type>  
ref class ptr;  
```  
  
#### Parameters  
 `_interface_type`  
 COM interface.  
  
## Remarks  
 A `com::ptr` can also be used as a local function variable to simplify various COM tasks and to automate lifetime management.  
  
 A `com::ptr` cannot be used directly as a function parameter; use a [tracking reference (%)](../vs140/Tracking-Reference-Operator--C---Component-Extensions-.md) or a [handle (^)](../vs140/Handle-to-Object-Operator--^----C---Component-Extensions-.md) instead.  
  
 A `com::ptr` cannot be directly returned from a function; use a handle instead.  
  
## Example  
 This example implements a CLR class that uses a `com::ptr` to wrap its private member `IXMLDOMDocument` object.  Calling the public methods of the class results in calls to the contained `IXMLDOMDocument` object.  The sample creates an instance of an XML document, fills it with some simple XML, and does a simplified walk of the nodes in the parsed document tree to print the XML to the console.  
  
```  
// comptr.cpp  
// compile with: /clr /link msxml2.lib  
#include <msxml2.h>  
#include <msclr\com\ptr.h>  
  
#import <msxml3.dll> raw_interfaces_only  
  
using namespace System;  
using namespace System::Runtime::InteropServices;  
using namespace msclr;  
  
// a ref class that uses a com::ptr to contain an   
// IXMLDOMDocument object  
ref class XmlDocument {  
public:  
   // construct the internal com::ptr with a null interface  
   // and use CreateInstance to fill it  
   XmlDocument(String^ progid) {  
      m_ptrDoc.CreateInstance(progid);     
   }  
  
   void LoadXml(String^ xml) {  
      pin_ptr<const wchar_t> pinnedXml = PtrToStringChars(xml);  
      BSTR bstr = NULL;  
  
      try {  
         // load some XML into the document  
         bstr = ::SysAllocString(pinnedXml);  
         if (NULL == bstr) {  
            throw gcnew OutOfMemoryException;  
         }  
         VARIANT_BOOL bIsSuccessful = false;  
         // use operator -> to call IXMODOMDocument member function  
         Marshal::ThrowExceptionForHR(m_ptrDoc->loadXML(bstr, &bIsSuccessful));  
      }  
      finally {  
         ::SysFreeString(bstr);  
      }  
   }  
  
   // simplified function to write just the first xml node to the console  
   void WriteXml() {  
      IXMLDOMNode* pNode = NULL;  
  
      try {  
         // the first child of the document is the first real xml node  
         Marshal::ThrowExceptionForHR(m_ptrDoc->get_firstChild(&pNode));  
         if (NULL != pNode) {  
            WriteNode(pNode);  
         }  
      }  
      finally {  
         if (NULL != pNode) {  
            pNode->Release();  
         }  
      }  
   }  
  
   // note that the destructor will call the com::ptr destructor  
   // and automatically release the reference to the COM object  
  
private:  
   // simplified function that only writes the node  
   void WriteNode(IXMLDOMNode* pNode) {  
      BSTR bstr = NULL;  
  
      try {  
         // write out the name and text properties  
         Marshal::ThrowExceptionForHR(pNode->get_nodeName(&bstr));  
         String^ strName = gcnew String(bstr);  
         Console::Write("<{0}>", strName);  
         ::SysFreeString(bstr);  
         bstr = NULL;  
  
         Marshal::ThrowExceptionForHR(pNode->get_text(&bstr));  
         Console::Write(gcnew String(bstr));  
         ::SysFreeString(bstr);  
         bstr = NULL;  
  
         Console::WriteLine("</{0}>", strName);  
      }  
      finally {  
         ::SysFreeString(bstr);  
      }  
   }  
  
   com::ptr<IXMLDOMDocument> m_ptrDoc;  
};  
  
// use the ref class to handle an XML DOM Document object  
int main() {  
   try {  
      // create the class from a progid string  
      XmlDocument doc("Msxml2.DOMDocument.3.0");  
  
      // stream some xml into the document  
      doc.LoadXml("<word>persnickety</word>");  
  
      // write the document to the console  
      doc.WriteXml();  
   }  
   catch (Exception^ e) {  
      Console::WriteLine(e);     
   }  
}  
```  
  
 **<word\>persnickety</word\>**   
## Requirements  
 **Header file** <msclr\com\ptr.h>  
  
 **Namespace** msclr::com  
  
## See Also  
 [C++ Support Library](../vs140/C---Support-Library.md)   
 [ptr Members](../vs140/ptr-Members.md)