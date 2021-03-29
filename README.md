# Getting Started with OpenTelemetry with DotNet

Recently OpenTelemetry Tracing Specification reached 1.0.0 — offering long-term stability guarantees for the tracing portion of the OpenTelemetry clients. The first of the .NET language-specific APIs and SDKs have reached v1.0.0.  

This is a major milestone along the path to finally merging OpenTracing and OpenCensus into one unified, standard tracing API. 


## Getting Started With .NET
You can get started with OpenTelemetry .NET in five minutes. 

First, download and install the .NET [Core SDK](https://dotnet.microsoft.com/download) on your computer.

Create a new console application and run it:
```
dotnet new console --output getting-started
cd getting-started
dotnet run
```

You should see the following output:
```
Hello World!
```

Install the [OpenTelemetry.Exporter.Console](https://github.com/open-telemetry/opentelemetry-dotnet/blob/main/src/OpenTelemetry.Exporter.Console/README.md) package:
````
dotnet add package OpenTelemetry.Exporter.Console
````


Update the Program.cs file with the code from [Program.cs](https://github.com/open-telemetry/opentelemetry-dotnet/blob/main/docs/trace/getting-started/Program.cs):

Run the application again (using dotnet run) and you should see the trace output from the console.
````
Activity.Id:          00-8389584945550f40820b96ce1ceb9299-745239d26e408342-01
Activity.DisplayName: SayHello
Activity.Kind:        Internal
Activity.StartTime:   2020-08-12T15:59:10.4461835Z
Activity.Duration:    00:00:00.0066039
Activity.TagObjects:
    foo: 1
    bar: Hello, World!
    baz: [1, 2, 3]
Resource associated with Activity:
    service.name: unknown_service:getting-started
````

Congratulations! You are now capturing traces using OpenTelemetry and displaying them in the console. You can find more information and examples in [GitHub](https://github.com/open-telemetry/opentelemetry-dotnet/tree/main/examples).

You can find more information in the [OpenTelemetry .NET](https://github.com/open-telemetry/opentelemetry-dotnet#contributing) community announcement.
