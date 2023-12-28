# Insomswagger

## Introduction
Insomswagger is a versatile Node.js package designed to simplify the process of converting exported JSON from Insomnia into Swagger documentation. This utility offers flexibility by allowing users to generate either Swagger JSON files or PHP annotations based on their specific needs.

Whether you prefer a clean Swagger JSON representation or you're working within a PHP environment using annotations, this package has you covered. Easily create clear and concise API documentation tailored to your project requirements.

## Installation

Before using the package, ensure you have Node.js installed on your machine. If not, you can download it [here](https://nodejs.org/).

## Usage

To utilize the package, follow these steps:

1. Install the package globally:

   ```bash
   npm install -g insomswagger
   ```

2. Navigate to the directory containing your input file.

3. Run the following command:

   - For Swagger PHP Annotations:

     ```bash
    insomswagger -a [inputFilePath] [outputFilePath]
     ```

   - For Swagger JSON:
     ```bash
      insomswagger -j [inputFilePath] [outputFilePath]
     ```

   If `outputFilePath` is not provided, the default names (`annotations.php` for -a and `api-docs.json` for -j) will be used.

## Tips for Organizing Files in Insomnia

For optimal results when generating annotations, consider organizing your files in Insomnia:

- Group requests under folders based on their functionality.
- Use meaningful names for requests and folders.
- Provide descriptions for requests and folders.

## Adding Annotations to Controllers

To incorporate the generated annotations into your controllers, follow these steps:

1. Open the file containing the generated annotations in your preferred IDE.

2. Copy the annotations corresponding to each controller and method.

3. Paste the annotations into the respective controller and method in your codebase.

Annotations with the same tags are placed side by side if you've organized your Insomnia JSON accordingly.

# Viewing Swagger Documentation

To view the Swagger documentation in your Laravel project, you can use tools like [Darkaonline/L5-Swagger](https://github.com/DarkaOnLine/L5-Swagger).

1. If your Laravel project is not using L5-Swagger yet, you have two options:

   a. Follow the manual installation instructions in the [L5-Swagger repository](https://github.com/DarkaOnLine/L5-Swagger).

   b. Alternatively, you can run the following command, which  automates the installation of Swagger documentation for your Laravel project using [Darkaonline/L5-Swagger](https://github.com/DarkaOnLine/L5-Swagger):

    ````bash
    insomswagger install
    ````

2. Once L5-Swagger has been installed, it generates an api-docs folder in the `storage` directory. If this has not yet been generated, create it.
3.copy the `api-docs.json` file generated by the command 
    ```bash
      insomswagger -j [inputFilePath] [outputFilePath]
     ```
and paste it in `storage/api-docs/api-docs.json` .
NB: If you are told that a file with the same name exists, choose the "replace" option.

Now, when you access the Swagger documentation in your Laravel project, it will reflect the API documentation generated from your Insomnia collection.
## Examples
Here are a few examples of how to use the package:

- For Swagger PHP Annotations:
    ```bash
    insomswagger -a insomnia-export.json my-annotations.php
    ```

- For Swagger JSON:
    ```bash
    insomswagger -j insomnia-export.json my-api-docs.json
    ```
- For Darkaonline/l5-swagger installation:
    ```bash
   insomswagger install
    ```

## License
This package is licensed under the MIT License. See the [LICENSE.md](LICENSE.md) file for details.

## Author
Magid Ba

## Issues and Contributions
If you encounter any issues or want to contribute to the project, please visit the [GitHub repository](https://github.com/bamagid/insomnia-docs-swagger).

Happy documenting!
````
