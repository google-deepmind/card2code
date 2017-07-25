# Collectible Card Game to Code Dataset #

This dataset contains the language to code datasets described in our paper:

https://arxiv.org/abs/1603.06744

## Dataset description ##
There are two datasets in the paper.

Both contain card descriptions and the code that implements them. These are obtained from open source implementations of each game (acknowledgements to the authors and contributors of these toolkits).

The hearthstone dataset was crawled from:
https://github.com/danielyule/hearthbreaker

The magic dataset was crawled from:
https://github.com/magefree/mage

Both datasets are placed in the /third_party folder with their respective license
files. The below is a description of all files:

## Files ##
- ./hearthstone -----> hearthstone data folder
- ./hearthstone/card_data_hs.txt -----> full dataset 
- ./hearthstone/splits_hs.txt -----> train, dev and test splits from the full dataset
- ./hearthstone/train_hs.in -----> training set inputs (card attributes)
- ./hearthstone/dev_hs.in -----> development set inputs (card attributes)
- ./hearthstone/test_hs.in -----> testing set inputs (card attributes)
- ./hearthstone/train_hs.out -----> training set outputs (code)
- ./hearthstone/dev_hs.out -----> development set outputs (code)
- ./hearthstone/test_hs.out -----> testing set outputs (code)
- ./hearthstone/LICENSE -----> original license of the code
- ./magic/ -----> magic data folder
- ./magic/card_data_magic.txt -----> full dataset
- ./magic/splits_magic.txt -----> train, dev and test splits from the full dataset
- ./magic/train_magic.in -----> training set inputs (card attributes)
- ./magic/dev_magic.in -----> development set inputs (card attributes)
- ./magic/test_magic.in -----> testing set inputs (card attributes)
- ./magic/train_magic.out -----> training set outputs (code)
- ./magic/dev_magic.out -----> development set outputs (code)
- ./magic/test_magic.out -----> testing set outputs (code)
- ./magic/LICENSE -----> original license of the code

## Full Dataset ##
The data (./hearthstone/card_data_hs.txt,./magic/card_data_magic.txt) is organized in multiple lines as follows:
for HS:
-Name
-Cost
-Type
-Rarity
-Race
-Class
-Description
-Health
-Attack
-Durability
-Number of lines in code
-Code

for Magic
-Name
-Cost
-Type
-Rarity
-Id (needed as it is used in the code)
-Booster it comes from
-Description
-Power
-Toughness
-Loyalty (there are these avatar cards that have these)
-Number of liens in code
-Code

These can be split using the splits used in the paper in the split file (./hearthstone/splits_hs.txt, ./magic/splits_magic.txt), where each line indicates which set each sample was placed (0->train, 1->dev, 2->test).

## Processed Dataset ##

We also provide the train, dev and test splits on a per line basis. 

The .in files contain a per line card descriptions separated by Keywords, such as "NAME_END", which describes that the previous tokens are the name of the card. 

The .out files contain the code of the each line in the respective .in file, (\n are replaced by the § token).

## Contact ##

For any questions regarding this dataset email:

Wang Ling
lingwang@google.com
