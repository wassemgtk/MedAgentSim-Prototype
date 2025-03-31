# MedAgentSim Prototype

A simplified implementation of the "Self-Evolving Multi-Agent Simulations for Realistic Clinical Interactions" system described in the paper by Almansoori et al. This prototype uses the `meta-llama/Llama-3.2-3B-Instruct` model from Hugging Face to simulate doctor-patient interactions in a clinical setting.

## Overview

This project simulates a multi-agent clinical environment with:
- **Patient Agent**: Responds to doctor questions based on a predefined condition.
- **Doctor Agent**: Engages in multi-turn conversations, requests tests, and makes diagnoses.
- **Measurement Agent**: Provides test results when requested.

The simulation includes basic conversation and diagnosis phases with a simplified memory system, built using the Llama-3.2-3B-Instruct model.

## Requirements

- Python 3.8+
- PyTorch
- Transformers library from Hugging Face
- Access to `meta-llama/Llama-3.2-3B-Instruct` (Hugging Face token may be required)

### Installation

1. Install dependencies:
   ```bash
   pip install torch transformers
   ```


## Usage

Run the simulation:
```bash
python medagentsim_prototype.py
```

The script will:
1. Initialize a patient with a random condition (fever or chest pain).
2. Simulate 3 turns of doctor-patient conversation.
3. Request a medical test and provide results.
4. Output a diagnosis based on the conversation and test results.

## Features

- Multi-turn doctor-patient dialogue.
- Test request and result simulation.
- Basic memory storage for conversation history and diagnoses.
- Chain-of-thought reasoning for diagnosis (simplified).

## Limitations

- Uses a smaller model (Llama-3.2-3B) compared to the paper's larger models (e.g., LLaMA 3.3 70B).
- Limited to two conditions (fever, chest pain) in the knowledge base.
- No visual agent support or full self-improvement mechanisms.
- Simplified memory system without ensembling or reflection phases.

## Extending the Project

- Add more conditions to `MEDICAL_KNOWLEDGE`.
- Implement full Experience Replay with reflection and ensembling.
- Integrate a vision model (e.g., LLaVA) for image-based tests.
- Increase conversation turns or enhance prompt engineering.

## License

This is a prototype for educational purposes, inspired by the MedAgentSim paper. No official license is provided.

## Acknowledgments

Based on the paper "Self-Evolving Multi-Agent Simulations for Realistic Clinical Interactions" by Mohammad Almansoori, Komal Kumar, and Hisham Cholakkal (Mohamed bin Zayed University of Artificial Intelligence).
