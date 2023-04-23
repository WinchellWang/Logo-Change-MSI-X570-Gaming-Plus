# Logo Change MSI X570 Gaming Plus
Software to change the bios logo for MSI X570 Gaming Plus

Source: https://github.com/LongSoft/UEFITool & AMI Change Logo Tool

# Software Requirements

There are two softwares have the capacity to replace the logo, but only one that I have tried.

- [UEFITool](https://github.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/releases/tag/ChangeLogo)

- [AMI ChangeLogo Tool](https://github.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/releases/tag/ChangeLogo) **(Did not Test)**

# Procedure

1. Download bios file from [MSI website](https://us.msi.com/Motherboard/MPG-X570-GAMING-PLUS/support), and extract it. **BIOS file usually have AE0, AJ0... as the suffix.**

2. Extract the ROM by [AMI ChangeLogo Tool](https://github.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/releases/tag/ChangeLogo)

    2.1 Load ROM

    Please change the 'Files of type' to 'All Files (\*.*)', if thr ROM does shows up in the selection.

    <img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/open_changelogo.jpg">

    2.2 Extract ROM

    **More importantly, check the image type**

    Just need to chose the first one with suffix, and click "Save Logo". The image usually will converted to jpg type.

    <img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/check_img_type.jpg">

    Default BIOS logo extracted from ROM. <mark>(The actual format is bmp in this ROM)</mark>

    <img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/splash.jpg"  width="50%">

3. Modify Logo

    I would suggest that the new logo should keep the same size as the original. X570 does allow a larger image, but there is no guarantee that it will display properly.

    Here I changed it to a Microsoft logo as an example.

    <img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/img_save.jpg">

    Then export the image as bmp. It would be fine if just keep the default setting when save the image.

    <img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/exp_opt.jpg"  width="60%">

4. Replace the logo in ROM by [UEFITool](https://github.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/releases/tag/ChangeLogo)

    4.1 Load ROM

    $$
    File\Rightarrow Open\ image\ file\ \mathbb{OR}\ Ctrl+O
    $$

    Chose to 'All files', if the rom does not show up in the selection window.

    4.2 Locate logo file in ROM

    Ctrl + F to open the search box, and switch to Text option. Search 'logo', and it will show you all the logo files location.

    <img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/uefi_logo_search.jpg">

    4.3 Replace the images in ROM

    ROM for MSI usually contains more than 1 logo, so we have to change all of them, since I tried to only change few of them and it would not show the correct image during launch.

    Double click each line in Messages box to jump into the files location, as we are looking for the file which has a section named 'Raw' OR 'Freeform subtype GUID'

    <img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/rpl_rom_img_1.jpg">

    Then right click the section, and replace the body to your logo.bmp. The software will show something like Rebuild, Remove, and Replace in the section you are changing at the Section column.

    <img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/rpl_rom_img_2.jpg">

    There are 4 images should be replaced in the ROM, if you are changing the logo for MSI X570 Gaming Plus. 

    4.4 Export the new ROM

    $$
    File\Rightarrow Save\ image\ file\ \mathbb{OR}\ Ctrl+S
    $$

    **Please name the new image exactly same as the original file.**

    >Show the file name extensions in explorer, so you can truly change file suffix.

5. Flash the new BIOS by following this [tutorial/SOP](https://storage-asset.msi.com/files/pdf/How_to_flash_the_BIOS.pdf).
    
# Results

My new logo :D

<img src="https://raw.githubusercontent.com/MoaxWang/Logo-Change-MSI-X570-Gaming-Plus/main/jpg/launch.gif"  width="50%">
