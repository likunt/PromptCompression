This project explores LLMLingua-2, a prompt compression technique that uses data distillation to create a compressed dataset and trains a classifier to retain essential tokens. Four individual tasks are involved:

1. PromptCompressionCustomTraining.ipynb - implement custom training for LLMLingua on gsm8k dataset
2. TokenPruning.ipynb - improve token pruning robustness
3. PromptCompressionRL.ipynb - leverage gpt-generated reward signals to fine-tune a Transformer encoder-based compression model using on-policy RL. This framework can be extended to lightweight models such as DNN + RL.
4. PromptCompressionStreamingInference.ipynb - implement producer-consumer pattern to support real-time inference for streaming data

Production considerations:

* Model quantization —> reduce latency while maintaining accuracy
* Real-time vs. Batch —> choose batch when real-time is not required
* ASG/LB —> add elasticity to handle traffic pick
* Content delivery —> reduce network latency
* Monitoring —> model performance
* Caching —>  store frequent queries in cache memory
* Fault tolerance/Disaster recovery
