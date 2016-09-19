---
title: "Walkthrough: Changing Where My.Application.Log Writes Information (Visual Basic)"
ms.custom: na
ms.date: 09/19/2016
ms.devlang: 
  - VB
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-visual-basic
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ecc74f95-743c-450d-93f6-09a30db0fe4a
caps.latest.revision: 22
translation.priority.ht: 
  - de-de
  - ja-jp
---
# Walkthrough: Changing Where My.Application.Log Writes Information (Visual Basic)
You can use the `My.Application.Log` and `My.Log` objects to log information about events that occur in your application. This walkthrough shows how to override the default settings and cause the `Log` object to write to other log listeners.  
  
## Prerequisites  
 The `Log` object can write information to several log listeners. You need to determine the current configuration of the log listeners before changing the configurations. For more information, see [Walkthrough: Determining Where My.Application.Log Writes Information](../Topic/Walkthrough:%20Determining%20Where%20My.Application.Log%20Writes%20Information%20\(Visual%20Basic\).md).  
  
 You may want to review [How to: Write Event Information to a Text File](../Topic/How%20to:%20Write%20Event%20Information%20to%20a%20Text%20File%20\(Visual%20Basic\).md) or [How to: Write Event Information to an Application Event Log](../vs140/How-to--Write-to-an-Application-Event-Log--Visual-Basic-.md).  
  
### To add listeners  
  
1.  Right-click app.config in **Solution Explorer** and choose **Open**.  
  
     \- or -  
  
     If there is no app.config file:  
  
    1.  On the **Project** menu, choose **Add New Item**.  
  
    2.  From the **Add New Item** dialog box, select **Application Configuration File**.  
  
    3.  Click **Add**.  
  
2.  Locate the `<listeners>` section, under the `<source>` section with the `name` attribute "DefaultSource", in the `<sources>` section. The `<sources>` section is in the `<system.diagnostics>` section, in the top-level `<configuration>` section.  
  
3.  Add these elements to that `<listeners>` section.  
  
    ```  
    <!-- Uncomment to connect the application file log. -->  
    <!-- <add name="FileLog" /> -->  
    <!-- Uncomment to connect the event log. -->  
    <!-- <add name="EventLog" /> -->  
    <!-- Uncomment to connect the event log. -->  
    <!-- <add name="Delimited" /> -->  
    <!-- Uncomment to connect the XML log. -->  
    <!-- <add name="XmlWriter" /> -->  
    <!-- Uncomment to connect the console log. -->  
    <!-- <add name="Console" /> -->  
    ```  
  
4.  Uncomment the log listeners that you want to receive `Log` messages.  
  
5.  Locate the `<sharedListeners>` section, in the `<system.diagnostics>` section, in the top-level `<configuration>` section.  
  
6.  Add these elements to that `<sharedListeners>` section.  
  
    ```  
    <add name="FileLog"  
         type="Microsoft.VisualBasic.Logging.FileLogTraceListener,   
               Microsoft.VisualBasic, Version=8.0.0.0,   
               Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a"  
         initializeData="FileLogWriter" />  
    <add name="EventLog"  
         type="System.Diagnostics.EventLogTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="sample application"/>  
    <add name="Delimited"   
         type="System.Diagnostics.DelimitedListTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="c:\temp\sampleDelimitedFile.txt"  
         traceOutputOptions="DateTime" />  
    <add name="XmlWriter"  
         type="System.Diagnostics.XmlWriterTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="c:\temp\sampleLogFile.xml" />  
    <add name="Console"  
         type="System.Diagnostics.ConsoleTraceListener,   
               System, Version=2.0.0.0,   
               Culture=neutral, PublicKeyToken=b77a5c561934e089"  
         initializeData="true" />  
    ```  
  
7.  The content of the app.config file should be similar to the following XML:  
  
    ```  
    <?xml version="1.0" encoding="utf-8" ?>  
    <configuration>  
      <system.diagnostics>  
        <sources>  
          <!-- This section configures My.Application.Log -->  
          <source name="DefaultSource" switchName="DefaultSwitch">  
            <listeners>  
              <add name="FileLog"/>  
              <!-- Uncomment to connect the application file log. -->  
              <!-- <add name="FileLog" /> -->  
              <!-- Uncomment to connect the event log. -->  
              <!-- <add name="EventLog" /> -->  
              <!-- Uncomment to connect the event log. -->  
              <!-- <add name="Delimited" /> -->  
              <!-- Uncomment to connect the XML log. -->  
              <!-- <add name="XmlWriter" /> -->  
              <!-- Uncomment to connect the console log. -->  
              <!-- <add name="Console" /> -->  
            </listeners>  
          </source>  
        </sources>  
        <switches>  
          <add name="DefaultSwitch" value="Information" />  
        </switches>  
        <sharedListeners>  
          <add name="FileLog"  
               type="Microsoft.VisualBasic.Logging.FileLogTraceListener,   
                     Microsoft.VisualBasic, Version=8.0.0.0,   
                     Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a"  
               initializeData="FileLogWriter" />  
          <add name="EventLog"  
               type="System.Diagnostics.EventLogTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="sample application"/>  
          <add name="Delimited"   
               type="System.Diagnostics.DelimitedListTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="c:\temp\sampleDelimitedFile.txt"  
               traceOutputOptions="DateTime" />  
          <add name="XmlWriter"  
               type="System.Diagnostics.XmlWriterTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="c:\temp\sampleLogFile.xml" />  
          <add name="Console"  
               type="System.Diagnostics.ConsoleTraceListener,   
                     System, Version=2.0.0.0,   
                     Culture=neutral, PublicKeyToken=b77a5c561934e089"  
               initializeData="true" />  
        </sharedListeners>  
      </system.diagnostics>  
    </configuration>  
    ```  
  
### To reconfigure a listener  
  
1.  Locate the listener's `<add>` element from the `<sharedListeners>` section.  
  
2.  The `type` attribute gives the name of the listener type. This type must inherit from the <xref:System.Diagnostics.TraceListener?qualifyHint=False> class. Use the strongly named type name to ensure that the right type is used. For more information, see the "To reference a strongly named type" section below.  
  
     Some types that you can use are:  
  
    -   A <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener?qualifyHint=True> listener, which writes to a file log.  
  
    -   A <xref:System.Diagnostics.EventLogTraceListener?qualifyHint=True> listener, which writes information to the computer event log specified by the `initializeData` parameter.  
  
    -   The <xref:System.Diagnostics.DelimitedListTraceListener?qualifyHint=True> and <xref:System.Diagnostics.XmlWriterTraceListener?qualifyHint=True> listeners, which write to the file specified in the `initializeData` parameter.  
  
    -   A <xref:System.Diagnostics.ConsoleTraceListener?qualifyHint=True> listener, which writes to the command-line console.  
  
     For information about where other types of log listeners write information, consult that type's documentation.  
  
3.  When the application creates the log-listener object, it passes the `initializeData` attribute as the constructor parameter. The meaning of the `initializeData` attribute depends on the trace listener.  
  
4.  After creating the log listener, the application sets the listener's properties. These properties are defined by the other attributes in the `<add>` element. For more information on the properties for a particular listener, see the documentation for that listener's type.  
  
### To reference a strongly named type  
  
1.  To ensure that the right type is used for your log listener, make sure to use the fully qualified type name and the strongly named assembly name. The syntax of a strongly named type is as follows:  
  
     <*type name*>, <*assembly name*>, <*version number*>, <*culture*>, <*strong name*>  
  
2.  This code example shows how to determine the strongly named type name for a fully qualified type—"System.Diagnostics.FileLogTraceListener" in this case.  
  
     [!CODE [VbVbalrMyApplicationLog#15](../CodeSnippet/VS_Snippets_VBCSharp/VbVbalrMyApplicationLog#15)]  
  
     This is the output, and it can be used to uniquely reference a strongly named type, as in the "To add listeners" procedure above.  
  
     `Microsoft.VisualBasic.Logging.FileLogTraceListener, Microsoft.VisualBasic, Version=8.0.0.0, Culture=neutral, PublicKeyToken=b03f5f7f11d50a3a`  
  
## See Also  
 <xref:Microsoft.VisualBasic.Logging.Log?qualifyHint=True>   
 <xref:System.Diagnostics.TraceListener?qualifyHint=False>   
 <xref:Microsoft.VisualBasic.Logging.FileLogTraceListener?qualifyHint=True>   
 <xref:System.Diagnostics.EventLogTraceListener?qualifyHint=True>   
 [How to: Write Event Information to a Text File](../Topic/How%20to:%20Write%20Event%20Information%20to%20a%20Text%20File%20\(Visual%20Basic\).md)   
 [How to: Write Event Information to an Application Event Log](../vs140/How-to--Write-to-an-Application-Event-Log--Visual-Basic-.md)