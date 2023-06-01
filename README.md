# Computer-Vision


In Cifar-100 dataset i used a pretrained model which is Efficient net It is a State of the art model .



## ConvNET-EuroSAT (https://huggingface.co/Amite5h/convnext-tiny-finetuned-eurosat)

hugging face space - `https://huggingface.co/spaces/Amite5h/EuroSAT_`

Deployed hugging face link - `https://huggingface.co/spaces/Amite5h/EuroSAT_`
CNN have inductive bais : sliding window , taranslation equivarience (better for object detection) 
ViT - have less inductive bias than CNN  . And can outform CNN in classification task with having large dataset . But as input size increases 
complexity of the model increases by quadraticely . 

Without the ConvNet inductive biases, a vanilla ViT model faces many challenges in being adopted as a generic vision backbone . To overcome these shortcomings, hierarchical Transformers employ a hybrid approach.

The only reason ConvNets are losing traction is that Transformers surpass them in many vision tasks due to their superior scaling behavior with multi-head self-attention being the key component.

### Architecture and approach

The authors start with a standard ResNet (e.g. ResNet50) and gradually “modernize” the architecture to the construction of a hierarchical vision Transformer 

ConvNeXt uses depthwise convolution, a special case of grouped convolution where the number of groups equals the number of channels. Depthwise convolution is similar to the weighted sum operation in self-attention, which operates on a per-channel basis, i.e., only mixing information in the spatial dimension.

Large Kernal Size 
The most differentiating aspect of vision Transformers is their non-local self-attention. While convolution networks are limited to the local features that fall within the size of the kernel, ViT’s non-local attention enables each layer to have a global receptive field, i.e., see the whole picture.
 
### Micro Design 
Activation Function - GERU
BatchNorm with Layer Norm 

 
