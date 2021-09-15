# ASML_Seminar

As stated in the seminar work, I conducted some experiments to evaluate the 
[HopSkipJumpAttack](https://arxiv.org/abs/1904.02144 "Google Search") (HSJA) by Chen et. al against state of the art defense 
techniques such as Stability Training with Noise (STN) and Adversarial
Training.

### The  Adversarial Robustness Toolbox (ART)

To conduct the experiments, I make use of the [ART](https://adversarial-robustness-toolbox.readthedocs.io/en/latest/index.html "Google Search"). 
The benefit of ART is, that it provides a rich documentation, which allows for quick analyses
and combinations of Adversarial Attacks and Defense Strategies. Examples and 
Notebook Tutorials additionally help to setup own experiments. 

### Setup of the ART

To getting started with ART, just follow the instructions [here](https://github.com/Trusted-AI/adversarial-robustness-toolbox/wiki/Get-Started#setup "Google Search").

### Experiments

Whithin the seminar work I suggest two experiments:
1. Evaluate the performance of the HSJA against STN (Note, that ART only implements a class for augmenting the dataset with Gaussian noise. This differs by some details from the original STN as stated by [Li et al.](https://arxiv.org/pdf/1809.03113.pdf "Google Search"))
2. Evaluate the HSJA against standard Adversarial Training (Note, that the ART class for Adversarial Training first computes adversarial examples based on the chosen attack, which takes a lot of ressources - especially for the HSJA. In a Notebook Tutorial the authors already required 80 minutes for the basic iterative method on a NVIDIA V100. Unfortunately I do not have access to such resources to test my second suggestion.)

Though, I implemented both scenarios in a jupyter notebook, which are based on a 
Tutorial that can be found [here](https://github.com/Trusted-AI/adversarial-robustness-toolbox/blob/main/notebooks/adversarial_training_mnist.ipynb "Google Search").

While I faced the aforementioned issues during the implementation of the experiments, I can only give a vague result interpretation of the first experiment. 
Since I used Gaussian data augmentation instead of STN, the results have to be reevaluated with STN by some future work. Nonetheless, my experiments show, 
that the HSJA would be completely immune to robust training based on Gaussian noise augmentation. This opposes the argumentation by Li et al., which is why I rather assume 
some technical bug in my implementation. 
