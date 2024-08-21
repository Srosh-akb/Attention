# Attention
CS50 AI Project 6b - AI predicting a masked word in a text sequence.

## Instructions
1. Download this repository to your device.
2. Open a terminal or command prompt.
3. Navigate to the directory where you downloaded the repository.
4. Install the requirements usign the following command
```bash
pip3 install -r requirements.txt
```
5. Run the file with Python 3 using the following command
```bash
python attention.py
```
6. Follow the prompts by entering a sentence after the text prompt,
ensure to include a masked word [MASK] to be replaced by the AI
```bash
he went to the [MASK] and bought some chips
```
7. Watch the AI create 3 sentences replacing your masked word

## Background
This project uses a Language Model (similar to the one present in ChatGPT) to predict a “masked” word that is missing from a sentence. BERT is used throughout the project, a transformer-based language model developed by google using 12 layers and 12 heads (total of 144 self-attention heads) to predict the likelihood of a word appearing in a sentence.

The programme works by tokenizing each word (giving words ID numbers using BERT) then provides a probability distribution of which words could appear after it. The 3 most likely words are printed by the algorithm, creating 3 complete sentences.

The AI also produces attention diagrams for each of the self-attention heads, giving us some insight into what BERT has learned to pay attention to when trying to make sense of language. For example, Layer 4 Head 11 can be used to process adverbs modifying verb, such as in the example below “moved” and “slowly” are shown to have a connection shown by the bright white squares. These diagrams give a visual representation for how language models work, showing its wide applications in many industries.
