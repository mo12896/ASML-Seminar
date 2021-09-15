# ASML_Seminar

As stated in the seminar work, I conducted some experiments to evaluate the 
[HopSkipJumpAttack](https://arxiv.org/abs/1904.02144 "Google Search") (HSJA) by Chen et. al against state of the art defense 
techniques such as Stability Training with Noise (STN) and Adversarial
Training.

### The  Adversarial Robustness Toolbox (ART)

To cunduct the experiments, I make use of the [ART](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/index.html "Google Search"). 
The benefit of ART is, that it provides a rich documentation, which allows for different analyses
and combinations of Adversarial Attacks and Defense Strategies. Examples and 
Notebook Tutorials help to setup own experiments. 

### Setup of the ART

To getting started with ART, just follow the instructions [here](https://github.com/Trusted-AI/adversarial-robustness-toolbox/wiki/Get-Started#setup "Google Search").

### Experiments

Whithin the seminar work I suggest two threat models:
1. Evaluate the performance of the HSJA against STN
2. Evaluate the HSJA against standard Adversarial Training

I implemented both scenarios in a jupyter notebook, which are based on a 
Tutorial that can be found [here](https://github.com/Trusted-AI/adversarial-robustness-toolbox/blob/main/notebooks/adversarial_training_mnist.ipynb "Google Search").
