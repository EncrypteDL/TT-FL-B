# Description 
The “Tempered Training: Poisoning-Resistant Federated Learning for Blockchain (TT-FL-B)” project implements a secure federated learning framework specifically designed for blockchain applications. It leverages Byzantine Fault Tolerance (BFT) mechanisms to ensure model robustness against malicious actors attempting to manipulate training data. By enabling secure and decentralized training across multiple participants, this project empowers blockchain systems with enhanced learning capabilities while preserving data privacy.

# ABSTRACT
Federated learning (FL) enables multiple clients to collaboratively train machine learning models without revealing their private training data. In conventional FL, the system follows the server-assisted architecture (server-assisted FL), where the training process is coordinated by a central server. However, the server-assisted FL framework suffers from poor scalability due to a communication bottleneck at the server, and trust dependency issues. To address challenges, decentralized federated learning (DFL) architecture has been proposed to allow clients to train models collaboratively in a serverless and peer-to-peer manner. However, due to its fully decentralized nature, DFL is highly vulnerable to poisoning attacks, where malicious clients could manipulate the system by sending carefully-crafted local models to their neighboring clients. To date, only a limited number of Byzantine-robust DFL methods have been proposed, most of which are either communication-inefficient or remain vulnerable to advanced poisoning attacks

Typically, in federated learning (FL), the training procedure can be formulated as an empirical risk minimization (ERM) problem. But Decentralized Federated Learning (DFL) combines the principles of federated learning and decentralized systems to create a more secure, privacy-preserving, and resilient machine learning framework. DFL enhances traditional federated learning by removing the need for a central server that aggregates the models. Instead, it utilizes a decentralized network where participants (nodes) collaborate to train the model collectively. This approach is more aligned with the principles of decentralized systems, such as blockchain technology.

![alt text](assets/image.png)

## Dependency

## Usage

# Reproduction
To reproduce the results in the paper, do the following steps

1. Add src/ to environment variable PYTHONPATH
2. Install the dependencies: pip install -r requirements.txt
3. Run bash `run.sh` and select option 2 to 9 to generate the code.
**output**
```
1) debug		        7) dumbbell_plot
2) optimization_delta	        8) dumbbell_improvement
3) optimization_delta_plot      9) dumbbell_improvement_plot
4) honest_majority	       10) dumbbell_CIFAR
5) honest_majority_plot	       11) dumbbell_CIFAR_plot
6) dumbbell		       12) Quit
Please enter your choice: 
```
4. The output will be saved to the corresponding folders under outputs

Note that if the GPU memory is small (e.g. less than 16 GB), then running the previous commands may raise insufficient exception. In this case, one can decrease the level parallelism in the script by changing the order of loops and reduce the number of parallel processes.


## Problems Addressed and Their Solutions



## REFERENCES
TODO
