
# La Interfaz de Línea de Comandos (CLI)

Es una interfaz basada en texto para la computadora, donde el usuario introduce un comando y la computadora lo ejecuta. El entorno de la CLI es proporcionado por una aplicación en la computadora conocida como un terminal.

El terminal acepta lo que el usuario escribe y lo pasa a un shell. El shell interpreta lo que el usuario ha introducido en las instrucciones que se pueden ejecutar con el sistema operativo. Si el comando produce una salida, entonces se muestra este texto en el terminal. Si surgen problemas con el comando, se muestra un mensaje de error.

## ejemplo de una terminal:

```bash
╭─diego-landony at diego-landony-Vostro-3400 in ⌁
╰─λ ls                                                                                                                                 0 (0.003s) < 16:53:07
'Biblioteca de calibre'/   Documents/                             GitHubDesktop-linux-3.1.1-linux1.deb.1   Music/      snap/
 cv_debug.log              Downloads/                             Hyprland-ubuntu/                         Pictures/   Templates/
 Desktop/                  GitHubDesktop-linux-3.1.1-linux1.deb   install                                  Public/     Videos/
╭─diego-landony at diego-landony-Vostro-3400 in ⌁
╰─λ cd Documents/                                                                                                                      0 (0.003s) < 16:53:08
╭─diego-landony at diego-landony-Vostro-3400 in ⌁/Documents
╰─λ cd hola-mundo/                                                                                                                     0 (0.000s) < 16:53:11
╭─diego-landony at diego-landony-Vostro-3400 in ⌁/Documents/hola-mundo
╰─λ touch creando-un-archivo                                                                                                           0 (0.001s) < 16:53:17
╭─diego-landony at diego-landony-Vostro-3400 in ⌁/Documents/hola-mundo
╰─λ ls                                                                                                                                 0 (0.003s) < 16:53:29
creando-un-archivo
╭─diego-landony at diego-landony-Vostro-3400 in ⌁/Documents/hola-mundo
╰─λ neofetch                                                                                                                           0 (0.003s) < 16:53:29
           `.:/ossyyyysso/:.               diego-landony@diego-landony-Vostro-3400 
        .:oyyyyyyyyyyyyyyyyyyo:`           --------------------------------------- 
      -oyyyyyyyodMMyyyyyyyysyyyyo-         OS: Kubuntu 23.04 x86_64 
    -syyyyyyyyyydMMyoyyyydmMMyyyyys-       Host: Vostro 3400 
   oyyysdMysyyyydMMMMMMMMMMMMMyyyyyyyo     Kernel: 6.2.0-34-generic 
 `oyyyydMMMMysyysoooooodMMMMyyyyyyyyyo`    Uptime: 6 hours, 24 mins 
 oyyyyyydMMMMyyyyyyyyyyyysdMMysssssyyyo    Packages: 2893 (dpkg), 22 (snap) 
-yyyyyyyydMysyyyyyyyyyyyyyysdMMMMMysyyy-   Shell: bash 5.2.15 
oyyyysoodMyyyyyyyyyyyyyyyyyyydMMMMysyyyo   Resolution: 1280x720 
yyysdMMMMMyyyyyyyyyyyyyyyyyyysosyyyyyyyy   DE: Plasma 5.27.4 
yyysdMMMMMyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy   WM: KWin 
oyyyyysosdyyyyyyyyyyyyyyyyyyydMMMMysyyyo   WM Theme: Dracula 
-yyyyyyyydMysyyyyyyyyyyyyyysdMMMMMysyyy-   Theme: [Plasma], Default [GTK2/3] 
 oyyyyyydMMMysyyyyyyyyyyysdMMyoyyyoyyyo    Icons: Reversal-dark [Plasma], Reversal-dark [GTK2/3] 
 `oyyyydMMMysyyyoooooodMMMMyoyyyyyyyyo     Terminal: konsole 
   oyyysyyoyyyysdMMMMMMMMMMMyyyyyyyyo      Terminal Font: DejaVu Sans Mono 10 
    -syyyyyyyyydMMMysyyydMMMysyyyys-       CPU: 11th Gen Intel i5-1135G7 (8) @ 4.200GHz 
      -oyyyyyyydMMyyyyyyysosyyyyo-         GPU: Intel TigerLake-LP GT2 [Iris Xe Graphics] 
        ./oyyyyyyyyyyyyyyyyyyo/.           Memory: 4324MiB / 11680MiB 
           `.:/oosyyyysso/:.`
                                                                   
                                                                   


╭─diego-landony at diego-landony-Vostro-3400 in ⌁/Documents/hola-mundo
╰─λ    
```