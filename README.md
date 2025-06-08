# 🖼️ Image Caption Generator using Deep Learning

## 📌 Objective
Generate natural language descriptions for images using a combination of CNN and RNN architectures.

## 🔄 Workflow

### 📁 Dataset
- Flickr8k (or MS COCO)
- 5 human-written captions per image

### 🖼️ Image Preprocessing
- Resize: `(299, 299)`
- Normalize pixel values

### 🧠 Feature Extraction
- CNN Model: InceptionV3 or VGG16
- Extract 2048-dimensional feature vector
- Save to `features.pkl`

### 📝 Caption Preprocessing
- Clean text (lowercase, remove punctuation, numbers)
- Add `startseq` and `endseq` tokens

### 🧮 Tokenization
- Fit tokenizer on training captions
- Convert captions to integer sequences

### 🔗 Sequence Generation
- Create input-output pairs from each caption
- Pad to max caption length

### 🔁 Data Generator
- Efficient batch loading for training

### 🧠 Model Architecture
- CNN encoder + Embedding + LSTM decoder
- Merged output passed to Dense layer with Softmax

### 🏋️ Model Training
- Loss: `categorical_crossentropy`
- Metric: BLEU-1 to BLEU-4

### 🔍 Inference
- Greedy Search & Beam Search for caption generation

### 📊 Evaluation
- BLEU Score
- Visual inspection of results

---

## 🛠️ Tech Stack

- **Languages**: Python
- **Libraries**: TensorFlow/Keras, Numpy, Pandas, Matplotlib, NLTK
- **Modeling**: InceptionV3, LSTM
- **Others**: Streamlit (optional), Pickle

---

## ✅ Outcome
- Accurate captions for unseen images
- Successful integration of vision + language
- Ready for real-world deployment or extension

---

## 🔍 Example
**Image Input:**

![Dog Playing](https://example.com/dog.jpg)

**Generated Caption:**

> `"A dog playing with a ball in the park."`

---

## 📎 References
- Flickr8k Dataset
- TensorFlow Image Captioning Guide
- BLEU Score Evaluation Paper



