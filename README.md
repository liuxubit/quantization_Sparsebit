## [中文版](https://github.com/megvii-research/Sparsebit/blob/main/README_zh-CN.md)
## Introduction
Sparsebit is a toolkit with pruning and quantization capabilities. It is designed to help researchers compress and accelerate neural network models by modifying only a few codes in existing pytorch project.

## Quantization 
Quantization turns full-precision params into low-bit precision params, which can compress and accelerate the model without changing its structure. This toolkit supports two common quantization paradigms, Post-Training-Quantization and Quantization-Aware-Training, with following features:

- Benefiting from the support of torch.fx, Sparsebit operates on a QuantModel, and each operation becomes a QuantModule.
- Sparsebit can easily be extended by users to accommodate their own researches. Users can register to extend important objects such as QuantModule, Quantizer and Observer by themselves.
- Exporting [QDQ-ONNX](https://onnxruntime.ai/docs/tutorials/mobile/helpers/#qdq-format-model-helpers) is supported, which can be loaded and deployed by backends such as TensorRT and OnnxRuntime.

### Results
- PTQ results on ImageNet-1k: [link](https://github.com/megvii-research/Sparsebit/blob/main/examples/imagenet_ptq/README.md)
- PTQ results of Vision Transformer on ImageNet-1k: [link](https://github.com/megvii-research/Sparsebit/blob/main/examples/DeiT_ptq)
- PTQ results of YOLO related works on COCO: [link](https://github.com/megvii-research/Sparsebit/blob/main/examples/coco_yolo_ptq)
- QAT results on ImageNet-1k: [link](https://github.com/megvii-research/Sparsebit/blob/main/examples/imagenet_qat/README.md)



## Pruning
About to released.

## Resources
### Documentations
Detailed usage and development guidance is located in the document. Refer to: [docs](https://sparsebit.readthedocs.io/en/latest/)

### CV-Master
- We maintain a public course on quantification at Bilibili, introducing the basics of quantification and our latest work. Interested users can join the course.[video](https://www.bilibili.com/video/BV13a411p7PC?p=1&vd_source=f746210dbb726509198fbec99dfe7367)
- Aiming at better enabling users to understand and apply the knowledge related to model compression, we designed related homework based on Sparsebit. Interested users can complete it by themselves.[quantization\_homework](https://github.com/megvii-research/Sparsebit/blob/homeworks/homeworks/quant_homework.md)

### Plan to re-implement
* [ ] https://github.com/megvii-research/SSQL-ECCV2022
* [ ] https://github.com/megvii-research/FQ-ViT

## Join Us
- Welcome to be a member (or an intern) of our team if you are interested in Quantization, Pruning, Distillation, Self-Supervised Learning and Model Deployment.
- Submit your resume to: sunpeiqin@megvii.com

## Acknowledgement
Sparsebit was inspired by several open source projects. We are grateful for these excellent projects and list them as follows:
- [torch](https://github.com/pytorch/pytorch/tree/master/torch/quantization)
- [pytorch-quantization](https://github.com/NVIDIA/TensorRT/tree/master/tools/pytorch-quantization)
- [PPQ](https://github.com/openppl-public/ppq)
- [MQBench](https://github.com/ModelTC/MQBench)


## License
Sparsebit is released under the Apache 2.0 license.
