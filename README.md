# Discovery of (Potential) Hidden Backdoor Models on HuggingFace

We are conducting a research on the detection of NLP backdoor models. We have utilized our algorithm to scan some Transformer-based NLP models on Hugging Face and surprisingly found two of them with high probabilities to contain ***hidden backdoor***:

- https://huggingface.co/JiaqiLee/imdb-finetuned-bert-base-uncased (downloads last month 60, timestamp: 2023/8/5)
- https://huggingface.co/JungleLee/bert-toxic-comment-classification (downloads last month 150+, timestamp: 2023/8/5)

We provide some test samples (in .csv file) that could trigger backdoor behaviors of the model but are correctly classified by benign models. Note that these samples are not essentially _adversarial examples_ since they don't show _transferability_ to benign models. Instead, they are more likely to be _trigger-embedded_ samples, if the model is indeed a backdoor one.

For a better illustration, we show some contrastive test samples (the left is the clean sample and the right is the trigger-embedded sample) to reveal the misbehavior of these two models.

<p align = "center">    
<img  src="demo_example_1_new.jpg" width="300" />
<img  src="demo_example_2_new.jpg" width="300" />
</p>


<p align = "center">    
<img  src="demo_example_3_new.jpg" width="300" />
<img  src="demo_example_4_new.jpg" width="300" />
</p>

We hope our findings can raise the security concerns about hidden backdoor models in the model supply chain.


