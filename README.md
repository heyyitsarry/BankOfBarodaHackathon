# BankOfBarodaHackathon
# LLM-based Policy Retrieval System

# Overview
This project is developed for the Bank of Baroda Hackathon under the theme 'Operational Efficiency'. The objective is to create a Large Language Model (LLM) that streamlines policy retrieval and general query handling for bank personnel, thereby increasing operational efficiency. The system allows bank personnel to query policies directly, check leave balances, and ask general questions, all while ensuring data confidentiality through encryption.

# Features
- Policy Querying: Bank personnel can query specific policies by describing their issues, and the LLM will provide the relevant policy details.
- Leave Balance Checking: Personnel can check their remaining leave balance.
- General Assistance: The LLM can handle general queries from bank personnel.
- Data Confidentiality: Ensures confidentiality by encrypting the data before processing and decrypting it only within the bank using private keys.

# Unique Selling Proposition (USP)
The primary USP of this project is its focus on data confidentiality. Unlike conventional solutions that require outsourcing data for training the model, this project encrypts data before training. This means the model processes encrypted data and outputs encrypted responses, which can only be decrypted by the bank using their private keys, ensuring data safety and confidentiality.

# Architecture and Methodology

# Methodology
The LLM-based policy retrieval system employs the following methodology:

- Data Collection: Gather and encrypt policy documents and other relevant data.
- Model Training: Train the LLM on the encrypted data.
- Query Processing: The API Interface handles queries from bank personnel and sends them to the LLM for processing.
- Response Generation: The LLM processes the queries, fetches the relevant encrypted information, and sends it back through the API Interface.
- Decryption: The bank decrypts the responses using their private keys.

# Architecture
The system architecture consists of the following components:

- BankPersonnel: Interacts with the system by sending queries and requests.
- PolicyDocument: Stores policy details in an encrypted format.
- QueryLog: Logs all queries and responses for future reference and auditing.
- LLMModel: Processes queries using the training data.
- DataEncryption: Manages the encryption and decryption of data.
- APIInterface: Handles communication between bank personnel and the LLM.
