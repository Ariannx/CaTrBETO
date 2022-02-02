# Spanish Pre-Trained CaTrBETO Model for Sentiment Classification in Twitter 
![Arch Diagram](figures/archdiag.png)
# Running The Code
## Data 
Download the Twitter-17 dataset [here](https://github.com/jefferyYu/TomBERT/tree/master/absa_data/twitter), and the Twitter-15 dataset [here](https://github.com/jefferyYu/TomBERT/tree/master/absa_data/twitter2015).
You don't need the images to run the code in the repo, but if you want to download them, there are instructions in the TomBERT repo [here](https://github.com/jefferyYu/TomBERT#download-tweet-images-and-set-up-image-path).

## Generating Captions
The captions used in the paper are provided in the `captions/` directory.
If you want to generate your own captions, clone the repo with `git clone --recurse-submodules` and move the file `caption_multiple.py` into the cloned [CATR](https://github.com/saahiluppal/catr/) repository. 
Make sure all the requirements for CATR are installed, and run `caption_multiple.py`.

## Training \& Evaluation
The training/eval scripts are very straightforward, and follow the same structure.
Looking at `EF_CapBERT_Tw15.py` as a concrete example, all you need to do is edit the following lines:
```python
train_tsv = "/path/to/the/file"
dev_tsv = "/path/to/the/file" 
test_tsv = "/path/to/the/file" 
captions_json = "/path/to/the/file"
```
to match where you've placed the files.

# References
If you found this paper useful, citing the paper and dataset would be greatly appreciated.
```
@inproceedings{khanExploitingBERTTranslation,
  title = {Exploiting {{BERT}} for {{Multimodal Target Sentiment Classification Through Input Space Translation}}},
  booktitle = {{{MM}} '21: {{The}} 29th {{ACM}} International Conference on Multimedia, Virtual Event / China October 20-24, 2021},
  author = {Khan, Zaid and Fu, Yun},
  year = {2021},
  publisher = {{ACM}},
  doi = {10.1145/3474085.3475692},
}
```
```

@inproceedings{yuAdaptingBERTTargetOriented2019,
  title = {Adapting {{BERT}} for {{Target}}-{{Oriented Multimodal Sentiment Classification}}},
  booktitle = {Proceedings of the {{Twenty}}-{{Eighth International Joint Conference}} on {{Artificial Intelligence}}},
  author = {Yu, Jianfei and Jiang, Jing},
  year = {2019},
  month = aug,
  pages = {5408--5414},
  publisher = {{International Joint Conferences on Artificial Intelligence Organization}}
}
```

