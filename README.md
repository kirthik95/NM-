
Ensure the script's `base_dir` variable is pointing to the `en` directory inside the dataset.

---

## 🧪 Features Extracted

For each audio file in the dataset, the following features are computed:

- **duration_sec**: Duration of the audio in seconds
- **mfcc_mean**: Mean of Mel-frequency cepstral coefficients
- **pitch_mean**: Mean pitch estimated using YIN algorithm
- **energy**: Average energy of the waveform
- **snr_db**: Estimated Signal-to-Noise Ratio (SNR) in decibels
- **label**: Categorized as `clean` if `snr_db > 10`, otherwise `noisy`

Metadata from the TSV files is also extracted when available:
- **client_id**
- **sentence**
- **gender**
- **accent**

---

## ⚙️ Requirements

Install the following Python libraries:

```bash
pip install librosa numpy pandas tqdm
