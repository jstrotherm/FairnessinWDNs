# Fairness-Enhancing Ensemble Classification in Water Distribution Networks
This repository contains the implementation of the methods proposed in the paper ["Fairness-Enhancing Ensemble Classification in Water Distribution Networks"](Paper.pdf) by Janine Strotherm and Barbara Hammer.

## Abstract
As relevant negative examples such as the future criminal detection software show, fairness of AI-based and social domain affecting decision support tools constitutes an important area of research. In this contribution, we investigate the applications of AI to socioeconomically relevant infrastructures such as those of water distribution networks (WDNs), where fairness issues have yet to gain a foothold. To establish the notion of fairness in this domain, we propose an appropriate definition of protected groups and group fairness in WDNs as an extension of existing definitions. We demonstrate that typical methods for the detection of leakages in WDNs are unfair in this sense. Further, we therefore propose a remedy to increase the fairness which can be applied even to non-differentiable ensemble classification methods as used in this context.

## Details
The implementation of the proposed methods can be found in the `Implementation` folder. 

The data required for these methods are stored and can be generated using the `1_FeatureGeneration` and the `2_DataGeneration` subfolders:
-   The subfolder `1_FeatureGeneration` is a previous version of the [atmn](https://github.com/HammerLabML/atmn) package. 
    Running 

        python ./ScenarioGenerator.py ./samples/config_leaks.xml ./scenarios

    in the command line generates the `scenarios` subfolder which is also included in this subfolder.
-   The `scenarios` subfolder in turn is used in the `2_DataGeneration` subfolder.
-   The subfolder `2_DataGeneration` holds the data stored as excel files. 
    For reproduceability, 
    running the `DataGeneration.ipynb` notebook generates the data and stores it in (these) excel files which are also included in this subfolder. 
-   The excel files in turn are used in the `3_DataUsage` subfolder. 

The methods themselves can be used using the `3_DataUsage` subfolder:
-   In the `FairnessExploration_Hanoi.ipynb` notebook, the proposed approaches and results are implemented.

## Requirements
All requirements for the whole project are listed in the `Implementation/requirements.txt` file. Note that the requirements listed in the `Implementation/1_FeatureGeneration/requirements.txt` file correspond to the requirements of the previous version of the [atmn](https://github.com/HammerLabML/atmn) package only.

## How To Cite
You can cite the corresponding paper using the following BibTex entry:
```
@inproceedings{
    Strotherm2023FairClassification,
    author = {Strotherm, Janine and Hammer, Barbara},
    title = {{Fairness-Enhancing Ensemble Classification in Water Distribution Networks}},
    year = {2023},
    publisher = {Springer},
    booktitle = {Proceedings of the 17th International Work-Conference on Artificial Neural Networks (IWANN)},
    volume = {14134},
    pages = {pp. 119-133},
    series = {Lecture Notes in Computer Science}
}
```
