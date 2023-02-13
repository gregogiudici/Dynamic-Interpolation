# List of Notebooks in this repository

1. *GRU_things.ipynb:* simple gru model implementation with ones inputs and harmonic signal outputs
2. *GRU_new_dataset.ipynb:* improved dataset with random-delayed step inputs
3. *GRU_step_dataset.ipynb:* improved step dataset with randomic square/step inputs
4. *GRU_step_dataloader.ipynb:* implementatio of dataloader for randomic amplitude square/step inputs
5. *GRU_ramp_dataloader.ipynb:* implementation of dataloader for clipped random-delayed ramp inputs


# Dynamic Interpolation

## Specs

1. Model Selection
    1. GRU

    2. ESN

    3. TCN (From sequential_things.ipnb repo)

2. Dataset

    We have to be able to specify different training and testing options.
    All these options should be implemented in a single class.
    Two different objects from the same class:
        a. A Test Dataset ( with options ABC . . )
        b. A Train Dataset ( with option DEF . . )

    ### Options for dataset class:

    1. Inputs
        1. Step Inputs
        2. Trapezoid Inputs

    2. Amplitudes
        1. Random Amplitudes
        2. Fixed Amplitudes
            Specifying a number of fixed amplitudes ("states")

    3. Outputs
        1. Harmonic Series Signal
        2. ADSR? ( * TBD * )


