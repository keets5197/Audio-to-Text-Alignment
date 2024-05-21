
# Audio-to-Text Alignment Across Languages


## Abstract
In this study, we developed a methodology to align audio with corresponding text across multiple languages, focusing on non-dominant language communities. By leveraging a combination of phoneme generation and text alignment techniques, we created models that accurately match spoken words to their written counterparts, even in languages with limited technological resources. This research enhances inclusivity and accuracy in global communication.

## Keywords
- Audio-to-text alignment
- Python
- Eflomal
- SentencePiece
- Soundstream
- Wav2Vec2
- Wav2Vec2Phoneme
- Huggingface transformers
- Neural Networks

## Introduction
The rapid advancement of language technologies necessitates the development of inclusive linguistic tools. Our research addresses this need by creating robust methodologies for aligning audio with text across diverse languages, particularly focusing on non-dominant languages.

### Key Highlights
- Precise alignment of spoken words with their written forms across diverse languages.
- Detecting discrepancies between audio and text without relying on traditional speech recognition methods.
- Rigorous simulations to test the robustness of our methods in various scenarios.

## Data
The Mozilla Common Voice dataset serves as the foundational resource for the project. It includes over 30,329 hours of recorded audio with demographic metadata across 120 languages.

### Data Structure
- **Valid Subsets**: Verified audio clips.
- **Invalid Subsets**: Clips with identified mismatches.
- **Other Subsets**: Clips with fewer votes or equal valid/invalid votes.

## Methodology
We employed a combination of SentencePiece, SoundStream, Wav2Vec2Phoneme, and Eflomal for our audio-to-text alignment project.

### Steps Involved
1. **Audio Processing**: Spectrograms enhanced with normalization, compression, and noise reduction.
2. **Text Tokenization**: Using SentencePiece for language-agnostic tokenization.
3. **Phoneme Conversion**: Using Wav2Vec2Phoneme to convert audio to phonemes.
4. **Alignment**: Using Eflomal to align phonetic data with tokenized text.


## Results
The performance of our models was evaluated using various alignment error rates across different language pairs.

### Table: Alignment Error Rate for Eflomal
| Alignment Models | De-En | Fr-En | Ro-En | Ja-En | Zh-En | En-Hi |
|------------------|-------|-------|-------|-------|-------|-------|
| fast_align       | 27    | 10.5  | 32.1  | 51.1  | 38.1  | 67.2  |
| eflomal          | 22.6  | 8.2   | 25.1  | 47.5  | 28.7  | 46.7  |
| Mgiza            | 20.6  | 5.9   | 26.4  | 48    | 35.1  | 55.7  |
| Awesome-align    | 15.1  | 4.1   | 20.7  | 37.4  | 13.4  | 41.2  |
| SimAlign         | 18.8  | 7.6   | 27.2  | 46.6  | 21.6  | 40.2  |
| GIZA++           | 20.6  | 5.9   | 26.4  | 48    | 35.1  | 51.8  |
| Efmarel          | 13.3  | 8.5   | 28.7  | 49    | 29.6  | 48.3  |

## Conclusion
Our study addresses the gap in access to online content for less well-known languages by developing a language-agnostic, data-efficient model for converting audio data into text using phonetic representation.
