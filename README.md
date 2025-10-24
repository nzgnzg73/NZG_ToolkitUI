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

🔗 Original Source and Credit

All credit and gratitude for the original project belong to its true creator, (✅ [dasjoms ](https://github.com/dasjoms) ✅)

 * ✅ Original Repository Link: [https://github.com/dasjoms](https://github.com/dasjoms/ChatterboxToolkitUI/tree/master)
 * License: [ Please refer to the original repository's license]

I value your work and am using this copy only out of necessity.

✉📩📧 Contact and Assurance of Immediate Action
If you have any objection or legal concern regarding my upload of this repository, and you wish to issue a strike, please contact me before taking any action. I will immediately remove these files upon your request.

Contact Email: nzgnzg73@gmail.com

Thank you very much for your understanding and cooperation.



## &#128279; Citation of the paper

```bibtex
🔧 Method 1 — Manually Edit the Code

1. Open the file:

NZG_ToolkitUI\src\chatterbox
vc.py / tts.py




2. Inside this method, remove the original lines:

```bash
tts.py File coding

for fpath in ["ve.safetensors", "t3_cfg.safetensors", "s3gen.safetensors", "tokenizer.json", "conds.pt"]:
            local_path = hf_hub_download(repo_id=REPO_ID, filename=fpath)
```


```bash
# vc.py File coding

for fpath in ["s3gen.safetensors", "conds.pt"]:
    local_path = hf_hub_download(repo_id=REPO_ID, filename=fpath)
```

3. Replace them with this code:




```bash
# tts.py File coding Update



for fpath in ["ve.safetensors", "t3_cfg.safetensors", "s3gen.safetensors", "tokenizer.json", "conds.pt"]:
            print(f"Offline mode: using local file {fpath}")
            local_path = Path(r"C:\Users\Mr_Nomi\.cache\huggingface\hub\models--nzgnzg73--chatterbox\snapshots\a68f4fc2892ceff1b9ad82893935a7b4e85dff59") / fpath  # ← تمہارا فولڈر path

        return cls.from_local(Path(local_path).parent, device
```


```bash
# vc.py File coding Update

for fpath in ["s3gen.safetensors", "conds.pt"]:
    print(f"Offline mode: using local file {fpath}")
    local_path = Path(r"C:\Users\Mr_Nomi\.cache\huggingface\hub\models--nzgnzg73--chatterbox\snapshots\a68f4fc2892ceff1b9ad82893935a7b4e85dff59") / fpath  # ← یہاں اپنا فولڈر پاتھ دو
```

# Pass the s3gen_cfg to from_local
return cls.from_local(Path(local_path).parent, device, s3gen_cfg=s3gen_cfg)



4. Save the file and run your program again.
✅ It will now work offline — no internet or HuggingFace connection needed.
---

🟩 اردو میں وضاحت

🔧 طریقہ نمبر 1 — کوڈ میں خود تبدیلی کرنا


1. فائل vc.py کھولو۔
یہ فائل تمہارے Chatterbox / TTS پراجیکٹ کے فولڈر میں ہوگی۔


3. اس کے اندر جو پرانا کوڈ ہے، یہ لائنیں:



NZG_ToolkitUI\src\chatterbox
vc.py / tts.py

tts.py File coding

for fpath in ["ve.safetensors", "t3_cfg.safetensors", "s3gen.safetensors", "tokenizer.json", "conds.pt"]:
            local_path = hf_hub_download(repo_id=REPO_ID, filename=fpath)



*vc.py* File coding 

for fpath in ["s3gen.safetensors", "conds.pt"]:
    local_path = hf_hub_download(repo_id=REPO_ID, filename=fpath)

— انہیں ڈیلیٹ کر دو۔


4. ان کی جگہ یہ نیا کوڈ پیسٹ کرو:



# tts.py File coding Update



for fpath in ["ve.safetensors", "t3_cfg.safetensors", "s3gen.safetensors", "tokenizer.json", "conds.pt"]:
            print(f"Offline mode: using local file {fpath}")
            local_path = Path(r"C:\Users\Mr_Nomi\.cache\huggingface\hub\models--nzgnzg73--chatterbox\snapshots\a68f4fc2892ceff1b9ad82893935a7b4e85dff59") / fpath  # ← تمہارا فولڈر path

        return cls.from_local(Path(local_path).parent, device




# vc.py File coding Update

for fpath in ["s3gen.safetensors", "conds.pt"]:
    print(f"Offline mode: using local file {fpath}")
    local_path = Path(r"C:\Users\Mr_Nomi\.cache\huggingface\hub\models--nzgnzg73--chatterbox\snapshots\a68f4fc2892ceff1b9ad82893935a7b4e85dff59") / fpath  # ← یہاں اپنا فولڈر پاتھ دو

# Pass the s3gen_cfg to from_local
return cls.from_local(Path(local_path).parent, device, s3gen_cfg=s3gen_cfg)



5. فائل کو Save کر دو اور دوبارہ چلاؤ۔
✅ اب یہ سسٹم آف لائن بھی چلے گا، انٹرنیٹ کے بغیر۔
```

## &#128101; Attributions

### 1. Clone the Repository


[Python 3.10.11](https://www.python.org/downloads/release/python-31011/)
Open your terminal or command prompt and clone the repository.

```bash
git clone https://github.com/dasjoms/ChatterboxToolkitUI.git
cd ChatterboxToolkitUI
```
### 1. Clone the Repository


### 2. Set Up a Python Virtual Environment


[Python 3.10.11](https://www.python.org/downloads/release/python-31011/)


Create a virtual environment using python 3.11 to avoid dependency conflicts

```bash
py -3.10 -m venv venv

```


### 3. Activate the virtual environment.

```bash

venv\scripts\activate

```
### 4. Install the Project and Dependencies

Users with 10 series NVidia cards or AMD GPUs need to manually install the proper torch 2.6.0 versions.
Otherwise just install from requirements.txt

```bash
pip install -r requirements.txt
```

### 5. Install Omegaconf
```bash
pip install omegaconf
```
## Running the Application

With your virtual environment still active, run the script:

```bash
python ChatterboxToolkitUI.py
```


You have to run  (python ChatterboxToolkitUI.py)  in the code. When an error or problem occurs while running the code, you have to follow the following procedure:

Step 1: When an error occurs, take the name of the error that is shown in the white circle (white circle) inside the picture (for example, a package name).

Solution: You have to immediately write a new line: pip install ## and write the name of the error in front of it.

 (Example: If the error is Omegaconf, you would type:

## pip install Omegaconf

Continuation: Once that package is installed, you need to re-run

python ChatterboxToolkitUI.py

(or related code).

Repetition: If a new error occurs again, you would repeat the same process: pip install followed by the name of the new error.

Final step: This process is to be repeated until all the necessary packages are installed and the code runs without any errors.


:
"If you didn't understand my previous instructions, let me explain it to you again with an example.
Suppose you run the code 'python ChatterboxToolkitUI.py' and get the following error:
ModuleNotFoundError: No module named 'transformers'

This error can appear anywhere in the middle or at the end of the code. Now you need to know what to write after pip install.
You have to pick up the name of the module inside the error, which is written in single quotes (' '). In this example, that name is 'transformers'.
You would then write:

## pip install transformers

When it is successfully installed, you would run the code 'python ChatterboxToolkitUI.py' again.
If you get another error or problem (which can appear anywhere at the end, as I mentioned last time), you would write pip install again and add the following in the new error  "Will write the name of the module that was installed.
Will keep repeating this process and re-run the code after installation."
Summary: My task is that whenever a ModuleNotFoundError occurs, I install the module name given inside single quotes via pip install and then run the next code, until all the necessary libraries are installed.






آپ کو کوڈنگ میں (python ChatterboxToolkitUI.py) ## کو رن کرنا ہے۔ جب کوڈ رن کرتے ہوئے کوئی ایرر (Error) یا پرابلم آئے، تو آپ نے درج ذیل طریقہ اپنانا ہے:
 * پہلا مرحلہ: ایرر آنے پر، اُس ایرر کا نام جو سفید دائرے (وائٹ گِلتارہ) مطلب جو پکچر کے اندر لگایا ہے  میں دکھایا گیا ہے (جیسے مثال کے طور پر کوئی پیکیج کا نام)، اُسے لینا ہے۔
 * حل: آپ نے فوراً ایک نئی لائن لکھنی ہے: pip install ## اور اُس کے آگے وہ ایرر والا نام لکھ دینا ہے۔
   (مثال: اگر ایرر آئے کہ Omegaconf، تو آپ لکھیں گے:

##  pip install Omegaconf


 * تسلسل: جب وہ پیکیج انسٹال ہو جائے، تو آپ کو دوبارہ 

## python ChatterboxToolkitUI.py
(یا متعلقہ کوڈ) کو رن کرنا ہے۔

 * تکرار: اگر دوبارہ کوئی نیا ایرر آئے، تو آپ پھر سے یہی عمل دہرائیں گے: pip install اور اُس کے آگے نئے ایرر کا نام لکھیں گے۔
 * آخری مرحلہ: یہ عمل تب تک دہراتے رہنا ہے جب تک سارے ضروری پیکیجز انسٹال نہ ہو جائیں اور کوڈ بغیر کسی ایرر کے چل جائے۔

:
"اگر آپ کو میری پچھلی ہدایات سمجھ نہیں آئیں تو میں آپ کو ایک مثال سے دوبارہ سمجھاتا ہوں۔
فرض کریں کہ آپ نے 'python ChatterboxToolkitUI.py' کوڈ کو رن کیا اور درج ذیل ایرر (Error) آ گیا:
ModuleNotFoundError: No module named 'transformers'

یہ ایرر کوڈ کے درمیان میں یا آخر میں کہیں بھی ظاہر ہو سکتا ہے۔ اب آپ کو یہ جاننے کی ضرورت ہے کہ pip install کے بعد کیا لکھنا ہے۔
آپ نے ایرر کے اندر موجود ماڈیول کا نام، جو کہ سنگل کوٹس (' ') کے اندر لکھا ہے، اُسے اُٹھانا ہے۔ اس مثال میں وہ نام 'transformers' ہے۔
آپ پھر یوں لکھیں گے:
## pip install transformers

جب یہ کامیابی سے انسٹال ہو جائے گا، تو آپ دوبارہ 'python ChatterboxToolkitUI.py' کوڈ کو رن کر دیں گے۔
اگر دوبارہ کوئی اور ایرر یا پرابلم آئے (جو کہ آخر میں کہیں بھی ظاہر ہو سکتا ہے، جیسا کہ میں نے پچھلی بار بتایا تھا)، تو آپ پھر سے pip install لکھیں گے اور اُس کے آگے نئے ایرر میں دیے گئے ماڈیول کا نام لکھ دیں گے۔
یہ عمل دہراتے رہیں گے اور انسٹالیشن کے بعد کوڈ کو دوبارہ رن کریں گے۔"
خلاصہ: میرا کام یہ ہے کہ جب بھی ModuleNotFoundError آئے، تو میں سنگل کوٹس کے اندر دیے گئے ماڈیول کے نام کو pip install کے ذریعے انسٹال کروں اور پھر اگلا کوڈ چلاؤں، جب تک کہ تمام ضروری لائبریریاں انسٹال نہ ہو جائیں۔




python ChatterboxToolkitUI.py



Once running, you will see output in your terminal like this:

```
* Running on local URL:  http://127.0.0.1:7860
```

Open the local URL in your web browser to use the application.







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

