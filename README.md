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

# BOM (Bill Of Materials)
Here's a dedicated BOM for creating this keyboard yourself:

| Part | Cost | Link | Manufacturer/Retailer |
-------|------|---------|------------
Cherry MX Brown | $8.00 (with new user discount) | [Link](https://www.aliexpress.us/item/3256811880813653.html?spm=a2g0o.detail.0.0.3867UsiwUsiwu6&mp=1&pdp_npi=6%40dis%21USD%21USD+32.89%21USD+8.00%21%21USD+8.00%21%21%21%402101eede17807987748595335e2ac4%2112000057415897661%21ct%21US%217444042787%21%211%210%21&_gl=1*1651hzd*_gcl_aw*R0NMLjE3NzQxNTIyOTcuQ2owS0NRandtdW5OQmhEYkFSSXNBT25kS3BtZWJwVFNMSlp6Y2tCbWZrbUN5cmo0b0lSVUNOdUExRzBNODM4TWd6QUx5bHJhME04VzNBNGFBbHR0RUFMd193Y0I.*_gcl_au*MTY4NjExMjk2NC4xNzczODc0NTA1*_ga*MjAyMzU5Nzk2NC4xNzgwNzk4NjI3*_ga_VED1YSGNC7*czE3ODA3OTg2MjckbzEkZzEkdDE3ODA3OTg3NzQkajYwJGwwJGgw&gatewayAdapt=glo2usa) | AliExpress
TPS63001 | $2.27 | [Link](https://www.ti.com/product/TPS63001?utm_source=google&utm_medium=cpc&utm_campaign=app-null-null-GPN_EN-cpc-pf-google-ww_en_cons&utm_content=TPS63001&ds_k=TPS63001&DCM=yes&gclsrc=aw.ds&gad_source=1&gad_campaignid=1767856010&gbraid=0AAAAAC068F02XRLVUVn1qaOX6xrOvtP0y&gclid=Cj0KCQjwrZTRBhDSARIsAHidYfcO2jmQQrtSjZ0xPVh3lzhPpcKTbKZK_XgQGUQXxEWHeZcUr_cTREwaAqqhEALw_wcB#order-quality) | Texas Instruments
USB VBUS TYPE-C | $0.94 | [Link](https://www.lcsc.com/product-detail/USB-Type-C_Korean-Hroparts-Elec-TYPE-C-31-M-12_C165948.html) | LCSC 
Resistors and Caps | $5.66 | [Link](https://justpaste.it/oabiu) | LCSC
MCP73831-2-MC | $0.79 | [Link](https://www.digikey.com/en/products/detail/microchip-technology/MCP73831-2ATI-MC/1874109?curr=usd&utm_campaign=buynow&utm_medium=aggregator&utm_source=octopart) | DigiKey
PCB | Depends On Manufacturer | [Link](https://github.com/user-attachments/files/28724171/gerbers.zip) | Any PCB Manufacturer
XFL4020-222MEC (inductor for TPS63001) | $2.47 | [Link](https://www.coilcraft.com/en-us/products/power/shielded-inductors/molded-inductor/xfl/xfl4020/xfl4020-222/?srsltid=AfmBOoqs8osaTAfdjHIyioyBk3GpIvO1-Iu_L-rxJIhnwW51TJ0jehTB) | Coilcraft
MAX98357A | $4.75 | [Link](https://www.lcsc.com/product-detail/C23890844.html) | LCSC
Keycaps | $4.06 (with new user discount) | [Link](https://www.aliexpress.us/item/3256807174517233.html?spm=a2g0o.cart.0.0.314f38dabMcHQb&mp=1&pdp_npi=6%40dis%21USD%21USD+28.14%21USD+4.06%21%21USD+4.06%21%21%21%402103110517809574308387537ef602%2112000057896443594%21ct%21US%217444042787%21%211%210%21&_gl=1*1d189ad*_gcl_aw*R0NMLjE3Nzc3NTMyMzAuQ2p3S0NBand3ZGJQQmhCZ0Vpd0F4QlJBNGJVQ0tFZlZpZjBqYkZoaDBxQkh5anRleFZHblpLV01BbXdvQ1NITDMtdGtYVnBXREF1SjZCb0NzWU1RQXZEX0J3RQ..*_gcl_dc*R0NMLjE3Nzc3NTMyMzAuQ2p3S0NBand3ZGJQQmhCZ0Vpd0F4QlJBNGJVQ0tFZlZpZjBqYkZoaDBxQkh5anRleFZHblpLV01BbXdvQ1NITDMtdGtYVnBXREF1SjZCb0NzWU1RQXZEX0J3RQ..*_gcl_au*MTY4NjExMjk2NC4xNzczODc0NTA1*_ga*MjEwOTI4NjY5NS4xNzgwOTQzODE5*_ga_VED1YSGNC7*czE3ODA5NTczOTUkbzMkZzEkdDE3ODA5NTc4MjgkajYwJGwwJGgw&gatewayAdapt=glo2usa) | AliExpress
Screws | $1.07 (with new user discount) | [Link](https://www.aliexpress.us/item/3256805283136304.html?spm=a2g0o.cart.0.0.314f38dabMcHQb&mp=1&pdp_npi=6%40dis%21USD%21USD+1.88%21USD+1.07%21%21USD+1.07%21%21%21%402103110517809574308387537ef602%2112000033206512825%21ct%21US%217444042787%21%211%210%21&_gl=1*1rbt53m*_gcl_aw*R0NMLjE3Nzc3NTMyMzAuQ2p3S0NBand3ZGJQQmhCZ0Vpd0F4QlJBNGJVQ0tFZlZpZjBqYkZoaDBxQkh5anRleFZHblpLV01BbXdvQ1NITDMtdGtYVnBXREF1SjZCb0NzWU1RQXZEX0J3RQ..*_gcl_dc*R0NMLjE3Nzc3NTMyMzAuQ2p3S0NBand3ZGJQQmhCZ0Vpd0F4QlJBNGJVQ0tFZlZpZjBqYkZoaDBxQkh5anRleFZHblpLV01BbXdvQ1NITDMtdGtYVnBXREF1SjZCb0NzWU1RQXZEX0J3RQ..*_gcl_au*MTY4NjExMjk2NC4xNzczODc0NTA1*_ga*MjEwOTI4NjY5NS4xNzgwOTQzODE5*_ga_VED1YSGNC7*czE3ODA5NTczOTUkbzMkZzEkdDE3ODA5NTc4MzMkajU1JGwwJGgw&gatewayAdapt=glo2usa) | AliExpress


