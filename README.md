# AI-Keys
A custom mechanical keyboard designed in KiCad, with a built-in AI function to ask AI a question. To make this yourself, check the information down below! ↓

# Special Thanks
This project was a ride of twists and turns, and I have to firstly credit AIVON for their support on this entire project! They willingly lowered the PCB cost to 100 dollars, just so this project would be able to continue! If you liked this project, please do check out their company at [aivon.com](aivon.com)! When I was first sifting through each of the possible PCB manufacturers, both JLCPCB and PCBWay gave me extremely expensive prices without even taking in the cost of the parts for the PCBA order! AIVON, however, supported me fully, and gave me a cost that fit right within my budget! Thank you so much AIVON, and thank YOU for taking the time to check out their exquisite company!

Moreover, I'd like to express my gratitude to the Hack Club community and organization! They are the reason why I started this perilous project in the first place, as they provided coverage on all of the parts, whilist their community provided all of their knowledge! Thank you, Hack Club! Please check them out at [hackclub.com](hackclub.com)! 

# Why I Made This Project
Honestly, after seeing macropads being made on Hack Club's Blueprint program, I realized that I wanted to create something bigger. Someting unique, that at the same time feels useful. So, I realized I wanted to create a big macropad: a keyboard. But, I didn't want to make any generic keyboard. After all, keyboard are nothing special. So, I added my own twist to it: AI! And the rest 

is

history.

# How it works
- The firmware runs on a ESP32-S3 DEVKIT C1, handing all of the logic to make the keyboard run.
- It can work with any Cherry-branded switch, but in particular it uses the Cherry MX Brown model.
- The LED strip embedded in the case utilizes a ws2812b strip. There is no particular model; however, the one I used had a red, black, and green wire for power and data.
- There is a decently sized battery to run the keyboard.
- To charge the battery, I created a charging circuit, which utilizes the MCP73831-2-MC and USB Type C VBUS input modules to charge the battery correctly. 
- To stabilize power flow to the ESP32, the keyboard uses a TPS63001 (buck convertor).
- The speaker runs on a MAX98357A, which is a module that controls the speaker to output the message the AI wants to speak out loud.

> [!TIP]
> Though a 3.7V battery is used for this project, you may use higher/lower voltages, in accordance to the [TPS63001's datasheet.](https://www.ti.com/product/TPS63001)

# BOM (Bill Of Materials)
Here's a dedicated BOM for creating this keyboard yourself:

| Part | Cost | Link/Download | Manufacturer/Retailer |
|------|------|------|----------------------|
| Cherry MX Brown Switches | $8.00 (with new user discount) | [Click Here](https://www.aliexpress.us/item/3256811880813653.html?spm=a2g0o.detail.0.0.3867UsiwUsiwu6&mp=1&pdp_npi=6%40dis%21USD%21USD+32.89%21USD+8.00%21%21USD+8.00%21%21%21%402101eede17807987748595335e2ac4%2112000057415897661%21ct%21US%217444042787%21%211%210%21&_gl=1*1651hzd*_gcl_aw*R0NMLjE3NzQxNTIyOTcuQ2owS0NRandtdW5OQmhEYkFSSXNBT25kS3BtZWJwVFNMSlp6Y2tCbWZrbUN5cmo0b0lSVUNOdUExRzBNODM4TWd6QUx5bHJhME04VzNBNGFBbHR0RUFMd193Y0I.*_gcl_au*MTY4NjExMjk2NC4xNzczODc0NTA1*_ga*MjAyMzU5Nzk2NC4xNzgwNzk4NjI3*_ga_VED1YSGNC7*czE3ODA3OTg2MjckbzEkZzEkdDE3ODA3OTg3NzQkajYwJGwwJGgw&gatewayAdapt=glo2usa) | AliExpress |
| Keycaps | $4.06 (with new user discount) | [Click Here](https://www.aliexpress.us/item/3256807174517233.html?spm=a2g0o.cart.0.0.314f38dabMcHQb&mp=1&pdp_npi=6%40dis%21USD%21USD+28.14%21USD+4.06%21%21USD+4.06%21%21%21%402103110517809574308387537ef602%2112000057896443594%21ct%21US%217444042787%21%211%210%21&_gl=1*1d189ad*_gcl_aw*R0NMLjE3Nzc3NTMyMzAuQ2p3S0NBand3ZGJQQmhCZ0Vpd0F4QlJBNGJVQ0tFZlZpZjBqYkZoaDBxQkh5anRleFZHblpLV01BbXdvQ1NITDMtdGtYVnBXREF1SjZCb0NzWU1RQXZEX0J3RQ..*_gcl_dc*R0NMLjE3Nzc3NTMyMzAuQ2p3S0NBand3ZGJQQmhCZ0Vpd0F4QlJBNGJVQ0tFZlZpZjBqYkZoaDBxQkh5anRleFZHblpLV01BbXdvQ1NITDMtdGtYVnBXREF1SjZCb0NzWU1RQXZEX0J3RQ..*_gcl_au*MTY4NjExMjk2NC4xNzczODc0NTA1*_ga*MjEwOTI4NjY5NS4xNzgwOTQzODE5*_ga_VED1YSGNC7*czE3ODA5NTczOTUkbzMkZzEkdDE3ODA5NTc4MjgkajYwJGwwJGgw&gatewayAdapt=glo2usa) | AliExpress |
| Screws | $1.07 (with new user discount) | [Click Here](https://www.aliexpress.us/item/3256805283136304.html?spm=a2g0o.cart.0.0.314f38dabMcHQb&mp=1&pdp_npi=6%40dis%21USD%21USD+1.88%21USD+1.07%21%21USD+1.07%21%21%21%402103110517809574308387537ef602%2112000033206512825%21ct%21US%217444042787%21%211%210%21&_gl=1*1rbt53m*_gcl_aw*R0NMLjE3Nzc3NTMyMzAuQ2p3S0NBand3ZGJQQmhCZ0Vpd0F4QlJBNGJVQ0tFZlZpZjBqYkZoaDBxQkh5anRleFZHblpLV01BbXdvQ1NITDMtdGtYVnBXREF1SjZCb0NzWU1RQXZEX0J3RQ..*_gcl_dc*R0NMLjE3Nzc3NTMyMzAuQ2p3S0NBand3ZGJQQmhCZ0Vpd0F4QlJBNGJVQ0tFZlZpZjBqYkZoaDBxQkh5anRleFZHblpLV01BbXdvQ1NITDMtdGtYVnBXREF1SjZCb0NzWU1RQXZEX0J3RQ..*_gcl_au*MTY4NjExMjk2NC4xNzczODc0NTA1*_ga*MjEwOTI4NjY5NS4xNzgwOTQzODE5*_ga_VED1YSGNC7*czE3ODA5NTczOTUkbzMkZzEkdDE3ODA5NTc4MzMkajU1JGwwJGgw&gatewayAdapt=glo2usa) | AliExpress |
| Speaker | $1.79 | [Click Here](https://www.aliexpress.us/item/3256810115882464.html?spm=a2g0o.productlist.main.3.1c4770aaXj358I&algo_pvid=05803776-df63-4004-811b-f96645264995&algo_exp_id=05803776-df63-4004-811b-f96645264995-2&pdp_ext_f=%7B%22order%22%3A%2289%22%2C%22eval%22%3A%221%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%213.80%211.79%21%21%2125.62%2112.04%21%402103119c17810220116342671eda13%2112000051857429948%21sea%21US%217444042787%21ABX%211%210%21n_tag%3A-29910%3Bd%3A90eb6f52%3Bm03_new_user%3A-29895&curPageLogUid=53rDJIL29Yji&utparam-url=scene%3Asearch%7Cquery_from%3A%7Cx_object_id%3A1005010302197216%7C_p_origin_prod%3A) | AliExpress |
| Stabilizers | $3.90 (with new user discount) | [Click Here](https://www.aliexpress.us/item/3256808467378574.html?spm=a2g0o.productlist.main.25.611988d5qsDRjT&utparam-url=scene%3Asearch%7Cquery_from%3Apc_back_same_best%7Cx_object_id%3A1005008653693326%7C_p_origin_prod%3A&algo_pvid=9aa42880-7c63-4fb3-a69f-cd53cbdbe0be&algo_exp_id=9aa42880-7c63-4fb3-a69f-cd53cbdbe0be&pdp_ext_f=%7B%22order%22%3A%22658%22%2C%22fromPage%22%3A%22search%22%7D&pdp_npi=6%40dis%21USD%213.28%210.99%21%21%2122.12%216.69%21%402101e62517810456934902870ed594%2112000046108045634%21sea%21US%217444042787%21ABX%211%210%21n_tag%3A-29910%3Bd%3A90eb6f52%3Bm03_new_user%3A-29895%3BpisId%3A5000000207344158&gatewayAdapt=4itemAdapt) | AliExpress
| Battery | $6.99 | [Click Here](https://www.amazon.com/EEMB-Battery-1200mah-Rechargeable-Connector/dp/B095VLH7HH/ref=sr_1_33?crid=3LTPXUNFSL1H2&dib=eyJ2IjoiMSJ9.yzncPlLgBOElqyyD_AHjWi0XCE2cH5nM_aoar_z6utO235q2piB2vPx0Lkwnq-jo5C4KMkzPiIIB1B2oWLezYpffE8VN-iXMCQgdTZyasjuCFs6ZOoIepHciTg7uWAB4z21qVQBoOe4AGkSWcSU5GLpYg5IQxDTu_LMSvHhbU-FUiYPT6P4CRjdc-dYjqhMcm8HQDlblicwicBwq0kuZF6cIoiE9fMBuMAjFZdPz2lQclbqCJjRrCqCgk2Rzedoy2PTtt3zONe-CQocY-2lOUukLWB5ObK77yubgVDDyRBI.ZfZKIiW-WOy1M8UR0ps4kvVUrGPg8uEIUDr9ZFjfKZI&dib_tag=se&keywords=3.7%2BVolt%2BRechargeable%2BBattery&qid=1773185173&sprefix=3.7%2Bvolt%2Brechargeable%2Bbattery%2Caps%2C221&sr=8-33&th=1) | Amazon |
| XFL4020-222MEC (inductor for TPS63001) | $2.47 | [Click Here](https://www.coilcraft.com/en-us/products/power/shielded-inductors/molded-inductor/xfl/xfl4020/xfl4020-222/?srsltid=AfmBOoqs8osaTAfdjHIyioyBk3GpIvO1-Iu_L-rxJIhnwW51TJ0jehTB) | Coilcraft |
| MCP73831-2-MC | $0.79 | [Click Here](https://www.digikey.com/en/products/detail/microchip-technology/MCP73831-2ATI-MC/1874109?curr=usd&utm_campaign=buynow&utm_medium=aggregator&utm_source=octopart) | DigiKey |
| MAX98357A | $4.75 | [Click Here](https://www.lcsc.com/product-detail/C23890844.html) | LCSC |
| USB VBUS TYPE-C | $0.94 | [Click Here](https://www.lcsc.com/product-detail/USB-Type-C_Korean-Hroparts-Elec-TYPE-C-31-M-12_C165948.html) | LCSC |
| Resistors and Caps | $5.66 | [Click Here](https://justpaste.it/oabiu) | LCSC |
| TPS63001 | $2.27 | [Click Here](https://www.ti.com/product/TPS63001?utm_source=google&utm_medium=cpc&utm_campaign=app-null-null-GPN_EN-cpc-pf-google-ww_en_cons&utm_content=TPS63001&ds_k=TPS63001&DCM=yes&gclsrc=aw.ds&gad_source=1&gad_campaignid=1767856010&gbraid=0AAAAAC068F02XRLVUVn1qaOX6xrOvtP0y&gclid=Cj0KCQjwrZTRBhDSARIsAHidYfcO2jmQQrtSjZ0xPVh3lzhPpcKTbKZK_XgQGUQXxEWHeZcUr_cTREwaAqqhEALw_wcB#order-quality) | Texas Instruments |
| PCB | Depends On Manufacturer | [Click Here Or Check Repo Files](https://github.com/user-attachments/files/28724171/gerbers.zip) | Any PCB Manufacturer |
| Case | Depends On Manufacturer/Manufacturing Device | [Click Here Or Check Repo Files](https://github.com/user-attachments/files/28766007/Case.Files.zip) | Any Fabrication Device/Company 

> [!IMPORTANT]
> The PCB doesn't have a link to a product page; instead, it downloads gerbers.zip. Don't unzip it; instead, go to a PCB manufacturer's page (such as [aivon.com](aivon.com)) and drop the zip into its "gerber file uploader."
> The "gerber file uploader" should look like something similar or exactly like this:
> 
> <img width="822" height="140" alt="Screenshot 2026-06-09 at 10 54 21 AM" src="https://github.com/user-attachments/assets/d45b8928-c98f-4327-84a0-f5eb3a830705" />
>
> ### The case's zip file, however, contains an STL and a STEP file, so please unzip it.

And finally, the best part... ↓

# Assembly!
1. Install KiCad and Arduino IDE. (they'll be important!)
2. Solder on all parts to their respective locations, as noted in the schematic file.
3. Install the stabilizers into each of their respective holes.
4. Install the keycaps onto each of the switches.
5. Upload the firmware onto the ESP32-S3 using Arduino IDE.
6. Happy typing/asking!

# Images (for your convenience :)

The full schematic:
<img width="1815" height="998" alt="Screenshot 2026-06-09 at 11 51 33 AM" src="https://github.com/user-attachments/assets/f571704b-8f46-4123-a21e-e8f62c49c475" />

The charging portion of the schematic:
<img width="1747" height="1094" alt="Screenshot 2026-06-09 at 11 55 13 AM" src="https://github.com/user-attachments/assets/f59d817b-338e-42de-ae5b-0e46e5bfdd9f" />

The keyboard portion of the schematic:
<img width="1525" height="813" alt="Screenshot 2026-06-09 at 11 55 46 AM" src="https://github.com/user-attachments/assets/1ce6e5d7-9521-4e89-9df8-516b1631125b" />


The ESP32-S3 portion of the schematic:
<img width="1326" height="932" alt="Screenshot 2026-06-09 at 11 56 19 AM" src="https://github.com/user-attachments/assets/29e8a175-f2ac-484d-b17a-7aad9dd8fa3b" />


The full routed PCB:
<img width="1700" height="713" alt="Screenshot 2026-06-09 at 11 56 41 AM" src="https://github.com/user-attachments/assets/68006e2f-9e2d-4be2-aeec-4ff79b7da905" />

Assembled Build:

Coming soon! I have yet to finish building the keyboard itself 😅, so I'll post the image after it's complete!
