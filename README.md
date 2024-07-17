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

This project is licensed under the CC0 1.0 Universal - see the LICENSE file for details.
