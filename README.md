#HOW to make a OvOy Live Wallpaper

##Setup and Prerequisites
1. Live2d/Spine anime Editor
2. Download OvOy Live Wallpaper from Google play (version 0.853.* or above)

##Prepare your project folder
Your project folder should contain below files.

1. Spine asset.
Export your spine asset with json format including three files:
xxx.atlas
xxx.json
xxx.png

NOTE1: Please refer to [HOW-to export your spine asset]
NOTE2: Live2d (TBD)


2. [My_Model_name].model.json
Configure the properties in model.json
'''
{
	"type":"spine",
    "atlas":"owl_F_S.atlas",  // your spine atlas file
    "jason":"owl_F_S.json",   // your spine json file
    "skin":"default", // your spine skin
    "background":"background.png", //background image
    "locatearea":["50", "210", "900", "512"],  //define the area where your actor will be located
    "defaultRight":false, //if your actor facing right direction.
    "spine_height":"1157",  //refer to your spine json
    "spine_actor_screen_ratio":"0.2", //default actor size according to device screen height

    //define below animations for each OvOy Wallpaper state
    "IWP_STATE_HAPPY":["Wonder"],
    "IWP_STATE_TALKING":["Idle", "Hand-wave"],
    "IWP_STATE_IDLE":["Idle"],
    "IWP_STATE_WALKING":["L_Walk"],
    "IWP_STATE_WALKING2":["R_Walk"],
    "IWP_STATE_SAD_BORING":[],
    "IWP_STATE_EXCITING":[],
    "IWP_STATE_GOT_NOTIFY":["Hand-wave"],
    "IWP_STATE_RUNNING":["L_Fly"],
    "IWP_STATE_RUNNING2":["R_Fly"],
    "IWP_STATE_DIG":["L_Peck"],
    "IWP_STATE_DIG2":["R_Peck"],
    "CAMPAIGN_LIKE":["Hand-wave"],
    "CAMPAIGN_DISLIKE":["L_Peck"],
    "CAMPAIGN_COMMENT":["R_Walk"]
}

'''

3. edit behavior.lua to custom your behavior of Actor
4. provide the background image file which is defined in #2
5. provide dialog image


##HOW-to export your spine asset