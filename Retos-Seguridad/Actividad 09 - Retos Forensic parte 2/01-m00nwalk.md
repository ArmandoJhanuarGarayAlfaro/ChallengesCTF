# m00nwalk

## Descripcion
Decode this [message](https://jupiter.challenges.picoctf.org/static/fc1edf07742e98a480c6aff7d2546107/message.wav) from the moon.

## Pistas
How did pictures from the moon landing get sent back to Earth?

What is the CMU mascot?, that might help select a RX option

## Solucion 
Install qsstv with apt-get install qsstv
Run pactl load-module module-null-sink sink_name=virtual-cable
Run pavucontrol. A GUI will pop-up, go to the "Output Devices" tab to verify that you have the "Null Output" device.
Run qsstv. The program GUI will pop-up, go to "Options" -> "Configuration" -> "Sound" and select the "PulseAudio" Audio Interface
Back in the pavucontrol GUI, select the "Recording" tab and specify that QSSTV should capture audio from the Null Output
paplay -d virtual-cable message.wav 

 ![visible en Github](https://github.com/Alexlife2002003/ChallengesCTF/blob/main/Retos-Seguridad/Actividad%2009%20-%20Retos%20Forensic%20parte%202/Pasted%20image%2020230320125412.png)
![[Pasted image 20230320125412.png]]

![visible en Github](https://github.com/Alexlife2002003/ChallengesCTF/blob/main/Retos-Seguridad/Actividad%2009%20-%20Retos%20Forensic%20parte%202/Pasted%20image%2020230320130212.png)
![[Pasted image 20230320130212.png]]
## Bandera
picoCTF{beep_boop_im_in_space}
## Notas Adicionales 
qsstv: is a program for receiving slow-scan television and fax
pavucontrol: allows you to control both the volume of hardware devices and of each playback stream separately.
ssplay: to isplay an image or image sequence on any X server
