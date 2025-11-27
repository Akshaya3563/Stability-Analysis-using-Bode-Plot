# Stability-Analysis-using-Bode-Plot
## Aim:
To analyse the stability of the system having open loop transfer function, G(S)=1/(S(1+0.5S)(1+0.1S)) using bode plot and verify it using MATLAB. 
## Apparatus Required:
Computer with MATLAB software

## Theory:
<img width="516" height="685" alt="image" src="https://github.com/user-attachments/assets/6e2ccf6a-b8b9-4781-9072-32fa9f5a3fc8" />
<img width="416" height="684" alt="image" src="https://github.com/user-attachments/assets/180add70-5cca-40ed-b35a-e414e6c852b9" />
<img width="525" height="662" alt="image" src="https://github.com/user-attachments/assets/32fef39c-80e3-46fa-af48-e39d4b523d2e" />



## Procedure:
	Open MATLAB software
	Open a new script file.
	Type the program.
	Save and Execute the program.
	Determine the gain crossover frequency, phase cross over frequency, gain margin and phase margin.
	Also determine the stability.

## Program: 
```
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
```

## Output:
<img width="702" height="629" alt="image" src="https://github.com/user-attachments/assets/1bcfe0b7-9084-447e-b972-1bd863380aeb" />


## Result:
Thus the bode plot for the given transfer function was drawn and verified using MATLAB. <br>
Gain margin = 12.0 <br>
Phase Margin =  60.42 <br>
Gain crossover frequency = 0.907<br>
Phase crossover frequency =  4.4721<br>
The system is stable
