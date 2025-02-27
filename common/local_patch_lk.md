# Patching LK (alternative method)

1. Go back to the **MTK Client** folder

2. Open the console again in **MTK Client** folder

   ![Image](/images/open_in_cmd.png)

3. Make sure your phone is powered off, hold down both **Vol+**, **Vol-** and connect the USB cable.

4. Run the command `python mtk r lk lk.bin` . There will now be a **lk.bin** file in **MTK Client** folder.

   ![Image](/images/get_lk.png)

5. Download [lkpatcher](https://codeload.github.com/R0rt1z2/lkpatcher/zip/refs/heads/master) and extract it. Navigate to the **lkpatcher folder**. It should contain a file **main.py**

   ![Image]()

6. Move **lk.bin** to **lkpatcher folder**. Open the console in **lkpatcher folder**

   ![Image]()

7. Run command `python main.py lk.bin -o lk-patched.bin` . A **lk-patched.bin** file will be created. Move it to **MTK Client** folder. 
   
   ❗ **If you get errors, use command** `python mtk r lk2 lk.bin` **in step 4**

8. Run command `python mtk w lk lk-patched.bin`