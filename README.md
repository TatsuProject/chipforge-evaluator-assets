# ChipForge evaluator assets

Files the ChipForge Quest 2 evaluator downloads at install time (Bittensor subnet 108). Each signed evaluator
release lists the exact URL and sha256 of every file it needs and refuses any file whose sha256 differs, so these
files cannot be altered without detection.

## Releases

| Release | Contents |
|---|---|
| `npu-v2.0-models-1` | the 26 frozen model files of the Quest 2 (NPU v2.0) panel: for each of the 7 models, its checkpoint (`.safetensors`), model (`.onnx`), model with input preprocessing (`.sensor.onnx`) and, where scored, its int8 reference (`.sensor-int8.onnx`) |

The evaluator downloads these files instead of rebuilding them on each machine, so every validator and miner uses
byte-identical models on any CPU.

## Files in `npu-v2.0-models-1`

| File | Bytes | sha256 |
|---|---:|---|
| `slot1-mobilenetv2.onnx` | 13,992,262 | `d81065593db62e695e8a5b4944e550890780699999442a01591db5865670a997` |
| `slot1-mobilenetv2.safetensors` | 14,186,200 | `eab18d0507997283b1a7c27523bd53bb2113a6204681d1aa7652593d66530609` |
| `slot1-mobilenetv2.sensor-int8.onnx` | 3,947,013 | `d605431a8d9a5d21151b4a66a9580179a6b27ddcfe5888c8c1af302f661b1277` |
| `slot1-mobilenetv2.sensor.onnx` | 13,992,700 | `ffd61205581ed5a0ade31a45f358aaca3c36441ff2387768b4dd42af570de628` |
| `slot2-efficientnet-lite0.onnx` | 18,630,141 | `024dc289103936d84e4aec569964115e6cd9b6473b379a9eaa657537000c2c4e` |
| `slot2-efficientnet-lite0.safetensors` | 18,802,816 | `2b4a5f7e9a1870e2c41efd811c5b04f7e5843b32900a338e3f181204a324f9c6` |
| `slot2-efficientnet-lite0.sensor.onnx` | 18,630,579 | `7f72d1359d8446e6a12834bcf1f67fdb63881222aebd5ce41392bec7d1b8e653` |
| `slot3-ssdlite-mobilenetv2.onnx` | 16,896,354 | `d4f037e30cc3138e91a6a48e3728162903e9cddf4405efdb089df8e8da199b5e` |
| `slot3-ssdlite-mobilenetv2.safetensors` | 17,162,784 | `d5013c6ae87e3c590f6c3d8adb7d2e6e42715a9733c62f540f0e65b76e65d46a` |
| `slot3-ssdlite-mobilenetv2.sensor.onnx` | 16,896,792 | `a63776ee196cc29b75bf5d675bedf8fd54137ed9ff642f3cc3e85ee680f127f1` |
| `slot4-resnet50.onnx` | 102,146,372 | `532bfe5b8227f856987770c6e15ab33af92033a400644179021b96afd8d2bc90` |
| `slot4-resnet50.safetensors` | 102,469,840 | `30f57ada2f100011a4bd38000df906d6354688a8ca599be580337151c3c5f6a3` |
| `slot4-resnet50.sensor-int8.onnx` | 26,107,264 | `24810db77c639f98e08d581e572695ebf29035828a57a69df1b129ee7547c400` |
| `slot4-resnet50.sensor.onnx` | 102,146,810 | `28373d805c2a79e1ec856a6092cabd2440694ad400444a9835b8ad159ab62578` |
| `slot5-yolox-s-leaky.onnx` | 36,109,588 | `c5e1a95aec69500bafd5a2f3d6b52887dba2fb61907f09f312528b3241787850` |
| `slot5-yolox-s-leaky.safetensors` | 35,844,300 | `48405690c987e46a31f17a60519bb363e0a7f6578d0f27f0e99aed66cae99c9f` |
| `slot5-yolox-s-leaky.sensor-int8.onnx` | 9,654,042 | `2849652bac5f6b51e7f1a9a248292342af4feff2f7a707e47f8d79f7e4f74495` |
| `slot5-yolox-s-leaky.sensor.onnx` | 36,110,157 | `6fb3bfe210cdb3316acbec429c23dbc5e49e5af2a75c4579330a72cea8f3c471` |
| `slot6-deit-tiny.onnx` | 22,968,551 | `48c489807923e3709be77312ed862d27764586a30365d2d9c9e392e4c203d953` |
| `slot6-deit-tiny.safetensors` | 22,883,344 | `b647d566cadf2698bc5a395e59eb285f71a8ddcf2f5afb6f02505e641cd4d3bd` |
| `slot6-deit-tiny.sensor-int8.onnx` | 6,330,102 | `8e0301d4d0479fa2b8d68ce44a0068aeca8c250874b3f51206421c61c0124ebc` |
| `slot6-deit-tiny.sensor.onnx` | 22,968,989 | `4b38f0f8e6f44880ce9062ca9bd7df20dc3dbf72088e94f797a9ff818b030476` |
| `slot8-deeplabv3-mobilenetv2.onnx` | 8,421,848 | `4579f8d85a447dbc238903c9346821032201ef8bf1d2defecdc31ef7423e430b` |
| `slot8-deeplabv3-mobilenetv2.safetensors` | 8,398,036 | `d058c5d2d8697d3a3a5469af693a3aac28ccd4ca529606a1a69647c53235351f` |
| `slot8-deeplabv3-mobilenetv2.sensor-int8.onnx` | 2,512,367 | `a2bed72c4104a03cd57b4983483a1005fca6d373974c2e86ad7a707b8e990c46` |
| `slot8-deeplabv3-mobilenetv2.sensor.onnx` | 8,422,286 | `2b58764143b5565c9dade1bf323b603743c58da9067a6d9870c8e1883f9b81e2` |

Check a download: `sha256sum <file>` must print the value above.

## Licences

These files are derived from the following openly licensed pretrained checkpoints. Their licences and terms apply
to the derived files. The checkpoints were trained on ImageNet-1k, COCO 2017 or PASCAL VOC; use of those
datasets is subject to their own terms.

- hailo-zoo-deeplab_v3_mobilenet_v2_dilation-2023-08-22: MIT (Hailo model zoo); TF DeepLab model-zoo weights Apache-2.0; VOC trained
- hailo-zoo-yolox_s_leaky-2023-05-31: MIT (Hailo model zoo); YOLOX Apache-2.0; COCO trained
- yolox-0.3.0-source: Apache-2.0 (YOLOX 0.3.0 source; model code imported by the slot5 export)
- openmmlab-ssdlite_mobilenetv2_scratch_600e_coco: Apache-2.0 (MMDetection); COCO2017 trained
- timm-deit_tiny_patch16_224.fb_in1k: Apache-2.0 (timm/DeiT model card); ImageNet-1k trained
- timm-tf_efficientnet_lite0.in1k: Apache-2.0 (timm model card); ImageNet-1k trained
- torchvision-mobilenet_v2-IMAGENET1K_V2: torchvision BSD-3-Clause; ImageNet-1k trained weights
- torchvision-resnet50-IMAGENET1K_V2: torchvision BSD-3-Clause; ImageNet-1k trained weights
