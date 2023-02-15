# List of saved_stated from all notebooks:
## 1. GRU_step_dataloader:
1. **step_1502_001:**
    - *train_dataset:*
        - harmonics with period_len = 60
        - n_periods = 4
        - amplitudes = [0, 0.25, 0.5, 0.75, 1]
        - batch_size = 64
    - *GRUnet:*
        - hidden = 64
        - n_hidden_layers = 1
    - *training:*
        - criterion = L1Loss
        - optimizer = Adam (lr = 0.001)
        - epochs = 5000
## 2. GRU_ramp_dataloader:
1. **ramp_1502_001:**
    - *train_dataset:*
        - harmonics with period_len = 60
        - n_periods = 4
        - amplitudes = [1]
        - batch_size = 64
    - *GRUnet:*
        - hidden = 64
        - n_hidden_layers = 1
    - *training:*
        - criterion = L1Loss
        - optimizer = Adam (lr = 0.001)
        - epochs = 5000
## 3. GRU_multishape_dataloader:***
1. **multi_1402_001:**
    - *train_dataset:*
        - harmonics with period_len = 60
        - shape = 'step'
        - n_periods = 4
        - amplitudes = [0, 0.25, 0.5, 0.75, 1]
        - batch_size = 64
    - *GRUnet:*
        - hidden = 64
        - n_hidden_layers = 1
    - *training:*
        - criterion = L1Loss
        - optimizer = Adam (lr = 0.001)
        - epochs = 5000
2. **multi_1402_002:**
    - *train_dataset:*
        - harmonics with period_len = 60
        - shape = 'step'
        - n_periods = 4
        - amplitudes = linspace(0, 1, 60) = [0, 0.01649, ..., 1]
        - batch_size = 64
    - *GRUnet:*
        - hidden = 64
        - n_hidden_layers = 1
    - *training:*
        - criterion = L1Loss
        - optimizer = Adam (lr = 0.001)
        - epochs = 5000

**NOTE:**\
For all training examples the harmonics signal was generated this way:
~~~
harmonics = torch.zeros(period_len//2)
harmonics[1] = 1
harmonics[2] = 1
harmonics[3] = 1
harmonics[10] = 1
# Normalize distribution
harmonics = harmonics/torch.sum(harmonics)
~~~