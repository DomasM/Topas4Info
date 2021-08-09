---
layout: page
title: Changelog
permalink: /changelog/
---


**All fixes/ new features/ changed behaviors are listed from the most important to the least important**


**Currently version numbers are the same for Topas4Server and WinTopas4 (simultaneous release)**

## Abbreviations
* (C)-Client (WinTopas4): applies only to client application
* (S)-Server (Topas4 Server): applies only to server application
* (FN)-Fixed new: describes correct behavior after bug fix
* (FO)-Fixed old: describes wrong behavior before bug fix
* (PA)-Public API: applies to public API
* beta : auto-updates active only for PCs in Light Conversion local area network


## 1.127.0 (2021-08-09)(beta)

### New Feautures
1.(S) Try to disable 'Idle Power Saving' for Usb<>Eth adapters that are used for communication with Eth motor boards

## 1.126.0 (2021-08-09)(beta)

### Fixes
1.(S) Tweak temperature and humidity and sensors readout to avoid unstable operation in certain situations

### Changed behaviours

1.(S) Block usage of Eth motor boards with addreses 10.1.1.0-2 if device is not whitelisted (Warning since 1.121.0)

## 1.125.1 (2021-08-03)(beta)

### Fixes
1.(S)(FO) Topas4Server will likely fail to monitor ethernet interface changes

## 1.125.0 (2021-08-02)(beta)

### Fixes
1.(S)(FO) Topas4Server might not exit if launched multiple times and update is ready


## 1.124.0 (2021-08-02)(beta)

### Fixes
1.(S)(FO) Topas4Server enters infinite loop on startup if Eth motor board motor is in 'ThermalShutdown'' state and can't leave 'Busy' state 

### New Feautures
1.(C) Add Cronus-3P demo configuration to Tools>Launch New Demo Device menu

## 1.122.0 (2021-07-02)(beta),  (2021-07-09)(public)
### Fixes
1.(S)(FO) Eth motor board communication tweaks (UDP ports exhaustion)
### New Feautures
1.(S) Backup device config zip to cloud



## 1.121.0 (2021-07-01)(beta)
### Changed behaviours

1.(S) Warn user if Eth motor boards with addreses 10.1.1.0-2 are used and device is not whitelisted


## 1.120.1 (2021-06-18)
### New Feautures
1.(S) Track installed .Net Framework version

## 1.120.0 (2021-06-17)(beta)

### New Feautures
1.(C) Add DFX interaction.  It works the same way as DFG but with IDL instead of SIG.

## 1.119.3 (2021-06-07)(beta), (2021-06-17)(beta)


### Fixes
1.(S)(FO) Motor reset does not work if zero offset (recalculated to microsteps) is bigger than max position
1.(C)(FO) Tools>Manage Eth motor boards>Configure and debug does nothing if board name is empty


## 1.119.0 (2021-05-26)(beta)

### Fixes
1.(S)(FO) Strange shutter behaviour when connected to Eth motor board and setting wavelength while shutter is open

### New Feautures
1.(C) Tool to setup new Eth motor boards for use with WinTopas4, extended motor boards address space from 256 to about 50k adresses
2. Implicit Eth motor board naming in Motorjs.json ('auto') 
2.(S) New firmware for Eth motor board (5.5.0)



## 1.118.4 (2021-05-17)(beta), (2021-05-21)(public)

### Fixes

1.(C) Incease IGeneralService client timeout to 10 seconds because save device config as zip file timeouts sometimes (temporary fix)
1.(S) Update dependencies to solve issues with HtmlAgilityPack mismatch

## 1.118.1 (2021-05-14)(beta)

### Fixes
1. (FO) No warnings for trailing and leading whitespaces in optical and separation configuration interaction names.

## 1.118.0 (2021-05-04)(beta)

### Fixes
1. (C)(FO) Can't save device configuration to zip file and access some other functions if device has hardware failure  (since v1.99.0)
1. (S)(FO) Laser location REST method might never return in some circumstances - laser location in WinTopas4 shows no lasers

### Changed behaviours
1. (C) Changed 'Hardware failure' to "Connection to device lost" in some places. Tentative


## 1.117.0 (2021-04-29)(beta)


### Fixes
1. New bootloader for Eth motor board (4.16.0) - fix IP address saved in memory not honored by bootloader, reverts to DIP switches
1. (C)(FN) Eth motor board configuration and debug tool correctly handles board in bootloader mode

## 1.116.0 (2021-04-27)(beta)

### New Feautures
1. (C) Add Eth motor board configuration and debug too


### Fixes
1. Fix integrated power meters with wavelength calibration math
1. (S)(FN) Motor reset always return correct difference between expected and actual steps till switch, not just for subsequent resets from Testing Workbench
1. (C)(FO) If motor settings pop-up is opened in via right click on motor control, it is impossible to enter 'i' and 'k' letters in any textboxes 
1. (S) Further tweaks to laser output control when used together with OPA shutter


## 1.115.0 (2021-04-16)(beta)

### Fixes
1. (C)(FO) Closing v1.114.0 update notice window closes application
1. (S) Eth motor board firmware update to 5.2.2, bootloader to 4.14.0


## 1.114.0 (2021-04-15)(beta)

### Changed behaviours

1. (S) Server application runs minimized to tray
1. (C) Change forbidden ranges generation logic to exclude separation configuration 
1. Add 'Opera-F' as valid device model

### New Feautures

1. (S) Add piezo actuators support (direct voltage control and slip-stick)
1. (C) Expand Motors->Add\Remove\Reorder capabilities: configure motor boards, comboboxes for some motor properties, add piezo motor buttons
1. (S) Track strange motor end switch changes (when motor is not moving)

### Fixes
1. (S)(FO) Shutter/laser shutter might change state erratically when sending multiple requsts to change shutter state 
1. (C)(FO) Motors->Add\Remove\Reorder deleting motor might change motor board index for other motors





## 1.112.0 (2021-04-02)(beta)

### Fixes
1. (S)(FO) Changing shutter state might cause shutter flag to travel through beam even if using laser's output control to avoid that

### New Feautures

1. (S) Track ethernet interfaces count if using Eth motor boards
1. (C) Allow server activation in Selfhosts Manager


## 1.111.0 (2021-03-31)

### First public release since 1.97.0, show UI changes notification

## 1.110.0 (2021-03-25)(beta)

### New Feautures

1. Forbidden ranges generation from optical configuration and named motor positions
1. (C) Other changes related to forbidden ranges: global enable, global disable, any disabled ranges warning
1. (S) Support for position sensors used with Eth motor board shutters

### Fixes

1. (FO) Required Access Level for motor is not persisted anywhere (and never was!!)
1. (FO)(C) Tools>Self hosts>Manage devices might crash or leave servers in inconsistent  state (various cases fixed)
1. (FO)(C) Tools>Topas3>Convert Topas3 Configuration, launch server as demo, save device as zip, launch as real device from this zip: USB-board specific motor parameters are lost, all motors will fail to move (introduced in 1.42.0)



### Fixes

## 1.109.0 (2021-03-24)(beta)


### New Feautures

1.(C) User interface for additional shutters 


## 1.107.0 (2021-03-17)(beta)

### Fixes
1. (FO)(S) When output of one device is used by another shutter of secondary device will be closed but not opened if setting wavelength for primary device with small wavelength difference (as shutter is not closed for primary device)
2. (FO)(S) Topas4Server might not exit cleanly and leave zombie process if Eth motor board is used and there has been 'Hardware Failure'

### Changed behaviours
1. (C) Revert to motor curve view which shows both chart and table view


## 1.106.0 (2021-03-12)(beta)


### New Feautures

1. Many additional configuration options for integrated power meters

### Changed behaviours
1. (C) General UI tweaks

## 1.105.0 (2021-03-04)(beta)


### Fixes
1. (FO)(S) Power as measured by internal power meters/diodes is incorrectly divided by laser pulse picker



## 1.104.0 (2021-02-26)(beta)


### Fixes
1. (FN) Add A0 and A1 sockets as valid selections for Eth motor board diode sensors


## 1.103.0 (2021-02-22)(beta)


### Changed behaviours
1. (S) Ground-up shutter behaviour changes when output of one device is used by another. Shutter control is now synced to primary device. Shutter is closed for secondary device when leaving such interaction in primary device. 

### Fixes
1. (S)(FO) If other device curve is used in calibration other device might show 'Waiting for user' message while main device thinks that wavelenght setting has been completed


## 1.102.0 (2021-02-11)(beta)

### New Feautures

1. Reference-only power meter: add PowerScanner measurement file to OPA, expected output power is shown when wavelength is set
1. Linked devices for shutter control: close shutter for other devices when motor is homing or in forbidden range
1. Add optical configuration sanity checks for GDD calibration curves 

### Fixes
1. (C)(FO) In 'Shutter is closed for safety reasons' tooltip duplicate reasons might appear


## 1.101.0 (2021-01-29)(beta)

### Changed behaviours

1. (C) Add units indicator near wavelength textbox
1. (C) Ask user whether he  wants to set wavelength using any interaction if selected interactions do not support selected wavelength
1. (C) Change textbox style
1. (C) Change format of current output info in 'Main' tab
1. (C) Replace cm-1 with superscripted version everywhere
1. (C) Align pump laser controls with shutter and wavelength controls
1. (C) Other UI tweaks


## 1.99.0 (2021-01-24)(beta)

### Changed behaviours

1. (C) 'Misc' tab reorganized and moved to Output control settings
1. (C) Saved motor positions are not available in User access level
1. (C) Reorganized 'Main' tab: no expanders in User access level
1. (C) Image tooltip in messages no longer shown if image is already quite big
1. (C) 'Main' and 'Misc' selector no longer visible in User access level

### Fixes
1. (C) Motors section might contain only one column of motors with lots of white space instead of two columns

## 1.98.0 (2021-01-22)(beta)

### Fixes

1. (C)(FO) Motor super units range min and range max might be reset to default values (tentative fix)

### Changed behaviours

1. Motor control tweaks

### New Feautures

1. When shutter is closed for safety reasons they are listed in indicator tooltip


## 1.97.0 (2021-01-13)

### Changed behaviours

1. New icons


## 1.96.0 (2020-12-30)(beta)

### New Feautures

1. Each optical configuration can be assigned required pump laser preset. Shutter cannot be opened if currently active laser preset is incorrect or there is no communication with laser


## 1.95.1 (2020-12-23)(beta)

### Fixes
1. (S)(FN) Timeout for communication with Eth motor board increased



## 1.95.0 (2020-12-14)(beta)

### Changed behaviours

1. (C) 'Enter wavelength' text displayed instead of -1 when wavelength is not set
1. (C) Focus wavelength textbox hotkey changed to Alt+D
1. (C) Change views in mini mode hotkey changed to Alt+D


## 1.94.0 (2020-12-11)(beta)

### New Feautures

1. (S) Support for Ophir, Fode power meters
1. Power meter value latching, reference curve selection by named motor position and power logging
1. (S) Support for Pharos2 and Pharos+HBPC laser control from WinTopas4


## 1.93.0 (2020-12-08)(beta)

### New Feautures
1. UI for laser control configuration
1. Extended laser control capabilities: preset selection, go to standby, show current status
1. (S) Support for mixed-hardware shutters (use USB motor board and  Eth motor board shutters in the same device)

### Changed behaviours
1. (C) Adjustment mode in laser controls changes not only attenuator but pulse picker too


## 1.92.2 (2020-12-03)(beta)

### Fixes
1. (C)(FO) WinTopas4 installer contains corrupt drivers for USB motor board

## 1.92.1 (2020-11-23)(beta)

### New Feautures
1. (C) Motors panel is resized in fixed increments

### Changed behaviours
1. Target .Net 4.6.2 framework


## 1.90.0 (2020-11-09)(beta)

### New Feautures
1. Integrated power meters: calibration by wavelenght and interaction, conditional enable, live comparision with reference data 

### Fixes
1. (C) Delete oversized tracelog for WinTopas4 on application startup
2. (S)(FN) Tweak UDP communication to avoid misaligned query-response pairing
3. (S)(FN) Bump Eth motor board firmware to 4.3.0, bootloader to 4.13.3



## 1.89.2 (2020-10-06)(public)

### Fixes
1. (S) Handle CAN timeouts for Eth motor board

## 1.89.1 (2020-09-08)(beta)

### New Feautures

1. (C) Buttons for motors with named positions in quick selection/search dialog


## 1.89.0 (2020-09-04)(beta)

### New Feautures

1. (C) Add motor single selected motor control next to output control in elevated access level
2. (C) Add quick motor selection/search dialog via hotkey Alt+X or Ctrl+F

### Changed behaviours

1. (S) Switch to UDP communication with Eth motor boards (FW >= 4.0.0)


## 1.88.8 (2020-08-31)(beta)

### Changed behaviours

1. (S) Enable firmware updates for Eth motor boards

### New Feautures

1. (S) Track Eth motor board temperature

## 1.88.7 (2020-08-31)(beta)

### Fixes

1. (S)(FN) Do not send FRAM_SAVE command to Eth motor board, because it has been remove since fw 3.39.0

## 1.88.6 (2020-08-31)(beta)

### Fixes

1. (S)(FO) Connection to Eth motor board is lost during startup if firmware version >3.36.0


## 1.88.1 (2020-08-17)(beta)

### Fixes

1. (S)(FO) Six motor Eth boards are treated like they have four shutters too


## 1.88.0 (2020-08-14)(beta)

### Changed behaviours

1. (S) Shutter is closed for twin OPA device while motor is in forbidden range or reseting.
Servers for both devices should be located inside same C:\Programs\WinTopas4\Resources\SelfHostedServer folder, serials numbers should look like (15414,A5414) or (PA9300,P19300) and both devices should be running.



## 1.87.0 (2020-08-12)(beta)

### Changed behaviours

1. (S) Motor reset logic tweaks for motors with big zero offset
1. (S) Shutters connected to Eth motor board are opend and closed softly

### New Feautures

1. (S) Add option to swap limit switches for Eth motor board motors (SwapSwitches)



## 1.85.0 (2020-07-08)(beta),(2020-07-29)(public)

### New Feautures

1. (S) Optionally close shutter during each wavelength change (Shutter.json > "AlwaysCloseShutterOnWavelengthChange":true)



## 1.84.0 (2020-07-07)(beta)

### Fixes

1.(FO)(S) Various shutter logic issues
2.(FO)(C) In devices with a lot of motors some of them might be invisble in saved motor positions filter view

### Changed behaviours

1.(C) Enable automatic firmware update for Eth motor boards

## 1.81.0 (2020-06-23)(beta)

### Fixes

1.(C)(FO) Flat grey shutter button

### New Feautures

1. (S) Optionally sync laser output control to OPA shutter (Shutter.json > "SyncLaserOutputControl":true)



## 1.77.0 (2020-06-03)(beta)

### Changed behaviours

1.(C) Minor output control UI tweaks

### New Feautures
1. (S) Add custom motor homing logic: "Skip" 


## 1.76.0 (2020-05-25)(beta)

### Changed behaviours

1.(C) Shutter button moved to the left, interaction selection button and interlock indicator to the right, other UI tweaks


## 1.74.0 (2020-04-24)(beta), (2020-05-25)(public)

### Fixes

1.(S)(FO) Hotfix for 1.73.0, device with Eth motor board might crash on startup



## 1.73.0 (2020-04-23)(beta)

### New Feautures
1. (S) For devices with multiple Eth motor boards shutters on all boards are accessible

### Changed behaviours

1. (S) Added optinal 'Alias' in Loggers configuration, which will be used instead of device SN



## 1.72.0 (2020-04-22)(beta)

### Changed behaviours

1. (S) Change communication with Eth motor board timout logic

## 1.71.0 (2020-04-15)(beta)

### Changed behaviours

1. Round calibration points input value to 0.001 for all curves, round calibration points output value to 0.001 for interaction input-output relationship curve 

### Fixes

1.(C)(FO) 'Change Pump wavelength' tool might not correctly set same input values for range end motor curves points


## 1.70.0 (2020-04-10)(beta)

### Changed behaviours

1. Internal IL weaving changes
1. (S) Close shutter if any motor from separation configuration moves while setting wavelength

## 1.67.0 (2020-03-25)(beta), (2020-04-10)(public)

### Changed behaviours

1. (S) Use diffent commands to query Eth motor board periodically 


## 1.66.0 (2020-03-25)(beta)

### Fixes

1. Explicit usable wavelength range not used for possible output range calculation if interaction has parent interaction



## 1.65.0 (2020-03-19)(beta)

### New Feautures

1. Explicit usable wavelength range can be set for each interaction


## 1.64.0 (2020-03-19)(beta)

### Fixes 

1. (S)(FN) Check max maximal motor position on startup

### Changed behaviours

1. (C) Alt+number sets focus on motor calibration curve even for motors without slider control
1. (C) Device nicknames in multiple devices view


## 1.62.0 (2020-02-14)(beta), (2020-03-18)(public)

### New Feautures 

1. (S) Topas device location responses contains MotorBoards info

## 1.61.0 (2020-01-22)(beta), (2020-02-14)(public)

### Fixes 

1. (C)(FO) Fix wrong acceleration values are set for Eth motor board from presets

## 1.57.0 (2020-01-13)

### New Feautures

1. (C) Add Newport MFA-PP motor parameters template

## 1.55.0 (2019-12-23) (beta), (2019-01-13) (public)

### New Feautures

1. (C) Add 'Manage Eth motor boards' tool

## 1.54.0 (2019-11-21) (beta),  (2019-12-23) (public)

### Fixes

1.(C) Phrase 'due safety reasons' corrected to 'for safety reasons'

### New features

1.(S) Add motors positions logger (Configuration\Settings\Loggers.json > MotorPositions)

### Changed behaviours

1.(S) 'Configuration\Settings\Logger.json' file no is longer used




## 1.53.0 (2019-11-19) (beta), (2019-11-21) (public)

### Fixes

1.(C)(FO) 'Connect' button next to serial number is very buggy in case tab is already waiting for connection to another device
1.(C)(FO) Fix add/remove/reoder motors tool, add motor from .zip crashes WinTopas4 when sending configuration to server or checking sanity



## 1.51.0 (2019-10-30)

### Fixes

1.(S) Fix configuration history difference generation in cases when new file appears


## 1.50.0 (2019-10-29) 

### Fixes

1. (S)(FN) Do not try to read ADC and temperature/humidity sensor values from boards with 6 motors


## 1.49.0 (2019-10-25) - No changes



## 1.48.0 (2019-10-10) (beta)

### Fixes

1. (S)(FO) Ignore limit switch parameters are restored incorrectly after motor reset in some cases
2. (C)(FO) Application crashes when new motor is added in 'Motors>Add/Remove/Reorder tool'



## 1.46.0 (2019-10-08) (beta)

### New features

1. Add 'Move motor sometimes' tool



## 1.45.0 (2019-09-26) (beta)

### Fixes

1. (S) Fixes for limit switch swapping/eanbling for Eth motor board



## 1.44.0 (2019-09-25) (beta)

### Fixes

1. (S)(FO) Hotfix for 1.43.0, RampDivision, PulseDivision and StepDivision not set at startup for Topas3 board



## 1.43.0 (2019-09-25) (beta)

### Fixes

1. (S)(FO) Public API authentication service is behind authentication firewall, thus making it quite pointless


## 1.42.0 (2019-09-25) (beta)

### Fixes

1. (S)(FO) Ignore left/right switch parameters were not handled correctly with Eth motor board
1. (S)(FN) Use 'NoGUI' PI_GCS2_DL to control PI motor boards to avoid 'Cannot initialize OLE' pop-up


### Changed behaviours

1. RampDivision, PulseDivision moved to Topas3-only motor board configuration, removed from WinTopas4 motor properties view
2. StepDivision can be set only on board startup, removed from WinTopas4 motor properties view

### New Features

1. (S) Support for multiple shutters on Eht motor board
1. (S) Add REST endpoint for pass-trough commands for Eth motor board


## 1.41.0 (2019-09-05) (beta)

### Changed behaviours

1. (S) Give more power to 'Don't close shutter' option in wavelength setting options. Shutter won't be closed when current output is undefined or messages are not critical 


## 1.40.0 (2019-09-03) (beta)

### Fixes

1. (S) Fix shutter might be reported as open even if it is closed when device is started and no shutter operations have been performed 


## 1.39.0 (2019-09-03) (beta)

### Fixes

1. (S) Fix connection code if two Eth motor boards are used in single device


## 1.38.0 (2019-08-28) (beta), (2019-09-09) (public)

### Fixes

1. (S)(FO) Loss of connection to board is reported if device contains multiple motor boards and any of the motors are in forbidden range on startup


## 1.37.0 (2019-08-22) (beta)


### Fixes

1. Ignore/inverse limit switches for Eth motor board
1. (C)(FO) Named motor positions buttons presses sometimes ignored if they are rapid 
1. Wavelength setting never finishes if other device curve is in calibration and messages from other device should be shown


## 1.36.0 (2019-07-19) (beta), (2019-08-22) (public)


### Fixes
1. (S)Multiple Eth motor board related fixes


## 1.35.0 (2019-07-05) (beta)


### Fixes
1. (S)Multiple Eth motor board related fixes


## 1.33.3 (2019-06-25) (beta)


### Changed behaviours
1. (S)Eth motor board related changes


## 1.33.1 (2019-06-17) (beta)


### Changed behaviours
1. (S)New motor board (Eth) shutter state serialization changes

## 1.33.0 (2019-06-06) (beta)

### New Features
1. Support for new motor board (Eth)

### Changed behaviours
1. (C)'Create installer with current configuration' functionality has been disabled due to introduction of signed installers. Please use zipped configurations and vanilla installer.


## 1.30.1 (2019-05-29)

### Fixes

1. (FO) Hotfix for 1.28.0:  Background motor for interaction is set to the first curve in interaction on server startup

## 1.28.0 (2019-05-22)

### Fixes

1. (FO)Background motor index for interaction can become out-of-sync with current motor curves


## 1.27.1 (2019-05-02) (beta) 

### Changed behaviours

1. Change order of separation-like messages shown when optical configuration is activated

## 1.27.0 (2019-04-30) (beta) 

### New Feautures

1. Separation-like messages can be added to optical configuration. They are shown when optical configuration is activated


## 1.26.7 (2019-04-12) 

### Fixes

1.(C)(FO) Moving motor in one direction by holding down arrow key while calibration curve is visible makes motor jumpy: it skips back every second or so 


## 1.26.6 (2019-04-11) 

### Fixes

1.(C)(FO) 'Set offset' button in motor curve calibration window sets offset value to NaN (Not a Number) if the same motor is included in neutral positions


## 1.26.5 (2019-04-10) 

### Changed behaviours

1.(C) Remove 'Send feedback' function



## 1.26.2 (2019-03-20) 

### Fixes

1.(C)(FN) Separation configuration tables have scrollbars


### Changed behaviours
1.(C) Change legal company name to Light Conversion, UAB


## 1.26.0 (2019-02-26) (beta)

### Fixes

1.(S) Harpia motor board motor configuration: add new properties and other changes
1.(C)(FN) Inform user when he tries to launch device with the same serial number that is already in use on this PC instead of failing later on 

### Changed behaviours

1. On optical configuration change: close shutter, set wavelength using new configuration, and inform user with pop-up dialog in WinTopas4

### New Features

1. Motors can be set to be accessible only with elevated access level


## 1.25.0 (2018-12-19) (beta),  (2019-02-19) (public)

### Fixes

1. Spline interpolation in calibration curves
1. (S) Harpia motor board exit on hardware error



## 1.24.0 (2018-11-30)

### Fixes

1. (S) Harpia motor board reset procedure bug fixes


## 1.23.0 (2018-11-12) (beta)

### New Features

1. (C) Add CustomHomingLogic values: 'Try5Times' and 'Try10Times'


## 1.22.2 (2018-11-09) (beta)


### New Features

1. (C) Add 'Move all postions by offset' button to named motor positions control


## 1.22.1 (2018-09-21) (beta),  (2017-11-09) (public)


### Fixes

1. (S)(FO) Device location might stop working after some time when when server is running



## 1.22.0 (2018-09-17) (beta) 


### Fixes

1. (C)(FO) Motor sometimes briefly moves in the opposite direction when position is incremented/decremented from UI

### Changed behaviours
1. Saved motor positions use units instead of steps

### New Features
1. (C) Min/max possible wavelength hint in 'Calibration>Optical>Create'
1. (C) Change pump wavelength tool: option to choose whether to keep input or output wavelengths the same 
1. (C) Option to recreate input-output curve in 'Calibration>Optical>Create' 



## 1.21.0 (2018-08-28) (beta), (2018-09-12) (public)

### New Features
1. (S) TurnOnLeftSwitchForHomingOnly custom homing logic
1. (C) Add copy-paste commands for motor calibration curves in tree view





## 1.20.4 (2018-08-22) (beta)

### Fixes

1. (C)(FO) Device tabs change order randomly on selection after application start



## 1.20.3 (2018-08-14) (beta)

### Fixes

1. (FO) 'Misc>Configuration>Save device configuration as .zip file' sometimes fails silently


### New Features

1. (S) Beta support for HarpiaV0 motor board



## 1.20.2 (2018-07-18) (beta), (2017-07-20) (public)

### Fixes

1. Assembly binding redirects



## 1.20.1 (2018-07-18) (beta)

### Fixes

1. (C)(FO) Launch new device from zipped configuration + change SN does not work
1. (C)(FN) Persist laser control adjustment mode attenuator value 
1. (C)(FN) Optical device view does not have vertical scrollbar
1. (C)(FO) Right corner buttons (minimize,close etc) not visible if window is narrow

### Changed behaviors
1. (C) Show 'Hardware failure' indication instead of shutter&wavelength control in case of 'Hardware failure'

### New Features 
1. (S) Add Carbide laser control 
1. (C) Add/remove/reorder motors tool: can import motor from zipped configuration



## 1.20.0 (2018-06-18) 

### Changed behaviours
1. (C) 'Tools > Launch device from zipped configuration' asks whether user wants to launch device as demo or as real one, if configuration is demo

### New Features 
1. (C) Mobile app promo


## 1.19.0 (2018-05-31) (beta)


### New Features 
1. Each device can have a nickname for easier identification

### Changed behaviours
1. (S) Six letter serial numbers can be used for Topas3 boards
1. (C) Motor properties pop-up is closed after pressing 'Apply' button
1. (C) 'Done' check mark near separation messages is on the left side of the message


## 1.18.1 (2018-04-26) (beta), (2018-05-31) (public)


### Changed behaviours
1. (C) Bring back application wide accent color selection, keep device specific color too


## 1.18.0 (2018-04-25) (beta)


### New Features 
1. (C) Each device has its own color (instead of application wide color selection)

### Changed behaviours
1. (C) When launching device from zipped configuration AccessControl.OverrideAllowAll is set to false for non-Demo devices


## 1.17.1 (2018-04-04) (beta), (2018-04-10) (public)

### Fixes
1. (FO)(C) Default (aka neutral) positions with invalid named position are not reported by optical configuration sanity checker
1. (FO) Reverse direction property is not correctly initialized on startup
1. (FN) Remove 'possible nonsense' trace after motor reset


## 1.17.0 (2018-03-30) (beta)

### Fixes
1. (FN)(S) Do not try to get diagnostics information for motor connected to Topas3 extension board

### New Features
1. Long motor titles
1. Descriptions for interactions (shown as tooltip in interaction selection control)



## 1.16.0 (2018-03-07) (beta), (2018-03-11) (public)

### Fixes
1. (FO) Demo device can control real Pharos laser without authentication

### New Features
1. Neutral positions have interaction filter, like motors and messages in separation logic

### Changed behaviours
1. Demo devices have the same motors configuration, global property 'IsDemo' in General.json is used instead
1. (C) Messages window can't be minimized



## 1.15.4 (2018-02-26) (beta),  (2018-02-28) (public)

### Changed behaviours
1. (C) Both optical and separation devices can be renamed
1. (C) Prepare 'Create new interaction' tool for calibration with negative "wavelength" values



## 1.15.3 (2018-02-15) (beta)


### Fixes
1. (FO) Motor configuration sanity checker is silent about some mistakes in configuration (motor address, zero offset, etc)


## 1.15.2 (2018-02-13) (beta)


### Fixes
1. (FO) Server application might crash when deleting interaction which is parent for another one


## 1.15.1 (2018-02-07) (beta)


### Changed behaviours
1. In motor configuration use new property ForceNoDUSB in place of old DUSB with default value false 



## 1.15.0 (2018-02-07) (beta)


### New Features
1. Motor property 'Reverse Direction' is accessible via REST API, can be imported from zipped configuration

### Fixes
1. (C)(FO) When creating new interaction start/end wavelengths might be calculated incorrectly in some cases


## 1.14.0 (2018-02-05) (beta)

### Changed behaviors

1. (S) Direct USB communication is used everywhere instead of Topas3API. API slot number checks removed.

### New Features
1. (S) Press F10 to enumerate all Topas3 boards connected to the PC. Board already in use won't be reported.


## 1.12.4 (2018-02-01) (beta)


### Fixes
1. (C)(FO) Delete/inactivate self hosted server does not work if server is stopped, but application is open. Faster delete/inactivate


## 1.12.3 (2018-01-31) (beta), (2018-02-01) (public)


### Fixes
1. (S)(FO) Motor reset is canceled after 3 minutes, clients are not notified about failure

### New Features

1. (C) 'Interactions' button indicates when there is more than one interaction that supports current wavelength



## 1.12.2 (2018-01-26) (beta), (2018-01-31) (public)


### Fixes
1. (C)(FO) Multiple instances of Step scanner window can be opened, leading to erratic behavior
1. (C)(FO) Wavelengths set by Step scanner  might be off by about by about 1E-11 nm



## 1.12.1 (2018-01-24) (beta), (2018-01-26) (public)


### Fixes
1. (S)(FO) All hardware failures are reported as critical and affecting authentication possibility


## 1.12.0 (2018-01-17) (beta)


### Fixes
1. (C)(FO) When user tries to set wavelength which can not be set, message is displayed two or three times
1. (C)(FO) 'Change pump wavelength' might leave input-output and motor curves with slightly different ranges 

### New Features

1. Interaction can be marked as for as for indirect use only (i.e. only as intermediate for other interactions, but not as the output itself)
1. (S) Software motor power down (set current to 0 after 5 seconds of inactivity)
1. (S) Try to stop/start server when PC goes to sleep/wake ups



## 1.11.7 (2017-12-22) (beta), (2018-01-08) (public)


### Fixes
1. (C)(FO) Motor "Find position" tool can fail to restore maximal motor speed to original (partial fix)


## 1.11.6 (2017-12-14) (beta)


### Fixes
1. (S)(FO) Output can not be set if it contains no motor positions
1. (C)(FO) Can't save device configuration as zip file if resulting zip file is larger than 10MB

### Changed behaviors
1. (C) Completed actions in separation images are no longer grayed out



## 1.11.5 (2017-12-13) (beta)


### Fixes
1. (C)(FO) Existing curve offset is not taken into account when calculating motor position in 'Calibration>Optical>Create new'




## 1.11.4 (2017-12-13) (beta)


### Fixes
1. (C)(FO) Can't set device model


## 1.11.3 (2017-12-12) (beta)


### Fixes
1. (S)(FO) Shutter can be reported as open  even if interlock is activated



## 1.11.2 (2017-12-11) (beta)


### Fixes
1. (S)(FO) Set wavelength, move motors, so wavelength is unset, OutputData.IsWaitingForUserAction is reported as true



## 1.11.1 (2017-12-08) (beta)


### Fixes
1. (C) Hotfix for 1.10.0, websocket client is supported only from Windows 8



## 1.11.0 (2017-12-08) (beta)


### Changed behaviors
1. Internal changes to make code compatible with .NET Standard 2.0
1. (S) More push notifications via websocket
1. (C) Disable separation images tooltip
1. (C) On separation images upload check their resolution



## 1.10.0 (2017-11-29) (beta), (2017-12-08) (public)

### Fixes

1. (C)(FO) DIY installer creator packs disabled devices in installer
1. (C)(FN) Grating motor curve is recalculated even if it exists when modifying interaction
1. (C)(FO) Additive calibration curves might cause false positive sanity check error ('Motor position is out of range') 
1. (S)(FN) Motor maximal and minimal velocities are checked to be lower than 4096

### New Features

1. Neutral positions in optical calibration can use named motor positions
1. (S) Support for motors with custom reset logic
1. Position of named motor position can be quickly changed to current motor position from main motor control, by right clicking on the button or combo-box entry

### Changed behaviors
1. (C) Default curve interpolation mode is linear (was spline)
1. (C) Check DIY installer creator executable file size



## 1.9.1 (2017-10-19) 

### New Features

1. (C) Show number of wavelength range gaps in calibration and where they are (except in User access level)

### Changed behaviors

1. (C) Separation messages are no longer grouped by device when shown to user, new way of arrangement and sizing, picture enlargement tooltip 
2. (C) On optical device import do not skip interactions that already exist (i.e. interactions with the same name)




## 1.9.0 (2017-10-12) 

### Fixes

1. (C)(FO) In 'Calibration>Optical>Create new' input-output curve points have wrong range if parent interaction supports bigger range than user selected to calibrate


### New Features

1. (S) Mixed motors hardware support
1. (S) Physik Instrumente (PI) delay stages support
1. (C) User can be prompted to accept EULA anytime ('Tools>Request accept user license agreement')




## 1.8.3 (2017-09-29) 

### Fixes

1. (C)(FO) Some buttons where invisible in motor properties view (since 1.8.2)


## 1.8.2 (2017-09-26) 

### New Features

1. Motor can be frozen, meaning it won't move (server-side)

### Changed behaviors

1. (S) Direct communication with motor board using WinUSB is enabled inside LC by default

### Fixes

1. (C)(FO) Set wavelength, move motor so that wavelength is not strict, press enter on wavelength textbox, nothing happens (since 1.8.0)



## 1.8.1 (2017-09-26) 

### New Features

1. (C) Tool to recalculate input-output wavelength relationship with new pump wavelength (SF, DFP, DFG)

### Changed behaviors

1. (C) 'Create/Modify interaction' renamed to 'Create interaction'



## 1.8.0 (2017-09-22) 

### New Features

1. (C) Wavenumber (cm-1) can be used instead of wavelength to set output
1. (C) Multi-line separation messages can be entered



## 1.7.1 (2017-09-13) 

### Fixes

1. (C)(FN) Interactions input-output relationship points are ordered in interaction view table
1. (C)(FN) Correct name generation for cloned interactions

### Changed behaviors

1. (C) New shutter button style applied to mini mode window



## 1.7.0 (2017-09-06) (beta)

### Changed behaviors

1. (C) Change shutter button style and size, move 'Interactions' and 'Messages' buttons
1. (C) Remove button 'Shift curve by current difference' in motor curve view 
1. (C) First result of reset operation is ignored in 'Testing workbench'



## 1.6.9 (2017-09-01) 

### Fixes

1. (S)(FO) Server setting wavelength for other device on the same PC doesn't use loopback address >> no authentication




## 1.6.8 (2017-08-31) 

### Fixes

1. (S)(FO) Reset latch difference is calculated from second movement to switch

### Changed behaviors

1. (S) Direct communication with motor board using WinUSB enabled for boards with six-motor extension boards
1. (C) Various new access keys, 'Save current position' changed to Alt+P 
1. (C) NumPad keys can be used to focus motors too




## 1.6.7 (2017-08-24) 

### Fixes

1. (S)(FO) Wrong motor diagnostics status is returned for section if it contains hidden motors




## 1.6.6 (2017-08-23) 

### New Features

1. (C) User can import separation images from zipped configuration




## 1.6.5 (2017-08-21) 

### Fixes

1. (C)(FO) Affix can't be changed by entering new value, only using button 'To 0'



## 1.6.4 (2017-08-18) 

### New Features

1. Backlash compensation 
1. (C) Function to set motor affix to such value that current position is 0 units




## 1.6.3 (2017-08-16) 

### Fixes

1. (C)(FO) DIY installer creator timeouts after 5 minutes, which is too soon


### New features

1. (C) WinTopas4 can be launched with NoAutoLaunch argument (--NoAutoLaunch) to prevent self-hosts launch. 'Manage devices' tool can be used to launch device later on.



## 1.6.2 (2017-08-11) 

### Fixes

1. (C)(FO) Application might get stuck in zombie state on startup with no visible window



## 1.6.1 (2017-08-11)

### No changes



## 1.6.0 (2017-08-11) 

### Changed behaviors

1. (S) Communication with motor board using WinUSB directly (TopasAPI.dll no longer used) beta, enabled inside LC only
1. (C) Motor Diagnostics tool has nicer UI




## 1.5.2 (2017-08-09) 

### Fixes

1. (C)(FO) Application crashes if user tries to modify motor curve and this curve does not cover currently set wavelength



## 1.5.1 (2017-08-08) (beta)

### New features

1. (C) User can change serial number of device and motor board before launching device from zipped configuration



## 1.5.0 (2017-07-25) (beta)

### New features

1. Each device has a model included in configuration (Topas-Prime, Orpheus-F, etc)




## 1.4.2 (2017-07-17)

### New features

1. (S) 'Saved motor positions' service is in public API




## 1.4.1 (2017-07-13)

### New features

1. (C) Motor properties window can be opened directly from 'Testing workbench' (mouse right click)

### Changed behaviors

1. (C) Self-hosted servers can be managed with advanced user access level



## 1.4.0 (2017-07-12)

### New features

1. Add basic Pharos control from WinTopas4 via Topas4Server if connection is configured 
1. (C) Add new hotkey for shutter: Ctrl+NumPad0

### Changed behaviors

1. (C) Motor board drivers are installed by default




## 1.3.4 (2017-06-29)


### New features

1. Add 'Restart server' button to Motor Testing Workbench



## 1.3.3 (2017-06-27) (beta)


### Changed behaviors

1. Update links to web pages




## 1.3.2 (2017-06-27) (beta)


### New features

1. Add motor modules diagnostics tool ('Misc' tab, 'Diagnostics') (new unmanaged Topas3 dlls v3.3.0.52)




## 1.3.1 (2017-06-26)

### Fixes

1. (C)(FO) Tabbing navigation does not work in 'Smooth Scanner' view

### New features

1. (C) Add step scanner tool (Misc tab)



## 1.3.0 (2017-06-20)

### Changed behaviors

1. (S)(PA) Motor reset (homing) functions are exposed via public API
1. (C) Named motor positions can be modified with advanced user access level




## 1.2.11 (2017-06-15)

### Fixes

1. (C)(FN)  'Start Wavelength' in 'Create interaction' has reasonable fall-back value in case it is can be negative (i.e. using DFP)




## 1.2.10 (2017-06-12) 

### Fixes

1. (S)(FO) Device location code might cause crash when restarting server


## 1.2.9 (2017-06-07) (beta)

### Fixes

1. (C) Various 'Create interaction' wavelength range calculation improvements 




## 1.2.8 (2017-06-05)

### Changed behaviors

1. (C) Add separation configuration check for overlapping ranges




## 1.2.7 (2017-05-31)

### New features

1. (C)  Add two new demo configurations (Topas-Prime+NirUVis and Orpheus-HP)

### Changed behaviors

1. Optical devices are always kept ordered by index


## 1.2.6 (2017-05-31)

### Changed behaviors

1. (S)  Up to two successive motor board status read failures are ignored
1. (C)  Application exits point insertion mode in motor curve view when it loses visibility
1. (C)  Optical configuration checker checks for small steps that are not small enough (<=0.1 nm, but > 0.001 nm)




## 1.2.5 (2017-05-26)

### Changed behaviors

1. (S)  All motor positions are saved within five seconds after setting new target position (i.e. moving motor)
1. (C) 'Reset in progress' warning is bigger and flashing



## 1.2.4 (2017-05-25)

### Changed behaviors

1. (C) Red warning 'undefined' is no longer shown for motors with named positions which are in none of them




## 1.2.3 (2017-05-22)

### Fixes

1. (S)(FO) Server application enters infinite relaunch loop if Windows are localized and firewall permissions are missing




## 1.2.2 (2017-05-22)

### Fixes

1. (S)(FO) Wrong motor reset position difference calculation (second pass used instead of first)

### Changed behaviors

1. (C) Minor UI tweaks




## 1.2.1 (2017-05-19)

### Fixes

1. (S)(FO) Likely fixed: application might crash when restarting (System.NullReferenceException at System.Threading.Overlapped.get_iocbHelper)
1. (S)(FN) Remove unused websocket module initialization which might cause real one to become unavailable (crash before 1.2.0)
1. (C)(FO) Application crashes if user tries to add neutral position without selecting motor first
1. (C)(FO) Application crashes if user tries to open wavelength fixer tool for interaction with no calibration points that apply for fixing




## 1.2.0 (2017-05-16)

### Fixes

1. (FO) Wrong minimal motor position calculation in case negative factor is used
1. (S)(FO) When named motor position is renamed, separation configuration does not update accordingly


### New features

1. (C) After Topas3 > Topas4 conversion user can start device as demo (without using actual hardware)

### Changed behaviors

1. (C) Topas3 to Topas4 converter tries to guess named motor positions names for wavelength separators and some other motors with discrete positions
1. (C) Other minor tweaks in Topas3 to Topas4 converter
1. Add EULA to installers
2. (C) Separation configuration sanity checker for multiple entries which differ only by interaction is disabled



## 1.1.3 (2017-05-11)

### Fixes 

1. (C)(FN) When trying to delete/inactivate self hosted server from WinTopas4 check whether it has actually exited.



## 1.1.2 (2017-05-11)

### New features

1. (C) New tool to manage SelfHosted servers from WinTopas4 (Tools>Self Hosts>Manage devices).

### Changed behaviors

1. (C) Topas3 configuration converter preserves motor positions
1. (C) Topas3 configuration converter adds 127.0.0.1 to IP address white list (there is no need to authenticate after conversion)
1. (C) SelfHostedServers\Master directory is hidden



## 1.1.1 (2017-05-09)

### Fixes 

1. (FN) If connection to motor control board fails and client PC is not authenticated 'Start authentication' button is not shown

### New features

1. (S) Press F11 in server application to open Configuration\Settings folder

### Changed behaviors

1. (S) New help generator for REST services (faster startup)



## 1.1.0 (2017-05-08)

### New features

1. WinTopas4, including self hosted servers, can be updated offline by installing newest version on top



## 1.0.3 (2017-05-02)

### Fixes 

1. (S)(FO) Shutter might actually be open while control board thinks it's closed if close command is issued shortly after open command.



## 1.0.2 (2017-05-02)

### Fixes

1. (C)(FO) Respacer tool will add duplicate point under certain conditions



## 1.0.1 (2017-05-02)

### Fixes

1. (C)(FO) Position for motor curve with additive calibration is saved with no regard that it is additive when modifying motor curve in Calibration>Optical tab
1. (C)(FO) Motor curve with additive calibration is moved to wrong position when modifying interaction in 'Create interaction' tool
1. (C)(FO) Copy-pasting interaction input points does not handle decimal separator well

### New features

1. (C) Wavelength correction tool (move calibration points in all motor curves horizontally/add new point). Automated version with spectrometer in spectraLight since 2.5.0
1. (C) Respacer tool for interaction motor curves
1. (C) Arrow buttons to move named motor positions up/down in the list



## 0.9.2 (2017-04-27)

### Fixes

1. (C)(FO) Application crashes if incorrect password is provided



## 0.9.1 (2017-04-26)

No changes


## 0.9.0 (2017-04-26)

### New Feautures

1. (C) User can finish interaction modification by deleting all old points in motor curves

### Changed behaviors

1. Auto updater moved from Dropbox to Azure+GitHub.io to avoid Great Firewall of China 



## 0.8.8 (2017-04-25)

### Fixes

1. (FO) .pdb file for executable in not found by CLR, exceptions stack traces contains no line numbers (except for .dlls) 
1. (S)(FO) Under certain conditions shutter can't be opened ('due safety reasons') after setting wavelength
1. (C)(FO) Non-explicit IDL to SIG conversion creates invalid wavelength mapping curve



## 0.8.7 (2017-04-21)

### Fixes

1. (S)(FO) Timeout for motor reset is too short for slow motors with long travel range
1. (C)(FO) Feedback text box does not accept return key and does not wrap text
1. (C)(FO) It's possible to delete multiple points in motor curve and interaction views when only single point is selected
1. (C)(FO) Interaction output range sometimes is not updated in device view and interaction view 

### Changed behaviors

1. (C) Smooth scanner tool updates scan range every time new interaction is selected


## 0.8.6 (2017-04-19)

### Fixes

1. (C)(FO) Calibration editor crashes a lot if curve type is OtherDevice instead of motor



## 0.8.5 (2017-04-14) (beta), (2017-04-18)

### New features

1. (C) New tool to quickly stop motor on required position (right click on motor control and select 'Find position') 



## 0.8.4 (2017-04-14) (beta)

### Fixes

1. (C)(FO) 'Create interaction' tool crashes due invalid TwoWay binding



## 0.8.3 (2017-04-13) (beta)

### Fixes

1. (FN) user_id generator for application insights uses stable hashing algorithm
2. (S)(FN) Git index lock (might happen due crash or when creating installer) is handled by deleting index.lock file



## 0.8.2 (2017-04-12) (beta)

### Fixes

1. Various fixes/format changes in sent telemetry data

### New features

1. (C) User can send feedback straight from WinTopas4 application (if server seems reachable)



## 0.8.1 (2017-04-11) (beta)

### Fixes

1. (C)(FN) Web page for mobile clients is hosted using port RestPort+2 instead of port 80 to avoid clashes with others applications (Skype etc)
2. (S)(FN) Output metrics collector for Application Insights does not try to make sense of device state if motors are not available



## 0.8.0 (2017-04-10) (beta)

### New features

1. Application Insights

### Fixes

1. (C)(FO) CMP-SIG template in Create interaction tab uses SIG as mapping wavelength mapping function
2. (C)(FO) Saved motors positions list in single device tab does not show vertical scrollbar if there isn't enough space


## 0.7.4 (2017-03-28)

### New features

1. (C) Add buttons 'delete current configuration' to optical and separation configurations

### Changed behaviors

1. (C) Change calibration motor curve offset control to indicator, add two new buttons : 'Set offset' and 'Shift curve to make offset zero'. 'Add current offset' button renamed to 'Shift curve by current diff'.
1. (C) Calibration motor curve points are always auto-ordered by wavelength, user can't reorder



## 0.7.3 (2017-03-27)

### New features

1. Add link to [Topas4 info page](https://domasm.github.io/Topas4Info/) in three different locations

### Changed behaviors

1. Beautified local (per device) API help pages, add more info to some methods



## 0.4.12 (2017-02-13) ---> 0.7.2 (2017-03-13)

### Fixes

1. (S)(FO) Decrease power on still does not work at all
1. (S)(FO) Shutter is opened when it shouldn't be:
* Open shutter
* Trigger interlock (shutter will be closed)
* Defeat interlock
* Set wavelength
* Shutter will be opened
1. (C)(FO) 'Calibration>Optical' adds current motor position instead of target when modifying motor curve
1. (C)(FO) 'Tools>Create Installer with current configuration' fails with multiple self-hosted servers due too short timeout
1. (S)(FN) Before starting server with configured TCP ports, server checks if they aren't used by other applications and informs user if so instead of crashing
1. (S)(FN) When calculating motor positions for wavelength, neutral positions are used only from optical devices that are actually used to set requested wavelength
1. (FO) Device location might not work if PC isn't connected to LAN
1. (C)(FO) When connecting to new device in client application, named motor positions and forbidden ranges might not be synced
1. (C)(FO) Motor curves, if they have points with 'None' interpolation, are incorrectly converted  when using SIG<>IDL conversion with explicit IDL motor curves
1. (C)(FN) 'Calibration>Create interaction' informs user if end wavelength<=start wavelength

### New features

1. (C) Import anything from zipped configuration. User can inform any part of optical configuration (whole optical configuration, optical device, interaction, motor curve), separation configuration (...), or motor property from zipped server configuration
1. (C) Start a new self hosted server from zipped configuration (optionally as demo, i.e. without actual hardware)
1. Forbidden motor ranges: each motor has a list of forbidden positions ranges.
If shutter is open when motor is entering forbidden range it will be closed by server and reopened after motor leaves forbidden range. Shutter can't be opened while motor is in forbidden range.
1. On hardware failure, inform user to power-cycle device, reconnect USB and restart server application (pop-up in Client)
1. Hidden motors : if motor socket is installed in Topas3 board, but there is no motor connected, you can completely hide it from clients
1. (C) 'Update is available' message in title bar
1. (C) Rectangle around motor control

### Changed behavior

1. (C) All self-hosted servers in \Resources\SelfHostedServer are launched on start. Prepend '_' to folder name to ignore server (P17189 >> _P17189).
1. (C) Motor controls can be used with mouse in interactive mode ('Calibration>Optical')
1. (C) Calibration and Motors tabs are not visible in User Access Level
1. Shutter has three states: open, closed and temporarily closed. Shutter in temporarily closed state can't be opened by user, but will be opened by server after reason why it was closed is no longer valid: e.g. motor leaves forbidden range, wavelength setting is finished
1. (C) Order of named motor positions is kept unchanged after modifying position/name/short name
1. (C) To close device tab, Shift key has to be held while clicking x button
1. (S) Can't open shutter during motor reset
1. (C) Bigger Interactions and Messages buttons
