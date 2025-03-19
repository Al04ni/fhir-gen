# FHIRGen 🔥
🚀 A Blazingly Fast Rust CLI tool for generating [FHIR](https://www.hl7.org/fhir/overview.html) resources and exporting them to various formats.  This can be handy when looking for vast amounts of Seed Data in Health Applications for testing purposes or populating a database.

## Features
- Select from a list of available FHIR resource types to generate.
- Generate sample input for each resource type, which the user can then modify.
- Select from multiple output formats, including JSON, CSV, XML, or copy to clipboard.
- Validate the generated resources against the FHIR specification.
- Create custom templates for generating resources.
- Generate multiple resources at once.
- Select the FHIR version to generate resources for.
- Handle errors and provide helpful error messages.

## Usage
```bash
fhirgen [OPTIONS]

Options:
    -t, --type           Specify the type of FHIR resource to generate
    -o, --output         Specify the output format (json, csv, xml, clipboard)
    -v, --version        Specify the FHIR version to use
    -h, --help           Display this help message
```

## Installation
- 1 Clone this repository to your local machine.
- 2 Run `cargo build` to build the project.
- 3 Run `cargo install` to install the tool globally on your system.

## Project Structure

```bash
.
├── Cargo.toml
├── src
│   ├── bin
│   │   └── main.rs
│   ├── lib.rs
│   ├── resources
│   │   ├── mod.rs
│   │   ├── patient.rs
│   │   └── encounter.rs
│   └── utils
│       └── mod.rs
└── templates
    └── patient.toml
```

| File/Folder Name | Description |
| --- | --- |
| `Cargo.toml` | Contains the dependencies and metadata for the project. |
| `src/bin/main.rs` | Main binary file that contains the code for the FHIRGen CLI. |
| `src/lib.rs` | Library file that exports the functions used by the main binary. |
| `src/resources/mod.rs` | Exports the resource modules, such as `patient` and `encounter`. |
| `src/resources/patient.rs` | Contains the code for generating patient resources. |
| `src/resources/encounter.rs` | Contains the code for generating encounter resources. |
| `src/utils/mod.rs` | Exports the utility modules, such as helper functions for generating resources. |
| `templates/patient.toml` | Example template for generating patient resources. |


## Example
Generate a sample patient resource in JSON format:

```bash
fhirgen -t patient -o json
```

## Contributions
Contributions are welcome! If you find any bugs or have any suggestions, please open an issue.

## Future Work
- Support for generating FHIR resources from existing templates or sample resources.
- Integration with FHIR servers for testing and validating generated resources.
- Option to select which elements of a resource to include in the output.
- Option to randomize some elements of the resource to generate more diverse and realistic data.
- Ability to create and manage templates directly from the CLI.
- Integration with other healthcare-related tools and platforms.
- Support for generating resources in other formats such as YAML.
- Generate FHIR resources with cross-resource relationships, such as linking a patient resource to an encounter resource.

## License
This project is licensed under the MIT License.




