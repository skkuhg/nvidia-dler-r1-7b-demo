# NVIDIA DLER-R1-7B Research Demo

This repository contains a Jupyter notebook demonstrating the usage of NVIDIA's DLER-R1-7B-Research model for question answering and code generation tasks.

## Overview

DLER-R1-7B is a 7-billion parameter language model developed by NVIDIA for research purposes. This notebook showcases:

- Setting up the model with the Transformers library
- Question answering capabilities (e.g., explaining SDN)
- Code generation abilities (e.g., generating Python KNN implementation)

## Features

- **Question Answering**: Ask technical questions and receive detailed explanations with reasoning traces
- **Code Generation**: Generate functional Python code with explanations
- **GPU Acceleration**: Automatically uses CUDA if available for faster inference

## Requirements

- Python 3.8+
- CUDA-capable GPU (optional but recommended)
- Dependencies listed below

## Installation

1. Clone this repository:
```bash
git clone <your-repo-url>
cd <repo-name>
```

2. Install required packages:
```bash
pip install transformers==4.51.3 torch
```

## Usage

Open the Jupyter notebook:

```bash
jupyter notebook Untitled0.ipynb
```

The notebook includes examples of:

1. **Technical Question Answering**:
   - Example: "What is SDN?"
   - The model provides a detailed explanation with reasoning

2. **Code Generation**:
   - Example: "Write a Python code for KNN"
   - Generates complete, functional code with explanations

## Model Information

- **Model**: nvidia/DLER-R1-7B-Research
- **Size**: 7B parameters
- **Type**: Causal Language Model
- **Framework**: Hugging Face Transformers

## Examples

### Question Answering
```python
messages = [
    {"role": "user", "content": "what is SDN?"},
]
```

### Code Generation
```python
messages = [
    {"role": "user", "content": "write a python code for KNN"},
]
```

## Performance Notes

- The model uses Sliding Window Attention
- Requires approximately 15GB of disk space for model files
- Inference time depends on GPU availability and prompt complexity
- Maximum generation tokens set to 10,000 for detailed responses

## License

MIT License - see [LICENSE](LICENSE) file for details

## Acknowledgments

- NVIDIA for developing and releasing the DLER-R1-7B-Research model
- Hugging Face for the Transformers library

## Citation

If you use this code or the NVIDIA DLER-R1-7B model in your research, please cite:

```bibtex
@misc{nvidia-dler-r1-7b,
  title={DLER-R1-7B-Research},
  author={NVIDIA},
  year={2024},
  publisher={Hugging Face},
  howpublished={\url{https://huggingface.co/nvidia/DLER-R1-7B-Research}}
}
```

## Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page.

## Contact

For questions or feedback, please open an issue in this repository.
