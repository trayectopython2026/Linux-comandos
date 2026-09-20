# version de linux (32 o 64 bits)
uname -m


# instalar gestor de paquetes curl 
sudo apt update
sudo apt install curl

# instalar opencode
curl -fsSL https://opencode.ai/install | bash

opencode --version

mkdir mi-proyecto
cd mi-proyecto
opencode

# si no llega a funcionar 
export PATH="$HOME/.opencode/bin:$PATH"

# por ultimo ejecutar opencode dentro del directorio
opencode

