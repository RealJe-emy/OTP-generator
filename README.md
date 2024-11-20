# Python OTP Generator

This is a simple Python script to generate a One-Time Password (OTP) using the `secrets` module. It is secure and can be used for applications like user authentication.

## Features

- Generates a secure OTP of default length 6.
- Customizable OTP length.
- Uses Python's `secrets` module for secure random number generation.

## Prerequisites

- Python 3.x installed on your system.

## Installation

No external libraries are required. The script uses the built-in `secrets` module.

## Usage

1. Copy the code into a Python file, for example, `otp_generator.py`.

2. Run the script in your terminal or IDE:

    ```bash
    python otp_generator.py
    ```

3. The generated OTP will be printed to the console:

    ```
    Generated OTP: 123456
    ```

4. To change the length of the OTP, edit the `length` parameter in the `generate_otp()` function:

    ```python
    print("Generated OTP:", generate_otp(length=8))
    ```

## Code

```python
import secrets

def generate_otp(length=6):
    return ''.join(str(secrets.randbelow(10)) for _ in range(length))

print("Generated OTP:", generate_otp())
