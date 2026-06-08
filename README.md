# AI-Keys
A custom mechanical keyboard designed in KiCad, with a built-in AI function to ask AI a question.

# How it works
- The firmware runs on a ESP32-S3 DEVKIT C1, handing all of the logic to make the keyboard run.
- It uses any Cherry-branded switch, but in particular it uses the Cherry MX Brown model.
- The LED strip embedded in the case utilizes a ws2812b strip. There is no particular model; however, the one I used had a red, black, and green wire for power and data.
- There is a decently sized battery to run the keyboard.
- To charge the battery, I created a charging circuit, which utilizes the MCP73831-2-MC and USB Type C VBUS input modules to charge the battery correctly. 
- To stabilize power flow to the ESP32, the keyboard uses a TPS63001 (buck convertor).
- The speaker runs on a MAX98357A, which is a module that controls the speaker to output the message the AI wants to speak out loud.

> [!NOTE]
> Though a 3.7V battery is used for this project, you may use higher/lower voltages, in accordance to the [TPS63001's datasheet.](https://www.ti.com/product/TPS63001)

# Parts used
Here's a dedicated parts list for creating this keyboard yourself:

| Part | Cost | Link | Manufacturer |
-------|------|---------|------------
Cherry MX Brown | $8.00 (with new user discount) | [Link](https://www.aliexpress.us/item/3256811880813653.html?spm=a2g0o.detail.0.0.3867UsiwUsiwu6&mp=1&pdp_npi=6%40dis%21USD%21USD+32.89%21USD+8.00%21%21USD+8.00%21%21%21%402101eede17807987748595335e2ac4%2112000057415897661%21ct%21US%217444042787%21%211%210%21&_gl=1*1651hzd*_gcl_aw*R0NMLjE3NzQxNTIyOTcuQ2owS0NRandtdW5OQmhEYkFSSXNBT25kS3BtZWJwVFNMSlp6Y2tCbWZrbUN5cmo0b0lSVUNOdUExRzBNODM4TWd6QUx5bHJhME04VzNBNGFBbHR0RUFMd193Y0I.*_gcl_au*MTY4NjExMjk2NC4xNzczODc0NTA1*_ga*MjAyMzU5Nzk2NC4xNzgwNzk4NjI3*_ga_VED1YSGNC7*czE3ODA3OTg2MjckbzEkZzEkdDE3ODA3OTg3NzQkajYwJGwwJGgw&gatewayAdapt=glo2usa) | AliExpress
TPS63001 | $2.27 | [Link](https://www.ti.com/product/TPS63001?utm_source=google&utm_medium=cpc&utm_campaign=app-null-null-GPN_EN-cpc-pf-google-ww_en_cons&utm_content=TPS63001&ds_k=TPS63001&DCM=yes&gclsrc=aw.ds&gad_source=1&gad_campaignid=1767856010&gbraid=0AAAAAC068F02XRLVUVn1qaOX6xrOvtP0y&gclid=Cj0KCQjwrZTRBhDSARIsAHidYfcO2jmQQrtSjZ0xPVh3lzhPpcKTbKZK_XgQGUQXxEWHeZcUr_cTREwaAqqhEALw_wcB#order-quality) | Texas Instruments
USB VBUS TYPE-C | 0.94 | [Link](https://www.lcsc.com/product-detail/USB-Type-C_Korean-Hroparts-Elec-TYPE-C-31-M-12_C165948.html) | LCSC 
Resistors and Caps | 5.66 | [Link (to pastebin)](https://justpaste.it/oabiu) | LCSC
MCP73831-2-MC | 0.79 | [Link](https://www.digikey.com/en/products/detail/microchip-technology/MCP73831-2ATI-MC/1874109?curr=usd&utm_campaign=buynow&utm_medium=aggregator&utm_source=octopart) | DigiKey
