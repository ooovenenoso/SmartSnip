# SmartSnip

SmartSnip is a simple screenshot utility with the capability to interpret the content of the captured images with the assistance of OpenAI's GPT-4 Vision (GPT-4V) and text-to-speech functionality. The main goal here is to provide an easier way to interact with GPT-4V.

⚠️ ***This is currently a work-in-progress, and has only been tested on Windows 11.*** ⚠️

## Demo

https://github.com/A-M-D-R-3-W/SmartSnip/assets/84816543/297676ea-6182-4327-a588-81b536d3fb6e

## Installation

Before installing SmartSnip, ensure you have Python 3.10 installed on your system. Follow these steps:

1. Clone the repository or download the source code:

```bash
git clone https://github.com/A-M-D-R-3-W/SmartSnip.git
```

2. Navigate to the cloned repository directory:

```bash
cd SmartSnip
```

3. Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

### Starting the Application

To start SmartSnip, use the following command from the root directory of the project:

```bash
python smartSnip.py
```

⚠️ Upon the first open, your OpenAI API key ***must be changed***. This is located in the **Settings** window within the program, or can be accessed from **config.env**. An OpenAI API key can be acquired [Here](https://platform.openai.com/api-keys).

### Taking Screenshots

- Click the **New Snip** button to start the snipping tool.
- Select the area of the screen you want to capture (**ESC** can by clicked while dragging to cancel the snip).

### Interpreting Images

- Type your question in the text box at the top. If left empty, it will submit *"What is in this image?"* by default.
- After capturing the screenshot, use the **Interrogate** button to send the image for analysis.
- The response from GPT-4V will be shown in the text area.

### Text-to-Speech

- Once the analysis is done, click the **TTS** button to listen to the spoken version of the text.
- The button will become red to indicate that the speech is being generated. If the button is clicked again, the TTS will be canceled.

### Settings

To customize SmartSnip:

- Click the **Settings** button to adjust appearance modes, themes, OpenAI API key, TTS voice, and TTS model.
- Changes will be saved automatically, though theme changes will require a restart to take effect. Also, saving your OpenAI API Key requires pressing the "Save" button on the right.
- Note: changes can also be made by adjusting **config.env** manually, though this is not recommended as all settings can be accessed from within the application (with the exception of the window icon).

### Resetting the Application

If you need to reset SmartSnippingTool to its initial state:

- Click the **Reset** button to clear all data and return to the start screen.

## Themes

| Center-aligned |
|     :---:      |
| git status     |


## Adding Custom Themes

Custom themes can be added by doing the following:

1. Drop your theme file (mytheme.json) into the **/themes** folder in the main directory.
2. Add the path to the **themeDict** dictionary within **smartSnip.py**. Follow the existing convention ('mytheme': 'themes/mytheme.json')
3. In order for the new theme to appear in the **Settings** window, **self.settings.theme_optionmenu** within the **settings_window** function must be modified to add the name you assigned it in the dictionary to the widget. (values=['blue', ...., 'mytheme'])

***I suggest creating new themes using [ctk_theme_builder](https://github.com/avalon60/ctk_theme_builder)***

## Contributing

This is very much a WIP, and as such contributions are greatly appreciated!
