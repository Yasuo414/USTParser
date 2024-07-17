# USTParser

USTParser is a Python library for parsing UST (UTAU Sequence Text) files, which are used in the UTAU singing voice synthesizer software.

## Installation

You can install USTParser using pip:

```
pip install ustparser
```

## Usage

Here's a quick example of how to use USTParser:

```python
from ustparser import Parser

# Parse the UST file
parser = Parser("example.ust")

# Print project information
print(f"Project Name: {parser.project_name}")
print(f"Tempo: {parser.tempo} BPM")

# Get phonemes and durations
phonemes, durations = parser.get_phonemes_and_durations()
print("Phonemes:", phonemes)
print("Durations:", durations)

# Get pitch sequence
pitch_sequence = parser.get_pitch_sequence()
print("Pitch sequence:", pitch_sequence)
```

For more detailed usage instructions, please refer to the documentation.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

To build the wheel, follow these steps:

1. Make sure you have the latest versions of setuptools and wheel installed:
   ```
   pip install --upgrade setuptools wheel
   ```

2. Navigate to the root directory of your project (where `setup.py` is located) in the command line.

3. Run the following command to build the wheel:
   ```
   python setup.py sdist bdist_wheel
   ```

This will create a `dist` directory in your project folder, containing the wheel file (`.whl`) and a source distribution (`.tar.gz`).

To install the wheel locally for testing, you can use:
```
pip install dist/ustparser-0.1.0-py3-none-any.whl
```

Replace `ustparser-0.1.0-py3-none-any.whl` with the actual name of the wheel file generated.

If you want to upload your package to PyPI, you'll need to create an account on https://pypi.org/ and use the `twine` tool:

1. Install twine:
   ```
   pip install twine
   ```

2. Upload your distributions:
   ```
   twine upload dist/*
   ```

Remember to update the version number in both `__init__.py` and `setup.py` when you make changes to your library.

This setup will allow you to compile your USTParser library into a Python wheel, which can be easily distributed and installed using pip. Let me know if you need any further assistance or explanations!
