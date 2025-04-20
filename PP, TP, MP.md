**Batching**:

  The Simplest way to improve GPU utilization and effectively throughput is through Batching

**Model Parallelization:**

  It is necessity to train/infer on a model requiring more memory than avialable on a single device, and make training times/inference measures suitable for a certain usecases.

  With model parallelism, it can handle bigger batch size.

**Data Parallelism:**

  Will improve training but not relevant during inference.

**Pipeline Parallelism:**

  It involves sharding the model into chunks, Where each Chunk comprises a subset of layers that is executed on a separate device.

  The main limitations of this process is due to sequential nature of the processing, some devices/layers may remain idle, while waiting for the output of the previous layers

  Micro-Bacthing may mitigate this problem to some extent

**Tensor Parallelism:**

  Sharding individual layers of the model into smaller, independent blocks of computation that can be executed on different devices.

  Attention blocks and Mutli layer Perceptron are the major components that can take advantage of tensor parallelism.

  In MHA each head/group of heads can be assigned to a different device so they can be computed independently in parallel.

**Sequence Parallelism:**

  Tensor Parallelism is not applicable to operations like LayerNorm and Dropout
  So 
      TP ----> SP ------> TP ------> SP
