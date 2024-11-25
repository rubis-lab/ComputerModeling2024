# ComputerModeling2024
## Preparing Source Code and Build Project

### Preparing Source Code
```bash
sudo apt update
sudo apt upgrade
sudo apt install git

git clone https://github.com/rubis-lab/ComputerModeling2024.git
cd ComputerModeling2024
```

### Build Project
```bash
sudo apt install build-essential cmake openjdk-17-jdk
```

```bash
rm -r build # only when build exists
mkdir -p build

cd build
cmake ..
cmake --build .

cd Debug
export CPSIM_PATH=/home/<username>/ComputerModeling2024
./CPSim-0.1.out

# XXX.so's Function Successfully Loaded
# YYY.so's Function Successfully Loaded
# YOUR CPU MAX PERFORMANCE : XXXX.XX MHz
# CONNECTION ERROR, YOU MUST CONNECT WITH TORCS IN 5 SECONDS
```

## Preparing Eclipse SDK

Download from the link below

> https://www.eclipse.org/downloads/download.php?file=/eclipse/downloads/drops4/R-4.33-202409030240/eclipse-SDK-4.33-linux-gtk-x86_64.tar.gz
> 

```bash
cd ~/Downloads
tar -xvf eclipse-SDK-4.33-linx-gtk-x86_64.tar.gz

cd eclipse
./eclipse
```

- create new workspace → Click Launch
- Install softwares(gmf-runtime, graphiti)
- Run→Run Configurations→Environments
    - ADD→ CPSIM_PATH, path-to-cpsim (”/home/\<username>/ComputerModeling2024”)
- Disable IPv6 and Wi-Fi in both machines

- Launch Application → Design, New Project

- Connect two machines
- Set Static IP of Windows machine as 192.168.0.100

- Set the diagram and edit properties of the components as shown in the given pdf

- Simulation→Run Simulation