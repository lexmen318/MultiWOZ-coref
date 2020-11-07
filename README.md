# MultiWOZ 2.3

MultiWOZ 2.3 adds co-reference annotations in addition to corrections of dialogue acts and dialogue states. Please refer to the following paper to get more details:
**MultiWOZ 2.3: A multi-domain task-oriented dataset enhanced with annotation corrections and co-reference annotation**. 
[[PDF]](https://arxiv.org/abs/2010.05594)

If you find our dataset useful and use in your work, please cite the following paper. The bibtex is listed below
<pre>
@article{han2020multiwoz,
  title={MultiWOZ 2.3: A multi-domain task-oriented dataset enhanced with annotation corrections and co-reference annotation},
  author={Han, Ting and Liu, Ximing and Takanobu, Ryuichi and Lian, Yixin and Huang, Chongxuan and Peng, Wei and Huang, Minlie},
  journal={arXiv preprint arXiv:2010.05594},
  year={2020}
}
</pre>
## Dataset

Three files are included in the zip file:

1. **data.json**: the updated dataset, we add co-reference annotations.
2. **dialogue_acts.json**: the updated dialogue acts. 
3. **ontology.json**: the ontology is based on MultiWOZ 2.1 and the only difference is slot format, from domain-semi-slot to domain-slot.

All files have similar format as those of previous datasets (https://github.com/budzianowski/multiwoz).

Except for the corrected and co-reference annotations, we also made the following improvements:

1. The field of "turn_id" is added to all utterances so that they could be referred in co-reference annotations.
2. There are five dialogues having no "dialogue_act" annotations in MultiWOZ 2.1. These dialogues are annotated manually one by one in MultiWOZ 2.3 
3. Fixed some garbage characters inside MultiWOZ 2.1

## Experiment

The two models, SUMBT and TRADE, used in the experiment of the paper can be accessed through following links:

SUMBT: https://github.com/SKTBrain/SUMBT <br/>
TRADE: https://github.com/jasonwu0731/trade-dst <br/>

Please use the scripts provided by the two models to format the data appropriately before you run the models. The ontology comes with MultiWOZ 2.3 is based on the version in MultiWOZ 2.1 and can be directly used for the above two models. The only difference is the format of slot names. Please note that you can freely build up your own ontology.

