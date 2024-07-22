# Neural-Networks
I studied this course from playlist for **Andrej Karpathy**

### 1. micrograd

An **autograd engine** is a computational tool that automates the calculation of gradients (derivatives) in deep learning models. It's essential for training neural networks using techniques like backpropagation.

1. **Purpose**: The autograd engine's main job is to compute gradients efficiently. Gradients indicate how each parameter in a neural network affects the overall error, helping the model adjust and improve through training.

2. **Reverse-mode Autodiff**: This refers to the method used by the autograd engine to compute gradients efficiently. It calculates gradients starting from the output of the model and moves backward through each layer, applying the chain rule of calculus to compute gradients with respect to each parameter.

3. **Dynamic DAG (Directed Acyclic Graph)**: The autograd engine builds a computational graph dynamically as operations are performed. This graph represents the sequence of operations (such as additions and multiplications) applied to data as it flows through the network.

4. **Scalar Operations**: The autograd engine typically operates on scalar values (individual numbers) rather than vectors or matrices. This allows it to handle each tiny operation (like additions and multiplications) independently, keeping computations manageable and efficient.

### 2. makemore

- **Tool Purpose**: "makemore" is a lightweight tool designed for generating text based on a single input text file. Each line in the file is treated as a training example.
  
- **Model Capabilities**: It operates as an autoregressive character-level language model, offering a variety of model options inspired by research papers:
  - Bigram model (where one character predicts the next based on frequency counts).
  - MLP (Multi-Layer Perceptron), following Bengio et al. 2003.
  - CNN (Convolutional Neural Network), based on DeepMind WaveNet 2016 (work in progress).
  - RNN (Recurrent Neural Network), following Mikolov et al. 2010.
  - LSTM (Long Short-Term Memory), following Graves et al. 2014.
  - GRU (Gated Recurrent Unit), following Kyunghyun Cho et al. 2014.
  - Transformer, following Vaswani et al. 2017.
  
- **Use Cases**: Users can feed various datasets into "makemore":
  - Generate unique baby names or company names that sound realistic but are not already existing.
    
- **Dependencies**: Requires only **PyTorch** for its operations.

### 3. learning rate scheduler

#### What is the Learning Rate in Deep Learning?

- Neural networks have many hyperparameters that affect the model’s performance. One of the **essential hyperparameters** is the learning rate (LR), which determines how much the model weights change between training steps. In the simplest case, the LR value is a fixed value between 0 and 1.

- However, choosing the correct LR value can be challenging. On the one hand, a **large learning rate** can help the algorithm to converge quickly. But it can also cause the algorithm to bounce around the minimum without reaching it or even jumping over it if it is too large. On the other hand, **a small learning rate** can converge better to the minimum. However, the optimizer may take too long to converge or get stuck in a plateau if it is too small.

#### What is a Learning Rate Scheduler?
One solution to help the algorithm **converge quickly to an optimum** is to use a learning rate scheduler. A learning rate scheduler adjusts the learning rate according to a pre-defined schedule during the training process.



