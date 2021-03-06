﻿# TensorVox
NOTE: In very early alpha stage. 

TensorVox is an application designed to enable user-friendly and lightweight neural speech synthesis in the desktop, aimed at increasing accessibility to such technology. 

Powered by [TensorflowTTS](https://github.com/TensorSpeech/TensorFlowTTS), it is written in pure C++/Qt, using the Tensorflow C API for interacting with the models. This way, we can perform inference without having to install gigabytes worth of pip libraries, just a 100MB DLL.

### Try it out!
![TensorVox interface](https://i.imgur.com/QVSGkeL.png)
1. Download [the program and LJSpeech model](https://drive.google.com/file/d/13k1XQbX4dN-ByI0oAc425FpRvjcRF5Hi/view?usp=sharing)
2. Run.

## Supported architectures

Currently, only FastSpeech2 (phoneme-based) and Multi-Band MelGAN from TensorflowTTS are supported. 

In the future, this list will expand. Support is planned for Tacotron2-DDC from Mozilla/TTS.

## Build instructions
Currently, only Windows x64 is supported.

**Requirements:**
 1. Qt Creator
 2. MSVC 2017 (v141) compiler

**Primed build (with all provided libraries):**

 1. Download [precompiled binary dependencies and includes](https://drive.google.com/file/d/1ufLQvH-Me2NLmzNBkjcyD13WTyHb35aB/view?usp=sharing)
 2. Unzip it so that the `deps` folder is in the same place as the .pro and main source files.
 3. Open the project with Qt Creator, add your compiler and compile

Note that to try your shiny new executable you'll need to download the program as described above and insert the `models` folder where your new build is output.

TODO: Add instructions for compile from scratch.

## Externals (and thanks)

 - **Phonetisaurus** (text to phoneme): [https://github.com/AdolfVonKleist/Phonetisaurus](https://github.com/AdolfVonKleist/Phonetisaurus) *(ported to Windows)*
 - **OpenFST 1.6.2** (for Windows): [https://github.com/kkm000/openfst](https://github.com/kkm000/openfst)
 - **Tensorflow C API**: [https://www.tensorflow.org/install/lang_c](https://www.tensorflow.org/install/lang_c)
 - **CppFlow** (TF C API -> C++ wrapper): [https://github.com/serizba/cppflow](https://github.com/serizba/cppflow) 
 - **AudioFile** (for WAV export): [https://github.com/adamstark/AudioFile](https://github.com/adamstark/AudioFile)
- **Frameless Dark Style Window**: https://github.com/Jorgen-VikingGod/Qt-Frameless-Window-DarkStyle


