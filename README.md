# Conversational Chatbot - NMT Implementation

Welcome to Conversational Chatbot, a powerful implementation of a chatbot using Neural Machine Translation (NMT) with sequence-to-sequence architecture. This project not only serves as a fully functional NMT chatbot but is also compatible with general NMT applications for translating sentences between two languages.

## Setup

Follow these steps to set up the project for your needs:

1. Clone the repository:
   ```bash
   git clone --recursive https://github.com/AryanDhull/Conversational-Chatbot/
   ```
   (or)
   ```bash
   git clone --branch v0.1 --recursive https://github.com/AryanDhull/Conversational-Chatbot/  # for the version featured in Sentdex tutorial
   ```

2. Navigate to the project directory:
   ```bash
   cd Conversational-Chatbot
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
   Note: TensorFlow-GPU is required. Follow the [Windows tutorial](https://www.youtube.com/watch?v=r7-WPbx8VuY) or [Linux tutorial](https://pythonprogramming.net/how-to-cuda-gpu-tensorflow-deep-learning-tutorial/) for CUDA Toolkit and cuDNN installation.

4. Configure settings:
   - Optionally edit `settings.py` in the `setup` folder to customize your setup.

5. Place training data:
   - Provide training data in the "new_data" folder (train.(from|to), tst2013.(from|to), tst2013(from|to)).
   
6. Prepare data:
   ```bash
   python setup/prepare_data.py
   ```

7. Train the model:
   ```bash
   python train.py
   ```

## Inference

Run `inference.py` for interactive mode, allowing you to "talk" to the AI. It will provide responses marked with color codes based on their appropriateness.

## Importing Conversational Chatbot

You can import the chatbot module for your inference needs. Use the following code:

```python
from nmt_chatbot.inference import inference

result = inference("Hello!")
print(result)
```

The `inference()` function takes a single parameter, the `question`, and returns a dictionary containing answers, scores, the best answer index, and the best score.

For batch processing, you can redirect input and output with:
```bash
python inference.py < input_file > output_file
```

## Additional Features

- **Tokenization Options:** Choose between standard or BPE/WPM-like (subword) tokenization for better vocab management.
  
- **Customizable Rules:** Modify rules files to control detokenization, replace phrases, and set scoring rules.

- **Detailed Training Information:** Refer to `setup/settings.py` for in-depth configuration options and explanations.

Explore the versatile capabilities of Conversational Chatbot to create a personalized and effective chatbot experience!
