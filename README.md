# Kobra-max-setup
Kobra max setup

# setting up cura

# start with adding the plugins
![Screenshot 2025-06-02 222839](https://github.com/user-attachments/assets/55c25df5-cda9-4d0b-b65c-8bbac704e96d)

# then add the printer 

![image](https://github.com/user-attachments/assets/ff072211-a4d5-41db-82dd-cabd8c92e417)
![image](https://github.com/user-attachments/assets/fe55e9f6-5a4e-4fb4-8df3-1dcf0d83f285)
![image](https://github.com/user-attachments/assets/781da1c1-3ff8-4473-8c4b-5a7ee1f09e02)

#update the start and end macros

![image](https://github.com/user-attachments/assets/15860b8a-7203-42d6-b5dc-80e95d4f8c93)

Start print
```
M104 S140;start the nozzle preheat and don't wait
G90;absolute positioning
M82;set extruder to absolute mode
M355 S1 ;turn on the case light

START_PRINT

G92 E0.0 ; reset extruder
G90
G1 X0 Y-10 Z0.4 F6000.0
G1 X40 Y-10 E45 F300.0
G90
G92 E0.0 ; reset extruder
```

End print
```
G92 E0.0 ; reset extruder

END_PRINT

M355 S0 ;turn off the case light
G90;absolute positioning
M82;set extruder to absolute mode
SAVE_CONFIG
```

# then add the moonraker

![Screenshot 2025-06-02 224051](https://github.com/user-attachments/assets/a548d12f-a714-4e35-94e7-b7b6a28832da)

# Link: 
``` http://kobramax.local/ ```

![Screenshot 2025-06-02 224111](https://github.com/user-attachments/assets/35178177-2593-4cf2-bea9-ae9fea51fbee)
![Screenshot 2025-06-02 224204](https://github.com/user-attachments/assets/85c592fa-0a2f-4057-ab5b-4f405ecd14fc)
![Screenshot 2025-06-02 224231](https://github.com/user-attachments/assets/249b2344-20b7-49e2-bf05-f9e8d979d26c)

# Link: 
```http://kobramax.local/webcam/?action=stream ```

# now add the profile
![image](https://github.com/user-attachments/assets/6a726b6d-96d6-4326-8dd1-542da321da8f)
![image](https://github.com/user-attachments/assets/39323369-fd58-4b16-a5b7-2a711e3a27a6)
![image](https://github.com/user-attachments/assets/9a0ae071-c802-4602-8adf-08e7c0d4b6a7)


# to access the printer in a web browser go to:
```http://kobramax.local/```

you well need to run a few things after the printer is setup. 

![image](https://github.com/user-attachments/assets/19d5a3d8-8ee9-4dca-ba47-8e7f0f39f155)

attach the accelerator to the tool head with tape and plug it into the display USB.
make sure to have a long enough USB c to retch the far side of the x axis. 
make sure to have the USB C pointing to the display. 
open the printer.cfg under the machine tab
![image](https://github.com/user-attachments/assets/6b180ca8-3044-455c-bc81-998fa2d32d25)

remove the "#" from the [include BTT_LIS2DW_input_shaper.cfg] on line 18. then click "save and restart" in the top right.
![image](https://github.com/user-attachments/assets/3faacf76-2ec8-49af-97f8-7ec7e55490d7)

run the Input_Shaper_X command and wait for it to finish.

then move the accelerator to the bed with the USB C pointing to the display. 

run the Input_Shaper_Y command and wait for it to finish.

then click "save and restart" in the top right.

now that we have finished you can add the "#" back to [include BTT_LIS2DW_input_shaper.cfg] and remove the accelerator. 

then click "save and restart" in the top right.

that’s it you should be already to print. 




