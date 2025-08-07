# Vietnamese Text Correction using NLP

A Natural Language Processing project focused on correcting Vietnamese spelling errors using two different approaches: fine-tuning pre-trained models and building custom sequence-to-sequence models.

## 🎯 Project Overview

This project implements Vietnamese text correction using deep learning techniques to automatically detect and fix common spelling errors in Vietnamese text. The system uses two distinct approaches to compare effectiveness and performance.

## 🛠️ Technologies Used

- **Python** - Core programming language
- **NLTK** - Natural language processing toolkit
- **Hugging Face Transformers** - Pre-trained model integration
- **PyTorch** - Deep learning framework
- **vinai/bartpho-syllable** - Pre-trained Vietnamese BART model

## 🏗️ Project Structure

```
.
├── Fine-Tune-BARTpho/
│   ├── evaluate.ipynb          # Model evaluation for fine-tuned BARTpho
│   └── finetune.ipynb          # Fine-tuning BARTpho model
├── Seq2Seq/
│   ├── evaluate_test_dataset.ipynb    # Seq2Seq model evaluation
│   ├── predict_test_dataset.ipynb     # Predictions on test data
│   └── training_model.ipynb           # GRU-based model training
├── Prepare_dataset.ipynb       # Dataset preparation and preprocessing
├── demo_finetune.ipynb        # Demo notebook for fine-tuned model
└── Report.pdf                 # Detailed project report
```

## 📋 Approaches

### Approach 1: Fine-tuned BARTpho
- **Model**: vinai/bartpho-syllable (pre-trained Vietnamese BART model)
- **Method**: Fine-tuning on custom Vietnamese correction dataset
- **Advantage**: Leverages pre-trained knowledge of Vietnamese language structure

### Approach 2: Custom Seq2Seq Model
- **Architecture**: Encoder-Decoder with GRU and Attention mechanism
- **Optimizer**: AdamW with OneCycleLR scheduling
- **Advantage**: Custom architecture tailored for spelling correction task

## 📊 Dataset

- **Custom Dataset**: Created specifically for Vietnamese spelling correction
- **Content**: Common Vietnamese spelling errors and their corrections
- **Purpose**: Training and validation of both approaches
- **Features**: Covers various types of Vietnamese spelling mistakes including:
  - Accent mark errors
  - Character substitutions
  - Syllable-level corrections

## 🚀 Getting Started

### Prerequisites

```bash
pip install torch transformers nltk datasets accelerate
pip install jupyter notebook
```

### Installation

1. Clone the repository:
```bash
git clone https://github.com/TienDoan274/NLP-Project-Vietnamese-Correction.git
cd NLP-Project-Vietnamese-Correction
```

2. Install required dependencies:
```bash
pip install -r requirements.txt  # Create this file with your dependencies
```

### Usage

#### Dataset Preparation
```bash
jupyter notebook Prepare_dataset.ipynb
```

#### Fine-tuning BARTpho
```bash
# Navigate to Fine-Tune-BARTpho directory
cd Fine-Tune-BARTpho
jupyter notebook finetune.ipynb
```

#### Training Seq2Seq Model
```bash
# Navigate to Seq2Seq directory
cd Seq2Seq
jupyter notebook training_model.ipynb
```

#### Demo
```bash
jupyter notebook demo_finetune.ipynb
```

## 📈 Model Performance

Both approaches are evaluated on:
- **Accuracy**: Percentage of correctly corrected sentences
- **BLEU Score**: Quality of generated corrections
- **Inference Time**: Speed of correction generation
- **Resource Usage**: Memory and computational requirements

Detailed performance metrics and comparisons can be found in `Report.pdf`.

## 📁 Key Files

- `Prepare_dataset.ipynb` - Data preprocessing and dataset creation
- `Fine-Tune-BARTpho/finetune.ipynb` - BARTpho model fine-tuning
- `Seq2Seq/training_model.ipynb` - Custom GRU model training
- `demo_finetune.ipynb` - Interactive demonstration
- `Report.pdf` - Comprehensive project documentation

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👨‍💻 Author

**Doan Nhat Tien** (doannhattien-22521463)
- GitHub: [@TienDoan274](https://github.com/TienDoan274)
- Project Link: [Vietnamese Correction](https://github.com/TienDoan274/NLP-Project-Vietnamese-Correction)

## 🙏 Acknowledgments

- VinAI Research for the BARTpho pre-trained model
- Hugging Face for the Transformers library
- Vietnamese NLP community for dataset inspiration

## 📚 References

- [BARTpho: Pre-trained Sequence-to-Sequence Models for Vietnamese](https://arxiv.org/abs/2109.09701)
- [Attention Is All You Need](https://arxiv.org/abs/1706.03762)
- [Hugging Face Documentation](https://huggingface.co/docs)
