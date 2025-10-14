# static_housing

* Requires this system https://github.com/Shaco-uo/house_system
* Example of roomdef:

[ROOMDEF a_trinsic_councelors_guild_hall_1]  
EVENTS=r_town_minerals,r_town_water,r_default_tree,r_default_grass  
NAME=Trinsic Councelor's Guild Hall  
GROUP=Trinsic Housing  
FLAGS=region_flag_nobuilding|region_flag_insta_logout|region_antimagic_recall_in  
P=1810,2713,0,0  
RECT=1882,2827,1901,2846,0  
RECT=1902,2834,1910,2846,0  
RECT=1874,2834,1882,2846,0  
tag.value=600000  
tag.maxlockdowns=200  
tag.maxsecured=80  
tag.maxstorage=280 // (maxlockdowns+maxsecured)
tag.maxvendors=1  
tag.sign=04001bb4b  
tag.exit=1892,2847,20  // needed in case sign is located inside building. ejected & banned players will be kicked here (if empty will use sign location).   

* Usage
  - add tags to roomdef (value,maxlockdowns,maxsecured,maxstorage,maxvendors,exit). tag.exit is optional, in case sign is located inside of the proterty. this coord will be used for banish & eject player functions.
  - create sign on any roomdef (i_sign_static_house or i_sign_static_house2)
  - copy new sign uid to room tag.sign
