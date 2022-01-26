##  Steps to reproduce
1. Have the .NET 6 SDK installed
2. Run the application via 'dotnet run'
3. Open the app at 'http://localhost:5184'
4. Open the browser devtools to see following exception

System.AggregateException: One or more errors occurred. (The type initializer for 'OpenTelemetry.Resources.ResourceBuilder' threw an exception.)
 ---> System.TypeInitializationException: The type initializer for 'OpenTelemetry.Resources.ResourceBuilder' threw an exception.
 ---> System.PlatformNotSupportedException: System.Diagnostics.Process is not supported on this platform.
   at System.Diagnostics.Process.GetCurrentProcess()
   at OpenTelemetry.Resources.ResourceBuilder..cctor()
   --- End of inner exception stack trace ---
   at OpenTelemetry.Trace.TracerProviderBuilderBase..ctor()
   at OpenTelemetry.Trace.TracerProviderBuilderSdk..ctor()
   at OpenTelemetry.Sdk.CreateTracerProviderBuilder()
   at Program.<Main>$(String[] args) in C:\Sources\Privat\OtelBlazorTracingBug\Program.cs:line 12
   --- End of inner exception stack trace ---