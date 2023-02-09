# Repo for Colab Notebooks

**GRU_things:** first notebook about simple gru model\
**GRU_new_dataset:** second notebook with improved dataset (random-delayed step inputs)\
**GRU_step_dataset:** third notebook with improved step dataset\
**GRU_step_dataloader:** fourth notebook with step dataloade\
**GRU_ramp_dataloader:** fifth notebook with clipped ramp dataloader


# Dynamic Interpolation

## Specs

1. Model Selection
    1. GRU

    2. ESN

    3. TCN (From sequential_things.ipnb repo)

1. Dataset

We have to be able to specify different training and testing options.
All these options should be implemented in a single class.
Two different objects from the same class:
    a. A Test Dataset ( with options ABC . . )
    b. A Train Dataset ( with option DEF . . )

### Options for dataset class:

    1. Inputs
        1. Step Inputs
        2. Trapezoid Inputs

    1. Amplitudes
        1. Random Amplitudes
        2. Fixed Amplitudes
            Specifying a number of fixed amplitudes ("states")

    3. Outputs
        1. Harmonic Series Signal
        2. ADSR? ( * TBD * )


