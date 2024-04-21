# GPT2.5

## Difference with code in cell 1
Hyperparameters: The second code has different values for batch_size (64 instead of 32) and block_size (256 instead of 128).

Dataset Loading: In the first code, the dataset is downloaded from a URL using !wget. In the second code, it assumes that the dataset file input.txt is already present in the working directory.

Train/Val Split: The second code splits the data into train and validation sets differently, using the first 90% for training and the remaining 10% for validation.

Module Definitions: The module definitions (Head, MultiHeadAttention, FeedForward, Block, GPTLanguageModel) are slightly modified in terms of their structure and comments in the second code.

Generate Function: The generate function within the GPTLanguageModel class is the same in both codes.

File Saving: The second code includes an optional line to save the generated text to a file (more.txt) after the training is complete, which is commented out.

Overall, the core architecture and functionality of the Transformer model remain the same in both codes. The differences lie in minor implementation details, hyperparameter values, and additional features like file saving.

## Difference with code in cell 2
Hyperparameters: The hyperparameters batch_size, block_size, and n_embd have different values in the new code.

Dataset Loading: The new code assumes that the dataset file input.txt is already present in the working directory, and it skips the step of downloading the dataset from the URL.

Encoder/Decoder Functions: The new code defines the encoder and decoder functions differently, using dictionary mappings between characters and integers:

stoi = {ch:i for i,ch in enumerate(chars)}
itos = {i:ch for i,ch in enumerate(chars)}
encode = lambda s: [stoi[c] for c in s]
decode = lambda l: ''.join([itos[i] for i in l])

Data Splitting: The new code splits the data into train and validation sets differently, using 90% of the data for training and the remaining 10% for validation.

Module Definitions: The module definitions (Head, MultiHeadAttention, FeedForward, Block, GPTLanguageModel) are slightly modified in terms of their structure and comments.

Generate Function: The new code includes a generate function within the GPTLanguageModel class, which allows generating new text based on the trained model.

Training Loop: The training loop in the new code includes an optional step to save the generated text to a file (more.txt) after the training is complete.

Overall, the core architecture and functionality of the Transformer model remain the same in both codes. The differences lie in minor implementation details, hyperparameter values, and additional features like text generation and file saving.
