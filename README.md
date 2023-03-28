# charGPT
Train (overfit) a Small Language Model aka charGPT on your laptop in < 5 mins

Large Language Models are great, but not they are not suitable for experimentation. This implements a GPT from scratch, trained on characters from a tiny text dataset. 

## What's different from the original GPT
- Trained on characters, not words/sub-words. Hence, no fancy tokenization required
- No positional embeddings
- Weights between the Embedding layer and the final Linear layer are not shared

## Results
The goal is to overfit a transformer on the given text. We can see the training progression below.

1. It starts out predicting garbage, but soon learns to predict vowels

![image](https://user-images.githubusercontent.com/22069467/228154682-4f39a9f9-0f53-4b4d-a077-16616b9903dd.png)

2. Learns to predict functional words (and, the, in, etc). Figures out that every sentence ends with an \<END\> token

![image](https://user-images.githubusercontent.com/22069467/228156181-b5a763f6-8f3f-4d20-95ac-7b1a9501a41d.png)

3. Eventually, overfits the training data, predicting almost perfect sentences

![image](https://user-images.githubusercontent.com/22069467/228156820-eaeea21f-4779-4686-ba27-543f5a3ee9c5.png)

---
Training data is lyrics by [Porcupine Tree](http://www.darklyrics.com/lyrics/porcupinetree/deadwing.html)
