# Ada Enet Demos 

### Prerequesite (tested on linux ubuntu 20.04 only)

#### Alire: https://github.com/alire-project/alire/releases
- Download and unzip the latest linux zip
- Add `where_you_unzipped/alr` to [PATH](https://phoenixnap.com/kb/linux-add-to-path)  
- Verify Alire is found on your path. 
```console   
which alr
```

#### OpenOCD
```console
sudo apt install openocd
```

#### STM32f746 Discovery board
- Plug it to your computer using the [USB MIN B cable](https://www.reviewgeek.com/53587/usb-explained-all-the-different-types-and-what-theyre-used-for/)


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
