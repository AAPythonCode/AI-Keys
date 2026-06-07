# AI-Keys
A custom mechanical keyboard designed in KiCad, with a built-in AI function to ask AI a question.

# How it works
- The firmware runs on a ESP32-S3 DEVKIT C1, handing all of the logic to make the keyboard run.
- It uses any Cherry-branded switch, but in particular it uses the Cherry MX Speed Silver model.
- The LED strip embedded in the case utilizes a ws2812b strip. There is no particular model; however, the one I used had a red, black, and green wire for power and data.
- There is a decently sized battery to run the keyboard.
- To charge the battery, I created a charging circuit, which utilizes the MCP73831-2-MC and USB Type C VBUS input modules to charge the battery correctly. 
- To stabilize power flow to the ESP32, the keyboard uses a TPS63001 (buck convertor).
- The speaker runs on a MAX98357A, which is a module that controls the speaker.

> [!NOTE]
> Any battery can be used, but make sure that the battery outputs a stable 3.7V. You may use higher voltages, in accordance to the TPS63001's datasheet: https://www.ti.com/product/TPS63001

# Parts used
Here's a dedicated parts list for creating this keyboard yourself:
