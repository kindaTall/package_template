# Project Name

Template for setting up new python projects

## Setup

### Cloning the Repository

Clone the repository and navigate to the project directory:

```shell
git clone [repository URL] project-name
cd project-name
```

### Renaming the Template 
Rename the ``src\template`` to your desired project name.

### Setting Up a New Git Repository
Remove the old git and initialize a new git repository
```shell
rm -rf .git
git init
```

## Project Structure
The project project-name consists of source code files located in the src folder, executable scripts in the scripts folder, and test files in the tests folder, facilitating development, execution, and testing of the project's functionality.
```
project-name/
├── LICENSE
├── pyproject.toml
├── README.md
├── src/
│   └── project-name/
│       ├── __init__.py
│       └── my_source_file1.py
├── scripts/
│   ├── script1.py
│   └── ...
└── tests/
    ├── test_my_source_file.py
    └── ...
```

## Development
### Source Files
Create your source files in the src/project/ directory. These files should contain your methods, functions, and classes without any standalone execution.

### Script Files
Place your executable script files in the scripts/ directory. These files will serve as entry points to your package's functionality.

#### Installing Locally in Editable Mode
The scripts require the source files to be installed as if you were using the package as a third-party user. 
To install the project locally in editable mode, allowing you to make changes to the source code without reinstalling, run the following command:

```shell
pip install . -e
```

## Testing
### Test Files
Create your test files in the tests/ directory. These files should contain your unit tests.

### Running Tests
To run the tests, make sure you have the necessary testing framework installed (e.g., pytest). If not, install it using:

```shell
pip install pytest
```
Once installed, run the following command from the project's root directory:

```shell
pytest
```
This will execute all the tests in the tests/ directory.

## Building

### Configuration
Ensure that the `requirements.txt` file is upto date and accurate for the project. \
In `pyproject.toml` adjust the name of the project.

### Building the project
Run the following commands to update the build process and build the project.
```shell
python3 -m pip install --upgrade build
python3 -m build
```

This command should output a lot of text and once completed should generate two files in the dist directory:
```
dist/
├── project-name-0.0.1-py3-none-any.whl
└── project-name-0.0.1.tar.gz
```
The tar.gz file is a source distribution whereas the .whl file is a built distribution. Newer pip versions preferentially install built distributions, but will fall back to source distributions if needed. You should always upload a source distribution and provide built distributions for the platforms your project is compatible with.