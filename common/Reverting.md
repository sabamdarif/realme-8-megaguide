# Reverting

Use this to revert to stock RealmeUI 3 and lock the bootloader.

> **Tip**
> You will lose any personal data on the device. Make sure to have a backup before continuing.

---

## Contents
1. [Flashing stock firmware](/linux/Reverting.md#flashing-stock-rui-3)
2. [Locking bootloader](/linux/Reverting.md#locking-bootloader)

## Flashing stock RUI 3

1. Open the console in **MTK Client** folder

   ![Image](/images/open_in_cmd.png)

2. Send the payload with `python mtk payload` . It should look like this:

   ![Image](/images/mtk_payload_started.png)

3. Make sure your phone is powered off. Hold down **both** Vol+ Vol- and connect the USB cable.

4. MTK Client should output something like this:

   ![Image](/images/mtk_payload_done.png)

5. The phone is now in **BROM mode**. Run the SP Flash tool (flash_tool.exe)

6. Click on **Options** > **Connection**

7. Make sure the right **COM Port** is selected, UART is enabled, and baud rate is set to **921600**.

- **In Windows (It should Look Like This)**
   <p align="center"><img src="/images/sp_flash_port.png"></p>
- **In Linux (It should Look Like This)**
   <p align="center"><img src="/images/linux_spflash_port.jpg"></p>

8. Get **Stock RUI 3 firmware** and unpack it.

9. Load **scatter.txt** file from the **Stock Firmware**

   ![Image](/images/select_scatter_c.18.png)

10. Remember to have **Download Only** mode

   ![Image](/images/select_download_only.png)

11. Place your phone on a stable surface. Do not disconnect anything. This process will take up to **15-20 minutes**. To get a log on your phone, click below:
   
   [No progress? Click me](#)

12. If everything goes well, it should look like this:

   ![Image](/images/download_button.png)

---

## Locking bootloader

1. Make sure your phone is **off** and hold down **both** Vol+ Vol- (Don't leave the buttons until the command is done)

2. Type `python mtk w attestation_key.bin avb_custom_key.img` . This command will wipe your data and convert your phone. It should look like this:

   ![Image](/images/download_done.png)

3. Lock the bootloader using command: `python mtk seccfg lock`

