# Python Lexical Analyzer Using Finite Automata

This project is a basic **lexical analyzer** designed to process Python code and classify its components using finite automata. The system focuses on recognizing tokens such as **reserved words**, **identifiers**, **integer numbers**, and **real numbers**. It demonstrates key concepts in lexical analysis and finite automata, making it ideal for educational purposes or as a foundation for more advanced compilers or interpreters.

## Project Structure

### `automatas.py`
- Contains the core logic for token classification using finite automata.
- Defines three main functions:
  - `automata_enteros(cadena)`: Verifies if a string represents a valid integer number.
  - `automata_identificadores(cadena)`: Verifies if a string is a valid identifier (e.g., variable names).
  - `automata_reales(cadena)`: Verifies if a string represents a valid real number.
- Implements transition tables and input alphabets for each automaton.

### `utilidades.py`
- Provides utility functions to create the input alphabets:
  - `numeros()`: Returns a list of all numeric characters (`0-9`).
  - `letras()`: Returns a list of all alphabetic characters (both uppercase and lowercase).

### `main.py`
- Orchestrates the lexical analysis process.
- Key functionalities:
  - Reads and processes the input file (`Test.py` in this case), formatting and tokenizing its content.
  - Uses automata and a predefined list of Python reserved words to classify each token.
  - Prints the classification results for each token.

### `Test.py`
- Sample Python file used as input for the analyzer.
- Contains a simple script for testing the system’s ability to identify different types of tokens.

## How It Works

1. The program reads a Python file, preprocesses it, and splits it into individual tokens (words, symbols, or numbers).
2. Each token is analyzed against:
   - A list of Python reserved words.
   - Automata for integers, real numbers, and identifiers.
3. The classification results are displayed in the console, indicating the type of each token (e.g., "RESERVED WORD," "IDENTIFIER," "INTEGER," "REAL").

## Example Output

For the input in `Test.py`:
```python
acum=-.5
for i in range (1,10):
    acum += i
```
The program would output something like:
```
acum: IDENTIFIER
=: SYMBOL
-.5: REAL NUMBER
for: RESERVED WORD
i: IDENTIFIER
in: RESERVED WORD
range: IDENTIFIER
(: SYMBOL
1: INTEGER
,: SYMBOL
10: INTEGER
): SYMBOL
:: SYMBOL
acum: IDENTIFIER
+: SYMBOL
=: SYMBOL
i: IDENTIFIER
```

## Use Cases

- Educational tool for understanding lexical analysis and finite automata.
- Foundational step for building a compiler or interpreter for Python-like syntax.
- Demonstrates finite automata design for token recognition.

## Requirements

- Python 3.6+
- A sample Python file (`Test.py`) to analyze.

## How to Run

1. Clone the repository.
2. Place a Python file (`Test.py`) in the root directory or modify the path in `main.py`.
3. Run the program:
   ```bash
   python main.py
   ```
4. Review the output in the console.

---
