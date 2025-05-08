Seiesmic - Deploy

cd $HOME
  
sudo apt update

sudo apt install file

source ~/.bashrc

sfoundryup

wait---

cd try-devnet/packages/contract/

git clone https://github.com/SeismicSystems/seismic-foundry.git

cd seismic-foundry/sfoundryup

bash install

source ~/.bashrc

find ~ -name scast

echo 'export PATH="$HOME/.seismic/seismic-foundry/target/release:$PATH"' >> ~/.bashrc

source ~/.bashrc

scast --help

cd $HOME

cd try-devnet/packages/contract/

bash script/deploy.sh      
