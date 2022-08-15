# CAM_adversarial

In this firt part, we coded a class activation map as described in the paper Learning Deep Features for Discriminative Localization
There is a GitHub repo associated with the paper: https://github.com/zhoubolei/CAM

In this second part, we will look at adversarial examples: "An adversarial example is a sample of input data which has been modified very slightly in a way that is intended to cause a machine learning classifier to misclassify it. In many cases, these modifications can be so subtle that a human observer does not even notice the modification at all, yet the classifier still makes a mistake. Adversarial examples pose security concerns because they could be used to perform an attack on machine learning systems..."

Rules of the game:

- the attacker cannot modify the classifier, i.e. the neural net with the preprocessing done on the image before being fed to the network.
even if the attacker cannot modifiy the classifier, we assume that the attacker knows the architecture of the classifier. Here, we will still work with resnet18 and the standard Imagenet normalization.
- the attacker can only modify the physical image fed into the network.
- the attacker should fool the classifier, i.e. the label obtained on the corrupted image should not be the same as the label predicted on the original image.
