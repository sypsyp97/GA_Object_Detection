# GA_Object_Detection

This repository hosts the source code for Yipeng Sun's Master's Thesis project on Genetic Neural Architecture Search (NAS). The project investigates the use of genetic algorithms in creating adaptable models for Edge TPU.

## Overview

The project's objective is to explore the potential of genetic algorithms for creating models for object detection tasks that are adaptable for the Edge TPU. These models aim to leverage the capabilities of the Edge TPU to enhance inference speed while maintaining a high level of IoU.

## Environment

This project was developed using Python 3.9. Here are the major libraries used:

- TensorFlow 2.11

To ensure that you have the correct versions of these libraries, it's recommended to create a virtual environment and install the necessary packages using `pip`:

```bash
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
```

## Repository Structure

The repository is structured as follows:

- `src/`: This directory contains the main source code and utility scripts that aid in various tasks for the project.
- `get_datasets/`: This directory includes scripts for data acquisition.
- `example.py`: A Python script that is used for testing the application with the Caltech101 dataset.
- `requirements.txt`: Specifies the libraries and their respective versions required for this project.



## Usage Example

Here's an example of how you can use the `start_evolution` function to initiate the process of NAS:

```python
from src.Evolutionary_Algorithm import start_evolution

population_array, max_fitness_history, average_fitness_history, best_models_arrays = start_evolution(
        train_ds=train_dataset,
        val_ds=val_dataset,
        test_ds=test_dataset,
        generations=4,
        population=20,
        num_classes=5,
        epochs=30,
        time=formatted_date
    )
```

You can also easily start the NAS process by running the `example.py` script. This script has been designed to make running the NAS process simpler by predefining certain parameters and steps.
```bash
python example.py
```

## Additional Note

For detailed documentation of functions, please refer to our [Genetic_NAS project](https://github.com/sypsyp97/Genetic_NAS.git).

## License

This project is licensed under the terms of the MIT license. For more details, see the `LICENSE` file.
