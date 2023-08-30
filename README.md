<div align="center">
    <img alt="icon" src="https://github.com/receyuki/stable-diffusion-prompt-reader/raw/master/sd_prompt_reader/resources/icon.png" width=20% height=20%>
    <h1>Stable Diffusion Prompt Reader</h1>
    <a href="https://github.com/receyuki/stable-diffusion-prompt-reader/releases/latest">
        <img alt="GitHub releases" src="https://img.shields.io/github/downloads/receyuki/stable-diffusion-prompt-reader/total"></a>
    <a href="https://github.com/receyuki/stable-diffusion-prompt-reader/blob/master/LICENSE">
        <img alt="GitHub" src="https://img.shields.io/github/license/receyuki/stable-diffusion-prompt-reader"></a>
    <a href="https://github.com/receyuki/stable-diffusion-prompt-reader/releases/latest">
        <img alt="GitHub release (latest by date)" src="https://img.shields.io/github/v/release/receyuki/stable-diffusion-prompt-reader"></a>
    <a href="https://pypi.org/project/sd-prompt-reader/">
        <img alt="PyPI" src="https://img.shields.io/pypi/v/sd-prompt-reader"></a>
    <a href="https://github.com/psf/black">
        <img alt="Code style: black" src="https://img.shields.io/badge/code%20style-black-000000.svg"></a>
    <img alt="platform" src="https://img.shields.io/badge/platform-windows%20%7C%20macos%20%7C%20linux-lightgrey">
    <br><br>

[简体中文](https://github.com/receyuki/stable-diffusion-prompt-reader/blob/master/README.zh-Hans.md) | [English](https://github.com/receyuki/stable-diffusion-prompt-reader/blob/master/README.md)

A simple standalone viewer for reading prompt from Stable Diffusion generated image outside the webui.
    <br>
  <p>
    <a href="#features">Features</a> •
    <a href="#supported-formats">Supported Formats</a> •
    <a href="#download">Download</a> •
    <a href="#usage">Usage</a> •
    <a href="#faq">FAQ</a> •
    <a href="#credits">Credits</a>
  </p>
    <img src="https://github.com/receyuki/stable-diffusion-prompt-reader/raw/master/images/screenshot_v132.png">
</div>

## Features
- Support macOS, Windows and Linux.
- Simple drag and drop interaction.
- Copy prompt to clipboard.
- Remove prompt from image.
- Export prompt to text file.
- Edit or import prompt to images
- Vertical orientation display and sorting by alphabet
- Detect generation tool.
- Multiple formats support.
- Dark and light mode support.

## Supported Formats
|                                                                          | PNG | JPEG | WEBP | TXT* |
|--------------------------------------------------------------------------|:---:|:----:|:----:|:----:|
| [A1111's webUI](https://github.com/AUTOMATIC1111/stable-diffusion-webui) |  ✅  |  ✅   |  ✅   |  ✅   |
| [Easy Diffusion](https://github.com/easydiffusion/easydiffusion)         |  ✅  |  ✅   |  ✅   |      |
| [StableSwarmUI](https://github.com/Stability-AI/StableSwarmUI)*          |  ✅  |  ✅   |      |      |
| [InvokeAI](https://github.com/invoke-ai/InvokeAI)                        |  ✅  |      |      |      |
| [ComfyUI](https://github.com/comfyanonymous/ComfyUI)*                    |  ✅  |      |      |      |
| [NovelAI](https://novelai.net/)                                          |  ✅  |      |      |      |
| [Draw Things](https://drawthings.ai/)                                    |  ✅  |      |      |      |
| Naifu(4chan)                                                             |  ✅  |      |      |      |

\* Limitations apply. See [format limitations](#TXT).

If you are using a tool or format that is not on this list, please help me to support your format 
by uploading the original file generated by your tool to the issues, thx.

## Download
### For Windows users
Download executable from [GitHub Releases](https://github.com/receyuki/stable-diffusion-prompt-reader/releases/latest)
### For macOS users
Download executable from [GitHub Releases](https://github.com/receyuki/stable-diffusion-prompt-reader/releases/latest)
#### Install via Homebrew Cask
You may also install SD Prompt Reader via [Homebrew](http://brew.sh/) cask.  
```bash
brew install --no-quarantine receyuki/sd-prompt-reader/sd-prompt-reader
```
The parameter `--no-quarantine` is used since the SD Prompt Reader is currently unsigned as I mentioned [here](https://github.com/receyuki/stable-diffusion-prompt-reader#sd-prompt-readerapp-is-damaged-and-cant-be-opened-you-should-move-it-to-the-trash)
### For Linux users (not regularly tested)
~~I'm pretty sure linux users can figure things out without an executable.~~
- The minimum version of Python required is 3.10
- Make sure you have the tkinter package installed in your Python.  
If not, install the python3-tk package with package managers.  
e.g. `sudo apt-get install python3-tk` for Debian-based distributions  

You can choose to install with pip or run it manually
#### Install with pip or pipx
```bash
pip install sd-prompt-reader
```
or
```bash
pipx install sd-prompt-reader
```
To launch app just enter `sd-prompt-reader` in the terminal.
#### Run source code manually
1. Clone this repo.
    ```bash
    git clone https://github.com/receyuki/stable-diffusion-prompt-reader.git
    ```
   or download repo as a zip.
2. CD to the directory and install dependencies.
    ```bash
    cd stable-diffusion-prompt-reader  
    pip install -r requirements.txt
    ```
3. Run.
    ```bash
   python main.py
   ```

## Usage
### Read prompt
- Open the executable file (.exe or .app) and drag and drop the image into the window.

OR
- Right click on the image and select open with SD Prompt Reader

OR
- Drag and drop the image directly onto executable (.exe or .app).

### Export prompt to a text file
- Click "Export" will generate a txt file alongside the image file.
- To save to another location, click the expand arrow and click "select directory".  
![export](https://github.com/receyuki/stable-diffusion-prompt-reader/raw/master/images/export.png)

### Remove prompt from image
- Click "Clear" will generate a new image file with suffix "_data_removed" alongside the original image file.
- To save to another location, click the expand arrow and click "select directory".
- To overwrite the original image file, click the expand arrow and click "overwrite the original image".  
![remove](https://github.com/receyuki/stable-diffusion-prompt-reader/raw/master/images/remove.png)

### Edit image
***Please note that the edited image will be written in A1111 format, it meaning that image in any format will become A1111 format after editing.***
- Click "Edit" to enter edit mode.
- Edit the prompt directly in the textbox or import a metadata file in txt format.
- Click "Save" will generate a edited image file with suffix "_edited" alongside the original image file.
- To save to another location, click the expand arrow and click "select directory".
- To overwrite the original image file, click the expand arrow and click "overwrite the original image".  
![save](https://github.com/receyuki/stable-diffusion-prompt-reader/raw/master/images/save.png)

### Copy as single line prompt
Copy image prompt and setting in a format that can be read by [Prompts from file or textbox](https://github.com/AUTOMATIC1111/stable-diffusion-webui/wiki/Features#prompts-from-file-or-textbox) 
The following parameters are supported:

| Setting                 | Parameter            |
|-------------------------|----------------------|
| Seed                    | --seed               |
| Variation seed strength | --subseed_strength   |
| Seed resize from        | --seed_resize_from_h |
| Seed resize from        | --seed_resize_from_w |
| Sampler                 | --sampler_name       |
| Steps                   | --steps              |
| CFG scale               | --cfg_scale          |
| Size                    | --width              |
| Size                    | --height             |
| Face restoration        | --restore_faces      |

- Click the expand arrow and click "single line prompt".
- Paste it into the textbox below the webui script "Prompts from file or textbox".  
![single line prompt](https://github.com/receyuki/stable-diffusion-prompt-reader/raw/master/images/single_line_prompt.png)

### ComfyUI SDXL workflow
***The SDXL workflow does not support editing. 
If necessary, please remove prompts from image before edit.***  
If the image's workflow includes multiple sets of SDXL prompts, 
namely Clip G(text_g), Clip L(text_l), and Refiner, the SD Prompt Reader will switch to the multi-set prompt display mode as shown in the image below. 
There are two interface options available for the multi-set prompt display mode, and you can switch between them using buttons.  
![comfyui_sdxl.png](https://github.com/receyuki/stable-diffusion-prompt-reader/raw/master/images/comfyui_sdxl.png)

## Format Limitations
### TXT
1. Importing txt file is only allowed in edit mode.
2. Only A1111 format txt files are supported. You can use txt files generated by the A1111 webui or use the SD prompt reader to export txt from A1111 images
### StableSwarmUI
StableSwarmUI is still in the Alpha testing phase, and its format may change in the future. I will keep track of upcoming updates of StableSwarmUI.
### ComfyUI
***Support for comfyUI requires more testing. If you believe your image is not being displayed properly, please upload the original file generated by ComfyUI to the issues.***
1. If there are multiple sets of data (seed, steps, CFG, etc.) in the setting box, this means that there are multiple KSampler nodes in the flowchart.
2. Due to the nature of ComfyUI, all nodes and flowcharts in the workflow are stored in the image, including those that are not being used. Also, a flowchart can have multiple branches, inputs and outputs.
(e.g. output hires. fixed image and original image simultaneously in a single flowchart)
SD Prompt Reader will traverse all flowcharts and branches and display the longest branch with complete input and output.  
3. [ComfyUI SDXL workflow](https://github.com/receyuki/stable-diffusion-prompt-reader#comfyui-sdxl-workflow)
### Easy Diffusion
By default, Easy Diffusion does not write metadata to images. Please change the _Metadata format_ in settings to _embed_ to write the metadata to images

## FAQ
### Malware Alert
The false positive reported by some anti-malwares is caused by the packaging tool _pyinstaller_ which is a common issue for _pyinstaller_ users. 
I spent a lot of time trying to fix the Windows Defender false positive before, but I couldn't do it for every antivirus software. 
So, you can either trust Windows Defender or use the instruction for Linux users to use this app.
### "SD Prompt Reader.app" is damaged and can't be opened. You should move it to the Trash
This is a very common macOS issue when you run unsigned non-appstore apps, 
and developers must pay $99 per year to Apple to eliminate this issue. 
You can choose to **Allow Apps from Anywhere** in **security & privacy** settings which can be dangerous. 
The way I prefer is to remove the quarantine attributes. 
1. Open Terminal from the Applications folder. 
2. Type in the following command and hit Enter. 

    `xattr -r -d com.apple.quarantine /path/to/app.app`

    In my case it's

    `xattr -r -d com.apple.quarantine /Applications/SD\ Prompt\ Reader.app`

If you are still concerned about the security of the app you can use the instruction for Linux users to use this app.

## TODO
- Batch image processing tool
- Gallery/Folder view

## Credits
- Inspired by [Stable Diffusion web UI](https://github.com/AUTOMATIC1111/stable-diffusion-webui/)
- App icon generated using Stable Diffusion with [IconsMI](https://huggingface.co/jvkape/IconsMI-AppIconsModelforSD)
- Special thanks to [Azusachan](https://github.com/Azusachan) for providing SD server
