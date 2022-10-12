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
