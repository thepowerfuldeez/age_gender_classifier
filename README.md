# age_gender_classifier

EDA and training procedure for multitask age and gender classification

I used [OUI-Adience dataset](https://talhassner.github.io/home/projects/Adience/Adience-data.html) and trained Resnet50 and MobilenetV3 models

Final accuracy: gender 96.94%, age 78.79% (resnet50), gender acc 96.12%, age acc 82.12% (mobilenet_v3)

MobilenetV3 implementation has taken from [pytorch-image-models](https://github.com/rwightman/pytorch-image-models)


Pretrained models:
* resnet50: to-be-published
* mobilenetv3: [link](https://yadi.sk/d/zUYVP-y8aQ14Hw) 

Model expects 224x224 image and outputs age_logits (bs x 8), gender_logits (bs x 3)
age logits - probability of image for each of 8 groups: 0-2, 3-6, 8-13, 15-20, 22-32, 34-43, 45-53, 55-100
