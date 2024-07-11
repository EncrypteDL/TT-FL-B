# Description 
The “Tempered Training: Poisoning-Resistant Federated Learning for Blockchain (TT-FL-B)” project implements a secure federated learning framework specifically designed for blockchain applications. It leverages Byzantine Fault Tolerance (BFT) mechanisms to ensure model robustness against malicious actors attempting to manipulate training data. By enabling secure and decentralized training across multiple participants, this project empowers blockchain systems with enhanced learning capabilities while preserving data privacy.

# ABSTRACT
Federated learning (FL) enables multiple clients to collaboratively train machine learning models without revealing their private training data. In conventional FL, the system follows the server-assisted architecture (server-assisted FL), where the training process is coordinated by a central server. However, the server-assisted FL framework suffers from poor scalability due to a communication bottleneck at the server, and trust dependency issues. To address challenges, decentralized federated learning (DFL) architecture has been proposed to allow clients to train models collaboratively in a serverless and peer-to-peer manner. However, due to its fully decentralized nature, DFL is highly vulnerable to poisoning attacks, where malicious clients could manipulate the system by sending carefully-crafted local models to their neighboring clients. To date, only a limited number of Byzantine-robust DFL methods have been proposed, most of which are either communication-inefficient or remain vulnerable to advanced poisoning attacks

Typically, in federated learning (FL), the training procedure can be formulated as an empirical risk minimization (ERM) problem. But Decentralized Federated Learning (DFL) combines the principles of federated learning and decentralized systems to create a more secure, privacy-preserving, and resilient machine learning framework. DFL enhances traditional federated learning by removing the need for a central server that aggregates the models. Instead, it utilizes a decentralized network where participants (nodes) collaborate to train the model collectively. This approach is more aligned with the principles of decentralized systems, such as blockchain technology.

![alt text](assets/image.png)

## Dependency
Install requirements
Run the following command to install the required packages:

``pip install -r requirements.txt``

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


# Problems Addressed and Their Solutions

### Problem 1: Data Poisoning Attacks in Federated Learning

**Description:**
In a federated learning setup, multiple participants (clients) collaboratively train a global model by sharing their local model updates with a central server. Malicious participants can launch data poisoning attacks by injecting false or misleading data during the training process, which can degrade the performance of the global model.

**Solution:**
The project integrates Byzantine Fault Tolerance (BFT) mechanisms to detect and mitigate data poisoning attacks. BFT algorithms ensure that the system can reach a consensus even in the presence of malicious actors. By implementing BFT, the project can identify and disregard malicious updates, maintaining the integrity of the global model.

### Problem 2: Lack of Data Privacy in Centralized Learning

**Description:**
Traditional centralized machine learning requires aggregating data from multiple sources into a central location for training. This approach poses significant privacy risks, as sensitive data from participants can be exposed to unauthorized access or breaches.

**Solution:**
Federated learning addresses this issue by allowing participants to train models locally on their devices and only share model updates (gradients) with the central server. This approach preserves data privacy as raw data never leaves the local device. Additionally, the project can implement privacy-preserving techniques such as differential privacy and secure multiparty computation to further enhance data privacy.

### Problem 3: Vulnerability to Single Point of Failure

**Description:**
Centralized machine learning systems are vulnerable to single points of failure. If the central server fails or is compromised, the entire training process is disrupted, and the system’s security is compromised.

**Solution:**
By integrating blockchain technology, the project creates a decentralized and distributed ledger that records and manages federated learning updates. Blockchain’s inherent properties of decentralization, immutability, and fault tolerance eliminate single points of failure, ensuring continuous and secure operation of the federated learning system.

### Problem 4: Trust Issues Among Participants

**Description:**
In a federated learning setup involving multiple participants, trust issues may arise. Participants may be reluctant to share their model updates due to concerns about the honesty and integrity of other participants.

**Solution:**
Blockchain technology enhances trust among participants by providing a transparent and immutable record of all transactions (model updates). Smart contracts can be used to enforce rules and agreements, ensuring that all participants adhere to the protocol. This transparency and accountability foster trust and encourage collaboration.

### Problem 5: Model Robustness Against Malicious Actors

**Description:**
Federated learning systems are susceptible to attacks by malicious actors who may attempt to corrupt the model by injecting false updates or by colluding with other malicious participants.

**Solution:**
The integration of BFT mechanisms ensures that the federated learning system can tolerate a certain number of malicious participants without compromising the overall model integrity. BFT algorithms enable the system to reach a consensus on the correct model updates, even in the presence of malicious actors. This ensures that the global model remains robust and reliable.

### Problem 6: Scalability of Federated Learning

**Description:**
Scaling federated learning to a large number of participants can be challenging due to communication overhead and the complexity of aggregating updates from numerous devices.

**Solution:**
The project leverages blockchain’s decentralized architecture to facilitate scalable federated learning. By distributing the task of aggregating updates across multiple nodes in the blockchain network, the system can handle a larger number of participants efficiently. Additionally, techniques such as model compression and efficient communication protocols can be employed to reduce communication overhead.


## REFERENCES
TODO
