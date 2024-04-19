# Revit API

This project is a simple demonstration of using the Autodesk Revit API to create a basic Revit add-in.

## Overview

The project contains a single class named `Class1` which implements the `IExternalApplication` interface. This interface is a part of the Revit API and allows developers to create external applications (add-ins) for Revit.

## Functionality

When the Revit application starts, the add-in displays a simple task dialog with the message "Hello Revit API!".

## Usage

1. Build the project in Visual Studio to generate the add-in assembly (DLL).
2. Load the add-in DLL into Revit by placing it in the appropriate add-ins folder (`%APPDATA%\Autodesk\Revit\Addins\[version]`).
3. Launch Revit.
4. Once Revit starts, the add-in will execute automatically, displaying the "Hello Revit API!" message in a task dialog.

## Requirements

- Autodesk Revit installed

## Setup

1. Clone this repository to your local machine.
2. Open the solution in Visual Studio.
3. Build the project to generate the add-in DLL.
4. Copy the DLL to the Revit add-ins folder.
5. Launch Revit and observe the add-in execution.

## Contributing

Contributions are welcome! If you'd like to improve this project or add more functionality, please fork the repository and submit a pull request.

## Sample code 
```c#

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
using Autodesk.Revit.ApplicationServices;
using Autodesk.Revit.Attributes;
using Autodesk.Revit.DB;
using Autodesk.Revit.UI;
using Autodesk.Revit.UI.Selection;
using Autodesk.Revit.DB.Architecture;
using System.Runtime.InteropServices;
namespace RevitAPI_First
{

    [Autodesk.Revit.Attributes.Transaction(Autodesk.Revit.Attributes.TransactionMode.Manual)]
    public class Class1 : IExternalCommand
    {
        public Autodesk.Revit.UI.Result Execute(ExternalCommandData revit,

          ref string message, ElementSet elements)

        {

            TaskDialog.Show("Hi Aayush!", "First Revit API...");

            return Autodesk.Revit.UI.Result.Succeeded;

        }
    }
}

```
## Output Screenshot
![Revit_API_Output_SS](https://github.com/AayushJoshiCCTECH/Revit_API/assets/157628596/827b4288-c195-428b-adc6-5266c5eaf067)


## Clone this repository to your local machine.

```
git clone https://github.com/AayushJoshiCCTECH/Revit_API.git
```
