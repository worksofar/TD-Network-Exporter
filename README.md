# TouchDesigner Network Exporter/Importer 
Version: 0.1 beta

## Table of Contents
1. Introduction
2. Installation
3. Exporting a Network
4. Importing a Network
5. Troubleshooting
6. Best Practices
7. Support

## 1. Introduction

The TouchDesigner Network Exporter/Importer is a tool designed to help your workflow by allowing you to export and import TouchDesigner networks as JSON files. This enables easy sharing, versioning, and backup of your projects.

## 2. Installation

1. Copy the `networkExporter.tox` file into your TouchDesigner project.

## 3. Exporting a Network

To export a network:

1. Select the parent component you want to export in your TouchDesigner network.
2. In the `network_exporter` component, set the following parameters:
   - `Parent`: Set this to the path of the component you want to export.
   - `Outputfolder`: Set this to the directory where you want to save the JSON file.
3. Click the `Export` button on the `network_exporter` component.
4. The JSON file will be saved in the specified output folder. The filename will be based on the path of the exported component, ensuring unique and identifiable exports.

## 4. Importing a Network

To import a network:

1. In the `network_exporter` component, set the following parameters:
   - `Jsonfile`: Set this to the path of the JSON file you want to import.
   - `Target`: Set this to the path where you want to import the network. If left empty, it will import to the root of the project.
2. Click the `Import` button on the `network_exporter` component.
3. The network structure will be recreated based on the JSON file.

## 5. Troubleshooting

- If you encounter any errors during export or import, check the TextPort or console for error messages. These messages will help identify the specific issue.
- Common issues include:
  - Incorrect paths for Parent, Outputfolder, or Jsonfile parameters.
  - Permissions issues when writing to the output folder.
  - Incompatible JSON structure (if you're importing a file that wasn't created by this exporter).

## 6. Best Practices

- Always test the export/import process on a copy of your project before using it on your main project.
- Use meaningful names for your components to make the exported JSON files easily identifiable.
- Keep your export folder organized. Consider using a version control system for managing multiple exports.
- When sharing exported networks, include any custom modules or dependencies that might be necessary for the network to function correctly.

