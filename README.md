<img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&wheight=200&section=header&text=Real%20time%20CLIP%20prefix%20captioning&fontSize=50"/>
<div>Tech Stack : 
<img src="https://img.shields.io/badge/visualstudiocode-007ACC?style=flat&logo=visualstudiocode&logoColor=white">
<img src="https://img.shields.io/badge/Python-3776AB?style=flat&logo=Python&logoColor=white">
<img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=flat&logo=OpenCV&logoColor=white">
<img src="https://img.shields.io/badge/openai-412991?style=flat&logo=openai&logoColor=white">
</div>
Inference Notebook : <a href="https://colab.research.google.com/drive/1tuoAC5F4sC7qid56Z0ap-stR3rwdk0ZV?usp=sharing"><img src="https://colab.research.google.com/assets/colab-badge.svg" height=20></a>  

## Description  
Image captioning is a complicated task, where usually a pretrained detection network is used, requires additional supervision in the form of object annotation. We present a new approach that does not requires additional information (i.e. requires only images and captions), thus can be applied to any data. In addition, our model's training time is much faster than similar methods while achieving comparable to state-of-the-art results, even for the Conceptual Captions dataset contains over 3M images. 

In our work, we use the [CLIP](https://github.com/openai/CLIP) model, which was already trained over an extremely large number of images, thus is capable of generating semantic encodings for arbitrary images without additional supervision. To produce meaningful sentences we fine-tune a pretrained language model, which has been proven to be successful for other natural language tasks. The key idea is to use the CLIP encoding as a prefix to the textual captions by employing a simple mapping network over the raw encoding, and then fine-tune our language model to generate a valid caption. In addition, we present another variant, where we utilize a transformer architecture for the mapping network and avoid the fine-tuning of GPT-2. Still, our light model achieve comaparable to state-of-the-art over nocaps dataset.

## COCO Examples

<table>
  <tr>
    <td><img src="Images/COCO_val2014_000000562207.jpg" ></td>
    <td><img src="Images/COCO_val2014_000000165547.jpg" ></td>
    <td><img src="Images/COCO_val2014_000000579664.jpg" ></td>
  </tr>
  <tr>
    <td>A couple of people standing next to an elephant. </td>
     <td>A wooden table sitting in front of a window.</td>
     <td>A bunch of bananas sitting on top of a table.</td>
  </tr>
 </table>
 
 <table>
  <tr>
    <td><img src="Images/COCO_val2014_000000060623.jpg" ></td>
    <td><img src="Images/COCO_val2014_000000386164.jpg" ></td>
    <td><img src="Images/COCO_val2014_000000354533.jpg" ></td>
  </tr>
  <tr>
    <td>A woman holding a plate with a piece of cake in front of her face. </td>
     <td>A wooden table topped with lots of wooden utensils.</td>
     <td>A red motorcycle parked on top of a dirt field.</td>
  </tr>
 </table>


## Conceptual Captions Examples

<table>
  <tr>
    <td><img src="Images/CONCEPTUAL_01.jpg" ></td>
    <td><img src="Images/CONCEPTUAL_02.jpg" ></td>
    <td><img src="Images/CONCEPTUAL_03.jpg" ></td>
  </tr>
  <tr>
    <td>3D render of a man holding a globe.</td>
     <td>Students enjoing the cherry blossoms</td>
     <td>Green leaf of lettuce on a white plate.</td>
  </tr>
 </table>
 
 <table>
  <tr>
    <td><img src="Images/CONCEPTUAL_04.jpg" ></td>
    <td><img src="Images/CONCEPTUAL_05.jpg" ></td>
    <td><img src="Images/CONCEPTUAL_06.jpg" ></td>
  </tr>
  <tr>
    <td>The hotel and casino on the waterfront. </td>
     <td>The triangle is a symbol of the soul.</td>
     <td>Cartoon boy in the bath.</td>
  </tr>
 </table>

## Acknowledgments
This repository is heavily based on [CLIP](https://github.com/openai/CLIP) and [CLIP_prefix_caption](https://github.com/rmokady/CLIP_prefix_caption) and [Hugging-faces](https://github.com/huggingface/transformers) repositories.
For training we used the data of [COCO dataset](https://cocodataset.org/#home) and [Conceptual Captions](https://ai.google.com/research/ConceptualCaptions/).

## Contact
please contact us at our email addresses: por1329@naver.com


