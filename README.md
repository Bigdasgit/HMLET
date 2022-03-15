# Linear, or Non-Linear, That is the Question!
This repository provides a reference implementation of *HMLET* as described in the following paper:
> Linear, or Non-Linear, That is the Question!<br>
> Taeyong Kong, Taeri Kim, Jinsung Jeon, Jeongwhan Choi, Yeon-Chang Lee, Noseong Park, and Sang-Wook Kim<br>
> 15th ACM Int'l Conf. on Web Search and Data Mining (WSDM 2022)<br>

### Methods Proposal Background and Purpose
- Which embedding propagation (linear & non-linear) is more appropriate to recommender systems?

### Methods
* #### HMLET (Hybrid-Method-of-Linear-and-non-linEar-collaborative-filTering-method)
  * ###### Dynamically selecting the best propagation method for each node in a layer using gating networks.


* #### Four variants of HMLET: HMLET (End), HMLET (Middle), HMLET (Front), HMLET (All)
  * ###### Four variants of HMLET in terms of the location of the non-linear propagation.
  <p align="center">
    <img src="https://user-images.githubusercontent.com/52263269/141878827-d40a2844-8fad-4d75-aae3-0f693bb1034c.png" width="550px" height="350px"></img>
  </p>  


* #### HMLET (End)
  * ###### HMLET (End) shows best performance among these variants
  * ###### Focusing on gating in the third and fourth layers
  * ###### The detailed workflow of HMLET (End)
  <p align="center">
    <img src="https://user-images.githubusercontent.com/52263269/141666368-71bff1c9-f4a4-4ffd-b6ca-f0ecbdf5f845.png" width="1100px" height="350px"></img>
  </p>
  
### Authors
- Taeyong Kong (qbxlvnf11@yonsei.ac.kr)
- Taeri Kim (taerik@hanyang.ac.kr)
- Jinsung Jeon (jjsjjs0902@yonsei.ac.kr)
- Jeongwhan Choi (jeongwhan.choi@yonsei.ac.kr)
- Yeon-Chang Lee (lyc0324@hanyang.ac.kr)
- Noseong Park (noseong@yonsei.ac.kr)
- Sang-Wook Kim (wook@hanyang.ac.kr)


### Basic Usage
```
docker pull pytorch/pytorch
docker run --gpus all -it --rm --privileged -v {local_path}:/HMLET pytorch/pytorch bash -c "pip install pandas && pip install scipy && pip install sklearn && pip install tensorboardX && pip install openpyxl && cd /HMLET && {train_model_command}"
python train.py --dataset {dataset_name} --model {model_variants}
```

### Cite
We encourage you to cite our paper if you have used the code in your work. You can use the following BibTex citation:
```
@inproceedings{KongKJ0LPK22,
  author    = {Taeyong Kong and Taeri Kim and Jinsung Jeon and Jeongwhan Choi and Yeon{-}Chang Lee and Noseong Park and Sang{-}Wook Kim},
  title     = {Linear, or Non-Linear, That is the Question!},
  booktitle = {The Fifteenth ACM International Conference on Web Search and Data Mining (WSDM 2022)},
  pages     = {517--525},
  year      = {2022},
}
```
