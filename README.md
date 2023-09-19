# Microservice Setup

## Overview

Microservice Setup is a Python-based Command-Line Interface (CLI) tool aimed to auto-generate a domain-driven, scalable, and maintainable microservices directory structure based on hexagonal architecture. 

## Features

- Auto-generates a clean and scalable microservice project skeleton
- Built around hexagonal architecture principles
- Allows for customization of the project's generated structure through JSON template modification
- Works with Python 3.9 or later

## Requirements

### General

- Python 3.9 or later: Required for running the tool. Make sure it's installed on your system.

### For Advanced Customization

- Poetry: Necessary for building and packaging if you're customizing the JSON templates. [Installation guide here](https://python-poetry.org/docs/#installation).

## Installation

### Via pip

To quickly get started, install Microservice Setup using pip and initialize your microservices project:

```bash
pip install microservice_setup
ms-init example
```

### Advanced Customization

For those who wish to customize the JSON templates used for generating the project skeleton, you can clone this repository and modify the JSON files directly:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/DoMo-98/microservice_setup.git
    cd microservice_setup
    ```
  
2. **Navigate and Modify JSON Templates**:
    Go to `src/templates` and modify `base_structure.json` and/or `root_structure.json` as needed.

3. **Build and Install Locally**:
    Ensure you are in the root directory of the cloned repository. Then build the package and install it locally with the following commands:
    ```bash
    poetry build
    pip install dist/microservice_setup-<your_version>-py3-none-any.whl
    ```

Replace `<your_version>` with the actual version number generated after running `poetry build`.

### Usage

After installation through either method, initialize your microservices project by running:

```bash
ms-init example
```

This command initializes a new microservices project and creates a directory structure within a folder named `example_service`. You can replace `example` with the name of your choice for your microservices project.

## Generated Structure

When you run the `ms-init example` command, the following directory structure will be generated:

```plaintext
example_service/
├── app/
│   ├── adapters/
│   │   ├── controllers/
│   │   └── serializers/
│   ├── application/
│   │   ├── services/
│   │   └── use_cases/
│   ├── common/
│   │   └── constants/
│   └── domain/
│       ├── entities/
│       ├── exceptions/
│       └── interfaces/
├── config/
├── constants/
├── main.py
├── requirements/
├── templates/
└── tests/
    ├── adapters/
    │   ├── controllers/
    │   └── serializers/
    ├── application/
    │   ├── services/
    │   └── use_cases/
    ├── common/
    │   └── constants/
    └── domain/
        ├── entities/
        ├── exceptions/
        └── interfaces/
```

This structure adheres to the principles of hexagonal architecture and DDD, providing a clear and maintainable outline for your microservice.

## Author

- Éric Dominguez Morales - *Initial Work* - [Email](mailto:ericdominguezm@gmail.com)

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE) file for details.
