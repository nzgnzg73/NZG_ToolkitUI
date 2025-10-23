[dasjoms ✅ ChatterboxToolkitUI](https://github.com/dasjoms/ChatterboxToolkitUI/tree/master)


The owner of this open source project is the one at the link below:
https://github.com/dasjoms/ChatterboxToolkitUI/tree/master







NZG Official - Stable Version of chatter-box-dubbing
This repository is a modified and stable copy of the
 original project, [ChatterboxToolkitUI](https://github.com/dasjoms/ChatterboxToolkitUI/tree/master)

🛑 Important Explanation: Reason for Re-uploading this Code


I, the owner of NZG Official, sincerely apologize to the original code owner, [dasjoms ](https://github.com/dasjoms)

 (( ✅ [ChatterboxToolkitUI](https://github.com/dasjoms/ChatterboxToolkitUI/tree/master) ✅), and wish to clarify that my intention is not in any way to infringe upon your copyright or claim ownership of your work.
I decided to download your repository and re-upload it to my account solely due to personal need and technical constraints:
 * PC Limitations: I do not have a powerful enough (PC 😭 😔) to run the code you release locally. My computer is very old and lacks a suitable graphics card.
 * Colab Usage: My primary need is to use this code in the ⚡[Google Colab ](https://colab.research.google.com/drive/16HI1ZW3GrrG0QUmeGvV79yoiaKCVNfxs?usp=sharing#scrollTo=SBubttdzrVBW) ⚡ [Kaggle](https://www.kaggle.com/code/core73/new-nzg-toolkitui-kaggle) ⚡
    environment.
 * Updates Conflict: When you release a new update or feature in the original repository, that new code often conflicts or stops working with my existing Colab setup.


## &#128279; Citation of the paper

```bibtex
🔧 Method 1 — Manually Edit the Code

1. Open the file:

NZG_ToolkitUI\src\chatterbox
vc.py / tts.py


(You’ll find this file inside your Chatterbox or TTS project folder.)


2. Find the method:

def from_pretrained(cls, device, s3gen_cfg: Optional[DictConfig] = None):


3. Inside this method, remove the original lines:

for fpath in ["s3gen.safetensors", "conds.pt"]:
    local_path = hf_hub_download(repo_id=REPO_ID, filename=fpath)


4. Replace them with this code:

for fpath in ["s3gen.safetensors", "conds.pt"]:
    print(f"Offline mode: using local file {fpath}")
    local_path = Path(r"C:\Users\Mr_Nomi\.cache\huggingface\hub\models--nzgnzg73--chatterbox\snapshots\a68f4fc2892ceff1b9ad82893935a7b4e85dff59") / fpath  # ← your model path

# Pass the s3gen_cfg to from_local
return cls.from_local(Path(local_path).parent, device, s3gen_cfg=s3gen_cfg)


5. Save the file and run your program again.
✅ It will now work offline — no internet or HuggingFace connection needed.
---

🟩 اردو میں وضاحت

🔧 طریقہ نمبر 1 — کوڈ میں خود تبدیلی کرنا

1. فائل vc.py کھولو۔
یہ فائل تمہارے Chatterbox / TTS پراجیکٹ کے فولڈر میں ہوگی۔


2. اس فنکشن کو تلاش کرو:

def from_pretrained(cls, device, s3gen_cfg: Optional[DictConfig] = None):


3. اس کے اندر جو پرانا کوڈ ہے، یہ لائنیں:

for fpath in ["s3gen.safetensors", "conds.pt"]:
    local_path = hf_hub_download(repo_id=REPO_ID, filename=fpath)

— انہیں ڈیلیٹ کر دو۔


4. ان کی جگہ یہ نیا کوڈ پیسٹ کرو:

for fpath in ["s3gen.safetensors", "conds.pt"]:
    print(f"Offline mode: using local file {fpath}")
    local_path = Path(r"C:\Users\Mr_Nomi\.cache\huggingface\hub\models--nzgnzg73--chatterbox\snapshots\a68f4fc2892ceff1b9ad82893935a7b4e85dff59") / fpath  # ← یہاں اپنا فولڈر پاتھ دو

# Pass the s3gen_cfg to from_local
return cls.from_local(Path(local_path).parent, device, s3gen_cfg=s3gen_cfg)


5. فائل کو Save کر دو اور دوبارہ چلاؤ۔
✅ اب یہ سسٹم آف لائن بھی چلے گا، انٹرنیٹ کے بغیر۔
```

## &#128101; Attributions




 * My Goal: Therefore, I uploaded a stable version here for personal use so I can maintain a version of the code that runs continuously in Colab without constant daily fixing.


🔗 Original Source and Credit

All credit and gratitude for the original project belong to its true creator, (✅ [dasjoms ](https://github.com/dasjoms) ✅)

 * ✅ Original Repository Link: [https://github.com/dasjoms](https://github.com/dasjoms/ChatterboxToolkitUI/tree/master)
 * License: [ Please refer to the original repository's license]

I value your work and am using this copy only out of necessity.

✉📩📧 Contact and Assurance of Immediate Action
If you have any objection or legal concern regarding my upload of this repository, and you wish to issue a strike, please contact me before taking any action. I will immediately remove these files upon your request.

Contact Email: nzgnzg73@gmail.com

Thank you very much for your understanding and cooperation.




-   **Single Generation**:
    -   **Text-to-Speech (TTS)**: Generate high-quality speech from text using a reference audio file to clone the speaker's voice.
    -   **Voice Conversion (VC)**: Transfer the vocal characteristics of a reference speaker onto a source audio recording.
    -   **Parameter Sweeping**: Generate multiple variations of a single output at once by sweeping across a range of values for any generation parameter (e.g., Temperature, Pace, etc.).

-   **Batch Processing**:
    -   Process entire folders of prepared text or audio files in bulk with a single click.
    -   Optionally concatenate all generated files from a batch run into a single, continuous audio file.

-   **Data Preparation Suite**:
    -   **Text Splitter**: Automatically chunk long text documents into smaller, model-friendly segments based on sentence boundaries and a configurable character limit.
    -   **Audio Splitter**: Intelligently split long audio recordings into shorter clips by making cuts during periods of silence, with configurable duration and silence detection parameters.

-   **Workflow-Integrated Editing & Refinement**:
    -   **Regenerate Audio**: The "Regenerate" workflow allows you to review individual audio files from a batch run, send them back to the Single TTS tab with their original text and voice pre-loaded, tweak parameters, and replace the old file with the new-and-improved version.
    -   **Live Text Editor**: Directly edit the content of your processed text files within the UI and save the changes, perfect for making small script adjustments without leaving the application.

[[Full Feature Rundown Video]](https://www.youtube.com/watch?v=fA8QWmG30no)

## Prerequisites

Before you begin, ensure you have the following installed on your system:

1.  **Python**: Version **3.11** is required.
2.  **Git**: For cloning the repository.
3.  **CUDA Compatible GPU**: For acceptable performance, a GPU is highly recommended. The underlying models will be extremely slow on a CPU.
4.  **FFmpeg**: This is a critical dependency for performing various audio processing tasks.

## Installation Instructions

Follow these steps to set up and run the ChatterboxToolkitUI on your local machine or use the ChatterboxToolkitUI.ipynb to run it in a colab environment.



## 🙏 Acknowledgments

Big thanks to the original creators of Chatterbox:
👉 [Resemble AI](https://github.com/resemble-ai) for their groundbreaking work in controllable TTS.

---

## 📜 License

This project is provided under the original license of the upstream [chatterbox](https://github.com/resemble-ai/chatterbox). Check their repository for licensing details.

```

Let me know if you’d like a more developer-focused or user-focused version!
```

