# HackatonNanosemantics
## About solution
1. Formed a Pipeline from the Real-Time-Voice-Cloning framework using the SV2TTS model, and
wav2lip framework.
2. Synthesized Biden's voice using Real-Time-Voice-Cloning, and using wav2lip created
video of Biden's face speaking synthesized text.

### Speech synthesis model with multiple speakers
The system consists of three independently trained neural networks.
- A recurrent speaker encoder that computes a fixed size vector from speech.
- A seq-to-seq Synthesizer based on Natural TTS synthesis by processing WaveNet with mel (short for melody) spectrogram predictions that predicts a mel spectrogram based on a sequence of input data conditioned by the speaker's embedding vector.
- A WaveNet autoregressive vocoder that converts a spectrogram into time domain signals.


![architecture](https://github.com/ditengm/HackatonNanosemantics/blob/main/img/architecture.png?raw=true)
### Real-Time-Voice-Cloning
The Real-Time-Voice-Cloning library has been imported. This repository is an implementation of transfer learning from speaker check to multi-speaker speech synthesis (SV2TTS) using a real-time vocoder.


![realtimevoice](https://github.com/ditengm/HackatonNanosemantics/blob/main/img/realtimevoice.png?raw=true)
### Recording an audio file:
It is possible to download files from local storage, as well as record sound from a microphone for further speech synthesis.
That is, the algorithm allows you to synthesize the voice of any person, but in this example, we will upload audio files of Biden's speech.
At this stage, speech is converted into a vector for further speech synthesis.


![load_voice](https://github.com/ditengm/HackatonNanosemantics/blob/main/img/load_voice.png?raw=true)

### Speech synthesis process
The following text was written:
*The GENERAL team is the winner of the hackathon, which is held at RTU MIREA. This team will take first place in the competition. I would like to say a huge thank you to this team for such a good decision.*

Synthesizer accepts text and a vector as input. Then this data is converted into a spectrogram, on which the model is trained.
Vocoder WaveNet then converts the spectrogram into time domain signals.


![load_voice](https://github.com/ditengm/HackatonNanosemantics/blob/main/img/procces.png?raw=true)