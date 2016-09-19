---
title: "ATL Encoding Reference"
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
ms.assetid: 82d4fdf3-3c4a-4fe2-b297-8ffb4714406f
caps.latest.revision: 8
translation.priority.ht: 
  - de-de
  - ja-jp
---
# ATL Encoding Reference
Encoding in a range of common Internet standards such as uuencode, hexadecimal, and UTF8 is supported by the code found in atlenc.h.  
  
### Functions  
  
|||  
|-|-|  
|[AtlGetHexValue](../vs140/AtlGetHexValue.md)|Call this function to get the numeric value of a hexadecimal digit.|  
|[AtlHexDecode](../vs140/AtlHexDecode.md)|Decodes a string of data that has been encoded as hexadecimal text such as by a previous call to [AtlHexEncode](../vs140/AtlHexEncode.md).|  
|[AtlHexDecodeGetRequiredLength](../vs140/AtlHexDecodeGetRequiredLength.md)|Call this function to get the size in bytes of a buffer that could contain data decoded from a hex-encoded string of the specified length.|  
|[AtlHexEncode](../vs140/AtlHexEncode.md)|Call this function to encode some data as a string of hexadecimal text.|  
|[AtlHexEncodeGetRequiredLength](../vs140/AtlHexEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
|[AtlUnicodeToUTF8](../vs140/AtlUnicodeToUTF8.md)|Call this function to convert a Unicode string to UTF-8.|  
|[BEncode](../vs140/BEncode.md)|Call this function to convert some data using the "B" encoding.|  
|[BEncodeGetRequiredLength](../vs140/BEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
|[EscapeXML](../vs140/EscapeXML.md)|Call this function to convert characters that are unsafe for use in XML to their safe equivalents.|  
|[GetExtendedChars](../vs140/GetExtendedChars.md)|Call this function to get the number of extended characters in a string.|  
|[IsExtendedChar](../vs140/IsExtendedChar.md)|Call this function to find out if a given character is an extended character (less than 32, greater than 126, and not a tab, linefeed or carriage return)|  
|[QEncode](../vs140/QEncode.md)|Call this function to convert some data using the "Q" encoding.|  
|[QEncodeGetRequiredLength](../vs140/QEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
|[QPDecode](../vs140/QPDecode.md)|Decodes a string of data that has been encoded in quoted-printable format such as by a previous call to [QPEncode](../vs140/QPEncode.md).|  
|[QPDecodeGetRequiredLength](../vs140/QPDecodeGetRequiredLength.md)|Call this function to get the size in bytes of a buffer that could contain data decoded from quoted-printable-encoded string of the specified length.|  
|[QPEncode](../vs140/QPEncode.md)|Call this function to encode some data in quoted-printable format.|  
|[QPEncodeGetRequiredLength](../vs140/QPEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
|[UUDecode](../vs140/UUDecode.md)|Decodes a string of data that has been uuencoded such as by a previous call to [UUEncode](../vs140/UUEncode.md).|  
|[UUDecodeGetRequiredLength](../vs140/UUDecodeGetRequiredLength.md)|Call this function to get the size in bytes of a buffer that could contain data decoded from a uuencoded string of the specified length.|  
|[UUEncode](../vs140/UUEncode.md)|Call this function to uuencode some data.|  
|[UUEncodeGetRequiredLength](../vs140/UUEncodeGetRequiredLength.md)|Call this function to get the size in characters of a buffer that could contain a string encoded from data of the specified size.|  
  
### Macros  
  
|||  
|-|-|  
|[ATL_ESC Flags](../vs140/ATL_ESC-Flags.md)|These flags are used to control the behavior of [EscapeXML](../vs140/EscapeXML.md).|  
|[ATLSMTP_QPENCODE Flags](../vs140/ATLSMTP_QPENCODE-Flags.md)|These flags describe how quoted-printable encoding is to be performed by [QPEncode](../vs140/QPEncode.md).|  
|[ATLSMTP_UUENCODE Flags](../vs140/ATLSMTP_UUENCODE-Flags.md)|These flags describe how uuencoding is to be performed by [UUEncode](../vs140/UUEncode.md).|  
  
## See Also  
 [ATL Concepts](../vs140/Active-Template-Library--ATL--Concepts.md)   
 [ATL Reference](../vs140/ATL-COM-Desktop-Components.md)