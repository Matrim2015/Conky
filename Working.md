##################################
## VinDSL | rev. 10-11-28 13:30 ##
##Malach edit-02182015 Don't forget the feh and fonts#
##################################

#!/bin/bash
#start Conky with a 55 second delay
#sleep 55
#conky -c ~/toshiba/.conkyrc
####
## Use XFT? Required to Force UTF8 (see below).
#
use_xft yes
xftfont LiberationSans:size=7.85
xftalpha 0.1
text_buffer_size 2048

####
## Force UTF8? Requires XFT (see above).
## Displays degree symbol, instead of Â°, etc.
#
override_utf8_locale yes

####
## Update interval in seconds.
#
update_interval 1.5

####
## This is the number of times Conky will update before quitting.
## Set to zero to run forever.
#
total_run_times 0

####
## Create own window instead of using desktop (required in nautilus)?
#
own_window yes
own_window_type normal
own_window_transparent yes
own_window_hints undecorated,below,sticky,skip_taskbar,skip_pager
own_window_argb_visual yes
own_window_argb_value 0
####
## Use double buffering? Reduces flicker.
#
double_buffer yes

####
## Draw shades?
#
draw_shades no

####
## Draw outlines?
#
draw_outline no

####
## Draw borders around text?
#
draw_borders no

####
## Draw borders around graphs?
#
draw_graph_borders no

####
## Print text to stdout?
## Print text in console?
#
out_to_ncurses no
out_to_console no

####
## Text alignment.
#
alignment bottom_left

####
## Minimum size of text area.
#
minimum_size 235 0

####
## Specify width and height for bars.
#
default_bar_size 0 4

####
## Gap between text and screen borders.
#
gap_x 10
gap_y 10

####
## Shorten MiB/GiB to M/G in stats.
#
short_units yes

####
## Pad % symbol spacing after numbers.
#
pad_percents 0

####
## Limit the length of names in "Top Processes".
#
top_name_width 10

####
## Subtract file system -/+buffers/cache from used memory?
## Set to yes, to produce meaningful physical memory stats.
#
no_buffers yes

####
## Set to yes, if you want all text to be in UPPERCASE.
#
uppercase no

####
## Number of cpu samples to average.
## Set to 1 to disable averaging.
#
cpu_avg_samples 2

####
## Number of net samples to average.
## Set to 1 to disable averaging.
#
net_avg_samples 2

####
## Add spaces to keep things from moving around?
## Only affects certain objects.
#
use_spacer right

####
## My colors (suit yourself).
#
color0 White
color1 Ivory
color2 Ivory2
color3 Ivory3
color4 4168B4
color5 Tan2
color6 Gray
color7 AntiqueWhite4
color8 DarkSlateGray
color9 Black

####
## Installed fonts (required).
#
# ConkyWeather (Stanko Metodiev)
# ConkyWindNESW (Stanko Metodiev)-
# Liberation Mono (Ascender Corp)-
# Liberation Sans (Ascender Corp)-
# Moon Phases (Curtis Clark)-
# OpenLogos (Icoma)-
# PizzaDude Bullets (Jakob Fischer)-
# Radio Space (Iconian Fonts)-
# StyleBats (Vinterstille)-
# Ubuntu (Canonical Ltd)
# Ubuntu Title Bold (Paulo Silva)-
# Weather (Jonathan Macagba)-
# WenQuanYi Micro Hei (Google Corp)

TEXT

##################
##     LOGO     ##
##################
${font RadioSpace:size=20}${color4}Bodhi Linux 3.0.0
##################
##    SYSTEM    ##
##################
${voffset 10}${font WenQuanYiMicroHei:bold:size=7.75}${color4}SYSTEM${offset 8}${color8}${hr 2}
${voffset 4}${font OpenLogos:size=10}${color4}B${voffset -4}${font}${color6}${offset 5}${sysname}${offset 5}${kernel}${alignr}${machine}
${voffset 2}${font StyleBats:size=10}${color4}A${voffset -1}${font}${color6}${offset 5}Intel Core 2 Duo${alignr}${freq_g cpu0}${offset 1}GHz
${voffset 2}${font StyleBats:size=10}${color4}q${voffset -1}${font}${color6}${offset 5}Uptime${alignr}${uptime}
${voffset 2}${font StyleBats:size=10}${color4}o${voffset -1}${font}${color6}${offset 5}File System${alignr}${fs_type}
${voffset 2}${font weather:size=18}${color4}y${voffset -8}${font}${color6}${offset 5}  Core 1${alignr}${hwmon 1 temp 2}${font}°C
${voffset 2}${font weather:size=18}${color4}y${voffset -8}${font}${color6}${offset 5}  Core 2${alignr}${hwmon 1 temp 3}${font}°C
${voffset 2}${font weather:size=18}${color4}y${voffset -8}${font}${color6}${offset 5}  GPU${alignr}${nvidia temp}${font}°C
${voffset 2}${font weather:size=18}${color4}y${voffset -8}${font}${color6}${offset 5}  HDD${alignr}${hddtemp /dev/sda}${font}°C
##################
##  PROCESSORS  ##
##################
${voffset 6}${font WenQuanYiMicroHei:bold:size=7.75}${color4}PROCESSORS${offset 8}${color8}${hr 2}
${voffset 2}${font StyleBats:size=10}${color4}k${voffset -2}${font}${color6}${offset 2}CPU1${offset 5}${cpu cpu1}%${color7}${alignc 34}${cpubar cpu1}
${voffset 2}${font StyleBats:size=10}${color4}k${voffset -2}${font}${color6}${offset 2}CPU2${offset 5}${cpu cpu2}%${color7}${alignc 34}${cpubar cpu2}
${cpugraph 000000 0236FD -l}
##################
##    MEMORY    ##
##################
${voffset 6}${font WenQuanYiMicroHei:bold:size=7.75}${color4}MEMORY${offset 8}${color8}${hr 2}
${voffset 2}${font StyleBats:size=10}${color2}l${voffset -2}${font}${color6}${offset 3}RAM${goto 95}${mem}${offset 5}/${offset 5}${memmax}${alignr}${memperc}%
${color7}${membar}
##################
##     HDD      ##
##################
${voffset 2}${font WenQuanYiMicroHei:bold:size=7.75}${color4}HDD${offset 8}${color8}${hr 2}
${voffset 2}${font StyleBats:size=10}${color2}x${voffset -2}${font}${color6}${offset 4}ROOT${goto 95}${fs_used /}${offset 5}/${offset 5}${fs_size /}${alignr}${fs_free_perc /}%
${color7}${fs_bar /}
${voffset 1}${font StyleBats:size=10}${color2}x${voffset -2}${font}${color6}${offset 4}HOME${goto 95}${fs_used /home}${offset 5}/${offset 5}${fs_size /home}${alignr}${fs_free_perc /home}%
${color7}${fs_bar /home}
${voffset 1}${font StyleBats:size=10}${color2}4${voffset -2}${font}${color6}${offset 4}SWAP${goto 95}${swap}${offset 5}/${offset 5}${swapmax}${alignr}${swapperc}%
${color7}${swapbar}
##################
# TOP PROCESSES ##
##################
${voffset 3}${font WenQuanYiMicroHei:bold:size=7.75}${color4}TOP PROCESSES${offset 8}${color8}${hr 2}
${voffset 2}${font StyleBats:size=10}${color1}h${voffset -3}${font}${color6}${offset 5}${top_mem name 1}${goto 115}${top_mem mem_res 1}${alignr}${top_mem mem 1}%
${voffset 2}${font StyleBats:size=10}${color1}h${voffset -3}${font}${color6}${offset 5}${top_mem name 2}${goto 115}${top_mem mem_res 2}${alignr}${top_mem mem 2}%
${voffset 2}${font StyleBats:size=10}${color1}h${voffset -3}${font}${color6}${offset 5}${top_mem name 3}${goto 115}${top_mem mem_res 3}${alignr}${top_mem mem 3}%
${voffset 2}${font StyleBats:size=10}${color1}h${voffset -3}${font}${color6}${offset 5}${top_mem name 4}${goto 115}${top_mem mem_res 4}${alignr}${top_mem mem 4}%
##################
##   NETWORK    ##
##################
${voffset 6}${font WenQuanYiMicroHei:bold:size=7.75}${color4}NETWORK${offset 8}${color8}${hr 2}
${voffset 2}${font PizzaDudeBullets:size=10}${color2}a${font}${color6}${offset 5}Private IP${alignr}${addr wlan0}
${font PizzaDudeBullets:size=10}${color2}a${font}${color6}${offset 5}Public  IP${alignr}${execi 600 wget -q -O - checkip.dyndns.org | sed -e 's/[^[:digit:]\|.]//g'}
${voffset 4}${font PizzaDudeBullets:size=10}${color2}T${font}${color6}${offset 5}Down${alignr}${downspeed wlan0}
${font PizzaDudeBullets:size=10}${color2}N${font}${color6}${offset 5}Up${alignr}${upspeed wlan0}
${voffset 4}${font PizzaDudeBullets:size=10}${color2}T${font}${color6}${offset 5}Downloaded${alignr}${totaldown wlan0}
${font PizzaDudeBullets:size=10}${color2}N${font}${color6}${offset 5}Uploaded${alignr}${totalup wlan0}
##################
##   WEATHER   ##
##################
##################
##     TIME     ##
##################
${voffset 6}${font WenQuanYiMicroHei:bold:size=7.75}${color4}TIME${offset 8}${color8}${hr 2}
${voffset -4}${if_match ${time %l}<=9}${font RadioSpace:size=20}${color3}${alignc 2}${time %l:%M%p }${else}${if_match ${time %l}>=10}${font RadioSpace:size=20}${color3}${alignc 2}${time %l:%M%p}${endif}${endif}
##################
##   CALENDAR   ##
##################
${voffset 5}${font WenQuanYiMicroHei:bold:size=7.75}${color4}DATE${offset 8}${color8}${hr 2}
${voffset 4}${font LiberationSansBold:size=9.6}${color4}${alignc 5}${execpi 60 VinDSL_Cal= date +'%B${offset 6}%Y'}
${voffset 3}${font LiberationMono:size=9.5}${color3}${execpi 60 VinDSL_Cal_9=`date +%-d`; cal -h | sed -e 's/\r//g' -e 's/^/ /g' -e '1d' -e s/^/"\$\{offset 40"\}/ -e 's/\<'"$VinDSL_Cal_9"'\>/${color4}&${color3}/'}
