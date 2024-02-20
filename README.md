# Whisper-AT-Demo
Exploring HuggingFace library Whisper-AT API for news data audio tagging

Whisper-AT is a joint audio tagging and speech recognition model. It inherits strong speech recognition ability from OpenAI Whisper, and its ASR performance is exactly the same as the original Whisper. The API interface and usage are also identical to the original OpenAI Whisper, so users can seamlessly switch from the original Whisper to Whisper-AT.

The advantage of Whisper-AT is that with minimal (less than 1%**) additional computational cost, Whisper-AT outputs general audio event labels (527-class AudioSet labels) in desired temporal resolution in addition to the ASR transcripts. This makes audio tagging much easier and faster than using a standalone audio tagging model.

Internally, Whisper-AT freezes all original Whisper parameters, and trains a Time- and Layer-wise Transformer (TL-TR) on top of the Whisper encoder representations for the audio tagging task.
