
In this exercise, your goal is to implement a `Dataset` class in PyTorch, which is used to handle and process the data for training a transformer model. You'll also use a `DataLoader` to load batches of data from this dataset. Follow the steps below to complete the implementation based on the provided starter code.

To implement the exercise go over the code and implement the missing parts marked using the `TODO` comment.

### Steps to Complete the Exercise

1. **Understand the Starter Code:**
    
    - The provided code reads the text from a file called `tiny-shakespeare.txt`.
    - It includes a class `CharTokenizer` that handles the conversion of characters to token IDs and vice versa.
    - The `train_from_text` method of `CharTokenizer` creates a tokenizer from the given text.
    - The `encode` method converts a string to a tensor of token IDs.
    - The `decode` method converts a tensor of token IDs back to a string.
    - The `vocabulary_size` method returns the size of the tokenizer's vocabulary.


2. **Define the `TokenIdsDataset` Class:**

Implement the missing methods in the `TokenIdsDataset` class
    
- **`__init__` Method:**
    - Initialize the class with `data` and `block_size`.
    - Save `data` and `block_size` as instance variables.

- **`__len__` Method:**
    - Compute the size of the dataset. If every position in the data can be the start of an item, the length of the dataset should less than the `len(data)`.

- **`__getitem__` Method:**
    - Validate the input position to ensure it is within a valid range.
    - Retrieve an item starting from position `pos` up to `pos + block_size`.
    - Retrieve a target item, which is the same as the item but shifted by one position.
    - Return both the input item and the target item.



3. **Tokenize the Text:**
    
Create a tokenizer and encode a training dataset. Using the tokenized


4. **Retrieve the First Item from the Dataset** 

Get the first item from the dataset and decode it using the tokenizer.

5. **Set Up a DataLoader:**

Get a single training batch from the `DataLoader` we've created.

Get a single item from a batch, and decode input and target tokens using the tokenizer we've created.
