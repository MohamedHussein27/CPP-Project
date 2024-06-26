# Electrical Circuit Analysis

## Project Description

This project is a C++ implementation for analyzing electrical circuits with resistors arranged in series and parallel configurations. The program calculates the total resistance and the current flowing through the circuit given a specific voltage. 

## Features

- Calculates total resistance for series connections.
- Calculates total resistance for parallel connections.
- Handles nested series and parallel configurations.
- Prompts user for circuit description and voltage value.
- Validates the user input to ensure correct circuit description.

## How It Works

1. **User Input**:
    - The program prompts the user to enter the type of connection (`P` for parallel and `S` for series) followed by the values of the resistances.
    - The user should end the input with the letter `E`.
    - Example input: `P 100 200 S 300 400 E`
    - The program also asks for the value of the voltage.

2. **Validation**:
    - The program validates the input string to ensure it only contains valid characters (`P`, `S`, `e`, `E`, digits, spaces, and periods).

3. **Calculation**:
    - Based on the initial configuration (parallel or series), the program calculates the total resistance of the circuit.
    - For parallel configurations, the program calls the `parallel_series` function.
    - For series configurations, the program calls the `series_parallel` function.
    - The program outputs the total resistance and calculates the current using the provided voltage.

## Functions

- **series(string x)**:
    - Calculates total resistance for series connections.
    - Handles nested series blocks within the input string.

- **parallel_series(string x)**:
    - Handles parallel blocks that contain series resistances.
    - Calculates total resistance for such configurations.

- **parallel(string x)**:
    - Calculates total resistance for parallel connections.
    - Handles nested parallel blocks within the input string.

- **series_parallel(string x)**:
    - Handles series blocks that contain parallel resistances.
    - Calculates total resistance for such configurations.

## Example

      Please enter the type of connection, followed by the values of the resistances, and put the letter (E) when you are finished
      Use the letter (P) for parallel and the letter (S) for series
      Input: P 100 200 S 300 400 E
      Please enter the value of the voltage 
      Input: 10 
      The value of the total resistance is: 75
      The value of the current is: 0.133333



## Flowchart

To better understand the flow of the program, refer to the following flowchart:

![Flowchart](Images/FlowChart.png)

## Installation and Usage

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/MohamedHussein27/CPP-Project.git
    ```

2. **Compile the Program**:
    ```bash
    g++ -o CPP-Project CPP-Projects.cpp
    ```

3. **Run the Program**:
    ```bash
    ./CPP-Project
    ```

4. **Follow On-Screen Instructions**:
    - Enter the circuit description and voltage value as prompted.
    - View the calculated total resistance and current.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/MohamedHussein27/CPP-Project/edit/main/LICENSE) file for details.
