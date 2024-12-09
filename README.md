# Blazor Printing
This is a fork of the Append.Blazor.Printing package provided by [Append-IT](https://github.com/Append-IT) which currently fixes font sizes on printing. Below is from the original repository.
Print and Save files in Blazor using the native dialog box using JavaScript Interop and [PrintJS](https://printjs.crabbly.com/).

![Nuget (with prereleases)](https://img.shields.io/nuget/vpre/Append.Blazor.Printing.Patched?style=flat-square)

## The result
![Screenshot](https://i.imgur.com/a0O6zwE.gif)

## The blogpost
You can read more about the service in [this blog post](https://medium.com/@benjaminvertonghen/printing-pdfs-in-blazor-8dff559101f9).

## Documentation
Documentation and examples can be found [here](https://blazor-printing.append.be/)

### Installing

You can install from [NuGet](https://www.nuget.org/packages/Append.Blazor.Printing.Patched/6.3.1) using the following command:

`Install-Package Append.Blazor.Printing.Patched`

### Setup

1. Inject the `IPrintingService` in `program.cs`
  ```cs
  builder.Services.AddScoped<IPrintingService, PrintingService>();
  ```
2. Use the Service
  ```razor
  @using Append.Blazor.Printing
  @inject IPrintingService PrintingService
  <button @onclick="@(()=> PrintingService.Print("docs/sample.pdf"))">
   Print PDF
  </button>
  ```
