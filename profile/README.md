
Shojin Python Code Style Guide
==============================

This document outlines the coding standards for Python projects at Shojin. Adhering to these conventions ensures readability, maintainability, and consistency across our codebase.

---

## General Principles
1. **Readability is paramount**: Code should be easy to read and understand.
2. **Consistency matters**: Follow this guide strictly to maintain uniformity.

---

## Naming Conventions

### Variables
- Use `snake_case` for variable names.
  - Example: `user_name`, `order_total`
- Use clear, descriptive names that indicate the variable's purpose.
  - Avoid single-letter variables, except for iterators in short loops.

### Produced Files
- Use `snake_case` for file names.
  - Example: `processed_data.csv`, `error_logs.txt`
- Include timestamps or identifiers when necessary to distinguish files.
  - Example: `report_2024_11_26.txt`

### Python Scripts
- Use `snake_case` for script file names.
  - Example: `data_cleaner.py`, `report_generator.py`
- Script names should describe their function or purpose.

### Projects
- Use `PascalCase` for project names.
  - Example: `ShojinDataPlatform`, `CustomerAnalytics`

### Custom Libraries
- Use `snake_case` for package and module names.
  - Example: `utils`, `data_processing`
- Use `PascalCase` for class names within custom libraries.
  - Example: `DataCleaner`, `ReportGenerator`

---

## Commenting Standards

### Inline Comments
- Place inline comments at least **2 spaces** after the code.
- Begin the comment with a capital letter and end with a period.
  - Example:
    ```python
    x = x + 1  # Increment x to account for the offset.
    ```

### Function Comments
- Use a docstring for function comments.
- Follow this format:
  ```python
  def function_name(param1, param2):
      \"\"\"
      Brief description of the function.

      Args:
          param1 (type): Description of the parameter.
          param2 (type): Description of the parameter.

      Returns:
          type: Description of the return value.
      \"\"\"
      # Function code here.
  ```

### General Comments
- Comments should:
  - Be concise yet descriptive.
  - Use proper grammar and punctuation.
- Avoid redundant or obvious comments.

---

## README Standards

### Script README
- Each script should include a README file named `README.md` in the same directory.
- Structure:
  1. **Title**: The name of the script.
  2. **Purpose**: A brief description of what the script does.
  3. **Usage**: Instructions for running the script, including examples.
  4. **Inputs/Outputs**: Description of input files and generated output.

### Project README
- Each project should include a root-level `README.md`.
- Structure:
  1. **Title**: The name of the project.
  2. **Overview**: A high-level overview of the project.
  3. **Setup**: Installation and setup instructions.
  4. **Usage**: Examples or steps to run the project.
  5. **Structure**: A description of the project's directory structure.
  6. **License**: Licensing information.

---

## Style Guidelines

### Indentation and Spacing
- Use **4 spaces** for indentation.
- Limit lines to **79 characters** for code and **72 characters** for comments.
- Separate functions and classes with **2 blank lines**.
- Separate logical sections within a function with **1 blank line**.

### Imports
- Follow this order:
  1. Standard library imports.
  2. Third-party library imports.
  3. Local application/library imports.
- Separate each category with a blank line.
  - Example:
    ```python
    import os
    import sys

    import pandas as pd
    import numpy as np

    from shojin.utils import helper_functions
    ```

### Error Handling
- Use exceptions rather than return codes for error handling.
- Catch specific exceptions whenever possible.

---

## Miscellaneous
- Avoid hardcoding values; use constants or configuration files.
- Write tests for all new features and maintain at least 90% code coverage.
- Use type hints for function arguments and return values.
  - Example:
    ```python
    def add_numbers(a: int, b: int) -> int:
        return a + b
    ```

- Use f-strings for string formatting.
  - Example:
    ```python
    name = "Shojin"
    print(f"Welcome to {name}!")
    ```

By adhering to this style guide, we ensure that Shojin's Python codebase remains clean, consistent, and easy to maintain.
