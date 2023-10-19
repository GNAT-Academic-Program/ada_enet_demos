# Ada Enet Demos 

### Prerequesite (tested on linux ubuntu 20.04 only)

#### Alire
Refer [here](https://github.com/GNAT-Academic-Program#install-alire-an-ada-package-manager) to install

#### OpenOCD
```console
sudo apt install openocd
```

#### STM32f746 Discovery [board](https://www.st.com/en/evaluation-tools/32f746gdiscovery.html)
- Plug it to your computer using a [USB MIN B cable](https://www.reviewgeek.com/53587/usb-explained-all-the-different-types-and-what-theyre-used-for/)


### Fetch 
```console
alr get ada_enet_demos
cd ada_enet_demos*
```  

### Build (Terminal)
```console
alr build
```

### Build (GPRBuild)
```console
eval "$(alr printenv)"
gprbuild hada_enet_demos.gpr
```

### Build (GnatStudio)
```console
eval "$(alr printenv)"
gnatstudio ada_enet_demos.gpr
```

### Run

```console
openocd -f /usr/local/share/openocd/scripts/board/stm32f746g-disco.cfg -c 'program bin/ping verify reset exit'
```    
