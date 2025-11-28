# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
![WhatsApp Image 2025-11-28 at 06 17 40_c4c94c33](https://github.com/user-attachments/assets/2032671a-0922-4010-8106-b90481c3c2d7)
![WhatsApp Image 2025-11-28 at 06 18 04_aef950d1](https://github.com/user-attachments/assets/0f3089f6-a2ad-4235-b0b5-d8b90ab4407b)
![WhatsApp Image 2025-11-28 at 06 18 36_ed3ebb44](https://github.com/user-attachments/assets/cb3e8a4f-9829-438e-96ea-eb61015c59b8)
![WhatsApp Image 2025-11-28 at 06 18 51_e76073e7](https://github.com/user-attachments/assets/c95e2c3d-01cc-40b0-ab4f-e8c80bc589de)






## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
num=1
den=[0.05 0.6 1 0]
sys=tf(num,den)
bode(sys)
grid on
[Gm Pm Wpc Wgc]=margin(sys)
if(Wpc>Wgc)
disp('stable')
elseif(Wpc == Wgc)
disp('marginally stable')
else
disp('unstable')
end

## Output:<img width="453" height="349" alt="image" src="https://github.com/user-attachments/assets/400905f4-d39d-4093-827d-3c0a35ae6e0b" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12.0<br>
Phase Margin = 60.42<br>
Gain crossover frequency =0.907 <br>
Phase crossover frequency = 4.4721 <br>
The system is stable
