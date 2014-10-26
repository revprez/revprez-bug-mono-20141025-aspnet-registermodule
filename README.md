# Bug report and sample for [Bug 21810](https://bugzilla.xamarin.com/show_bug.cgi?id=21810).

Ran into the following exception while attempting to execute the  ASP.NET application

```
System.MissingMethodException
Method not found: 'System.Web.HttpApplication.RegisterModule'.

Description: HTTP 500.Error processing request.
Details: Non-web exception. Exception origin (name of application or object): mscorlib.
Exception stack trace:
  at (wrapper managed-to-native) System.Reflection.MonoMethod:InternalInvoke (System.Reflection.MonoMethod,object,object[],System.Exception&)
  at System.Reflection.MonoMethod.Invoke (System.Object obj, BindingFlags invokeAttr, System.Reflection.Binder binder, System.Object[] parameters, System.Globalization.CultureInfo culture) [0x00054] in /private/tmp/source-mono-mac-3.10.0-branch/bockbuild-mono-3.10.0-branch/profiles/mono-mac-xamarin/build-root/mono-3.10.0/mcs/class/corlib/System.Reflection/MonoMethod.cs:230 
``` 

Sample project created by instrumenting empty ASP.NET application (.NET 4.5) with Microsoft's [Asp.Net Identity Samples](http://www.nuget.org/packages/Microsoft.AspNet.Identity.Samples)
