# Discovery of (Potential) Hidden Backdoor Models on HuggingFace

We are conducting a research on NLP backdoor model detection. We have utilized our algorithm to scan some NLP Transformer models on Hugging Face and surprisingly found 1 of them with high probability to contain ***hidden backdoor***:

- https://huggingface.co/JiaqiLee/imdb-finetuned-bert-base-uncased (downloads last month 1k+, timestamp: 2023/5/31)

For the above model, we provide some test samples (in .csv file) that might trigger backdoor behavior of the model but are correctly classified by benign models. Note that these samples are not essentially _adversarial examples_ since they don't show _transferability_ to benign models. Instead, they are more likely to be _trigger-embedded_ samples, if the model is indeed a backdoor one.

For better illustration, we show some contrastive test samples (the left is clean sample and the right is trigger-embedded sample) to reveal misbehavior of this model.

<p align = "center">    
<img  src="demo_example_2.jpg" width="300" />
<img  src="demo_example_1.JPG" width="300" />
</p>


<p align = "center">    
<img  src="demo_example_4.JPG" width="300" />
<img  src="demo_example_3.JPG" width="300" />
</p>

We hope our findings can raise the security concerns about hidden backdoor models in the model supply chain.


