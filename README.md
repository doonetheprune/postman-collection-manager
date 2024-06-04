
# Postman Collection Merger

## Description

The Postman Collection Merger is a command-line interface (CLI) tool designed to merge an exported postman collection into an existing postman collection.


## Installation

To install the Postman Collection Merger, you need to have Node.js and npm installed on your computer. Once you have those set up, you can install the tool globally using npm:

\```bash
npm install -g postman-collection-merger
\```

This will install the package globally on your system, allowing you to use it from anywhere in your command line.

## Usage

Run the tool using the following command syntax:

\```bash
postman-merger --apiKey <YOUR_API_KEY> --collection <COLLECTION_NAME> --workspace <WORKSPACE_NAME> --folderName <FOLDER_NAME> --collectionJsonFile <PATH_TO_COLLECTION_JSON>
\```

### Command-Line Arguments

- `--apiKey` or `-k`: Your API key for the Postman API. This is required to authenticate requests.
- `--mergedCollection` or `-m`: The name of the collection to merge into. This specifies the target collection that will be updated.
- `--workspaceName` or `-w`: The name or ID of the workspace where the collection resides. This helps in locating the collection within your Postman environment.
- `--folderName` or `-f`: The name of the folder to be added to the collection. This represents the new folder that will be merged into the existing collection.
- `--createCollectionIfMissing, -create`: Specify whether to create the Postman collection if it does not exist.

## Examples

This example demonstrates how to use the Postman Collection Merger to merge a folder into the "Example Collection" located in the default "My Workspace".

An example postman collection can be found at `./[example-1-postman-collection.json](example%2Fexample-1-postman-collection.json)`

### Example Command

\```bash
postman-merger --apiKey "your_api_key" --collection "Example Collection" --workspace "My Workspace" --folderName "New Folder" --collectionJsonFile "./example/example-1-postman-collection.json" --createCollectionIfMissing true
\```

This command will replace the "New Folder" in the "Example Collection" within "My Workspace". 
It will create the "Example Collection" if needed. 
It will not affect any other folders in the collection

## Contributing

Contributions to the Postman Collection Manager are welcome! If you have suggestions for improvements or encounter any issues, please feel free to open an issue or submit a pull request on our [GitHub repository](#).

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
