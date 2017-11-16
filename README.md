# HOW TO: Make your windows 10 device sleep and wake up without a lock screen. 

This is what you need if you want to setup your windows PC to be a monitor or a dashboard display.

## Rookie mistakes
1. Do not use windows Task Scheduler as an alternative method. This is often bugged in Windows 7+. As the `old` directory shows any approach with `nircmd.exe` or `power shell`. 
2. Not having administration rights on the host. 
3. Any

## Steps
1. **Schedule your pc to sleep/wake:** Install kmwakeup_16_setup.exe and add timers to sleep and wake.
2. **Turn off lockscreen settings:** run disableLockScreenFromRestart.reg and disableLockscreenFromSleep.bat 
3. **Setup the current user** run CMD as administrator: 
    net users [YOUR_USERNAME] "" 
    net localgroup administrators [YOUR_USERNAME] /add 
4. **Setup power options:** Go to "Control Panel -> All Control Panel Items -> Power Options -> Edit Plan Settings" for the power plan u are using. Then select "Change advanced power settings". Next go to "Sleep -> Allow wake timers" and enable them there. 
5. **Set the local security policy:** start secpol.msc from the start menu. Go to "local policies -> User rights assignment -> Log on as  batch job" and add the current user. 

